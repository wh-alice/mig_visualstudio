---
title: "Troubleshooting Exceptions: System.MethodAccessException | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "MethodAccessException class"
ms.assetid: 1c276666-e451-489e-8b95-25d737787030
caps.latest.revision: 13
author: "mikeblome"
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
# Troubleshooting Exceptions: System.MethodAccessException
A <xref:System.MethodAccessException> exception is thrown when there is an invalid attempt to access a private or protected method inside a class.  
  
## Associated Tips  
 **If the access level of a method in a class library has changed, recompile any assemblies that reference the library.**  
 This exception typically occurs when the caller does not have access permission to the member.  
  
## See Also  
 <xref:System.MethodAccessException>   
 [Use the Exception Assistant](http://msdn.microsoft.com/en-us/Library/e0a78c50-7318-4d54-af51-40c00aea8711)