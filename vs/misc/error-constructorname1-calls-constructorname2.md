---
title: "&lt;error&gt;: &#39;&lt;constructorname1&gt;&#39; calls &#39;&lt;constructorname2&gt;&#39; | Microsoft Docs"
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
  - "vbc30297"
  - "bc30297"
helpviewer_keywords: 
  - "BC30297"
ms.assetid: dfca67d7-f4d7-4451-a937-68f22b8527d5
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
# &lt;error&gt;: &#39;&lt;constructorname1&gt;&#39; calls &#39;&lt;constructorname2&gt;&#39;
A circular constructor call occurs. A constructor makes a call to `Me.New()` or `MyClass.New()`. One possible cause is an attempt to call an overloaded constructor with a different argument list.  
  
 **Error ID:** BC30297  
  
### To correct this error  
  
-   Use a different argument list to call an overloaded constructor.  
  
-   If there are no accessible overloads, remove the call to `Me.New()` or `MyClass.New()`.  
  
## See Also  
 [NOT IN BUILD: Using Constructors and Destructors](http://msdn.microsoft.com/en-us/548eebe1-86c4-4377-b2f5-447cb8be3d90)