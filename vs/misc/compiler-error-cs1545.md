---
title: "Compiler Error CS1545"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1545"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1545"
ms.assetid: 56c377b5-4cf1-4c7d-b51d-463bad78f3ef
caps.latest.revision: 16
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
# Compiler Error CS1545
Property, indexer, or event 'property' is not supported by the language; try directly calling accessor methods 'set accessor' or 'get accessor'  
  
 The code is consuming an object that has a non-default [indexer](../Topic/Indexers%20\(C%23%20Programming%20Guide\).md) and tried to use the indexed syntax. To resolve this error, call the property's `get` or `set` accessor method.  
  
## Example  
  
```  
// CPP1545.cpp  
// compile with: /clr /LD  
// a Visual C++ program  
using namespace System;  
public ref struct Employee {  
   Employee( String^ s, int d ) {}  
  
   property String^ name {  
      String^ get() {  
         return nullptr;  
      }  
   }  
};  
  
public ref struct Manager {  
   property Employee^ Report [String^] {  
      Employee^ get(String^ s) {  
         return nullptr;  
      }  
  
      void set(String^ s, Employee^ e) {}  
   }  
};  
```  
  
## Example  
 The following sample generates CS1545.  
  
```  
// CS1545.cs  
// compile with: /r:CPP1545.dll  
  
class x {  
   public static void Main() {  
      Manager Ed = new Manager();  
      Employee Bob = new Employee("Bob Smith", 12);  
      Ed.Report[ Bob.name ] = Bob;   // CS1545  
      Ed.set_Report( Bob.name, Bob);   // OK  
   }  
}  
```