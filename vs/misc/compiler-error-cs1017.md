---
title: "Compiler Error CS1017 | Microsoft Docs"
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
  - "CS1017"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1017"
ms.assetid: e0902e8a-b042-4711-a8a6-83456a3f88cb
caps.latest.revision: 9
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
# Compiler Error CS1017
Catch clauses cannot follow the general catch clause of a try statement  
  
 A `catch` block that does not take any parameters must be the last in a series of `catch` blocks. For more information on exceptions, see [Exception Handling Statements](/dotnet/csharp/language-reference/keywords/exception-handling-statements).  
  
## Example  
 The following sample generates CS1017:  
  
```  
// CS1017.cs  
using System;  
  
namespace x  
{  
    public class b : Exception  
    {  
    }  
  
    public class a  
    {  
        public static void Main()  
        {  
            try  
            {  
            }  
  
            catch   // CS1017, must be last catch  
            {  
            }  
  
            catch(b)  
            {  
                throw;  
            }  
        }  
    }  
}  
```