---
title: "Compiler Warning (level 1) CS3023 | Microsoft Docs"
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
  - "CS3023"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS3023"
ms.assetid: fd7782f9-f18a-4ce8-843b-95bf19b54317
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
# Compiler Warning (level 1) CS3023
CLSCompliant attribute has no meaning when applied to return types.  Try putting it on the method instead.  
  
 Function return types are not checked for CLS Compliance, since the CLS Compliance rules apply to methods and type declarations.  
  
## Example  
 The following example generates warning CS3023:  
  
```  
// C3023.cs  
  
[assembly:System.CLSCompliant(true)]  
public class Test  
{  
    [return:System.CLSCompliant(true)]  // CS3023  
    // Try this instead:  
    // [method:System.CLSCompliant(true)]  
    public static int Main()  
    {  
        return 0;  
    }  
}  
```