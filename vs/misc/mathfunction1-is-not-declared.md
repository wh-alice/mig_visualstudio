---
title: "&#39;&lt;mathfunction1&gt;&#39; is not declared | Microsoft Docs"
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
  - "bc30819"
  - "vbc30819"
helpviewer_keywords: 
  - "BC30819"
ms.assetid: 4d30785f-a8fe-438a-846a-8e15ff3f49f5
caps.latest.revision: 10
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
# &#39;&lt;mathfunction1&gt;&#39; is not declared
'\<mathfunction1>' is not declared. Function has moved to the System.Math class and is now called '\<mathfunction2>'.  
  
 Several functions that were intrinsic to [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] in previous versions have been moved to the <xref:System.Math?displayProperty=fullName> namespace. This makes their functionality more generally available to all programming languages.  
  
 **Error ID:** BC30819  
  
### To correct this error  
  
-   Use the methods declared in <xref:System.Math?displayProperty=fullName>.  
  
## See Also  
 <xref:System.Math>   
 [Programming Element Support Changes Summary](http://msdn.microsoft.com/en-us/0483590a-6309-449c-a2fa-effa26a03b95)