---
title: "IDiaSession::findLinesByAddr | testtitle"
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
  - "IDiaSession::findLinesByAddr method"
ms.assetid: 640403c0-14cf-403c-ad19-38b3bdc28ca8
caps.latest.revision: 8
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
# IDiaSession::findLinesByAddr
Retrieves the lines in a specified compiland that contain a specified address.  
  
## Syntax  
  
```cpp#  
HRESULT findLinesByAddr (   
   DWORD                 seg,  
   DWORD                 offset,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `seg`  
 [in] Specifies the section component of the specific address.  
  
 `offset`  
 [in] Specifies the offset component of the specific address.  
  
 `length`  
 [in] Specifies the number of bytes of address range to cover with this query.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumLineNumbers](../debug-interface-access/idiaenumlinenumbers.md) object that contains a list of all the line numbers that cover the specified address range.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Example  
 This example shows a function that obtains all line numbers contained in a function using the function's address and length.  
  
```cpp#  
IDiaEnumLineNumbers* GetLineNumbersByAddr(IDiaSymbol *pFunc,  
                                          IDiaSession *pSession)  
{  
    IDiaEnumLineNumbers* pEnum = NULL;  
    DWORD                seg;  
    DWORD                offset;  
    ULONGLONG            length;  
  
    if (pFunc->get_addressSection ( &seg ) == S_OK &&  
        pFunc->get_addressOffset ( &offset ) == S_OK)  
    {  
        pFunc->get_length ( &length );  
        pSession->findLinesByAddr( seg, offset, static_cast<DWORD>( length ), &pEnum );  
    }  
    return(pEnum);  
}  
```  
  
## See Also  
 [IDiaEnumLineNumbers](../debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [IDiaSession::findLinesByVA](../debug-interface-access/idiasession--findlinesbyva.md)