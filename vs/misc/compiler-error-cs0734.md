---
title: "Compiler Error CS0734 | Microsoft Docs"
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
  - "CS0734"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0734"
ms.assetid: 9e1b0e49-bfc3-400c-9fd1-37e3c827e656
caps.latest.revision: 7
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
# Compiler Error CS0734
The /moduleassemblyname option may only be specified when building a target type of 'module'  
  
 The compiler option **/moduleassemblyname** should only be used when building a .netmodule. See [/moduleassemblyname (C# Compiler Option)](/dotnet/csharp/language-reference/compiler-options/moduleassemblyname-compiler-option) for more information.  
  
 For more information on building a .netmodule, see [/target:module (C# Compiler Options)](../Topic/-target:module%20\(C%23%20Compiler%20Options\).md).  
  
## Example  
 The following sample generates CS0734. To resolve, add **/target:module** to the compilation.  
  
```  
// CS0734.cs  
// compile with: /moduleassemblyname:A  
// CS0734 expected  
public class Test {}  
```