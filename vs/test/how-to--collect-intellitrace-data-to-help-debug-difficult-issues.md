---
title: "How to: Collect IntelliTrace Data to Help Debug Difficult Issues | hehe"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "IntelliTrace, configuring test settings"
  - "Diagnostic Data Adapter, InteliTrace"
  - "debugging [Visual Studio ALM], difficult issues using IntelliTrace"
  - "Test Runner, InteliTrace"
ms.assetid: 02b6716f-569e-4961-938a-e790a0c74b5c
caps.latest.revision: 92
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
# How to: Collect IntelliTrace Data to Help Debug Difficult Issues
Using [!INCLUDE[TCMext](../code-quality/includes/tcmext_md.md)] or Visual Studio, you can configure the diagnostic data adapter for IntelliTrace to collect specific diagnostic trace information. Tests can use this adapter, the test can collect significant diagnostic events for the application that a developer can use later to trace through the code to find the cause of a bug. The diagnostic data adapter for IntelliTrace can be used for either manual or automated tests.  
  
> [!NOTE]
>  IntelliTrace works only on an application that is written by using managed code. If you are testing a Web application that uses a browser as a client, you should not enable IntelliTrace for the client in your test settings because no managed code is available to trace. In this case, you may want to set up an environment and collect IntelliTrace data remotely on your Web server. For more information about environments, see [Setting Up Test Machines to Run Tests or Collect Data](../test/setting-up-test-machines-to-run-tests-or-collect-data.md).  
  
 The IntelliTrace data is stored in a file that has an extension of .iTrace. When you run your test and a test step fails, you can create a bug. The IntelliTrace file that contains the diagnostic information is automatically attached to this bug.  
  
> [!NOTE]
>  The diagnostic data adapter for IntelliTrace does not create an IntelliTrace file when a test pass is successful. It saves a file only on a failed test case or when you submit a bug.  
  
 The data that is collected in the IntelliTrace file increases debugging productivity by reducing the time that is required to reproduce and diagnose an error in your code. Additionally, because you can share the IntelliTrace file with another individual who can replicate your local session on their computer, it reduces the probability that a bug will be non-reproducible.  
  
> [!CAUTION]
>  If you enable IntelliTrace in your test settings, collecting code coverage data will not work. [!INCLUDE[crdefault](../code-quality/includes/crdefault_md.md)][Code Coverage configuration using Test Settings is deprecated](../test_notintoc/code-coverage-configuration-using-test-settings-is-deprecated.md)  
  
> [!CAUTION]
>  The diagnostic data adapter for IntelliTrace works by instrumenting a managed process, which must be performed after the tests for the test run are loaded. If the process that you want to monitor has already started, no IntelliTrace files will be collected because the process is already running. To circumvent this, make sure that the process is stopped before the tests are loaded. Then start the process after the tests are loaded or the first test is started.  
  
 The following procedure describes how to configure the IntelliTrace data that you want to collect. These steps apply to both the configuration editor in [!INCLUDE[TCMext](../code-quality/includes/tcmext_md.md)] and Test Settings dialog box in Visual Studio.  
  
> [!NOTE]
>  The user account for the test agent that is used to collect IntelliTrace data must be a member of the administrators group. For more information, see [Install and configure test agents](../test/install-and-configure-test-agents.md).  
  
## Configure the Data to Collect with the IntelliTrace Diagnostic Data Adapter  
 Before you perform the steps in this procedure, you must open your test settings from either [!INCLUDE[TCMext](../code-quality/includes/tcmext_md.md)] or Visual Studio and select the **Data and Diagnostics** page.  
  
#### To configure the data to collect with the IntelliTrace Diagnostic Data Adapter  
  
1.  Select the role to use to collect IntelliTrace data.  
  
2.  Select **IntelliTrace**.  
  
3.  If you are adding IntelliTrace for a Web client role or for an ASP.NET Web application, you must also select **ASP.NET Client Proxy for IntelliTrace and Test Impact**.  
  
     This proxy enables you to collect information about the http calls from a client to a Web server for the IntelliTrace and Test Impact diagnostic data adapters.  
  
    > [!WARNING]
    >  If you decide to use a custom account for the identity that is being used for the application pool on the Internet Information Server (IIS) where you intend to collect Intellitrace data, you must create the local user profile on the IIS machine for the custom account that is being used. You can create the local profile for the custom account either by logging on to the IIS machine locally one time or by running the following command line by using the custom account credentials:  
    >   
    >  **runas /user:domain\name /profile cmd.exe**  
  
