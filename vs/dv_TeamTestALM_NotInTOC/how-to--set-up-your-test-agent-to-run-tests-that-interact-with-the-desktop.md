---
title: "How to: Set Up Your Test Agent to Run Tests that Interact with the Desktop"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "agents, configuring for interaction with desktop"
ms.assetid: 3a94dd07-6d17-402c-ae8f-7947143755c9
caps.latest.revision: 41
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
# How to: Set Up Your Test Agent to Run Tests that Interact with the Desktop
If you want to run automated tests that interact with the desktop, you must set up your agent to run as a process instead of a service. For example, if you want to run a coded UI test remotely using a test controller and test agent, or you want to run a test and capture a video recording when you run it, you must set up your agent to run as a process. When you assign agents to roles in your test settings using Visual Studio, or you assign agents to roles in your environment by using [!INCLUDE[TCMext](../dv_TeamTestALM/includes/tcmext_md.md)], you must change the set up for any agents assigned to roles that have to interact with the desktop. For more information about test settings, roles and environments, see [Setting Up Test Machines to Run Tests or Collect Data](../dv_TeamTestALM/setting-up-test-machines-to-run-tests-or-collect-data.md).  
  
> [!WARNING]
>  If you use [!INCLUDE[TCMext](../dv_TeamTestALM/includes/tcmext_md.md)] to set up a lab environment, the test agent is installed by [!INCLUDE[TCMshort](../dv_TeamTestALM/includes/tcmshort_md.md)]. You can specify in the environment creation wizard that you want to configure one of the roles to run coded UI tests. For more information, see [Creating Lab Environments](../dv_TeamTestALM/creating-lab-environments.md).  
  
> [!IMPORTANT]
>  The computer that is running an agent on which you want to run coded UI tests cannot be locked or have an active screen saver.  
  
 If you are running coded UI tests that start a browser, the service account for the test agent is used to start that browser. This service account must be the same as the user account that is the active user on this computer. If it is not the same user account, the browser will not start.  
  
> [!IMPORTANT]
>  If you are running a coded UI test that starts a browser as part of a build definition, the service account for the build service is used to start that browser. This service account must be the same as the user account that is the active user on this computer. If it is not the same user account, the browser will not start. For more information about how to run tests as part of the build process, see [How to: Configure and Run Scheduled Tests After Building Your Application](assetId:///32acfeb1-b1aa-4afb-8cfe-cc209e6183fd).  
  
 Use the following procedure to set up any agents that are assigned to a role that performs a task that needs to interact with the desktop.  
  
### To set up an agent to run as a process  
  
1.  To configure the test agent you have installed to run as a process, go to **Start**, **All Programs**, **Microsoft Visual Studio**, **Microsoft Visual Studio Test Agent Configuration Tool**.  
  
     The **Configure Test Agent** dialog box is displayed.  
  
2.  To view the page to select to run as a process, choose **Run Options**.  
  
     The page that enables you to choose to run the agent as a process or a service is displayed.  
  
3.  Select **Interactive Process**. The test agent will be started as a process instead of a service. Choose **Next**.  
  
     You can now enter the details for the user to use when you start the test agent as a process, and other options.  
  
    > [!NOTE]
    >  The user who you add to start the process must also be added as a member of the TeamTestAgentService group on the computer for the test controller for this agent. If this user is the current user, when you add this user to the test controller computer, you must log off or reboot this computer.  
  
4.  Type the name in **User name**.  
  
5.  Type the password in **Password**.  
  
     **Important user account information:**  
  
    -   Null passwords are not supported for user accounts.  
  
    -   If you want to use the IntelliTrace or the network emulation data and diagnostic adapter, the user account must be a member of the Administrators group. If the machine that is running the test agent is using [!INCLUDE[wiprlhext](../dv_TeamTestALM/includes/wiprlhext_md.md)] or later versions, or any OS that has Least-Privileged User Account, you have to run it as an administrator also (elevated).If the agent user name is not in the agent service it will try to add it, which requires permissions on the test controller.  
  
    -   The user trying to use the test controller must be in the test controller's Users account or the they will not be able to run the tests against the controller.  
  
6.  To make sure that a computer that has a test agent can run tests after rebooting, you can set up the computer to log on automatically as the test agent user. Select **Log on automatically**. This will store the user name and password in an encrypted form in the registry.  
  
    > [!NOTE]
    >  When you are connected to the lab environment using a remote desktop or guest-based connection, you might experience frequent, unexpected disconnects. One possible cause of the loss of the connection is that the machine is configured to automatically log onto the network.  
  
7.  To make sure that the screen saver is disabled because this might interfere with any automated tests that must interact with the desktop, select **Ensure screen saver is disabled**.  
  
    > [!CAUTION]
    >  There are security risks if you log on automatically or disable the screen saver. By enabling automatic log on, you enable other users to start this computer and to be able to use the account that automatically logs on. If you disable the screen saver, the computer might not prompt for a user to log on to unlock the computer. This enables anyone to access the computer if they have physical access to the computer. If you enable these features on a computer, you should make sure that these computers are physically secure. For example, these computers are located in a physically secure lab. If you clear **Ensure screen saver is disabled**, this does not enable your screen saver.  
  
     To change the agent back to run as a service, you can use this tool and select **Service**.  
  
8.  To apply your changes, choose **Apply Settings**.  
  
     A **Configuration summary** dialog box is displayed that shows the status of each of the steps to configure your test agent.  
  
9. To close the **Configuration summary** dialog box, choose **Close**. Then choose **Close** again to close the Test Agent Configuration Tool.  
  
    > [!NOTE]
    >  There is a notification area icon that runs on the computer for a test agent that is running as a process. It shows the status of the test agent. You can start, stop or restart the agent if it is running as a process using this tool. To start the test agent as a process if it is not running, choose **Start**, **All Programs**, **Microsoft Visual Studio**, **Microsoft Visual Studio Test Agent**.  
  
     If the test controller for this test agent is registered with [!INCLUDE[esprtfs](../dv_TeamTestALM/includes/esprtfs_md.md)], the status of a test agent that is running as an interactive process is displayed in the **Controllers** view in the **Lab Center** for [!INCLUDE[TCMext](../dv_TeamTestALM/includes/tcmext_md.md)]. It is listed with a preceding asterisk symbol to denote that it is running as an interactive process. To restart this test agent you must use the tool that runs on the computer for the test agent and not the **Controllers** view.  
  
## See Also  
 [How to: Configure and Run Scheduled Tests After Building Your Application](assetId:///32acfeb1-b1aa-4afb-8cfe-cc209e6183fd)   
 [Setting Up Test Machines to Run Tests or Collect Data](../dv_TeamTestALM/setting-up-test-machines-to-run-tests-or-collect-data.md)   
 [Install and configure test agents](../dv_TeamTestALM/install-and-configure-test-agents.md)