---
title: "Compiler Warning (level 1) CS1584"
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
  - "CS1584"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1584"
ms.assetid: 56c8f9bf-4cce-4269-b573-d60e5b11f9ab
caps.latest.revision: 12
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
# Compiler Warning (level 1) CS1584
XML comment on 'member' has syntactically incorrect cref attribute 'invalid_syntax'  
  
 One of the parameters passed to a tag for documentation comments has invalid syntax. For more information, see [Recommended Tags for Documentation Comments](../Topic/Recommended%20Tags%20for%20Documentation%20Comments%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS1584.  
  
```  
// CS1584.cs  
// compile with: /W:1 /doc:CS1584.xml  
/// <remarks>Test class</remarks>  
public class Test  
{  
   /// <remarks>Called in <see cref="Test.Mai()n"/>.</remarks>   // CS1584  
   // try the following line instead  
   // /// <remarks>Called in <see cref="Test.Main()"/>.</remarks>  
   public static void Test2() {}  
  
   /// <remarks>Main method</remarks>  
   public static void Main() {}  
}  
```