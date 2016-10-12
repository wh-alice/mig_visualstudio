---
title: "Could not bind to dependency &#39;assembly&#39;"
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
  - "vs.tasklisterror.cantbinddependency"
ms.assetid: 0f76190d-d57e-4e0e-bec4-532aec978d08
caps.latest.revision: 8
ms.author: "mblome"
manager: "douge"
translation.priority.ht: 
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
# Could not bind to dependency &#39;assembly&#39;
One of your project's references itself contains an assembly reference (dependency) that was located but is not a valid assembly. This error will not prevent the project from building. However, a run-time error is possible.  
  
 This situation implies that the following three conditions are all true:  
  
-   There is more than one file on your disk with the same name.  
  
-   One of the files is not an assembly, but the other is.  
  
-   Your references path first searches the directory that contains the file that is not an assembly.  
  
 **To correct this error**  
  
-   Modify the order in which your project searches directories, looking for references. See [NIB: Reference Paths Dialog Box (Visual Basic)](assetId:///8e549b39-7256-456a-8fd7-089b23facf9c) for more information.  
  
## See Also  
 [Troubleshooting Broken References](../VS_IDE/troubleshooting-broken-references.md)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Assemblies in the Common Language Runtime](assetId:///33a0bc6a-6bb3-44c7-ada7-4a046e8c0945)