---
title: "Compiler Error CS0271 | Microsoft Docs"
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
  - "CS0271"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0271"
ms.assetid: eadc9fb5-7770-4ec4-94f6-3c7cf37eec06
caps.latest.revision: 11
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
# Compiler Error CS0271
The property or indexer 'property/indexer' cannot be used in this context because the get accessor is inaccessible  
  
 This error occurs when you try to access an inaccessible `get` accessor. To resolve this error, increase the accessibility of the accessor, or change the calling location. For more information, see [Accessor Accessibility](../Topic/Restricting%20Accessor%20Accessibility%20\(C%23%20Programming%20Guide\).md) and [Properties](../Topic/Properties%20\(C%23%20Programming%20Guide\).md).  
  
 The following example generates CS0271:  
  
```  
// CS0271.cs  
public class MyClass  
{  
   public int Property  
   {  
      private get { return 0; }  
      set { }  
   }  
  
   public int Property2  
   {  
      get { return 0; }  
      set { }  
   }  
}  
  
public class Test  
{  
   public static void Main(string[] args)   
   {  
      MyClass c = new MyClass();  
      int a = c.Property;   // CS0271  
      int b = c.Property2;   // OK  
   }  
}  
```