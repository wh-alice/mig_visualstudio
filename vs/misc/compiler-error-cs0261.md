---
title: "Compiler Error CS0261 | Microsoft Docs"
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
  - "CS0261"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0261"
ms.assetid: c2af7b31-4a48-457a-8d9b-0956dd0d46f9
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
# Compiler Error CS0261
Partial declarations of 'type' must be all classes, all structs, or all interfaces  
  
 This error occurs if a partial type is declared as a different type of construct in various places. For more information, see [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0261:  
  
```  
// CS0261.cs  
partial class A  // CS0261 – A declared as a class here, but as a struct below  
{  
}  
  
partial struct A  
{  
}  
```