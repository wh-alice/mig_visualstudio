---
title: "Walkthrough: Command-Line Profiling Using Instrumentation"
ms.custom: na
ms.date: "10/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "profiling tools, walkthroughs"
  - "performance tools, walkthroughs"
  - "performance tools, command-line tools"
ms.assetid: 1c6f1586-3d6a-431f-bedf-c54088e280ba
caps.latest.revision: 15
ms.author: "mikejo"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Walkthrough: Command-Line Profiling Using Instrumentation
This walkthrough takes you through profiling a [!INCLUDE[dnprdnshort](../VS_debugger/includes/dnprdnshort_md.md)] stand-alone application to collect detailed timing and call count data by using the instrumentation method of the Profiling Tools. In this walkthrough, you will accomplish the following tasks:  
  
-   Use the [VSInstr](../VS_IDE/vsinstr.md) command line tool to generate instrumented binaries.  
  
-   Use the [VSPerfCLREnv](../VS_IDE/vsperfclrenv.md) tool to set the environment variables to collect .NET profiling data.  
  
-   Use the [VSPerfCmd](../VS_IDE/vsperfcmd.md) tool to collect profiling data.  
  
-   Use the [VSPerfReport](../VS_IDE/vsperfreport.md) tool to generate file-based reports of the profiling data.  
  
## Prerequisites  
  
-   [!INCLUDE[vsprvsts](../dv_TeamTestALM/includes/vsprvsts_md.md)]  
  
-   Intermediate understanding of C#  
  
-   Intermediate understanding of working with command-line tools  
  
-   A copy of the [PeopleTrax Sample](../VS_IDE/peopletrax-sample--profiling-tools-.md)  
  
-   To work with the information provided by profiling, it is best to have debugging symbol information available. For more information, see [How to: Reference Windows Symbol Information](../VS_IDE/how-to--reference-windows-symbol-information.md).  
  
## Command Line Profiling Using the Instrumentation Method  
 Instrumentation is a profiling method by which specially built versions of the profiled binaries contain probe functions that collect timing information at the entry and exit to functions in an instrumented module. Because this method of profiling is more invasive than sampling, it incurs a greater amount of overhead. Instrumented binaries are also larger than debug or release binaries and are not intended for deployment.  
  
> [!NOTE]
>  Do not send instrumented binaries to your customers. Instrumented binaries can contain several risks. The binaries include information that makes your application easier to reverse engineer, as well as security risks.  
  
#### To profile the PeopleTrax application by using the instrumentation method  
  
1.  Install the PeopleTrax sample application and build the Release version.  
  
2.  Open a command prompt window and add the **Profiling Tools** directory to the local Path environment variable.  
  
3.  Change the working directory to the directory containing the PeopleTrax binaries.  
  
4.  Create a directory to contain the file based reports. Type the following command:  
  
    ```  
    md Reports  
    ```  
  
5.  Use the VSInstr command-line tool to instrument the binaries in the application. Type the following commands on separate command lines:  
  
    ```  
    VSInstr PeopleTrax.exe  
    VSInstr PeopleTrax.exe  
    VSInstr People.dll  
    VSInstr Person.dll  
    VSInstr Operation.dll  
    ```  
  
     **Note** By default, VSInstr saves a non-instrumented backup of the original file. The backup file name has the extension .orig. For example, the original version of "MyApp.exe" would be saved as "MyApp.exe.orig."  
  
6.  Type the following command to set the appropriate environment variables:  
  
    ```  
    VsPerfCLREnv /traceon  
    ```  
  
7.  To start the profiler, type the following command:  
  
    ```  
    VsPerfCmd /start:trace /output:Reports\Report.vsp  
    ```  
  
8.  After you start the profiler in trace mode, run the instrumented version of the PeopleTrax.exe process to collect data.  
  
     The **PeopleTrax** application window appears.  
  
9. Click **Get People**.  
  
     The PeopleTrax data grid populates with data.  
  
10. Click **Export Data**.  
  
     Notepad starts and displays a new file that contains a list of people from the **PeopleTrax** application.  
  
11. Close Notepad, and then close the **PeopleTrax** application.  
  
12. Shut down the profiler. Type the following command:  
  
    ```  
    VSPerfCmd /shutdown  
    ```  
  
13. Type the following command to reset the environmental variables:  
  
    ```  
    VSPerfCLREnv /off  
    ```  
  
14. Use the VSPerfReport tool to generate or comma-separated value (.csv) report files. Type:  
  
    ```  
    VSPerfReport Reports\Report.vsp /output:Reports /summary:all  
    ```  
  
     You can analyze the generated reports in a spreadsheet program, or you can use the [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] IDE to analyze the profiling data in the Report.vsp file. For more information, see [Analyzing Performance Tools Data](../VS_IDE/analyzing-performance-tools-data.md).  
  
## See Also  
 [Performance Session Overview](../VS_IDE/performance-session-overview.md)   
 [Profiling from the Command-Line](../VS_IDE/using-the-profiling-tools-from-the-command-line.md)   
 [VSPerfCmd](../VS_IDE/vsperfcmd.md)   
 [Understanding Sampling Data Values](../VS_IDE/understanding-sampling-data-values.md)   
 [Performance Report Views](../VS_IDE/performance-report-views.md)