---
title: "__gc"
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
  - "__gc"
  - "__gc_cpp"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "__gc types"
  - "classes [C++], managed"
  - "managed classes"
ms.assetid: 63b1e7ab-d1c8-4582-aa89-21bfddf694a9
caps.latest.revision: 11
ms.author: "mblome"
manager: "douge"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# __gc
> [!NOTE]
>  This topic applies only to version 1 of Managed Extensions for C++. This syntax should only be used to maintain version 1 code. See [Classes and Structs](../Topic/Classes%20and%20Structs%20%20\(C++%20Component%20Extensions\).md) for information on using the equivalent functionality in the new syntax.  
  
 Declares a __gc type.  
  
## Syntax  
  
```  
  
      __gc array-specifier  
__gc class-specifier  
__gc struct-specifier  
__gc interface-specifier  
__gc pointer-specifier  
__gc new  
```  
  
## Remarks  
 A __gc type is a C++ language extension that simplifies .NET Framework programming by providing features such as interoperability and garbage collection.  
  
> [!NOTE]
>  Every member function of an abstract __gc class must be defined unless the member function is pure virtual.  
  
 In Managed Extensions for C++, the equivalents to a C# class and a C# struct are as follows:  
  
|Managed Extensions for C++|C#|For more information|  
|----------------------------------|---------|--------------------------|  
|__gc struct or \__gc class|class|[class](../Topic/class%20\(C%23%20Reference\).md) keyword|  
|__value struct or \__value class|struct|[struct](../Topic/struct%20\(C%23%20Reference\).md) keyword|  
  
## Example  
 In the following example, a managed class (`X`) is declared with a public data member, which is manipulated through a managed pointer:  
  
```  
// keyword__gc.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__gc class X {  
public:  
   int i;  
   int ReturnInt() { return 5; }  
};  
  
int main() {  
   // X is a __gc class, so px is a __gc pointer  
   X* px;  
   px = new X;   // creates a managed object of type X  
   Console::WriteLine(px->i);  
  
   px->i = 4;   // modifies X::i through px  
   Console::WriteLine(px->i);  
  
   int n = px->ReturnInt();   // calls X::ReturnInt through px  
   Console::WriteLine(n);  
}  
```  
  
## Output  
  
```  
0  
4  
5  
```