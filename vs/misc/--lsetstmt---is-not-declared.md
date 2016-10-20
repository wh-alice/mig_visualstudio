---
title: "&#39;&lt;lsetstmt&gt;&#39; is not declared | Microsoft Docs"
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
  - "bc30820"
  - "vbc30820"
helpviewer_keywords: 
  - "BC30820"
ms.assetid: 8666dd52-58ea-4b84-b59a-8ebd8b2cb23b
caps.latest.revision: 10
ms.author: "billchi"
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
# &#39;&lt;lsetstmt&gt;&#39; is not declared
'\<lsetstmt>' is not declared. LSet statements are no longer supported; use Microsoft.VisualBasic.LSet instead.  
  
 Several functions that were intrinsic to [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] in previous versions have been moved to the <xref:Microsoft.VisualBasic?displayProperty=fullName> namespace. This makes their functionality more generally available to all programming languages.  
  
 **Error ID:** BC30820  
  
### To correct this error  
  
-   Use the `LSet` function in the `Microsoft.VisualBasic` namespace instead.  
  
## See Also  
 [NOT IN BUILD: LSet Function](http://msdn.microsoft.com/en-us/591d286c-6b7a-4350-ae74-99fee00fd964)   
 [Programming Element Support Changes Summary](http://msdn.microsoft.com/en-us/0483590a-6309-449c-a2fa-effa26a03b95)