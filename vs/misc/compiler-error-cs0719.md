---
title: "Compiler Error CS0719 | Microsoft Docs"
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
  - "CS0719"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0719"
ms.assetid: 308a1a54-43b9-4970-8206-88e8f76d394e
caps.latest.revision: 6
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
# Compiler Error CS0719
'type': array elements cannot be of static type  
  
 An array of static type does not make sense since array elements are instances, but it is not possible to create instances of static types.  
  
 The following sample generates CS0719:  
  
```  
// CS0719.cs  
public static class SC  
{  
   public static void F()  
   {  
   }  
}  
  
public class CMain  
{  
   public static void Main()  
   {  
      SC[] sca = new SC[10];  // CS0719  
   }  
}  
```