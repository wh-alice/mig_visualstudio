---
title: "IDiaEnumSectionContribs | hehe"
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
  - "IDiaEnumSectionContribs interface"
ms.assetid: 0d6c0632-310f-4a99-8921-58149a1817e3
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
# IDiaEnumSectionContribs
Enumerates the various section contributions contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumSectionContribs : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumSectionContribs`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumSectionContribs::get__NewEnum](../debug-interface-access/idiaenumsectioncontribs--get__newenum.md)|Retrieves the [IEnumVARIANT Interface](http://msdn.microsoft.com/en-us/139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumSectionContribs::get_Count](../debug-interface-access/idiaenumsectioncontribs--get_count.md)|Retrieves the number of section contributions.|  
|[IDiaEnumSectionContribs::Item](../debug-interface-access/idiaenumsectioncontribs--item.md)|Retrieves section contributions by means of an index.|  
|[IDiaEnumSectionContribs::Next](../debug-interface-access/idiaenumsectioncontribs--next.md)|Retrieves a specified number of section contributions in the enumeration sequence.|  
|[IDiaEnumSectionContribs::Skip](../debug-interface-access/idiaenumsectioncontribs--skip.md)|Skips a specified number of section contributions in an enumeration sequence.|  
|[IDiaEnumSectionContribs::Reset](../debug-interface-access/idiaenumsectioncontribs--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumSectionContribs::Clone](../debug-interface-access/idiaenumsectioncontribs--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Note for Callers  
 Obtain this interface from the [IDiaSession::getEnumTables](../debug-interface-access/idiasession--getenumtables.md) method. See the example for details.  
  
## Example  
 This example shows how to obtain (the `GetEnumSectionContribs` function) and use (the `ShowSectionContribs` function) the `IDiaEnumSectionContribs` interface. For a more complete example of using section contributions, see the [IDiaSectionContrib](../debug-interface-access/idiasectioncontrib.md) interface.  
  
```cpp#  
  
      IDiaEnumSectionContribs* GetEnumSectionContribs(IDiaSession *pSession)  
{  
    IDiaEnumSectionContribs* pUnknown    = NULL;  
    REFIID                   iid         = __uuidof(IDiaEnumSectionContribs);  
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
  
void ShowSectionContribs(IDiaSession *pSession)  
{  
    IDiaEnumSectionContribs* pEnumSectionContribs;  
  
    pEnumSectionContribs = GetEnumSectionContribs(pSession);  
    if (pSectionContrib != NULL)  
    {  
        IDiaSectionContrib* pSectionContrib;  
        ULONG celt = 0;  
  
        while(pEnumSectionContribs->Next(1, &pSectionContrib, &celt) == S_OK &&  
              celt == 1)  
        {  
            PrintSectionContrib(pSectionContrib, pSession);  
            pSectionContrib->Release();  
        }  
        pSectionContrib->Release();   
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession::getEnumTables](../debug-interface-access/idiasession--getenumtables.md)   
 [IDiaSectionContrib](../debug-interface-access/idiasectioncontrib.md)