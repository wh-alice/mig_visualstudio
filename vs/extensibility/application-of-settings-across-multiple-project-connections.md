---
title: "Application of Settings Across Multiple Project Connections"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "source control plug-ins, application of settings"
ms.assetid: 2116d3d0-c46c-4d0a-b482-08a178584f46
caps.latest.revision: 15
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# Application of Settings Across Multiple Project Connections
A source control plug-in built using the Source Control Plug-in API 1.2, can use a batch operation to execute the same source control operation across multiple projects or multiple connection contexts. Batches can be used to eliminate redundant, per-project dialog boxes from the user experience.  
  
 If a user selects multiple items that belong to more than one connection in a source control plug-in built using the Source Control Plug-in API 1.1,  (for example, two Web projects on different file-share machines) and checks them out, the user sees the same dialog box repeatedly. This happens even if the user clicks the **Apply to All** check box in the dialog box, because the IDE resets its state for each connection context.  
  
## New Capability Flag  
 `SccBeginBatch` Function sets the `SCC_CAP_BATCH` flag to indicate that a batch operation is in progress  
  
## New Functions  
 The following new functions support the batch operation:  
  
-   [SccBeginBatch](../extensibility/sccbeginbatch-function.md)  
  
-   [SccEndBatch](../extensibility/sccendbatch-function.md)  
  
 The `SCCBeginBatch` function starts a group of source control operations. `SccEndBatch` closes the group. The groups may not be nested.  
  
## See Also  
 [What's New in the Source Control Plug-in API Version 1.2](../extensibility/what-s-new-in-the-source-control-plug-in-api-version-1.2.md)