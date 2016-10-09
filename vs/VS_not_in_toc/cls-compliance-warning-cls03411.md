---
title: "CLS Compliance Warning CLS03411"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CLS03411"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLS03411"
ms.assetid: 79b0955a-5a86-46a8-90e9-4419c9068bbe
caps.latest.revision: 9
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
# CLS Compliance Warning CLS03411
The CLS only allows a subset of the encodings of custom attributes  
  
 The CLS only allows a subset of types as parameters to the constructor of a custom attributes, or as the type of data members of a custom attribute. The only types that shall appear are:  
  
-   System.Type  
  
-   System.String  
  
-   System.Char  
  
-   System.Boolean  
  
-   System.Byte  
  
-   System.Int16  
  
-   System.Int32  
  
-   System.Int64  
  
-   System.Single  
  
-   System.Double  
  
-   any enumeration types based on a CLS-compliant base integer type.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS03411:  
  
```  
// CLS03411.cpp  
// compile with: /clr /LD  
// CLS03411 expected  
using namespace System;  
using namespace System::Reflection;  
using namespace cli::language;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
// CLS03411  
[AttributeUsage(AttributeTargets::All, AllowMultiple=true)]  
public ref class MyAttribute1 : public Attribute {  
public:  
   MyAttribute1(Object^ parameter) {}  
};  
  
// OK  
[AttributeUsage(AttributeTargets::All, AllowMultiple=true)]  
public ref class MyAttribute3 : public Attribute {  
public:  
   MyAttribute3(Char parameter) {}  
};  
```