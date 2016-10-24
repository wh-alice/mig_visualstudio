---
title: "Find-Command Box | Microsoft Docs"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.findcommandbox"
helpviewer_keywords: 
  - "Find/Command box"
ms.assetid: c81736dd-7a26-4e11-95c8-c2a2e56d7a41
caps.latest.revision: 17
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
# Find/Command Box
You can search for text and run Visual Studio commands from the **Find/Command** box. The **Find/Command** box is still available as a toolbar control, but is no longer visible by default. You can display the **Find/Command** box by choosing **Add or Remove Buttons** on the **Standard** toolbar and then choosing **Find**.  
  
 To run a [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] command, preface it with a greater than (>) sign.  
  
 The **Find/Command** box retains the last 20 items entered and displays them in a drop-down list. You can navigate through the list by choosing the arrow keys.  
  
 ![Find&#47;Command Box](../ide/media/findcommandbox.png "FindCommandBox")  
Find/Command Box  
  
## Searching for Text  
 By default, when you specify text in the **Find/Command** box and then choose the ENTER key, Visual Studio searches the current document or tool window using the options that are specified in the **Find in Files** dialog box. For more information, see [Finding and Replacing Text](../ide/finding-and-replacing-text.md).  
  
## Entering Commands  
 To use the **Find/Command** box to issue a single [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] command or alias rather than search for text, enter the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] command, prefaced with a greater than (>) symbol. For example:  
  
```  
>File.NewFile c:\temp\MyFile /t:"General\Text File"  
```  
  
 Alternatively, you can also use the Command window to enter and execute single or multiple commands. Some commands or aliases can be entered and executed by themselves; others have required arguments in their syntax. For a list of commands that have arguments, see [Visual Studio Commands](../reference/visual-studio-commands.md).  
  
## Escape Characters  
 A caret (^) character in a command line means that the character immediately following it is interpreted literally, rather than as a control character. This can be used to embed straight quotation marks ("), spaces, leading slashes, carets, or any other literal characters in a parameter or switch value, with the exception of switch names. For example,  
  
```  
>Edit.Find ^^t /regex  
```  
  
 A caret functions the same whether it is inside or outside quotation marks. If a caret is the last character on the line, it is ignored.  
  
## See Also  
 [Command Window](../reference/command-window.md)   
 [Finding and Replacing Text](../ide/finding-and-replacing-text.md)