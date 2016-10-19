---
title: "Registering the Program"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "programs, registration"
  - "debugging [Debugging SDK], program registration"
ms.assetid: d726a161-7db3-4ef4-b258-9f6a5be68418
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Registering the Program
After the debug engine has acquired a port, represented by an [IDebugPort2](../extensibility/idebugport2.md) interface, the next step in enabling the program to be debugged is to register it with the port. Once registered, the program is available for debugging by one of the following means:  
  
-   The process of attaching, which allows the debugger to gain complete debugging control of a running application.  
  
-   Just-in-time (JIT) debugging, which allows for after-the-fact debugging of a program that runs independently of a debugger. When the run-time architecture catches a fault, the debugger is notified before the operating system or runtime environment releases the memory and resources of the faulting program.  
  
## Registering Procedure  
  
#### To register your program  
  
1.  Call the [AddProgramNode](../extensibility/idebugportnotify2--addprogramnode.md) method implemented by the port.  
  
     `IDebugPortNotify2::AddProgramNode` requires a pointer to an [IDebugProgramNode2](../extensibility/idebugprogramnode2.md) interface.  
  
     Typically, when the operating system or run-time environment loads a program, it creates the program node. If the debug engine (DE) is asked to load the program then the DE creates and registers the program node.  
  
     The following example shows the debug engine launching the program and registering it with a port.  
  
    > [!NOTE]
    >  This is not the only way to launch and resume a process; this is mainly an example of registering a program with a port.  
  
    ```cpp#  
    // This is an IDebugEngineLaunch2 method.  
    HRESULT CDebugEngine::LaunchSuspended(/* omitted parameters */,  
                                          IDebugPort2 *pPort,  
                                          /* omitted parameters */,  
                                          IDebugProcess2**ppDebugProcess)  
    {  
        // do stuff here to set up for a launch (such as handling the other parameters)  
        ...  
  
        // Now get the IPortNotify2 interface so we can register a program node  
        // in CDebugEngine::ResumeProcess.  
        CComPtr<IDebugDefaultPort2> spDefaultPort;  
        HRESULT hr = pPort->QueryInterface(&spDefaultPort);  
        if (SUCCEEDED(hr))  
        {  
            CComPtr<IDebugPortNotify2> spPortNotify;  
            hr = spDefaultPort->GetPortNotify(&spPortNotify);  
            if (SUCCEEDED(hr))  
            {  
                // Remember the port notify so we can use it in ResumeProcess.  
                m_spPortNotify = spPortNotify;  
  
                // Now launch the process in a suspended state and return the  
                // IDebugProcess2 interface  
                CComPtr<IDebugPortEx2> spPortEx;  
                hr = pPort->QueryInterface(&spPortEx);  
                if (SUCCEEDED(hr))  
                {  
                    // pass on the parameters we were given (omitted here)  
                    hr = spPortEx->LaunchSuspended(/* omitted paramters */,ppDebugProcess)  
                }  
            }  
        }  
        return(hr);  
    }  
  
    HRESULT CDebugEngine::ResumeProcess(IDebugProcess2 *pDebugProcess)  
    {  
        // Make a program node for this process  
        HRESULT hr;  
        CComPtr<IDebugProgramNode2> spProgramNode;  
        hr = this->GetProgramNodeForProcess(pProcess, &spProgramNode);  
        if (SUCCEEDED(hr))  
        {  
            hr = m_spPortNotify->AddProgramNode(spProgramNode);  
            if (SUCCEEDED(hr))  
            {  
                // resume execution of the process using the port given to us earlier.  
               // (Querying for the IDebugPortEx2 interface is valid here since  
               // that's how we got the IDebugPortNotify2 interface in the first place.)  
                CComPtr<IDebugPortEx2> spPortEx;  
                hr = m_spPortNotify->QueryInterface(&spPortEx);  
                if (SUCCEEDED(hr))  
                {  
                    hr  = spPortEx->ResumeProcess(pDebugProcess);  
                }  
            }  
        }  
        return(hr);  
    }  
  
    ```  
  
## See Also  
 [Getting a Port](../extensibility/getting-a-port.md)   
 [Enabling a Program to Be Debugged](../extensibility/enabling-a-program-to-be-debugged.md)