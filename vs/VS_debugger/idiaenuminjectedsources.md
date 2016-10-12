---
title: "IDiaEnumInjectedSources"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "IDiaEnumInjectedSources interface"
ms.assetid: f97e2392-22e1-48da-b7ce-ad94c8b684b0
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
# IDiaEnumInjectedSources
Enumerate the various injected sources contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumInjectedSources : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumInjectedSources`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumInjectedSources::get__NewEnum](../VS_debugger/idiaenuminjectedsources--get__newenum.md)|Retrieves the [IEnumVARIANT Interface](assetId:///139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumInjectedSources::get_Count](../VS_debugger/idiaenuminjectedsources--get_count.md)|Retrieves the number of injected sources.|  
|[IDiaEnumInjectedSources::Item](../VS_debugger/idiaenuminjectedsources--item.md)|Retrieves an injected source by means of an index.|  
|[IDiaEnumInjectedSources::Next](../VS_debugger/idiaenuminjectedsources--next.md)|Retrieves a specified number of injected sources in the enumeration sequence.|  
|[IDiaEnumInjectedSources::Skip](../VS_debugger/idiaenuminjectedsources--skip.md)|Skips a specified number of injected sources in an enumeration sequence.|  
|[IDiaEnumInjectedSources::Reset](../VS_debugger/idiaenuminjectedsources--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumInjectedSources::Clone](../VS_debugger/idiaenuminjectedsources--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 This interface is obtained by calling the [IDiaSession::findInjectedSource](../VS_debugger/idiasession--findinjectedsource.md) method with the name of a specific source file or by calling the [IDiaSession::getEnumTables](../VS_debugger/idiasession--getenumtables.md) method with the GUID of the `IDiaEnumInjectedSources` interface.  
  
## Example  
 This example shows how to obtain (the `GetEnumInjectedSources` function) and use (the `DumpAllInjectedSources` function) the `IDiaEnumInjectedSources` interface. See the [IDiaPropertyStorage](../VS_debugger/idiapropertystorage.md) interface for an implementation of the `PrintPropertyStorage` function. For an alternative output, see the [IDiaInjectedSource](../VS_debugger/idiainjectedsource.md) interface.  
  
```cpp#  
  
IDiaEnumInjectedSources* GetEnumInjectedSources(IDiaSession *pSession)  
{  
    IDiaEnumInjectedSources* pUnknown    = NULL;  
    REFIID                   iid         = __uuidof(IDiaEnumInjectedSources);  
    IDiaEnumTables*          pEnumTables = NULL;  
    IDiaTable*               pTable      = NULL;  
    ULONG                    celt        = 0;  
  
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
  
void DumpAllInjectedSources( IDiaSession* pSession)  
{  
    IDiaEnumInjectedSources* pEnumInjSources;  
  
    pEnumInjSources = GetEnumInjectedSources(pSession);  
    if (pEnumInjSources != NULL)  
    {  
        IDiaInjectedSource* pInjSource;  
        ULONG celt = 0;  
  
        while(pEnumInjSources->Next(1, &pInjSource, &celt) == S_OK &&  
              celt == 1)  
        {  
            IDiaPropertyStorage *pPropertyStorage;  
            if (pInjSource->QueryInterface(__uuidof(IDiaPropertyStorage),  
                                           (void **)&pPropertyStorage) == S_OK)  
            {  
                PrintPropertyStorage(pPropertyStorage);  
                pPropertyStorage->Release();  
            }  
            pInjSource->Release();  
        }  
        pEnumInjSources->Release();  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../VS_debugger/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession::findInjectedSource](../VS_debugger/idiasession--findinjectedsource.md)   
 [IDiaSession::getEnumTables](../VS_debugger/idiasession--getenumtables.md)   
 [IDiaPropertyStorage](../VS_debugger/idiapropertystorage.md)   
 [IDiaInjectedSource](../VS_debugger/idiainjectedsource.md)