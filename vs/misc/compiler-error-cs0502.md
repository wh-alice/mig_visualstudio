---
title: "Compiler Error CS0502 | Microsoft Docs"
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
  - "CS0502"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0502"
ms.assetid: 6cd6deda-73a1-42d8-893b-45a685e63380
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
# Compiler Error CS0502
'member' cannot be both abstract and sealed  
  
 A class member cannot be both [abstract](/dotnet/csharp/language-reference/keywords/abstract) and [sealed](/dotnet/csharp/language-reference/keywords/sealed).  
  
 The following sample generates CS0502:  
  
```  
// CS0502.cs  
public class B  
{  
   abstract public void F();  
}  
  
public class C : B  
{  
   abstract sealed override public void F()   // CS0502  
   {  
   }  
}  
  
public class CMain  
{  
    public static void Main()  
    { }  
}  
```