---
title: "Alias definition is recursive. | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.message.0x800A00DA"
  - "vs.message.VS_E_RECURSIVEALIAS"
ms.assetid: e48a2908-9b94-4c6a-9807-beeeba71531c
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
# Alias definition is recursive.
This error generally occurs when an alias has been defined that directly or indirectly references itself.  
  
### To correct this error  
  
1.  Change the definition of the alias and try again.  
  
     —or—  
  
2.  Review the current list of aliases and their definitions by entering `>alias` in the **Command** window and try again.  
  
## See Also  
 [Alias Command](../reference/alias-command.md)   
 [Visual Studio Command Aliases](../reference/visual-studio-command-aliases.md)