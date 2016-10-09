---
title: "Unable to sign file &#39;&lt;filename&gt;&#39;: &lt;error&gt;"
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
  - "bc31028"
  - "vbc31028"
helpviewer_keywords: 
  - "BC31028"
ms.assetid: 2cb22e75-5ee2-4e07-afc0-680a0bd543d4
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
# Unable to sign file &#39;&lt;filename&gt;&#39;: &lt;error&gt;
An error occurred when trying to sign the specified file. This error may have occurred for several reasons:  
  
-   Insufficient permissions.  
  
-   Missing system files required for Authenticode signing.  
  
-   A reference to a non-existent certificate or private-key file.  
  
-   Incorrect spelling of a file name or URL.  
  
 **Error ID:** BC31028  
  
### To correct this error  
  
1.  Enter correct certificate and private key file names.  
  
2.  If you are using Authenticode signing, check that the files, Signcode.exe and Javasign.dll, are present, and that their read-only attribute is not set.  
  
3.  Make sure you have `Write` permission to the file.  
  
## See Also  
 [File Signing Tool (Signcode.exe)](assetId:///2d299154-34ea-41ba-ad12-17075bb7e1db)   
 [Deployment and Authenticode Signing](assetId:///ecc3f059-da2e-445b-9b87-5b2978e2f8b2)