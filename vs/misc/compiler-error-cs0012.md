---
title: "Compiler Error CS0012"
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
  - "CS0012"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0012"
ms.assetid: 5523e349-22f4-4b0b-b4b0-c4bf26c461f4
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
# Compiler Error CS0012
The type 'type' is defined in an assembly that is not referenced. You must add a reference to assembly 'assembly'.  
  
 The definition for a referenced type was not found. This could occur if a required .DLL file is not included in the compilation. For more information, see [Add Reference Dialog Box](http://msdn.microsoft.com/en-us/2feb0fe2-0805-4cc9-8cba-b0315849dfb7) and [/reference (C# Compiler Options)](../Topic/-reference%20\(C%23%20Compiler%20Options\).md).  
  
 The following sequence of compilations will result in CS0012:  
  
```  
// cs0012a.cs  
// compile with: /target:library  
public class A {}  
```  
  
 Then:  
  
```  
// cs0012b.cs  
// compile with: /target:library /reference:cs0012a.dll  
public class B  
{  
   public static A f()  
   {  
      return new A();  
   }  
}  
```  
  
 Then:  
  
```  
// cs0012c.cs  
// compile with: /reference:cs0012b.dll  
class C  
{  
   public static void Main()  
   {  
      object o = B.f();   // CS0012  
   }  
}  
```  
  
 You could resolve this CS0012 by compiling with `/reference:cs0012b.dll;cs0012a.dll`, or in Visual Studio by using the [Add Reference Dialog Box](http://msdn.microsoft.com/en-us/2feb0fe2-0805-4cc9-8cba-b0315849dfb7) to add a reference to cs0012a.dll in addition to cs0012b.dll.