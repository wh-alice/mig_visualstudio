---
title: "Compiler Error CS0262"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0262"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0262"
ms.assetid: 44f8661f-c934-483f-84cd-00ca8257e50a
caps.latest.revision: 8
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
# Compiler Error CS0262
Partial declarations of 'type' have conflicting accessibility modifiers  
  
 This error occurs if a partial type has inconsistent modifiers such as public, private, protected, internal, or abstract. These modifiers must be consistent in all partial declarations for that type. For more information, see [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0262:  
  
```  
// CS0262.cs  
class A  
{  
    public partial class C  // CS0262  
    {  
    }  
    private partial class C  
    {  
    }  
}  
```