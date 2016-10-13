---
title: "Extender instance is no longer valid."
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
  - "vs.message.VS_E_EXT_EXTINVALID"
ms.assetid: 6361ba35-f2c5-4024-9362-46d7d9daf651
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
# Extender instance is no longer valid.
The Extender instance could not be created successfully or was destroyed.  
  
### To correct this error  
  
1.  Get the Extender instance again from the Extendee Object  
  
     —or—  
  
     Get the Extender instance again by calling DTE.ObjectExtenders.GetExtender().  
  
## See Also  
 \<xref:EnvDTE.ObjectExtenders>   
 \<xref:EnvDTE.ObjectExtenders.GetExtender*>