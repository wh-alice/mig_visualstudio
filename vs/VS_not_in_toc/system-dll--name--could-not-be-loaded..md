---
title: "System DLL &lt;name&gt; could not be loaded."
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
  - "vs.message.VB_E_TERRSYSDLLNOTLOADED"
  - "vs.message.0x800A0085"
ms.assetid: d4ccb3b1-fbc3-4395-a9b1-be50a4d7bf44
caps.latest.revision: 6
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
# System DLL &lt;name&gt; could not be loaded.
A .dll file provided by the operating system, such as DDEML.DLL, VERSION.DLL, or WINSPOOL.DRV, couldn't be found. This error generally occurs if one of the following is true: the file is not on the proper path, the DLL has been corrupted or deleted, or there isn't enough memory.  
  
### To correct this error  
  
1.  Check that the DLL is on the Windows system path.  
  
     —or—  
  
     Reload the DLL.  
  
     —or—  
  
     Try to free up memory by closing other open applications.