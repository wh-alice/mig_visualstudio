---
title: "Compiler Warning (level 4) CS1712 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1712"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1712"
ms.assetid: d9a8be26-c0ba-41fa-b082-1ce4ba7724b7
caps.latest.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
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
# Compiler Warning (level 4) CS1712
Type parameter 'type parameter' has no matching typeparam tag in the XML comment on 'type' (but other type parameters do)  
  
 The documentation of a generic type is missing a **typeparam** tag. For more information, see [\<typeparam>](http://msdn.microsoft.com/en-us/Library/9b99d400-e911-4e55-99c6-64367c96aa4f).  
  
## Example  
 The following code generates warning CS1712. To resolve this error, add a **typeparam** tag for the type parameter S.  
  
```  
// CS1712.cs  
// compile with: /doc:cs1712.xml  
using System;  
class Test  
{  
    public static void Main() {}  
    /// <param name="j"> This is the j parameter.</param>  
    /// <typeparam name="T"> This is the T type parameter.</typeparam>  
    public void bar<T,S>(int j) {}  // CS1712  
}  
```