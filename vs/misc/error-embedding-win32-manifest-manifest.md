---
title: "Error embedding Win32 manifest: &lt;manifest&gt; | Microsoft Docs"
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
  - "vbc31191"
  - "bc31191"
helpviewer_keywords: 
  - "BC31191"
ms.assetid: 5babed58-d024-4acd-9838-fab8f07c4a37
caps.latest.revision: 4
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
# Error embedding Win32 manifest: &lt;manifest&gt;
The file specified for the `/win32manifest` compiler option cannot be embedded. This can be a result of insufficient security privileges to the manifest file.  
  
 **Error ID:** BC31191  
  
### To correct this error  
  
1.  Ensure that the identity running the Visual Basic compiler command has access to the Win32 manifest file.  
  
## See Also  
 [/win32manifest (Visual Basic)](/dotnet/visual-basic/reference/command-line-compiler/win32manifest)   
 [Visual Basic Command-Line Compiler](/dotnet/visual-basic/reference/command-line-compiler/index)