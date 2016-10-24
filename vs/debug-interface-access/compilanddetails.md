---
title: "CompilandDetails | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CompilandDetails symbol"
ms.assetid: ddc7d794-c622-4c63-b2a6-72f8b2d0022a
caps.latest.revision: 19
ms.author: "mikejo"
manager: "ghogen"
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
# CompilandDetails
Compiland information is split between symbols with a `SymTagCompiland` tag (low detail) and a `SymTagCompilandDetails` tag (high detail). `SymTagCompilandDetails` requires loading additional symbols. However, it provides a wealth of information about the compiland that is not available with a `SymTagCompiland` symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_backEndBuild](../debug-interface-access/idiasymbol--get_backendbuild.md)|`DWORD`|Back-end build number of the compiler.|  
|[IDiaSymbol::get_backEndMajor](../debug-interface-access/idiasymbol--get_backendmajor.md)|`DWORD`|Back-end major version number of the compiler.|  
|[IDiaSymbol::get_backEndMinor](../debug-interface-access/idiasymbol--get_backendminor.md)|`DWORD`|Back-end minor version number of the compiler.|  
|[IDiaSymbol::get_compilerName](../debug-interface-access/idiasymbol--get_compilername.md)|`BSTR`|Name of the compiler that produced this compiland (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_editAndContinueEnabled](../debug-interface-access/idiasymbol--get_editandcontinueenabled.md)|`BOOL`|`TRUE` if Edit and Continue were enabled at compilation.|  
|[IDiaSymbol::get_frontEndBuild](../debug-interface-access/idiasymbol--get_frontendbuild.md)|`DWORD`|Front-end build number of the compiler.|  
|[IDiaSymbol::get_frontEndMajor](../debug-interface-access/idiasymbol--get_frontendmajor.md)|`DWORD`|Front-end major version number of the compiler.|  
|[IDiaSymbol::get_frontEndMinor](../debug-interface-access/idiasymbol--get_frontendminor.md)|`DWORD`|Front-end minor version number of the compiler.|  
|[IDiaSymbol::get_hasDebugInfo](../debug-interface-access/idiasymbol--get_hasdebuginfo.md)|`BOOL`|`TRUE` if this compiland has debug information (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasManagedCode](../debug-interface-access/idiasymbol--get_hasmanagedcode.md)|`BOOL`|`TRUE` if this compiland contains managed code (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_hasSecurityChecks](../debug-interface-access/idiasymbol--get_hassecuritychecks.md)|`BOOL`|`TRUE` if the compiland was compiled with the [/GS (Buffer Security Check)](../Topic/-GS%20\(Buffer%20Security%20Check\).md) compiler switch (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_isCVTCIL](../debug-interface-access/idiasymbol--get_iscvtcil.md)|`BOOL`|`TRUE` if compiland was converted from Common Intermediate Language (CIL) code to native code.|  
|[IDiaSymbol::get_isDataAligned](../debug-interface-access/idiasymbol--get_isdataaligned.md)|`BOOL`|`TRUE` if user-defined types (UDT) have been aligned to some specified memory boundary (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_isHotpatchable](../debug-interface-access/idiasymbol--get_ishotpatchable.md)|`BOOL`|`TRUE` if compiland was compiled with the [/hotpatch (Create Hotpatchable Image)](../Topic/-hotpatch%20\(Create%20Hotpatchable%20Image\).md) compiler switch (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_isLTCG](../debug-interface-access/idiasymbol--get_isltcg.md)|`BOOL`|`TRUE` if compiland was compiled with the [/LTCG (Link-time Code Generation)](../Topic/-LTCG%20\(Link-time%20Code%20Generation\).md) compiler switch (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_isMSILNetmodule](../debug-interface-access/idiasymbol--get_ismsilnetmodule.md)|`BOOL`|TRUE if compiland is a Microsoft Intermediate Language (MSIL) module (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_language](../debug-interface-access/idiasymbol--get_language.md)|`DWORD`|Source code language.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the compiland.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_platform](../debug-interface-access/idiasymbol--get_platform.md)|`DWORD`|Platform on which the compiland was compiled (one of the [CV_CPU_TYPE_e Enumeration](../debug-interface-access/cv_cpu_type_e.md) values).|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagCompilandDetails` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
  
## Remarks  
 Compilers often come in a form known as a two-pass compiler; in some compiler versions, each pass is handled by a separate program. These are known as front-end and back-end compilers, respectively, hence the symbol properties for back-end and front-end version numbers.  
  
## See Also  
 [Compiland](../debug-interface-access/compiland.md)   
 [Lexical Hierarchy of Symbol Types](../debug-interface-access/lexical-hierarchy-of-symbol-types.md)