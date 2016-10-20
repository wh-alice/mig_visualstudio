---
title: "SccCheckout Function | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "SccCheckout"
helpviewer_keywords: 
  - "SccCheckout function"
ms.assetid: 06e9ecd7-fc09-40c1-9dd1-2b56c622c80b
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
# SccCheckout Function
Given a list of fully qualified file names, this function checks them out to the local drive. The comment applies to all files being checked out. The comment argument can be a `null` string.  
  
## Syntax  
  
```cpp#  
SCCRTN SccCheckout (  
   LPVOID    pvContext,  
   HWND      hWnd,  
   LONG      nFiles,  
   LPCSTR*   lpFileNames,  
   LPCSTR    lpComment,  
   LONG      fOptions,  
   LPCMDOPTS pvOptions  
);  
```  
  
#### Parameters  
 pvContext  
 [in] The source control plug-in context structure.  
  
 hWnd  
 [in] A handle to the IDE window that the source control plug-in can use as a parent for any dialog boxes that it provides.  
  
 nFiles  
 [in] Number of files selected to be checked out.  
  
 lpFileNames  
 [in] Array of fully qualified local path names of files to be checked out.  
  
 lpComment  
 [in] Comment to be applied to each of the selected files being checked out.  
  
 fOptions  
 [in] Command flags (see [Bitflags Used by Specific Commands](../extensibility/bitflags-used-by-specific-commands.md)).  
  
 pvOptions  
 [in] Source control plug-in-specific options.  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Check out was successful.|  
|SCC_E_FILENOTCONTROLLED|The selected file is not under source code control.|  
|SCC_E_ACCESSFAILURE|There was a problem accessing the source control system, probably due to network or contention issues. A retry is recommended.|  
|SCC_E_NOTAUTHORIZED|The user is not allowed to perform this operation.|  
|SCC_E_NONSPECIFICERROR|Nonspecific failure. The file was not checked out.|  
|SCC_E_ALREADYCHECKEDOUT|The user already has the file checked out.|  
|SCC_E_FILEISLOCKED|The file is locked, prohibiting the creation of new versions.|  
|SCC_E_FILEOUTEXCLUSIVE|Another user has done an exclusive checkout on this file.|  
|SCC_I_OPERATIONCANCELED|The operation was cancelled before completion.|  
  
## See Also  
 [Source Control Plug-in API Functions](../extensibility/source-control-plug-in-api-functions.md)   
 [Bitflags Used by Specific Commands](../extensibility/bitflags-used-by-specific-commands.md)