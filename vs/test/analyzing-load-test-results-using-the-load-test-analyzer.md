---
title: "Analyzing Load Test Results Using the Load Test Analyzer | hehe"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "load tests, test results"
  - "load tests, analyzing test results"
  - "load tests, managing test results"
ms.assetid: 8a4ba300-425d-447c-91d9-c53f4345feee
caps.latest.revision: 38
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
# Analyzing Load Test Results Using the Load Test Analyzer
Find bottlenecks, identify errors, and measure improvements in your app when you use the Load Test Analyzer. Analyze load test results in these ways:  
  
-   Monitor a load test when it is running.  
  
-   Analyze a load test after it has completed.  
  
-   View results from a previous load test.  
  
 You can also create reports that compare two or more reports for trend analysis to share with stakeholders. See [Reporting Load Tests Results for Test Comparisons or Trend Analysis](../test/reporting-load-tests-results-for-test-comparisons-or-trend-analysis.md).  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
 You can complete these tasks whether you run your load test from Visual Studio Enterprise or from the command line, and whether you run your load test on a single computer or on a remote machine.  
  
## Differences between Analyzing a Running and a Completed Load Test  
 When you run a load test, the Load Test Analyzer displays in a separate tab, together with the name of your load test and the time that the test was started (for example, **LoadTest1 [12:40 PM]**). When a load test runs, a smaller set of the performance counter data is maintained in memory. You can monitor this set of data when your load test runs. After a load test has completed, you can analyze the full set of data from the database. Differences exist in what data is displayed when a load test runs and what data that you can see after a load test has completed. For example, 90 percent and 95 percent response time data is not calculated until the load test has completed. Some differences also occur in the functionality of the tools that are available to analyze the data.  
  
 When you run the load test, two views are available: The Graphs view and the Tables view. The Graphs view allows you to graph performance counters that are collected. The Tables view gives you information about each of the tests, pages, transactions, and requests that are collected. You also get a table that lists the errors.  
  
 By default, when the load test run has completed, the Summary view is displayed. You can switch between the Summary, Graphs, Tables, and Details views by using the toolbar. The Load Test Analyzer can be docked or set to float by using the usual [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] window manipulation techniques. When you analyze completed load test runs, you can have multiple Load Test Analyzers open at the same time to compare the different load test runs.  
  
 For a more comprehensive overview of the Load Test Analyzer, see [Load Test Analyzer Overview](../test/load-test-analyzer-overview.md).  
  
## Tasks  
  
|Tasks|Associated topics|  
|-----------|-----------------------|  
|**Accessing the results of your load test:** When you run a load test from the Load Test Editor, the load test results open automatically and the running load test is displayed in the Load Test Analyzer.|-   [How to: Access Load Test Results for Analysis](../test/how-to--access-load-test-results-for-analysis.md)|  
|**Add analysis notes to your load test:** You can add comments to your load test when you conduct your analysis. The comments are stored permanently, together with the load test result. The description that you enter also displays in the **Description** column that is associated with the load test in the Open and Manage Test Results dialog box in the Load Test Editor.<br /><br /> For more information, see [How to: Access Load Test Results for Analysis](../test/how-to--access-load-test-results-for-analysis.md).<br /><br /> Additionally, the comments are displayed when you create an Excel report for the load test results.<br /><br /> For more information, see [Reporting Load Tests Results for Test Comparisons or Trend Analysis](../test/reporting-load-tests-results-for-test-comparisons-or-trend-analysis.md).|-   [How to: Add Comments while Analyzing a Completed Load Test](../test/e6b68940-4fb6-4bd6-bcde-f6477adc7af9.md)|  
|**Analyzing the results of your load test:** After you access the load test run data, you can analyze the resulting data. You can view the Load Test Summary to understand the results quickly. The load test summary shows the key results in a compact and easily read format.<br /><br /> You can print the load test summary. This makes it convenient to use when you communicate results to stakeholders.<br /><br /> You can analyze the details of your load test results by using the graphs and tables in the results. These include Errors, Pages, Requests, SQL Trace, Tests, Thresholds, and Transactions.|-   [Load Test Analyzer Overview](../test/load-test-analyzer-overview.md)<br />-   [Load Test Results Summary Overview](../test/load-test-results-summary-overview.md)<br />-   [How to: View Web Page Response](../test/how-to--view-web-page-response-time-in-a-load-test-using-the-load-test-analyzer.md)<br />-   [Analyzing Threshold Rule Violations](../test/analyzing-threshold-rule-violations-in-load-tests-using-the-load-test-analyzer.md)<br />-   [Analyzing Load Test Results in the Graphs View](../test/analyzing-load-test-results-in-the-graphs-view-of-the-load-test-analyzer.md)<br />-   [Analyzing Load Test Results and Errors in the Tables View](../test/0a84bda3-6051-45eb-9c7f-d57419e1f97d.md)|  
|**Analyzing the virtual user activity in your load test results to isolate performance issues:** You can use the Virtual User Activity Chart to visualize what virtual users are doing during a load test. This can help you isolate spikes in a CPU or drops in requests/sec, and determine which tests or pages are running during these spikes and drops.|-   [Analyzing Virtual User Activity in the Details View](../test/63f4bd42-3cfb-4eee-af68-e8334976539e.md)|  
  
## Related Tasks  
 [Running Load and Web Performance Tests](http://msdn.microsoft.com/en-us/a4fd686e-69ec-485d-a335-acf12348aa30)  
  
 Before you conduct analysis of a load test, you must run a test one or more times. You can observe the test results in real time when the test is running.  
  
 [Managing Load Test Results in the Load Test Results Repository](../test/managing-load-test-results-in-the-load-test-results-repository.md)  
  
 When you run your load tests, any information that is gathered during a load test run may be stored in the Load Test Results Repository, which is an SQL database. The Load Test Results Repository contains performance counter data and any information about recorded errors.  
  
 You can manage load test results from the Load Test Editor by using the Open and Manage Load Test Results dialog box. You can open, import, export, and remove load test results.  
  
 [Reporting Load Tests Results for Test Comparisons or Trend Analysis](../test/reporting-load-tests-results-for-test-comparisons-or-trend-analysis.md)  
  
 You can create a [!INCLUDE[ofprexcel](../code-quality/includes/ofprexcel_md.md)] report to help determine issues and discover trends. The reports can be shared with the stakeholders without requiring their access to the Team Foundation Server.  
  
## External resources  
  
### Guidance  
 [Testing for Continuous Delivery with Visual Studio 2012 – Chapter 6: A Testing Toolbox](http://go.microsoft.com/fwlink/?LinkID=255203)  
  
## See Also  
 [Creating and Editing Load and Web Performance Tests](http://msdn.microsoft.com/en-us/a3e3e7e6-46fc-45b1-b999-f461773f071b)   
 [Web performance and load tests in Visual Studio](../test_notintoc/web-performance-and-load-tests-in-visual-studio.md)   
 [Reviewing Test Results in Microsoft Test Manager](http://msdn.microsoft.com/en-us/9fb3e429-78df-4fe2-89ed-0ad1db0738f4)   
 [Reporting Load Tests Results for Test Comparisons or Trend Analysis](../test/reporting-load-tests-results-for-test-comparisons-or-trend-analysis.md)