---
title: "IDiaEnumSourceFiles | hehe"
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
  - "IDiaEnumSourceFiles interface"
ms.assetid: 5c0779a6-a2ea-408a-90da-ebdecf2b83c0
caps.latest.revision: 12
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
# IDiaEnumSourceFiles
Enumerates the various source files contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumSourceFiles : IUknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumSourceFiles`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumSourceFiles::get__NewEnum](../debug-interface-access/idiaenumsourcefiles--get__newenum.md)|Retrieves the `IEnumVARIANT Interface` version of this enumerator.|  
|[IDiaEnumSourceFiles::get_Count](../debug-interface-access/idiaenumsourcefiles--get_count.md)|Retrieves the number of source files.|  
|[IDiaEnumSourceFiles::Item](../debug-interface-access/idiaenumsourcefiles--item.md)|Retrieves a source file by means of an index.|  
|[IDiaEnumSourceFiles::Next](../debug-interface-access/idiaenumsourcefiles--next.md)|Retrieves a specified number of source files in the enumeration sequence.|  
|[IDiaEnumSourceFiles::Skip](../debug-interface-access/idiaenumsourcefiles--skip.md)|Skips a specified number of source files in an enumeration sequence.|  
|[IDiaEnumSourceFiles::Reset](../debug-interface-access/idiaenumsourcefiles--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumSourceFiles::Clone](../debug-interface-access/idiaenumsourcefiles--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling the `QueryInterface` method on an [IDiaTable](../debug-interface-access/idiatable.md) object. See the example for details.  
  
## Example  
 This example shows how to obtain the `IDiaEnumSourceFiles` interface from the list of tables in a DIA session object. For an example of accessing source file information, see the [IDiaSourceFile](../debug-interface-access/idiasourcefile.md) interface.  
  
```cpp#  
  
IDiaEnumSourceFiles* GetEnumSourceFiless(IDiaSession *pSession)  
{  
    IDiaEnumSourceFiles * pUnknown    = NULL;  
    REFIID                iid         = __uuidof(IDiaEnumSourceFiles);  
    IDiaEnumTables*       pEnumTables = NULL;  
    IDiaTable*            pTable      = NULL;  
    ULONG                 celt        = 0;  
  
    if (pSession->getEnumTables(&pEnumTables) != S_OK)  
    {  
        wprintf(L"ERROR - GetTable() getEnumTables\n");  
        return NULL;  
    }  
    while (pEnumTables->Next(1, &pTable, &celt) == S_OK && celt == 1)  
    {  
        // There is only one table that matches the given iid  
        HRESULT hr = pTable->QueryInterface(iid, (void**)&pUnknown);  
        pTable->Release();  
        if (hr == S_OK)  
        {  
            break;  
        }  
    }  
    pEnumTables->Release();  
    return pUnknown;  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession::findFile](../debug-interface-access/idiasession--findfile.md)   
 [IDiaSession::findLinesByLinenum](../debug-interface-access/idiasession--findlinesbylinenum.md)   
 [IDiaTable](../debug-interface-access/idiatable.md)