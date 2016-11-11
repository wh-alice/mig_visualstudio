---
title: "Event &#39;&lt;eventname&gt;&#39; event specified by the &#39;DefaultEvent&#39; attribute is not a publicly accessible event for this class | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30770"
  - "bc30770"
helpviewer_keywords: 
  - "BC30770"
ms.assetid: 7524fba7-2a37-4bc3-b789-87d73a166575
caps.latest.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
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
# Event &#39;&lt;eventname&gt;&#39; event specified by the &#39;DefaultEvent&#39; attribute is not a publicly accessible event for this class
The <xref:System.ComponentModel.DefaultEventAttribute> attribute must specify the name of publicly accessible event in the class to which the attribute is applied.  
  
 **Error ID:** BC30770  
  
### To correct this error  
  
1.  Make sure the class defines a publicly accessible event.  
  
2.  Make sure that the name of the event in the class matches the name specified by the <xref:System.ComponentModel.DefaultEventAttribute> attribute.  
  
## See Also  
 <xref:System.ComponentModel.DefaultEventAttribute>   
 [Event Statement](/dotnet/visual-basic/language-reference/statements/event-statement)   
 [Class Statement](/dotnet/visual-basic/language-reference/statements/class-statement)   
 [Public](/dotnet/visual-basic/language-reference/modifiers/public)