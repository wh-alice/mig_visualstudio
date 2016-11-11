---
title: "Compiler Error CS0546 | Microsoft Docs"
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
  - "CS0546"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0546"
ms.assetid: d259c86f-ee29-4e2d-b381-6ba7252af87e
caps.latest.revision: 13
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
# Compiler Error CS0546
'accessor' : cannot override because 'property' does not have an overridable set accessor  
  
 An attempt to override one of the accessor methods for a property failed because the accessor cannot be overridden. This error can occur if:  
  
-   the base class property is not declared as [virtual](/dotnet/csharp/language-reference/keywords/virtual).  
  
-   the base class property does not declare the [get](/dotnet/csharp/language-reference/keywords/get) or [set](/dotnet/csharp/language-reference/keywords/set) accessor you are trying to override.  
  
 If you do not want to override the base class property, you can use the [new](/dotnet/csharp/language-reference/keywords/new) keyword before the property in derived class.  
  
 For more information, see [Using Properties](/dotnet/csharp/programming-guide/classes-and-structs/using-properties).  
  
## Example  
 The following sample generates CS0546 because the base class does not declare a set accessor for the property.  
  
```  
// CS0546.cs  
// compile with: /target:library  
public class a  
{  
   public virtual int i  
   {  
      get  
      {  
         return 0;  
      }  
   }  
  
   public virtual int i2  
   {  
      get  
      {  
         return 0;  
      }  
  
      set {}  
   }  
}  
  
public class b : a  
{  
   public override int i  
   {  
      set {}   // CS0546 error no set  
   }  
  
   public override int i2  
   {  
      set {}   // OK  
   }  
}  
```  
  
## See Also  
 [Properties](/dotnet/csharp/programming-guide/classes-and-structs/properties)