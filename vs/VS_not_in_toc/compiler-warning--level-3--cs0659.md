---
title: "Compiler Warning (level 3) CS0659"
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
  - "CS0659"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0659"
ms.assetid: 63435ee6-c92f-4124-95d4-d8f4e5f0af80
caps.latest.revision: 9
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
# Compiler Warning (level 3) CS0659
'class' overrides Object.Equals(object o) but does not override Object.GetHashCode()  
  
 The compiler detected an override of the **Equals** function but no override for **GetHashCode**. An override of **Equals** implies that you also want to override **GetHashCode**.  
  
 For more information, see  
  
-   \<xref:System.Collections.Hashtable>.  
  
-   [Equality Operators](../Topic/Equality%20Operators.md)  
  
-   [NIB: Implementing the Equals Method](assetId:///30f28aaf-8b9e-46cd-a746-58a12473af2c)  
  
-   \<xref:System.Object.GetHashCode*>  
  
 The following sample generates CS0659:  
  
```  
// CS0659.cs  
// compile with: /W:3 /target:library  
class Test     
{  
   public override bool Equals(object o) { return true; }   // CS0659  
}  
  
// OK  
class Test2  
{  
   public override bool Equals(object o) { return true; }  
   public override int GetHashCode() { return 0; }  
}  
```