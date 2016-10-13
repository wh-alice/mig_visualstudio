---
title: "Command does not accept additional switches or arguments if the switch &quot;-stop&quot; has been specified."
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.message.0x800A00CD"
  - "vs.message.VS_E_NOTVALIDWITHSTOP"
ms.assetid: 1dea2450-034e-4a7f-b959-2060811329b6
caps.latest.revision: 7
ms.author: "mblome"
manager: "douge"
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
# Command does not accept additional switches or arguments if the switch &quot;/stop&quot; has been specified.
This error generally occurs when the `/stop` switch has been entered, along with additional switches for the **Find in Files** or **Replace in Files** commands.  
  
### To correct this error  
  
1.  If you want to stop the current Find in Files operation, enter:  
  
    ```  
    Edit.FindinFiles /stop.  
    ```  
  
2.  If you want to stop the current Replace in Files operation, enter:  
  
    ```  
    Edit.ReplaceinFiles /stop  
    ```  
  
3.  If you want to start a new Find in Files or Replace in Files operation, re-enter the command, omitting `/stop`.  
  
## See Also  
 [Replace In Files Command](../reference/replace-in-files-command.md)   
 [Find in Files Command](../reference/find-in-files-command.md)   
 [Visual Studio Commands](../reference/visual-studio-commands.md)