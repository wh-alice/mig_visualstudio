---
title: "Compiler Error CS0274 | Microsoft Docs"
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
  - "CS0274"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0274"
ms.assetid: bbd2d64e-a756-4713-b9ed-711d50b65e00
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
# Compiler Error CS0274
Cannot specify accessibility modifiers for both accessors of the property or indexer 'property/indexer'  
  
 This error occurs when you declare a property or indexer with access modifiers on both its accessors. To resolve this error, use an access modifier on only one of the two accessors. For more information, see [Accessor Accessibility](/dotnet/csharp/programming-guide/classes-and-structs/restricting-accessor-accessibility).  
  
 The following example generates CS0274:  
  
```  
// CS0274.cs  
public class MyClass  
{  
    public int Property   // CS0274  
    {  
        public get { return 0; }  
        protected set { }  
    }  
}  
```