---
title: "Compiler Error CS0177"
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
  - "CS0177"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0177"
ms.assetid: 852a8c2a-2411-4800-af7c-4c572d9900d3
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
# Compiler Error CS0177
The out parameter 'parameter' must be assigned to before control leaves the current method  
  
 A parameter marked with the [out](../Topic/out%20\(C%23%20Reference\).md) keyword was not assigned a value in the method body. For more information, see [Passing Parameters](../Topic/Passing%20Parameters%20\(C%23%20Programming%20Guide\).md)  
  
 The following sample generates CS0177:  
  
```  
// CS0177.cs  
public class MyClass  
{  
   public static void Foo(out int i)   // CS0177  
   {  
   // uncomment the following line to resolve this error  
   //   i = 0;  
   }  
  
   public static void Main()  
   {  
       int x = -1;  
       Foo(out x);  
   }  
}  
```