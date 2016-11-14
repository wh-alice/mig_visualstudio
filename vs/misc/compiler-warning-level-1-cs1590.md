---
title: "Compiler Warning (level 1) CS1590 | Microsoft Docs"
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
  - "CS1590"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1590"
ms.assetid: 0d6e5594-d6a6-43bf-8aa8-a452fa5748df
caps.latest.revision: 7
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
# Compiler Warning (level 1) CS1590
Invalid XML include element -- Missing file attribute  
  
 A path or doc attribute, passed to the [\<include>](http://msdn.microsoft.com/en-us/Library/a8a70302-6196-4643-bd09-ef33f411f18f) tag, was missing or incomplete.  
  
 The following sample generates CS1590:  
  
```  
// CS1590.cs  
// compile with: /W:1 /doc:x.xml  
  
/// <include path='MyDocs/MyMembers[@name="test"]/*' />   // CS1590  
// try the following line instead  
// /// <include file='x.doc' path='MyDocs/MyMembers[@name="test"]/*' />  
class Test  
{  
   public static void Main()  
   {  
   }  
}  
```