---
title: "CA1824: Mark assemblies with NeutralResourcesLanguageAttribute"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CA1824"
  - "MarkAssembliesWithNeutralResourcesLanguage"
helpviewer_keywords: 
  - "MarkAssembliesWithNeutralResourcesLanguage"
  - "CA1824"
ms.assetid: 10e97f8a-aa6e-47aa-b253-1e5d3a295d82
caps.latest.revision: 12
ms.author: "douge"
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
# CA1824: Mark assemblies with NeutralResourcesLanguageAttribute
|||  
|-|-|  
|TypeName|MarkAssembliesWithNeutralResourcesLanguage|  
|CheckId|CA1824|  
|Category|Microsoft.Performance|  
|Breaking Change|Non-breaking|  
  
## Cause  
 An assembly contains a **ResX**-based resource but does not have the \<xref:System.Resources.NeutralResourcesLanguageAttribute?displayProperty=fullName> applied to it.  
  
## Rule Description  
 The **NeutralResourcesLanguage** attribute informs the **ResourceManager** of the language that was used to display the resources of the neutral culture for an assembly. When it looks up resources in the same culture as the neutral resources language, the **ResourceManager** automatically uses the resources that are located in the main assembly. It does this instead of searching for a satellite assembly that has the current user interface culture for the current thread. This improves lookup performance for the first resource that you load and can reduce your working set.  
  
## Fixing Violations  
 To fix a violation of this rule, add the attribute to the assembly, and specify the language of the resources of the neutral culture.  
  
## Specifying the Language  
  
#### To specify the language of the resource of the neutral culture  
  
1.  In **Solution Explorer**, right-click your project, and then Click **Properties**.  
  
2.  From the left navigation bar select **Application**, and then click **Assembly Information**.  
  
3.  In the **Assembly Information** dialog box, select the language from the **Neutral Language** drop-down list.  
  
4.  Click **OK**.  
  
## When to Suppress Warnings  
 It is permissible to suppress a warning from this rule. However, startup performance might decrease.