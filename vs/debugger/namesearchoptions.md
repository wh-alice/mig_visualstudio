---
title: "NameSearchOptions"
ms.custom: ""
ms.date: "10/14/2016"
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
  - "NameSearchOptions enumeration"
ms.assetid: 67dfbede-2678-47df-b664-5c49841d0b9b
caps.latest.revision: 15
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
# NameSearchOptions
Specifies the search options for symbol and file names.  
  
## Syntax  
  
```cpp#  
enum NameSearchOptions {   
   nsNone,  
   nsfCaseSensitive     = 0x1,  
   nsfCaseInsensitive   = 0x2,  
   nsfFNameExt          = 0x4,  
   nsfRegularExpression = 0x8,  
   nsfUndecoratedName   = 0x10,  
  
// For backward compatibility:  
   nsCaseSensitive           = nsfCaseSensitive,  
   nsCaseInsensitive         = nsfCaseInsensitive,  
   nsFNameExt                = nsfCaseInsensitive | nsfFNameExt,  
   nsRegularExpression       = nsfRegularExpression | nsfCaseSensitive,  
   nsCaseInRegularExpression = nsfRegularExpression | nsfCaseInsensitive  
};  
```  
  
## Elements  
 `nsNone`  
 No options are specified.  
  
 `nsfCaseSensitive`  
 Applies a case-sensitive name match.  
  
 `nsfCaseInsensitive`  
 Applies a case-insensitive name match.  
  
 `nsfFNameExt`  
 Treats names as paths and applies a filename.ext name match.  
  
 `nsfRegularExpression`  
 Applies a case-sensitive name match using asterisks (*) and question marks (?) as wildcards.  
  
 `nsfUndecoratedName`  
 Applies only to symbols that have both undecorated and decorated names.  
  
## Remarks  
 The values from this enumeration are passed to the following methods:  
  
-   [IDiaSession::findChildren](../debugger/idiasession--findchildren.md)  
  
-   [IDiaSession::findFile](../debugger/idiasession--findfile.md)  
  
-   [IDiaSymbol::findChildren](../debugger/idiasymbol--findchildren.md)  
  
## Requirements  
 Header: dia2.h  
  
## See Also  
 [Enumerations and Structures](../debugger/enumerations-and-structures.md)   
 [IDiaSession::findChildren](../debugger/idiasession--findchildren.md)   
 [IDiaSession::findFile](../debugger/idiasession--findfile.md)   
 [IDiaSymbol::findChildren](../debugger/idiasymbol--findchildren.md)