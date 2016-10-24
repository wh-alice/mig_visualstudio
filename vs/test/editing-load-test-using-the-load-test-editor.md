---
title: "Editing Load Test Using the Load Test Editor | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Load Test Editor"
  - "load tests, Load Test Editor"
ms.assetid: ba16ed02-137e-40bf-a4cb-45d87d922d37
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
# Editing Load Test Using the Load Test Editor
Edit existing load tests by using the Load Test Editor. Before you can edit a load test, you must first create one by using the New Load Test Wizard. See [Creating load tests](../test_notintoc/creating-load-tests.md).  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
 Load tests can contain both unit tests and Web performance tests. The main purpose of a load test is to simulate many users accessing a server at the same time. A load test gives you access to application stress and performance data. A load test can be configured to emulate various load conditions such as user loads and network types.  
  
 ![Load Test Architecture](../test/media/load_test_editor.png "Load_Test_Editor")  
Load Test Editor Hierarchy  
  
 **Load Tests Created in the New Load Test Wizard**  
  
 Any of the initial configuration options and settings that you specified in the New Load Test Wizard when you created a load test can be modified in the Load Test Editor after the wizard is finished. The Load Test Editor lets you to modify an existing load test's properties, and add more scenarios, counter sets, and run settings.  
  
## Tasks  
  
|Tasks|Associated topics|  
|-----------|-----------------------|  
|**Edit load test scenario settings:** A scenario is used to model how a group of users interacts with a server application. A scenario consists of a load pattern, a test mix model, a test mix, a browser mix, and network mix. A load test can have more than one scenario and a single scenario can contain Web performance tests and unit tests. By grouping similar settings together, a scenario lets you to group and run tests of a similar nature together.|-   [Editing Load Test Scenarios](../test/editing-load-test-scenarios-using-the-load-test-editor.md)<br />-   [Load Test Scenario Properties](../test/load-test-scenario-properties.md)|  
|**Configure and manage performance counter sets specified for computers that are used in a load test:** Load tests provide named counter sets, organized by technology, that are useful when you analyze performance counter data. The counter sets include Load Test, IIS, ASP.NET, and SQL. When you create a load test with the New Load Test Wizard, an initial set of predefined and important counter set are configured by default for the computers that you specify to include in the load test. You manage your counters in the Load Test Editor.|-   [Specifying the Counter Sets and Threshold Rules for Computers in a Load Test](../test/specifying-the-counter-sets-and-threshold-rules-for-computers-in-a-load-test.md)|  
|**Configure and manage load test run settings:** Run settings are a set of properties that influence the way a load test runs. Run settings are organized by categories in the Properties window.|-   [Configuring Load Test Run Settings](../test/configuring-load-test-run-settings.md)<br />-   [Load Test Run Settings Properties](../test/load-test-run-settings-properties.md)|  
|**Specify 64-bit processes for load testing:** You can configure the test setting that you are using with your load test to specify that you want to use 64-bit processes.|-   [How to: Specify 64-Bit Process Using Test Settings](../test_notintoc/how-to--specify-64-bit-process-using-test-settings.md)|  
|**Configuration considerations for load tests:** You can configure load test to ideal settings by modifying such settings as sample rates and think times. You can also configure your load test for optimal settings if it includes Web performance tests.|-   [Considerations for Load Testing](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337)|  
  
## Related Tasks  
 [Configuring Load Test Run Settings](../test/configuring-load-test-run-settings.md)  
  
 Run settings are a set of properties that influence the way a load test runs. Run settings are organized by categories in the Properties window.  
  
 [Distributing Load Test Runs Across Multiple Test Machines Using Test Controllers and Test Agents](../test/6e67a587-8aad-48cc-a8c0-6d4b399f3731.md)  
  
 You can use a group of computers to generate simulated load for testing, and to run tests remotely and concurrently on several computers.  
  
## External resources  
  
### Guidance  
 [Testing for Continuous Delivery with Visual Studio 2012 – Chapter 6: A Testing Toolbox](http://go.microsoft.com/fwlink/?LinkID=255203)  
  
## See Also  
 [Creating and Editing Load Tests](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337)   
 [Creating load tests](../test_notintoc/creating-load-tests.md)   
 [Load Test Walkthroughs](http://msdn.microsoft.com/en-us/21c5ebd2-cd1e-4aed-a112-1027b4ee4fbf)   
 [Troubleshooting Load Tests](../test_notintoc/troubleshooting-load-tests.md)   
 [Analyzing Load Test Results](../test/analyzing-load-test-results-using-the-load-test-analyzer.md)   
 [Analyzing Threshold Rule Violations](../test/analyzing-threshold-rule-violations-in-load-tests-using-the-load-test-analyzer.md)   
 [Considerations for Load Testing](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337)