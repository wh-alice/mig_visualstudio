---
title: "Compiler Error CS0154"
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
  - "CS0154"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0154"
ms.assetid: 815150da-09b4-4593-825f-1dd435c92da8
caps.latest.revision: 9
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
# Compiler Error CS0154
The property or indexer 'property' cannot be used in this context because it lacks the get accessor  
  
 An attempt to use a [property](../Topic/Using%20Properties%20\(C%23%20Programming%20Guide\).md) failed because no get accessor method was defined in the property. For more information, see [Fields](../Topic/Fields%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0154:  
  
```  
// CS0154.cs  
public class MyClass2  
{  
    public int i  
    {  
        set  
        {  
        }  
        // uncomment the get method to resolve this error  
        /*  
        get  
        {  
            return 0;  
        }  
        */  
    }  
}  
  
public class MyClass  
{  
    public static void Main()  
    {  
        MyClass2 myClass2 = new MyClass2();  
        int j = myClass2.i;   // CS0154, no get method  
    }  
}  
```