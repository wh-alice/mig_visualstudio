---
title: "IDiaEnumFrameData | Microsoft Docs"
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
  - "IDiaEnumFrameData interface"
ms.assetid: 2ca7fd5a-b2fa-4b3a-9492-0263eafc435b
caps.latest.revision: 13
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
# IDiaEnumFrameData
Enumerates the various frame data elements contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumFrameData : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumFrameData`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumFrameData::get__NewEnum](../debug-interface-access/idiaenumframedata--get__newenum.md)|Retrieves the `IEnumVARIANT Interface` version of this enumerator.|  
|[IDiaEnumFrameData::get_Count](../debug-interface-access/idiaenumframedata--get_count.md)|Retrieves the number of frame data elements.|  
|[IDiaEnumFrameData::Item](../debug-interface-access/idiaenumframedata--item.md)|Retrieves a frame data element by means of an index.|  
|[IDiaEnumFrameData::Next](../debug-interface-access/idiaenumframedata--next.md)|Retrieves a specified number of frame data elements in the enumeration sequence.|  
|[IDiaEnumFrameData::Skip](../debug-interface-access/idiaenumframedata--skip.md)|Skips a specified number of frame data elements in an enumeration sequence.|  
|[IDiaEnumFrameData::Reset](../debug-interface-access/idiaenumframedata--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumFrameData::Clone](../debug-interface-access/idiaenumframedata--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[IDiaEnumFrameData::frameByRVA](../debug-interface-access/idiaenumframedata--framebyrva.md)|Returns a frame by relative virtual address (RVA).|  
|[IDiaEnumFrameData::frameByVA](../debug-interface-access/idiaenumframedata--framebyva.md)|Returns a frame by virtual address (VA).|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface from the [IDiaSession::getEnumTables](../debug-interface-access/idiasession--getenumtables.md) method. See the example for details.  
  
## Example  
 This example shows how to obtain (the `GetEnumFrameData` function) and use (the `ShowFrameData` function) the `IDiaEnumFrameData` interface. See the [IDiaFrameData](../debug-interface-access/idiaframedata.md) interface for an example of the `PrintFrameData` function.  
  
```cpp#  
  
      IDiaEnumFrameData* GetEnumFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pUnknown    = NULL;  
    REFIID             iid         = __uuidof(IDiaEnumFrameData);  
    IDiaEnumTables*    pEnumTables = NULL;  
    IDiaTable*         pTable      = NULL;  
    ULONG              celt        = 0;  
  
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
  
void ShowFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pEnumFrameData = GetEnumFrameData(pSession);;  
  
    if (pEnumFrameData != NULL)  
    {  
        IDiaFrameData* pFrameData;  
        ULONG celt = 0;  
  
        while(pEnumFrameData->Next(1, &pFrameData, &celt) == S_OK &&  
              celt == 1)  
        {  
            PrintFrameData(pFrameData);  
            pFrameData->Release();  
        }  
        pEnumFrameData->Release();   
    }  
}  
```  
  
## Requirements  
 **Header:** Dia2.h  
  
 **Library:** diaguids.lib  
  
 **DLL:** msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession::getEnumTables](../debug-interface-access/idiasession--getenumtables.md)   
 [IDiaFrameData](../debug-interface-access/idiaframedata.md)