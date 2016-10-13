---
title: "MSBuild Error MSB3162"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MSBuild.GenerateBootstrapper.DependencyNotFound"
helpviewer_keywords: 
  - "MSB3162"
ms.assetid: 35189e5d-c065-4d57-bf78-6433771a5063
caps.latest.revision: 4
ms.author: "mblome"
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
# MSBuild Error MSB3162
**MSB3162: Item '\<package>' could not find dependent item '\<package>'.**  
  
 This error occurs when one bootstrapper package depends on another, but the manifest for the dependent bootstrapper prerequisite cannot be found.