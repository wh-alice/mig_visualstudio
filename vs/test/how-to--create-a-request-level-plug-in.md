---
title: "How to: Create a Request-Level Plug-In | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "request-level plug-in, creating"
  - "Web performance tests, requests"
ms.assetid: d0b5b23c-7e94-4637-be6c-2620a5442d46
caps.latest.revision: 43
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
# How to: Create a Request-Level Plug-In
*Requests* are the declarative statements that constitute Web performance tests. Web performance test plug-ins enable you to isolate and reuse code outside the main declarative statements in your Web performance test. You can create plug-ins and add them to an individual request as well as to the Web performance test that contains it. A customized  *request plug-in* offers you a way to call code as a particular request is run in a Web performance test.  
  
 Every Web performance test request plug-in has a PreRequest method and a PostRequest method. After you attach a request plug-in to a particular http request, the PreRequest event will be fired before the request is issued and the PostRequest fired after the response is received.  
  
 You can create a customized Web performance test request plug-in by deriving your own class from the <xref:Microsoft.VisualStudio.TestTools.WebTesting.WebTestRequestPlugin> base class.  
  
 You can use customized Web performance test request plug-ins with the Web performance tests you have recorded. Customized Web performance test request plug-ins enable you to write a minimal amount of code to attain a greater level of control over your Web performance tests. However, you can also use them with coded Web performance tests. See [How to: Create a Coded Web Performance Test](../test_notintoc/how-to--create-a-coded-web-performance-test.md).  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
### To create a request-level plug-in  
  
1.  In Solution Explorer, right-click the solution, . select **Add** and then choose **New Project**.  
  
     The **Add New Project** dialog box is displayed.  
  
2.  Under **Installed Templates**, select **Visual C#**.  
  
3.  In the list of templates, select **Class Library**.  
  
4.  In the **Name** text box, type a name for your class and Choose **OK**.  
  
     The new class library project is added to Solution Explorer and the new class appears in the Code Editor.  
  
5.  In Solution Explorer, right-click the **References** folder in the new class library and select **Add Reference**.  
  
     The **Add Reference** dialog box is displayed.  
  
6.  Choose the **.NET** tab, scroll down, select **Microsoft.VisualStudio.QualityTools.WebTestFramework** and then choose **OK**  
  
     The reference to **Microsoft.VisualStudio.QualityTools.WebTestFramework** is added to the **Reference** folder in Solution Explorer.  
  
7.  In Solution Explorer, right-click the top node of the Web performance and load test project that contains the load test to which you want to add the Web performance test request test plug-in. Select **Add Reference**.  
  
     The **Add Reference dialog box is displayed**.  
  
8.  Choose the **Projects** tab, select the Class Library Project and then choose **OK** .  
  
9. In the Code Editor, write the code of your plug-in. First, create a new public class that derives from <xref:Microsoft.VisualStudio.TestTools.WebTesting.WebTestRequestPlugin>.  
  
10. Implement code inside one or both of the <xref:Microsoft.VisualStudio.TestTools.WebTesting.WebTestRequestPlugin.PreRequest*> and <xref:Microsoft.VisualStudio.TestTools.WebTesting.WebTestRequestPlugin.PostRequest*> event handlers. See the following Example section for a sample implementation.  
  
11. After you have written the code, build the new project.  
  
12. Open the Web performance test to which you want to add the request plug-in.  
  
13. Right-click the request to which you want to add the request plug-in, and select **Add Request Plug-in**.  
  
     The **Add Web Test Request Plug-in** dialog box is displayed.  
  
14. Under **Select a plug-in**, select your new plug-in.  
  
15. In the **Properties for selected plug-in** pane, set the initial values for the plug-in to use at run time.  
  
    > [!NOTE]
    >  You can expose as many properties as you want from your plug-ins; just make them public, settable, and of a base type such as Integer, Boolean, or String. You can also change the Web performance test plug-in properties later by using the Properties window.  
  
16. Choose **OK**.  
  
     The plug-in is added to the **Request Plug-ins** folder, which is a child folder of the HTTP request.  
  
    > [!WARNING]
    >  You might get an error similar to the following when you run a Web performance test or load test that uses your plug-in:  
    >   
    >  **Request failed: Exception in \<plug-in> event: Could not load file or assembly '\<"Plug-in name".dll file>, Version=\<n.n.n.n>, Culture=neutral, PublicKeyToken=null' or one of its dependencies. The system cannot find the file specified.**  
    >   
    >  This is caused if you make code changes to any of your plug-ins and create a new DLL version **(Version=0.0.0.0)**, but the plug-in is still referencing the original plug-in version. To correct this problem, follow these steps:  
    >   
    >  1.  In your Web performance and load test project, you will see a warning in references. Remove and re-add the reference to your plug-in DLL.  
    > 2.  Remove the plug-in from your test or the appropriate location and then add it back.  
  
## Example  
 You can use the following code to create a customized Web performance test plug-in that displays two dialog boxes. On dialog box displays the URL that is associated with the request to which you attach the request add-in. The second dialog box displays the computer name for the agent.  
  
> [!NOTE]
>  The following code requires that you add a reference to System.Windows.Forms.  
  
```  
using System;  
using System.Collections.Generic;  
using System.Windows.Forms;  
using Microsoft.VisualStudio.TestTools.WebTesting;  
  
namespace RequestPluginNamespace  
{  
    public class MyWebRequestPlugin : WebTestRequestPlugin  
    {  
        public override void PostRequest(object sender, PostRequestEventArgs e)  
        {  
            MessageBox.Show(e.WebTest.Context.AgentName);  
        }  
        public override void PreRequest(object sender, PreRequestEventArgs e)  
        {  
            MessageBox.Show(e.Request.Url);  
        }  
    }  
}  
```  
  
## See Also  
 <xref:Microsoft.VisualStudio.TestTools.WebTesting.WebTestRequestPlugin>   
 [Create custom code and plug-ins for load tests](../test/create-custom-code-and-plug-ins-for-load-tests.md)   
 [Coding a custom extraction rule for a web performance test](../test/coding-a-custom-extraction-rule-for-a-web-performance-test.md)   
 [Coding a custom validation rule for a web performance test](../test/coding-a-custom-validation-rule-for-a-web-performance-test.md)   
 [How to: Create a Load Test Plug-In](../test/how-to--create-a-load-test-plug-in.md)   
 [How to: Create a Coded Web Performance Test](../test_notintoc/how-to--create-a-coded-web-performance-test.md)   
 [How to: Edit an Existing Web Performance Test](http://msdn.microsoft.com/en-us/3b39a054-4bbd-430a-a14d-f38990fbadff)