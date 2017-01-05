---
title: "Could not find standard library: &#39;&lt;filename&gt;&#39;"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc40049"
  - "bc40049"
helpviewer_keywords: 
  - "BC40049"
ms.assetid: a292f97e-4852-4021-b300-7ab47beb95d9
caps.latest.revision: 7
ms.author: "shoag"
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
# Could not find standard library: &#39;&lt;filename&gt;&#39;
[!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] is unable to find or open one of the standard DLL libraries needed for compilation and linking.  
  
 The unusable library is most likely to be either mscorlib.dll or microsoft.visualbasic.dll.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC40049  
  
### To correct this error  
  
1.  Verify that the file cited in the error message is present on the hard disk from which you are running [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]. Normally the standard libraries should reside in a subdirectory under \WINNT\Microsoft.NET\Framework or \WINDOWS\Microsoft.NET\Framework.  
  
2.  Verify that neither the file nor the directory has a setting or attribute that prevents read access by [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)].  
  
3.  Verify that the file name and extension are spelled correctly. Capitalization is not a concern.  
  
4.  If the file appears to be properly placed and accessible, it might be corrupted on the disk. Reinstall [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] if possible.  
  
5.  Note the exact file name and extension and contact Microsoft Product Support Services.  
  
## See Also  
 [Building from the Command Line](../Topic/Building%20from%20the%20Command%20Line%20\(Visual%20Basic\).md)   
 [How to: Invoke the Command-Line Compiler](../Topic/How%20to:%20Invoke%20the%20Command-Line%20Compiler%20\(Visual%20Basic\).md)   
 [Talk to Us](../ide/talk-to-us.md)