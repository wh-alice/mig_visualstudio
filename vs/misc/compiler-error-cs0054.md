---
title: "Compiler Error CS0054 | Microsoft Docs"
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
  - "CS0054"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0054"
ms.assetid: 49346f55-d887-497a-af71-be4cbbf1de24
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
# Compiler Error CS0054
Inconsistent accessibility: indexer return type 'type' is less accessible than indexer 'indexer'  
  
 A public construct must return a publicly accessible object. For more information, see [Access Modifiers](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0054:  
  
```  
// CS0054.cs  
class MyClass  
// try the following line instead  
// public class MyClass  
{  
}  
  
public class MyClass3  
{  
   public MyClass this[int i]   // CS0054  
   {  
      get  
      {  
         return new MyClass();  
      }  
   }  
}  
  
public class MyClass2  
{  
   public static void Main()  
   {  
   }  
}  
```