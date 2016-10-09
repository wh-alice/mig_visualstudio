---
title: "Compiler Error CS0591"
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
  - "CS0591"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0591"
ms.assetid: b8acbcdb-dc66-4338-9ddd-d606e5a2c57e
caps.latest.revision: 6
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
# Compiler Error CS0591
Invalid value for argument to 'attribute' attribute  
  
 An attribute was passed either an invalid argument or two mutually exclusive arguments.  
  
## Example  
 The following sample generates CS0591:  
  
```  
// CS0591.cs  
using System;  
  
[AttributeUsage(0)]   // CS0591  
class I: Attribute  
{  
}  
  
public class a  
{  
    public static void Main()  
    {  
    }  
}  
```