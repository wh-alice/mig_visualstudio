---
title: "Compiler Error CS0844"
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
  - "CS0844"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0844"
ms.assetid: ccf74e01-292a-42d0-897c-8add7aee2118
caps.latest.revision: 5
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
# Compiler Error CS0844
Cannot use local variable 'name' before it is declared. The declaration of the local variable hides the field 'name'.  
  
 An identifier can have only one meaning in a given block. Local variables that have the same name as class fields can hide the field by introducing a second meaning for the identifier. Therefore the compiler generates an error when you refer to a class field in a method, and then declare a local variable by the same name.  
  
### To correct this error  
  
-   Use `this.num` to refer to the class field.  
  
-   Give the local variable a different name from the class field.  
  
## Example  
 The following code generates CS0844:  
  
```  
class Test  
    {  
        int num;  
        public void TestMethod()  
        {  
            num = 5; // CS0844  
            int num = 6;        }  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```