---
title: "Possible problem detected while building assembly &#39;&lt;assemblyname&gt;&#39;: &lt;error&gt;"
ms.custom: na
ms.date: "10/10/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc40010"
  - "bc40010"
helpviewer_keywords: 
  - "BC40010"
ms.assetid: 3a4f4a4a-a5ad-4501-bf4c-0fbf25c50734
caps.latest.revision: 11
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
# Possible problem detected while building assembly &#39;&lt;assemblyname&gt;&#39;: &lt;error&gt;
The ALink tool, called by the [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)] compiler, reports an error building the assembly. Possible causes include the following:  
  
-   A signed assembly making reference to an unsigned assembly. In this case, you should consider whether the referenced assembly satisfies your security criteria.  
  
-   Building a 64-bit application on a 32-bit platform. In this case, you must ensure that 64-bit versions of all referenced assemblies are installed on the target platform. For a common language runtime (CLR) assembly, this is handled automatically, although this error message is still generated.  
  
 This message is a warning. The compiler is continuing to generate the assembly. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC40010  
  
### To correct this error  
  
1.  Examine the quoted error message and take appropriate action.  
  
2.  Compile the program again to see if the error recurs.  
  
3.  If the error recurs, reinstall the [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)] compiler.  
  
4.  If the error persists after reinstallation, gather information about the circumstances and notify Microsoft Product Support Services.  
  
## See Also  
 [PAVEOVER Product Support and Accessibility](http://msdn.microsoft.com/14e1d293-7b6d-40a6-bf3e-a92f8ee6c88c)   
 [Common Language Runtime Overview](http://msdn.microsoft.com/0fd9aeae-af10-435f-86d4-e76619741e4a)