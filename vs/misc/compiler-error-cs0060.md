---
title: "Compiler Error CS0060 | testtitle"
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
  - "CS0060"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0060"
ms.assetid: ae6d4fb7-5ff9-4883-82c3-f55b190f439a
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
# Compiler Error CS0060
Inconsistent accessibility: base class 'class1' is less accessible than class 'class2'  
  
 Class accessibility should be consistent between the base class and inherited class.  
  
 The following sample generates CS0060:  
  
```  
// CS0060.cs  
class MyClass  
// try the following line instead  
// public class MyClass  
{  
}  
  
public class MyClass2 : MyClass   // CS0060  
{  
   public static void Main()  
   {  
   }  
}  
```  
  
## See Also  
 [Access Modifiers](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)