---
title: "IDiaEnumInjectedSources | hehe"
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
|[IDiaEnumInjectedSources::get__NewEnum](../debug-interface-access/idiaenuminjectedsources--get__newenum.md)|Retrieves the [IEnumVARIANT Interface](http://msdn.microsoft.com/en-us/139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumInjectedSources::get_Count](../debug-interface-access/idiaenuminjectedsources--get_count.md)|Retrieves the number of injected sources.|  
|[IDiaEnumInjectedSources::Item](../debug-interface-access/idiaenuminjectedsources--item.md)|Retrieves an injected source by means of an index.|  
|[IDiaEnumInjectedSources::Next](../debug-interface-access/idiaenuminjectedsources--next.md)|Retrieves a specified number of injected sources in the enumeration sequence.|  
|[IDiaEnumInjectedSources::Skip](../debug-interface-access/idiaenuminjectedsources--skip.md)|Skips a specified number of injected sources in an enumeration sequence.|  
|[IDiaEnumInjectedSources::Reset](../debug-interface-access/idiaenuminjectedsources--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumInjectedSources::Clone](../debug-interface-access/idiaenuminjectedsources--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 This interface is obtained by calling the [IDiaSession::findInjectedSource](../debug-interface-access/idiasession--findinjectedsource.md) method with the name of a specific source file or by calling the [IDiaSession::getEnumTables](../debug-interface-access/idiasession--getenumtables.md) method with the GUID of the `IDiaEnumInjectedSources` interface.  
  
## Example  
 This example shows how to obtain (the `GetEnumInjectedSources` function) and use (the `DumpAllInjectedSources` function) the `IDiaEnumInjectedSources` interface. See the [IDiaPropertyStorage](../debug-interface-access/idiapropertystorage.md) interface for an implementation of the `PrintPropertyStorage` function. For an alternative output, see the [IDiaInjectedSource](../debug-interface-access/idiainjectedsource.md) interface.  
  
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
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession::findInjectedSource](../debug-interface-access/idiasession--findinjectedsource.md)   
 [IDiaSession::getEnumTables](../debug-interface-access/idiasession--getenumtables.md)   
 [IDiaPropertyStorage](../debug-interface-access/idiapropertystorage.md)   
 [IDiaInjectedSource](../debug-interface-access/idiainjectedsource.md)