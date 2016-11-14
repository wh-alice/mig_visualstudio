---
title: "Troubleshooting Exceptions: System.Threading.AbandonedMutexException | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "System.Threading.AbandonedMutexException exception"
  - "AbandonedMutexException exception"
ms.assetid: 11157066-32ed-492c-83af-29983f915eec
caps.latest.revision: 5
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
# Troubleshooting Exceptions: System.Threading.AbandonedMutexException
The exception that is thrown when one thread is waiting on a Mutex object, and another thread abandons the Mutex by exiting without releasing it.  
  
## Remarks  
 An abandoned Mutex typically indicates a serious error in the code. When a thread exits without releasing the Mutex, the data structures protected by the Mutex might not be in a consistent state. The next thread to request ownership of the Mutex can handle this exception and proceed if the integrity of the data structures can be verified.  
  
## See Also  
 <xref:System.Threading.AbandonedMutexException>   
 <xref:System.Threading.Mutex>   
 [Use the Exception Assistant](http://msdn.microsoft.com/en-us/Library/e0a78c50-7318-4d54-af51-40c00aea8711)   
 [Threading](http://msdn.microsoft.com/en-us/Library/552f6c68-dbdb-4327-ae36-32cf9063d88c)