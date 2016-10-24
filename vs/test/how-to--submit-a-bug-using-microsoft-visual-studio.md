---
title: "How to: Submit a Bug Using Microsoft Visual Studio | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "bugs, submitting from Visual Studio ALM"
ms.assetid: dde0d6c5-2d9a-4b86-9825-4b7b74c396f8
caps.latest.revision: 26
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
# How to: Submit a Bug Using Microsoft Visual Studio
You can submit a bug using Visual Studio at any time during the software development process. For example, you perform ad hoc testing and find a bug, or you notice incorrect behavior while you’re discussing the application under test with your team mates. You can manually attach information to this bug and link it to other work items.  
  
> [!NOTE]
>  Using Visual Studio to submit a bug does not automatically add data that was collected when a test was run, unlike when you create a bug using Test Runner or the Exploratory Testing window from Microsoft Test Manager. For more information about these methods, see [Submitting Bugs](../test_notintoc/submitting-bugs-in-microsoft-test-manager.md).  
  
 ![Create bug in Visual Studio](../test/media/vs_createbug1.png "VS_CreateBug1")  
  
 ![New bug form in Vsual Studio](../test/media/vs_createbug2.png "VS_CreateBug2")  
  
### To submit a bug using Microsoft Visual Studio  
  
1.  To create a bug, you must first connect to your Team Foundation Server. On the **TEAM** menu, choose **Connect to Team Foundation Server**. Select the server from the list of servers.  
  
     For more information about how to connect to [!INCLUDE[esprtfs](../code-quality/includes/esprtfs_md.md)], see [How to: Connect to a Team Project in Team Foundation Server](http://msdn.microsoft.com/en-us/25b3fe4f-ee89-4b58-ba19-4c94a47636a6).  
  
2.  To connect to a specific team project, select the team project and then choose **Connect**.  
  
3.  To create a bug, on the **TEAM** menu, choose **New Work Item** and then **Bug**.  
  
     The **New Bug** tab is displayed.  
  
4.  Type an appropriate title in **Title**.  
  
5.  Under **STATUS**, perform the following optional steps:  
  
    -   (Optional) To select the user to assign to this bug, use the drop-down list for **Assigned to**.  
  
    -   (Optional) To change the state of this bug from the default state of active, use the drop-down list for **State**.  
  
    -   (Optional) To change the reason for the bug, use the drop-down list for **Reason**.  
  
6.  Under **DETAILS**, perform the following optional steps:  
  
    -   (Optional) Add text in the **Effort** field.  
  
    -   (Optional) To assign a severity to the bug, use the drop-down list for **Severity**.  
  
    -   (Optional) Use the drop-down list for **Area** to select the appropriate area in the team project for this bug.  
  
    -   (Optional) Add text for the **Backlog Priority** field.  
  
7.  (Optional) Add comments applicable to the error causing the bug under **HISTORY**.  
  
8.  (Optional) To link this bug to other work items, choose **LINKS** and then choose **Link to**.  
  
9. (Optional) To add attachments to this bug, choose **Attachments**. Any file can be added. For example, you could add a video recording file, a screen shot file, or a log file.  
  
10. To save the bug, choose **Save Work Item** on the toolbar.  
  
## See Also  
 [Submitting Bugs](../test_notintoc/submitting-bugs-in-microsoft-test-manager.md)