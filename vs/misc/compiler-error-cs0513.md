---
title: "Compiler Error CS0513"
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
  - "CS0513"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0513"
ms.assetid: 6f8569df-713d-4c9c-a675-6576dad139ce
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
# Compiler Error CS0513
'function' is abstract but it is contained in nonabstract class 'class'  
  
 A method cannot be an [abstract](../Topic/abstract%20\(C%23%20Reference\).md) member of a nonabstract class.  
  
 The following sample generates CS0513:  
  
```  
// CS0513.cs  
namespace x  
{  
   public class clx  
   {  
      abstract public void f();   // CS0513, abstract member of nonabstract class  
   }  
}  
```