---
title: "How to: Access Load Test Results for Analysis | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "results, load test"
  - "load test results, accessing"
  - "Load Test Viewer"
  - "load tests, accessing"
  - "load tests, analyzing"
  - "load tests, results"
  - "Load Test Viewer, viewing"
ms.assetid: b0a3e694-2894-479b-b270-7e61e9fafacd
caps.latest.revision: 52
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
# How to: Access Load Test Results for Analysis
When you run a load test from the Load Test Editor, the load test results open automatically and the running load test is displayed in the Load Test Analyzer. When you run a load test from the command line, you must access the load test results manually. For more information about the different ways to run a load test, see [Running Load Tests](../test_notintoc/running-load-tests.md).  
  
 The load test result for the completed load test contains performance counter samples and error information that was collected periodically from the computers-under-test. A large number of performance counter samples can be collected over the course of a load test run. The amount of performance data that is collected depends on the length of the test run, the sampling interval, the number of computers under test, the number of counters being collected, the data collectors that are configured, and the logging levels. For a large load test, the amount of performance data that is collected can easily be several gigabytes. For more information, see [Distributing Load Test Runs Across Multiple Test Machines Using Test Controllers and Test Agents](../test/6e67a587-8aad-48cc-a8c0-6d4b399f3731.md) and [Considerations for Load Testing](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337).  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
## Load Test Analyzer Procedures  
  
#### To access a load test result  
  
1.  From a Web performance and load test project, open a load test.  
  
2.  In the Load Test Editor's toolbar, choose the **Open and Manage Results** button.  
  
     The **Open and Manage Results** dialog box appears.  
  
3.  In **Enter a controller name to find load test results**, select a controller. Select **\<local> - No controller** to access results stored locally.  
  
4.  In **Show results for the following load test**, select the load test whose results you want to view. Select **\<Show results for all tests>** to see all results for all tests.  
  
     If there are load test results available, they appear in the **Load test results** list. The columns are **Time**, **Duration**, **User**, **Outcome**, **Test**, and **Description**. **Test** contains the name of the test, and **Description** contains the optional description that is added before the test is run.  
  
    > [!NOTE]
    >  The results appear with the most recent results at the top of the list.  
  
5.  In the **Load test results** list, select the load test results you want to analyze and choose **Open**.  
  
6.  The Load Test Analyzer appears. The selected load test result is displayed in the Summary view. For more information, see [Load Test Results Summary Overview](../test/load-test-results-summary-overview.md).  
  
     You can manage other aspects of load test results in the Open and Manage Results dialog box including importing, exporting, and removing load test results. For more information, see [Managing Load Test Results in the Load Test Results Repository](../test/managing-load-test-results-in-the-load-test-results-repository.md).  
  
## See Also  
 [Analyzing Load Test Results](../test/analyzing-load-test-results-using-the-load-test-analyzer.md)   
 [Creating and Editing Load and Web Performance Tests](http://msdn.microsoft.com/en-us/a3e3e7e6-46fc-45b1-b999-f461773f071b)