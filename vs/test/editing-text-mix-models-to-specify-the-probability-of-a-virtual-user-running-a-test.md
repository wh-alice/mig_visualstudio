---
title: "Editing Text Mix Models to Specify the Probability of a Virtual User Running a Test"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "load tests, scenarios"
  - "load tests, virtual users"
ms.assetid: e3b7d952-9012-400a-8131-3444390a6066
caps.latest.revision: 31
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
# Editing Text Mix Models to Specify the Probability of a Virtual User Running a Test
The *test mix model* specifies the probability of a virtual user running a given test in a load test scenario. This lets you simulate load more realistically. Instead of having just one workflow through your applications, you can have several workflows, which is a closer approximation of how end-users interact with your applications.  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
## Test Mix Model Options  
 You can specify one of the following test mix model options for your load test scenario:  
  
-   **Based on the total number of tests:** Determines which Web performance or unit test is run when a virtual user starts a test iteration. At the end of the load test, the number of times that a particular test was run matches the assigned test distribution. Use this test mix model when you are basing the test mix on transaction percentages in an IIS log or in production data.  
  
-   **Based on the number of virtual users:** Determines the percentage of virtual users who will run a particular Web performance or unit test. At any point in the load test, the number of users who are running a particular test matches the assigned distribution. Use this test mix model when you are basing the test mix on the percentage of users running a particular test.  
  
-   **Based on user pace:** Over the course of the load test, each Web performance test or unit test is run a specified number of times per users, per hour. Use this test mix model when you want virtual users to run test at a certain pace throughout the load test.  
  
-   **Based on sequential order:** Each virtual user runs the Web performance or unit tests in the order that the tests are defined in the scenario. The virtual user continues cycling through the tests in this order until the load test is complete.  
  
## Tasks  
  
|Tasks|Associated Topics|  
|-----------|-----------------------|  
|**Specifying the test mix for your load test:** When you create a load test, you specify settings for the load test in the New Load Test Wizard. In the New Load Test Wizard, you choose existing Web and unit tests to add to the initial scenario. After you have added tests to the scenario, you specify the test mix for the scenario.<br /><br /> You use load modeling options to more accurately predict the expected real-world usage of a Web site or application that you are load-testing. It is important to do this because a load test that is not based on an accurate load model can generate misleading results.|-   [Create and run a load test](http://msdn.microsoft.com/en-us/7041cbcf-9ab1-4579-98ff-8f296aeaded4)<br />-   [Emulating Expected Real-World Usage of a Web Site or Application](../test/b7fae849-0538-40d1-ab35-2bb3a0fe4393.md)|  
|**Edit the test mix model:** You can change a load test scenario to use one of the test mix models by using the Load Test Editor. [!INCLUDE[crdefault](../codequality/includes/crdefault_md.md)] the procedure [Changing the Test Mix Model in a Scenario](../test/editing-text-mix-models-to-specify-the-probability-of-a-virtual-user-running-a-test.md#EditTestMixModelHowTo) in this topic.||  
|**Configure pacing delay for a user paced test mix model:** If your load test scenario is configured to use the **Based on user pace test mix model**, you can specify how you want the distribution Pacing Delay configured.|-   [How to: Apply Distribution to Pacing Delay When Using a User Pace Test Mix Model](../test/how-to--apply-distribution-to-pacing-delay-when-using-a-user-pace-test-mix-model.md)|  
  
##  <a name="EditTestMixModelHowTo"></a> Changing the Test Mix Model in a Scenario  
 After you create your load test by using the **New Load Test Wizard**, you can use the **Load Test Editor** to change the scenarios properties to meet your testing needs and goals. For more information, see [Create and run a load test](http://msdn.microsoft.com/en-us/7041cbcf-9ab1-4579-98ff-8f296aeaded4).  
  
> [!NOTE]
>  For a complete list of the load settings properties and their descriptions, see [Load Test Scenario Properties](../test/load-test-scenario-properties.md).  
  
 Using the Load Test Editor, you can change the test mix model in a load test scenario by editing the **Test Mix Type** property in the Properties window.  
  
#### To change the test mix model  
  
1.  Open a load test.  
  
     The Load Test Editor appears. The load test tree is displayed.  
  
2.  In **Scenarios** folder of the load test tree, choose the scenario node for which you want to specify the maximum number of test iterations.  
  
3.  On the **View** menu, select **Properties Window**.  
  
     The categories and properties of the scenario are displayed.  
  
4.  In the **Test Mix Type** property, choose the ellipsis button ( **…**).  
  
     The Edit Test Mix dialog box is displayed.  
  
5.  Choose the drop-down list under **Test mix model** and select the test mix model that you want to use for the scenario.  
  
6.  (Optional) Modify the test mix by using the **Add**, **Remove** and **Distribute** buttons and distribution sliders. For more information, see [Editing the Test Mix to Specify Which Tests to Include in a Load Test Scenario](../test/303e1d70-5d98-424a-b51e-e0898e16d3f8.md).  
  
7.  (Optional) Specify a Web performance and unit test to initialize or end by using the check boxes and selecting the desired tests. For more information, see [Emulating Expected Real-World Usage of a Web Site or Application](../test/b7fae849-0538-40d1-ab35-2bb3a0fe4393.md).  
  
8.  Choose **OK**.  
  
     The **Properties** window displays the new test mix model for the **Test Mix Type** property.  
  
9. After you change the property, choose **Save** on the **File** menu. You can then run your load test by using the new **Test Mix Type** value.  
  
## See Also  
 [Editing Load Test Scenarios](../test/editing-load-test-scenarios-using-the-load-test-editor.md)   
 [Load Test Scenario Properties](../test/load-test-scenario-properties.md)   
 [Create and run a load test](http://msdn.microsoft.com/en-us/7041cbcf-9ab1-4579-98ff-8f296aeaded4)