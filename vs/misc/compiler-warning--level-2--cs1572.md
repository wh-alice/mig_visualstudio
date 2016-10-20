---
title: "Compiler Warning (level 2) CS1572 | Microsoft Docs"
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
  - "CS1572"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1572"
ms.assetid: 24bc8b96-29d2-4201-bc4e-6b9b5a4f5a1d
caps.latest.revision: 7
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
# Compiler Warning (level 2) CS1572
XML comment on 'construct' has a param tag for 'parameter', but there is no parameter by that name  
  
 When using the [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) compiler option, a comment was specified for a parameter that does not exist for the method. Change the value passed to the name attribute or remove one of the comment lines.  
  
 The following sample generates CS1572:  
  
```  
// CS1572.cs  
// compile with: /W:2 /doc:x.xml  
  
/// <summary>help text</summary>  
public class MyClass  
{  
   /// <param name='Int1'>Used to indicate status.</param>  
   /// <param name='Char1'>Used to indicate status.</param>  
   /// <param name='Char2'>???</param> // CS1572  
   public static void MyMethod(int Int1, char Char1)  
   {  
   }  
  
   /// <summary>help text</summary>  
   public static void Main ()  
   {  
   }  
}  
```