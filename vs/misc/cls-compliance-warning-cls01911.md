---
title: "CLS Compliance Warning CLS01911 | hehe"
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
  - "CLS01911"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLS01911"
ms.assetid: 673a701a-166b-4782-bff4-a198f70becd5
caps.latest.revision: 8
ms.author: "corob"
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
# CLS Compliance Warning CLS01911
CLS-compliant interfaces shall not define static methods, nor shall they define fields  
  
 A CLS-compliant interface cannot contain static methods or fields.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](http://msdn.microsoft.com/en-us/3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01911:  
  
```  
// CLS01911.cpp  
// compile with: /clr /LD  
// CLS01911 expected  
  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public interface class IOne {  
   static void Method1() {}   // interface static method not cls compliant  
};  
```