---
title: "Compiler Error CS0418 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0418"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0418"
ms.assetid: b78fafde-428b-4fa2-a933-c4614760bb71
caps.latest.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
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
# Compiler Error CS0418
'class name': an abstract class cannot be sealed or static  
  
 An abstract class cannot be used to create objects unless it is derived from, so it makes no sense to be sealed. An abstract class cannot meaningfully be static either; abstract classes are designed to support an object hierarchy that will use the abstract class as a base.  
  
## Example  
 The following sample generates CS0418:  
  
```  
// CS0418.cs  
public abstract sealed class C  // CS0418  
{  
}  
  
sealed static class S  // CS0418  
{  
}  
  
public class MyClass  
{  
    public static void Main()  
    {  
    }  
}  
```