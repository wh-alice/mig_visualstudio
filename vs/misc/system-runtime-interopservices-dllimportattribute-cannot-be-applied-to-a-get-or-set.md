---
title: "&#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a &#39;Get&#39; or &#39;Set&#39; | Microsoft Docs"
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
  - "vbc31524"
  - "bc31524"
helpviewer_keywords: 
  - "BC31524"
ms.assetid: 3603e33a-a80b-448d-83e0-e5dbc9af4dcf
caps.latest.revision: 8
author: "stevehoag"
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
# &#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a &#39;Get&#39; or &#39;Set&#39;
The `DllImportAttribute` attribute was applied to a `Get` or `Set` property procedure.  
  
 **Error ID:** BC31524  
  
### To correct this error  
  
1.  Remove `DllImportAttribute` from `Get` and `Set` property procedures.  
  
## See Also  
 <xref:System.Runtime.InteropServices.DllImportAttribute>   
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)