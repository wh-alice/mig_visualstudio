---
title: "Compiler Error CS0811"
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
  - "CS0811"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0811"
ms.assetid: 99f81ad3-684f-47aa-adb8-360e24901454
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
# Compiler Error CS0811
The fully qualified name for 'name' is too long for debug information. Compile without '/debug' option.  
  
 There are size constraints on variable and type names in debug information.  
  
### To correct this error  
  
1.  If modifying the name is not possible, the only alternative is to compile without the [/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md) option.  
  
## Example  
 The following code generates CS0811:  
  
```  
// cs0811.cs  
//Compile with: /debug  
using System;  
using System.Collections.Generic;  
  
namespace TestNamespace  
{  
    using Long = List<List<List<List<List<List<List<List<List<List<List<List<List  
   <List<List<List<List<List<List<List<List<List<List<List<List<List<List<List<int>>>>>>>>>>>>>>>>>>>>>>>>>>>>; // CS0811  
  
    class Test  
    {  
        static int Main()  
        {  
            return 1;  
        }  
    }  
}  
```