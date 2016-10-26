---
title: "Compiler Error CS2016"
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
  - "CS2016"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS2016"
ms.assetid: 69f77502-f726-4856-ac87-e556eeb67349
caps.latest.revision: 7
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
# Compiler Error CS2016
Code page 'codepage' is invalid or not installed  
  
 The [/codepage](../Topic/-codepage%20\(C%23%20Compiler%20Options\).md) compiler option was passed an invalid value.  
  
 The following sample generates CS2016:  
  
```  
// CS2016.cs  
// compile with: /codepage:x  
// CS2016 expected  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```