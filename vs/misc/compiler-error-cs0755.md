---
title: "Compiler Error CS0755 | Microsoft Docs"
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
  - "CS0755"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0755"
ms.assetid: 80613029-a009-4bdf-b1c2-1eec1e60c7b4
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
# Compiler Error CS0755
Both partial method declarations must be extension methods or neither may be an extension method.  
  
 A partial method consists of a defining declaration (signature) and an optional implementing declaration (body). If the defining declaration is an extension method, the implementing declaration, if one is defined, must also be an extension method. And if the defining method is not an extension method, the implementing must not be one either.  
  
### To correct this error  
  
1.  Either remove the `this` modifier from one of the parts, or add it to the other.  
  
## Example  
 The following example generates CS0755:  
  
```  
// cs0755.cs  
    public static partial class Ext  
    {  
        static partial void Part(this C c); //Extension method  
  
        // Typically the implementing declaration is in a separate file.  
        static partial void Part(C c) //CS0755  
        {  
        }  
    }  
  
    public partial class C  
    {  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```  
  
## See Also  
 [Extension Methods](/dotnet/csharp/programming-guide/classes-and-structs/extension-methods)