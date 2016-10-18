---
title: "Compiler Error CS1917"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1917"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1917"
ms.assetid: 05688706-e4b4-4273-9244-48cce1f7f9b9
caps.latest.revision: 6
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
# Compiler Error CS1917
Members of read-only field 'name' of type 'struct name' cannot be assigned with an object initializer because it is of a value type.  
  
 Read-only fields that are value types can only be assigned in a constructor.  
  
### To correct this error  
  
-   Change the struct to a class type.  
  
-   Initialize the struct with a constructor.  
  
## Example  
 The following code generates CS1917:  
  
```  
// cs1917.cs  
class CS1917  
{  
    public struct TestStruct  
    {  
        public int i;  
    }  
    public class C  
    {  
        public readonly TestStruct str = new TestStruct();  
        public static int Main()  
        {  
            C c = new C { str = { i = 1 } }; // CS1917  
            return 0;  
        }  
    }  
}  
```