---
title: "Compiler Warning (level 1) CS1574 | hehe"
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
  - "CS1574"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1574"
ms.assetid: 4cd2b474-ab01-4397-aed7-63e5f0081649
caps.latest.revision: 8
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
# Compiler Warning (level 1) CS1574
XML comment on 'construct' has syntactically incorrect cref attribute 'name'  
  
 A string passed to a cref tag, for example, within an \<exception> tag, referred to a member that is not available within the current build environment. The string that you pass to a cref tag must be the syntactically correct name of a member or field.  
  
 For more information, see [Recommended Tags for Documentation Comments](../Topic/Recommended%20Tags%20for%20Documentation%20Comments%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS1574:  
  
```  
// CS1574.cs  
// compile with: /W:1 /doc:x.xml  
using System;  
  
/// <exception cref="System.Console.WriteLin">An exception class.</exception>   // CS1574  
// instead, uncomment and try the following line  
// /// <exception cref="System.Console.WriteLine">An exception class.</exception>  
class EClass : Exception  
{  
}  
  
class TestClass  
{  
   public static void Main()  
   {  
      try  
      {  
      }  
      catch(EClass)  
      {  
      }  
   }  
}  
```