4.  Choose **Configure** for **IntelliTrace** to modify default IntelliTrace settings.  
  
     The dialog box to configure the data that will be collected is displayed.  
  
    > [!CAUTION]
    >  If you enable collecting IntelliTrace data, collecting code coverage data will not work.  
  
5.  Choose the **General** tab. Select **IntelliTrace events only** to record significant diagnostic events that have minimal impact on performance when you test.  
  
     **-**or-  
  
     Select **IntelliTrace events and call information** to record diagnostic events and method level tracing that shows call information. This level of tracing might have performance impact when you run your tests.  
  
6.  To collect data from your [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] application that is running on Internet Information Services, select **Collect data from ASP.NET applications that are running on Internet Information Services**. Set up and configure your test agent on the Web server role. See [Install and configure test agents](../test/install-and-configure-test-agents.md).  
  
7.  Choose the **Modules** tab. Select either **Collect data from all modules except for the following** and use **Add** to add to the list of modules and **Remove** to remove a module. This option lets you include all the modules that are running on the system except the modules that you specify.  
  
     -or-  
  
     Select **Collect data from only the following modules** and use **Add** to add to the list of modules and **Remove** to remove a module. This option lets you specify exactly which modules you want.  
  
    > [!NOTE]
    >  If possible, select the specific processes that you want to monitor. This is recommended for optimum performance.  
  
8.  Choose the **Processes** tab. Select **Collect data from all processes except for the following** and use **Add** to add to the list of processes and **Remove** to remove a process. This option lets you include all the processes that are running on the system except the processes that you specify.  
  
     -or-  
  
     Select **Collect data from specified processes only** and use **Add** to add to the list of processes and **Remove** to remove a process. This option lets you specify exactly which processes you want.  
  
9. (Optional) Choose the **IntelliTrace Events** tab. Select or clear each IntelliTrace event category that you want to include or exclude when you collect diagnostic events.  
  
10. (Optional) Expand each IntelliTrace event category and select or clear each specific event that you want to include or exclude in the IntelliTrace events.  
  
    > [!NOTE]
    >  For more information, see [Configure IntelliTrace](http://msdn.microsoft.com/en-us/7657ecab-e07e-4b1b-872d-f05d966be37e).  
  
11. (Optional) Choose the **Advanced** tab. Next, choose the arrow next to **Maximum amount of disk space for recording** and select the maximum size that you want to enable for the IntelliTrace file to use.  
  
    > [!NOTE]
    >  If you increase the size of the recording, a time-out issue might occur when you save this recording together with your test results. For more information about how to increase the time-out values for diagnostic data adapters, see [How to: Prevent Time-Outs for Diagnostic Data Adapters](../test/how-to--prevent-time-outs-for-diagnostic-data-adapters.md).  
  
12. If you are using [!INCLUDE[TCMext](../code-quality/includes/tcmext_md.md)], choose **Save**. If you are using Visual Studio, choose **OK**. The IntelliTrace settings are now configured and saved for your test settings.  
  
    > [!NOTE]
    >  To reset the configuration for this diagnostic data adapter, choose **Reset to default configuration** for Visual Studio or **Reset to default** for [!INCLUDE[TCMext](../code-quality/includes/tcmext_md.md)].  
  
 **Guidance**  
  
 For more information, see [Testing for Continuous Delivery with Visual Studio 2012 – Chapter 6: A Testing Toolbox](http://go.microsoft.com/fwlink/?LinkID=255203).  
  
## See Also  
 [Collect more diagnostic data](../test/collect-more-diagnostic-data-in-manual-tests.md)   
 [Create Test Settings for Automated System Tests Using Microsoft Test Manager](../test_notintoc/create-test-settings-for-automated-system-tests-using-microsoft-test-manager.md)   
 [Specifying Test Settings for Visual Studio Tests](../test/specifying-test-settings-for-visual-studio-tests.md)   
 [Setting Up Machines and Collecting Diagnostic Information Using Test Settings](../test/setting-up-machines-and-collecting-diagnostic-information-using-test-settings.md)   
 [Using IntelliTrace](../debugger/intellitrace.md)   
 [Including Diagnostic Trace Data with Bugs that are Difficult to Reproduce](../test_notintoc/including-diagnostic-trace-data-with-bugs-that-are-difficult-to-reproduce.md)