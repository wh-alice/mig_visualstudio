---
title: "Compiler Error CS0316 | Microsoft Docs"
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
  - "CS0316"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0316"
ms.assetid: 8b70abbe-dd4f-473f-8dfe-f8309abef276
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
# Compiler Error CS0316
The parameter name 'name' conflicts with an automatically-generated parameter name.  
  
 Reserved words cannot be used as parameter names. In the example that follows, `value` is a reserved word in the context of a default property or indexer accessor.  
  
### To correct this error  
  
1.  Change the name of the parameter.  
  
## Example  
 The following code generates CS0316:  
  
```  
// cs0316.cs  
// Compile with: /target:library  
public class Test  
{  
    public int this[int value] // CS0316  
    {  
        get { return 1; }  
        set { }  
    }  
}  
```  
  
## See Also  
 [Indexers](/dotnet/csharp/programming-guide/indexers/index)   
 [C# Keywords](/dotnet/csharp/language-reference/keywords/index)