---
title: "Configuring Load Test Run Settings"
ms.custom: ""
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "load tests, configuring run settings"
ms.assetid: 0c86918b-cd63-4468-8f49-6d547a1276dc
caps.latest.revision: 48
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
# Configuring Load Test Run Settings
*Run settings* are a set of properties that influence the way a load test runs. Run settings are organized by categories in the Properties window.  
  
 You can have more than one run setting in a load test. Only one of the run settings may be active for a load test run. The other run settings provide a quick way to select an alternative setting to use for subsequent test runs.  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
 The initial run setting is created when you create a load test by using the New Load Test Wizard. For more information, see [Creating load tests](../test_notintoc/creating-load-tests.md).  
  
 ![Load Test Run Settings](../test/media/loadtestrunsettings.png "LoadTestRunSettings")  
Load Test Run Settings  
  
## Tasks  
  
|Tasks|Associated Topics|  
|-----------|-----------------------|  
|**Add more run settings to your load test:** In addition to the run setting that is created when you run the New Load Test Wizard, you can add more run settings to your load test so that you can run the test under different conditions.|-   [How to: Add Additional Run Settings to a Load Test](../test/how-to--add-additional-run-settings-to-a-load-test.md)|  
|**Specify the active run setting to use with the load test:** You can select the run setting that you want to use with your load test using the Load Test Editor. The active run setting is identified by the "[Active]" suffix.|-   [How to: Select the Active Run Setting for a Load Test](../test/how-to--select-the-active-run-setting-for-a-load-test.md)|  
|**Edit run setting properties:** You can edit your run setting properties for such things as logging options (see more below), determining the length of the test, warm-up duration, maximum number of error details reported, sampling rate, connection model (Web performance tests only), results storage type, validation level and SQL tracing. The run settings should reflect the goals of your load test.|-   [Load Test Run Settings Properties](../test/load-test-run-settings-properties.md)<br />-   [Changing Run Setting Properties](../test/load-test-run-settings-properties.md#LoadTestRunSettingsHowToChange)|  
|**Specify test iteration count in load test run settings:** You can specify the number of times to run all of the Web performance and unit tests in all of the scenarios of your load tests by configuring the **Test Iterations** property.|-   [How to: Specify the Number of Test Iterations in a Run Setting](../test/how-to--specify-the-number-of-test-iterations-in-a-load-test-run-setting.md)|  
|**Specify the sampling rate for a load test run setting:** You can specify how frequently to have the load test collect performance counter data by configuring the **Sample Rate** property.|-   [How to: Specify the Sample Rate](../test/how-to--specify-the-sample-rate-for-a-load-test-run-setting.md)|  
|**Specify the timing details storage option:** You can specify how you want the details of the load test saved by configuring the **Timing Details Storage** property.|-   [How to: Specify the Timing Details Storage Property](../test/how-to--specify-the-timing-details-storage-property-for-a-load-test-run-setting.md)|  
|**Specify the test resource retention period:** Speed up the test > fix > retest cycle by retaining the test resources for a specified period by setting the **Resources Retention Time** property.|-   [Retain the resources to speed up load testing](https://www.visualstudio.com/docs/test/performance-testing/getting-started/getting-started-with-performance-testing#retain-resources)|  
|**Use context parameters:** You can use context parameters to parameterize a string. For example, if your load test contains a Web performance tests that uses a parameterized Web server, you can add a context parameter to the run settings that maps to a different server.|-   [How to: Add Context Parameters to a Run Setting](../test/how-to--add-context-parameters-to-a-load-test-run-setting.md)|  
|**Configuring test logging properties:** You can configure how frequently data is written to the log that is associated with you load test run settings. This can be important when you are running a large or complex load test because the log could become several gigabytes. [!INCLUDE[crdefault](../code-quality/includes/crdefault_md.md)][Considerations for Load Testing](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337).<br /><br /> You can also configure the log file to be automatically saved when your load test fails to help in debugging and analyzing your application.|-   [Modifying Load Test Logging Settings](../test/modifying-load-test-logging-settings.md)|  
|**Configuring SQL properties to collect SQL Server data:** You can use the SQL tracing tool in your load tests to help you monitor and improve the performance of your Web applications that use SQL Server to store data.|-   [Collecting SQL Trace Data to Monitor and Improve Performance in Load Tests](../test_notintoc/collecting-sql-trace-data-to-monitor-and-improve-performance-in-load-tests.md)|  
  
## External resources  
  
### Guidance  
 [Testing for Continuous Delivery with Visual Studio 2012 – Chapter 6: A Testing Toolbox](http://go.microsoft.com/fwlink/?LinkID=255203)  
  
## See Also  
 [Creating and Editing Load Tests](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337)   
 [Running Load Tests](../test_notintoc/running-load-tests.md)