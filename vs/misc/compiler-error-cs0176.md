---
title: "Compiler Error CS0176"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0176"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0176"
ms.assetid: 783c13d8-5ac3-4aeb-bd63-0468cb05550d
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
# Compiler Error CS0176
Static member 'member' cannot be accessed with an instance reference; qualify it with a type name instead  
  
 Only a class name can be used to qualify a [static](../Topic/static%20\(C%23%20Reference\).md) variable; an instance name cannot be a qualifier. For more information, see [Static Classes and Static Class Members](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0176:  
  
```  
// CS0176.cs  
public class MyClass2  
{  
    public static int num;  
}  
  
public class Test  
{  
    public static void Main()  
    {  
        MyClass2 mc2 = new MyClass2();  
        int i = mc2.num;   // CS0176  
        // try the following line instead  
        // int i = MyClass2.num;  
    }  
}  
  
```