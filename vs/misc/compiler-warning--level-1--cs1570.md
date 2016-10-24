---
title: "Compiler Warning (level 1) CS1570 | testtitle"
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
  - "CS1570"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1570"
ms.assetid: a121d5c4-8b90-4cda-af5b-6ba8f23b2b1e
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
# Compiler Warning (level 1) CS1570
XML comment on 'construct' has badly formed XML — 'reason'  
  
 When using [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md), any comments in the source code must be in XML. Any error with your XML markup will generate CS1570. For example:  
  
-   If you are passing a string to a **cref**, such as in an [\<exception>](../Topic/%3Cexception%3E%20\(C%23%20Programming%20Guide\).md) tag, the string must be enclosed in double quotation marks.  
  
-   If you are using a tag, such as [\<seealso>](../Topic/%3Cseealso%3E%20\(C%23%20Programming%20Guide\).md), which does not have a closing tag, you must specify a forward slash before the closing angle bracket.  
  
-   If you need to use a greater-than or less-than symbol in the text of description, you need to represent them with **&gt;** or **&lt;**.  
  
-   The file or path attribute on an [\<include>](../Topic/%3Cinclude%3E%20\(C%23%20Programming%20Guide\).md) tag was missing or improperly formed.  
  
 The following sample generates CS1570:  
  
```  
// CS1570.cs  
// compile with: /W:1  
namespace ns  
{  
   // the following line generates CS1570  
   /// <summary> returns true if < 5 </summary>  
   // try this instead  
   // /// <summary> returns true if <5 </summary>  
  
   public class MyClass  
   {  
      public static void Main ()  
      {  
      }  
   }  
}  
```