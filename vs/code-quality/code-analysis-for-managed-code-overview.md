---
title: "Code Analysis for Managed Code Overview"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.projectpropertypages.codeanalysis"
helpviewer_keywords: 
  - "code analysis, managed code"
  - "managed code, code analysis"
ms.assetid: 12ec0dab-46a4-43d8-984a-440730ef37a9
caps.latest.revision: 35
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
# Code Analysis for Managed Code Overview
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

Code analysis for managed code analyzes managed assemblies and reports information about the assemblies, such as violations of the programming and design rules set forth in the Microsoft .NET Framework Design Guidelines.  
  
 The analysis tool represents the checks it performs during an analysis as warning messages. Warning messages identify any relevant programming and design issues and, when it is possible, supply information about how to fix the problem.  
  
## IDE (integrated development environment) Integration  
 As a developer, you can run code analysis on your project automatically or you can run it manually.  
  
 To run code analysis each time that you build a project, you select **Enable Code Analysis on Build (defines CODE_ANALYSIS constant)** on the project's Property Page. For more information, see [How to: Enable and Disable Automatic Code Analysis](../code-quality/how-to--enable-and-disable-automatic-code-analysis-for-managed-code.md).  
  
 To run code analysis manually on a project, on the **Analyze** menu, click **Run Code Analysis on***ProjectName*. For more information, see [How to: Enable and Disable Automatic Code Analysis](../code-quality/how-to--enable-and-disable-automatic-code-analysis-for-managed-code.md).  
  
## Rule Sets  
 Code analysis rules for managed code are grouped into *rule sets*. You can use one of the Microsoft standard rule sets, or you can create a custom rule set to fulfill a specific need. For more information, see [Using Rule Sets to Group Code Analysis Rules](../code-quality/using-rule-sets-to-group-code-analysis-rules.md).  
  
## In Source Suppression  
 Frequently, it is useful to indicate that a warning is non-applicable. This informs the developer, and other people who might review the code later, that a warning was investigated and then either suppressed or ignored.  
  
 In Source Suppression of warnings is implemented through custom attributes. To suppress a warning, add the attribute `SuppressMessage` to the source code as shown in the following example:  
  
 `[System.Diagnosis.CodeAnalysis.SuppressMessage("Microsoft.Design", "CA1039:ListsAreStrongTyped")]`  
  
 `Public class MyClass`  
  
 `{`  
  
 `// code`  
  
 `}`  
  
 For more information, see [Suppress Warnings By Using the SuppressMessage Attribute](../code-quality/suppress-warnings-by-using-the-suppressmessage-attribute.md).  
  
## Run code analysis as part of check-in policy  
 As an organization, you might want to require that all check-ins satisfy certain policies. In particular, you want to make sure that you follow these policies:  
  
-   There were no build errors in code being checked in.  
  
-   Code analysis was run as part of the most recent build.  
  
 You can accomplish this by specifying check-in policies. For more information, see [Enhancing Code Quality with Team Project Check-in Policies](../code-quality/enhancing-code-quality-with-team-project-check-in-policies.md).  
  
## Team Build Integration  
 You can use the integrated features of the build system to run the analysis tool as part of the build process. For more information, see [Build the application](http://msdn.microsoft.com/library/a971b0f9-7c28-479d-a37b-8fd7e27ef692).  
  
## See Also  
 [Using Rule Sets to Group Code Analysis Rules](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)   
 [How to: Enable and Disable Automatic Code Analysis](../code-quality/how-to--enable-and-disable-automatic-code-analysis-for-managed-code.md)