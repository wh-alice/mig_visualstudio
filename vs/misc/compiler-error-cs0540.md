---
title: "Compiler Error CS0540 | hehe"
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
  - "CS0540"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0540"
ms.assetid: 2da2cd4a-0ff1-45ea-bb72-ea078bc95dea
caps.latest.revision: 12
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
# Compiler Error CS0540
'interface member' : containing type does not implement interface 'interface'  
  
 You attempted to implement an interface member in a [class](../Topic/class%20\(C%23%20Reference\).md) that does not derive from the [interface](../Topic/interface%20\(C%23%20Reference\).md). You should either delete the implementation of the interface member or add the interface to the base-class list of the class.  
  
## Example  
 The following sample generates CS0540.  
  
```  
// CS0540.cs  
interface I  
{  
   void m();  
}  
  
public class Clx  
{  
   void I.m() {}   // CS0540  
}  
  
// OK  
public class Cly : I  
{  
   void I.m() {}  
   public static void Main() {}  
}  
```  
  
## Example  
 The following sample generates CS0540.  
  
```  
// CS0540_b.cs  
using System;  
class C {  
   void IDisposable.Dispose() {}   // CS0540  
}  
  
class D : IDisposable {  
   void IDisposable.Dispose() {}  
   public void Dispose() {}  
  
   static void Main() {  
      using (D d = new D()) {}  
   }  
}  
```