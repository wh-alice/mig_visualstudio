---
title: "Compiler Error CS0508 | Microsoft Docs"
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
  - "CS0508"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0508"
ms.assetid: 28403573-6e64-4496-918d-fb50c8851e51
caps.latest.revision: 10
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
# Compiler Error CS0508
'Type 1': return type must be 'Type 2' to match overridden member 'Member Name'  
  
 An attempt was made to change the return type in a method override. To resolve this error, make sure both methods declare the same return type.  
  
## Example  
 The following sample generates CS0508.  
  
```  
// CS0508.cs  
// compile with: /target:library  
abstract public class Clx  
{  
   public int i = 0;  
   // Return type is int.  
   abstract public int F();  
}  
  
public class Cly : Clx  
{  
   public override double F()  
   {  
      return 0.0;   // CS0508  
   }  
}  
```