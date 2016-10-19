---
title: "SccWillCreateSccFile Function"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "SccWillCreateSccFile"
helpviewer_keywords: 
  - "SccWillCreateSccFile function"
ms.assetid: 0d7542f0-4351-41b3-b24c-960ab99c05a1
caps.latest.revision: 12
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
# SccWillCreateSccFile Function
This function determines whether the source control plug-in supports the creation of the MSSCCPRJ.SCC file for each of the given files.  
  
## Syntax  
  
```cpp#  
SCCRTN SccWillCreateSccFile(  
   LPVOID  pContext,  
   LONG    nFiles,  
   LPCSTR* lpFileNames,  
   LPBOOL  pbSccFiles  
);  
```  
  
#### Parameters  
 pContext  
 [in] The source control plug-in context pointer.  
  
 nFiles  
 [in] The number of file names included in the `lpFileNames` array as well as the length of the `pbSccFiles` array.  
  
 lpFileNames  
 [in] An array of fully qualified file names to check (array must be allocated by caller).  
  
 pbSccFiles  
 [in, out] Array in which to store the results.  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Success.|  
|SCC_E_INVALIDFILEPATH|One of the paths in the array is invalid.|  
|SCC_E_NONSPECIFICERROR|Nonspecific failure.|  
  
## Remarks  
 This function is called with a list of files to determine if the source control plug-in provides support in the MSSCCPRJ.SCC file for each of the given files (for more information on the MSSCCPRJ.SCC file, see [MSSCCPRJ.SCC File](../extensibility/mssccprj.scc-file.md)). Source control plug-ins can declare whether they have the capability of creating MSSCCPRJ.SCC files by declaring `SCC_CAP_SCCFILE` during initialization. The plug-in returns `TRUE` or `FALSE` per file in the `pbSccFiles` array to indicate which of the given files have MSSCCPRJ.SCC support. If the plug-in returns a success code from the function, the values in the return array are honored. On failure, the array is ignored.  
  
## See Also  
 [Source Control Plug-in API Functions](../extensibility/source-control-plug-in-api-functions.md)   
 [MSSCCPRJ.SCC File](../extensibility/mssccprj.scc-file.md)