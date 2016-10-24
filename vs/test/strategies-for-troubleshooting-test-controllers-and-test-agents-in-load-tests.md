---
title: "Strategies for Troubleshooting Test Controllers and Test Agents in Load Tests | testtitle"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "load tests, test controllers"
  - "load tests, troubleshooting"
  - "load tests, test agents"
  - "troubleshooting, test controllers and agents in load tests"
ms.assetid: 77329348-3a5d-43de-b6cb-90f93296a081
caps.latest.revision: 30
ms.author: "ahomer"
manager: "douge"
translation.priority.ht: 
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
# Strategies for Troubleshooting Test Controllers and Test Agents in Load Tests
Common problems that might happen when you work with test controllers and test agents in Visual Studio Enterprise:  
  
 [Unable to Collect Performance Counters on Test Agent Computer](#UnableToCollectVistaPerfCounters)  
  
 [Setting the Logging Level on a Test Controller Computer](#Logging)  
  
 [Binding a Test Controller to a Network Adapter](#BindToNIC)  
  
##  <a name="UnableToCollectVistaPerfCounters"></a> Unable to Collect Performance Counters on Test Agent Computer  
 When you run a load test, you might receive errors when you try to connect to a test agent computer and collect performance counters. The Remote Registry service is the service responsible for providing performance counter data to a remote computer. By default, on computers that run [!INCLUDE[wiprlhext](../debugger/includes/wiprlhext_md.md)], the Remote Registry service does not start automatically. To fix this problem, manually start the Remote Registry service.  
  
> [!NOTE]
>  You can access the Remote Registry service in **Control Panel.** Choose **Administrative Tools** and then choose **Services**.  
  
 Another cause of this problem is that you do not have sufficient permissions to read performance counters. For local test runs, the account of the user who is running the test must be a member of the Power Users group or higher, or be a member of the Performance Monitor Users group. For remote test runs, the account that the controller is configured to run as must be a member of the Power Users group or higher, or be a member of the Performance Monitor Users group.  
  
##  <a name="Logging"></a> Setting the Logging Level on a Test Controller Computer  
 You can control the level of logging on a test controller computer. This is useful when you are trying to diagnose a problem when you are running a load test on an environment.  
  
#### To set the logging level on a test controller computer  
  
1.  Stop the test controller service. At a command prompt, type `net stop vsttcontroller`.  
  
2.  Open the file QTController.exe.config. This file is located in the controller installation directory.  
  
3.  Edit the entry for the `EqtTraceLevel` switch in the system diagnostics section of the file. Your code should resemble this:  
  
    ```  
    <system.diagnostics>  
        <trace autoflush="true" indentsize="4">  
            <listeners>  
                <add name="myListener" type="System.Diagnostics.TextWriterTraceListener" initializeData="d:\VSTestHost.log" />  
            </listeners>  
        </trace>  
        <switches>  
            <!-- You must use integral values for "value":  
                    0 = off,   
                    1 = error,  
                    2 = warn,  
                    3 = info,   
                    4 = verbose. -->  
            <add name="EqtTraceLevel" value="4" />  
        </switches>  
    </system.diagnostics>  
    ```  
  
4.  Save the file.  
  
5.  Start the controller service. At a command prompt, type `net start vsttcontroller`.  
  
 This applies to the test controller, the test agent service, and the test agent process. When diagnosing problems, it is helpful to enable logging on all three processes. The procedure to set the logging level is the same for all three processes, as specified earlier for the test controller. To set the logging levels for the test agent service and the agent process, use the following configuration files:  
  
-   **QTController.exe.config** Conttoller service  
  
-   **QTAgentService.exe.config** Agent service  
  
-   **QTDCAgent(32).exe.config** Agent data adapter process for 32 bit architecture.  
  
-   **QTDCAgent(64).exe.config** Agent data adapter process for 64 bit architecture.  
  
-   **QTAgent(32).exe.config** Agent test process for 32 bit architecture.  
  
-   **QTAgent(64).exe.config** Agent test process for 64 bit architecture.  
  
##  <a name="BindToNIC"></a> Binding a Test Controller to a Network Adapter  
 When you try to set up a test agent, you might receive the following error:  
  
 **Error 8110. Can not connect to the specified controller computer or access the controller object.**  
  
 This error can be caused by installing the test controller on a computer that has more than one network adapter.  
  
> [!NOTE]
>  It is also possible to install test agents successfully, and not see this problem until you try to run a test.  
  
 To fix this error, you must bind the test controller to one of the network adapters. You have to set the `BindTo` property on the test controller, and then change the test agent to refer to the test controller by IP address instead of by name. The steps are provided in the following procedures.  
  
#### To obtain the IP address of the network adapter  
  
1.  Choose **Start**, and then choose **Run**.  
  
     The **Run** dialog box is displayed.  
  
2.  Type `cmd` and then choose **OK**.  
  
     A command prompt opens.  
  
3.  Type `ipconfig /all`.  
  
     The IP addresses for your network adapters are displayed. Record the IP address of the network adapter that you want to bind your controller to.  
  
#### To bind a test controller to a network adapter  
  
1.  Stop the test controller service. At a command prompt, type `net stop vsttcontroller`.  
  
2.  Open the file QTController.exe.config. This file is located in \<drive letter:>\Program Files (x86)\Microsoft Visual Studio 12.0\Common7\IDE\\.  
  
3.  Add an entry for the `BindTo` property to the application settings. Specify the IP address of the network adapter that you want to bind the controller to. Your code should resemble this:  
  
    ```  
    <appSettings>  
        <add key="LogSizeLimitInMegs" value="20" />  
        <add key="AgentSyncTimeoutInSeconds" value="120" />  
        <add key="ControllerServicePort" value="6901" />  
        <add key="ControllerUsersGroup" value="TeamTestControllerUsers" />  
        <add key="ControllerAdminsGroup" value="TeamTestControllerAdmins" />  
        <add key="CreateTraceListener" value="no" />  
        <add key="BindTo" value="<YOUR IP ADDRESS>" />  
    </appSettings>  
    ```  
  
4.  Save the file.  
  
5.  Start the test controller service. At a command prompt, type `net start vsttcontroller`.  
  
#### To connect a test agent to a bound controller  
  
-   Run the test agent installation again. This time, specify the IP address for the test controller instead of the test controller name.  
  
 This applies to the test controller, the test agent service, and the test agent process. The `BindTo` property must be set for each process that is running on a computer that has more than one network adapter. The procedure to set the `BindTo` property is the same for all three processes, as specified earlier for the test controller. To set the logging levels for the test agent service and the test agent process, use the configuration files that are listed in [Setting the Logging Level on a Test Controller Computer](#Logging).  
  
## See Also  
 [Distributing Load Test Runs Across Multiple Test Machines Using Test Controllers and Test Agents](../test/6e67a587-8aad-48cc-a8c0-6d4b399f3731.md)   
 [Configuring Test Controllers and Test Agents for Load Testing](../test/configuring-test-controllers-and-test-agents-for-load-testing.md)