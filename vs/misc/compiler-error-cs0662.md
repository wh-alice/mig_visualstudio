---
title: "Compiler Error CS0662"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0662"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0662"
ms.assetid: 836fa15e-3bf3-4af5-8acf-072d7d731dcd
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
# Compiler Error CS0662
'method' cannot specify only Out attribute on a ref parameter. Use both In and Out attributes, or neither.  
  
 An interface method has a parameter that uses [ref](../Topic/ref%20\(C%23%20Reference\).md) with just the [Out](frlrfSystemRuntimeInteropServicesOutAttributeClassTopic) attribute. A `ref` parameter that uses the **Out** attribute must also use the [In](frlrfSystemRuntimeInteropServicesInAttributeClassTopic) attribute.  
  
 The following sample generates CS0662:  
  
```  
// CS0662.cs  
using System.Runtime.InteropServices;  
  
interface I  
{  
   void method([Out] ref int i);   // CS0662  
   // try one of the following lines instead  
   // void method(ref int i);  
   // void method([Out, In]ref int i);  
}  
  
class test  
{  
   public static void Main()  
   {  
   }  
}  
```