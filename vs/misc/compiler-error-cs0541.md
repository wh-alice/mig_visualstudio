---
title: "Compiler Error CS0541 | Microsoft Docs"
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
  - "CS0541"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0541"
ms.assetid: ed812c07-24f7-43c6-9a44-553f27f6249d
caps.latest.revision: 7
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
# Compiler Error CS0541
'declaration' : explicit interface declaration can only be declared in a class or struct  
  
 An explicit [interface](/dotnet/csharp/language-reference/keywords/interface) declaration was found outside a [class](/dotnet/csharp/language-reference/keywords/class) or [struct](/dotnet/csharp/language-reference/keywords/struct).  
  
 The following sample generates CS0541:  
  
```  
// CS0541.cs  
namespace x  
{  
   interface IFace  
   {  
      void F();  
   }  
  
   interface IFace2 : IFace  
   {  
      void IFace.F();   // CS0541  
   }  
}  
```