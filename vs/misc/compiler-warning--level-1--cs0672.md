---
title: "Compiler Warning (level 1) CS0672"
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
  - "CS0672"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0672"
ms.assetid: 140a8708-97d0-444b-980b-62e74328cafb
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
# Compiler Warning (level 1) CS0672
Member 'member1' overrides obsolete member 'member2. Add the Obsolete attribute to 'member1'  
  
 The compiler found an `override` to a method marked as `obsolete`. However, the overriding method was not itself marked as obsolete. The overriding method will still generate [CS0612](../misc/compiler-warning--level-1--cs0612.md), if called.  
  
 Review your method declarations and explicitly indicate whether a method (and all of its overrides) should be marked `obsolete`.  
  
 The following sample generates CS0672:  
  
```  
// CS0672.cs  
// compile with: /W:1  
class MyClass  
{  
   [System.Obsolete]  
   public virtual void ObsoleteMethod()  
   {  
   }  
}  
  
class MyClass2 : MyClass  
{  
   public override void ObsoleteMethod()   // CS0672  
   {  
   }  
}  
  
class MainClass  
{  
   static public void Main()  
   {  
   }  
}  
```