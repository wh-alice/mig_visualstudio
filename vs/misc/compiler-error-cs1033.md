---
title: "Compiler Error CS1033 | Microsoft Docs"
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
  - "CS1033"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1033"
ms.assetid: eb0f4001-84a6-4918-a648-cf710d038de7
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
# Compiler Error CS1033
Source file has exceeded the limit of 16,707,565 lines representable in the PDB; debug information will be incorrect  
  
 A source-code file exceeded the maximum allowable number of lines that the compiler can process. To resolve this error, create two or more source-code files from the original file. The maximum number of lines is 268,435,454 lines. If you are using **/debug**, using more than 16,707,566 will result in corrupted debug information.