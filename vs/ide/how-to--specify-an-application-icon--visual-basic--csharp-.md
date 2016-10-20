---
title: "How to: Specify an Application Icon (Visual Basic, C#) | Microsoft Docs"
ms.custom: ""
ms.date: "10/18/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "icons [Visual Studio], application"
  - "application properties [Visual Studio], icons"
  - "application icons [Visual Studio]"
ms.assetid: ad8e14ed-adc2-45b6-a0be-818b16d5616f
caps.latest.revision: 18
ms.author: "kempb"
manager: "ghogen"
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
# How to: Specify an Application Icon (Visual Basic, C#)
The `Icon` property for a project specifies the icon file (.ico) that will be displayed for the compiled application in File Explorer and in the Windows taskbar.  
  
 The `Icon` property can be accessed in the **Application** pane of the **Project Designer**; it contains a list of icons that have been added to a project either as resources or as content files.  
  
> [!NOTE]
>  After you set the icon property for an application, you might also set the `Icon` property of each **Window** or **Form** in the application. For information about window icons for Windows Presentation Foundation (WPF) standalone applications, see <xref:System.Windows.Window.Icon*> property.  
  
### To specify an application icon  
  
1.  In **Solution Explorer**, choose a project node (not the **Solution** node).  
  
2.  On the menu bar, choose **Project**, **Properties**.  
  
3.  When the **Project Designer** appears, choose the **Application** tab.  
  
4.  **(Visual Basic)** In the **Icon** list, choose an icon (.ico) file.  
  
     **C#** Near the **Icon** list, choose the **\<Browse...>** button, and then browse to the location of the icon file that you want.  
  
## See Also  
 [Application Page, Project Designer (Visual Basic)](../reference/application-page--project-designer--visual-basic-.md)   
 [Application Page, Project Designer (C#)](../reference/application-page--project-designer--csharp-.md)   
 [Managing Application Properties](../ide/application-properties.md)  
 [How to: Add or Remove Resources](http://msdn.microsoft.com/en-us/7b77bc06-3952-4799-b029-def3f8f7f88d)