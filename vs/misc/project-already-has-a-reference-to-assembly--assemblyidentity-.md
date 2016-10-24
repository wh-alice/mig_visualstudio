---
title: "Project already has a reference to assembly &lt;assemblyidentity&gt;"
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
  - "bc32208"
  - "vbc32208"
helpviewer_keywords: 
  - "BC32208"
ms.assetid: a9f73a2c-5135-4315-bf2c-710ef216095d
caps.latest.revision: 7
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
# Project already has a reference to assembly &lt;assemblyidentity&gt;
Project already has a reference to assembly \<assemblyidentity>. A second reference to '\<filepath>' cannot be added.  
  
 A project makes more than one reference to the same assembly.  
  
 The assembly identity includes the assembly's name, version, public key if any, and culture.  
  
 One possible cause of this error is a reference to another copy of the assembly through a different file path than that of the original reference.  
  
 **Error ID:** BC32208  
  
### To correct this error  
  
-   Remove the second reference. It is unnecessary because it refers to the same assembly.  
  
## See Also  
 [Managing references in a project](../ide/managing-references-in-a-project.md)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](http://msdn.microsoft.com/en-us/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Troubleshooting Broken References](../ide/troubleshooting-broken-references.md)