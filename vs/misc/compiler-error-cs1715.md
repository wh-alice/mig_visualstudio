---
title: "Compiler Error CS1715 | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1715"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1715"
ms.assetid: 740044d1-a61c-4156-bc6a-adf26c7499ec
caps.latest.revision: 9
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
# Compiler Error CS1715
'Type1': type must be 'Type2' to match overridden member 'MemberName'  
  
 This error is the same as [Compiler Error CS0508](../misc/compiler-error-cs0508.md), except that CS0508 now only applies to methods that have return types, while CS1715 applies to properties and indexers that only have 'types' instead of 'return types'.  
  
## Example  
 The following code generates CS1715.  
  
```  
// CS1715.cs  
abstract public class Base  
{  
    abstract public int myProperty  
    {  
        get;  
        set;  
    }  
}  
  
public class Derived : Base  
{  
    int myField;  
    public override double myProperty  // CS1715  
    // try the following line instead  
    // public override int myProperty  
    {  
        get { return myField; }  
        set { myField;= value; }  
    }  
  
    public static void Main()  
    {  
        Derived d = new Derived();  
        d.myProperty = 5;  
    }  
}  
```