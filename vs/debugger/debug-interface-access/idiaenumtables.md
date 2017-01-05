---
title: "IDiaEnumTables"
ms.custom: ""
ms.date: "12/07/2016"
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
  - "IDiaEnumTables interface"
ms.assetid: 016190c5-09e4-48f2-bf60-9b02603a03e0
caps.latest.revision: 10
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
# IDiaEnumTables
[!INCLUDE[vs2017banner](../../code-quality/includes/vs2017banner.md)]

Enumerates the various tables contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumTables : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumTables`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumTables::get__NewEnum](../../debugger/debug-interface-access/idiaenumtables--get__newenum.md)|Retrieves the [IEnumVARIANT Interface](http://msdn.microsoft.com/en-us/139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumTables::get_Count](../../debugger/debug-interface-access/idiaenumtables--get_count.md)|Retrieves the number of tables.|  
|[IDiaEnumTables::Item](../../debugger/debug-interface-access/idiaenumtables--item.md)|Retrieves a table by means of an index or a name.|  
|[IDiaEnumTables::Next](../../debugger/debug-interface-access/idiaenumtables--next.md)|Retrieves a specified number of tables in the enumeration sequence.|  
|[IDiaEnumTables::Skip](../../debugger/debug-interface-access/idiaenumtables--skip.md)|Skips a specified number of tables in an enumeration sequence.|  
|[IDiaEnumTables::Reset](../../debugger/debug-interface-access/idiaenumtables--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumTables::Clone](../../debugger/debug-interface-access/idiaenumtables--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling the [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession--getenumtables.md) method.  
  
## Example  
 This example shows how to obtain the `IDiaEnumTables` interface from a session. For a more complete example of using tables, see the [IDiaTable](../../debugger/debug-interface-access/idiatable.md) interface.  
  
```cpp#  
void ShowTableNames(IDiaSession *pSession)  
{  
    CComPtr<IDiaEnumTables> pTables;  
    if ( FAILED( psession->getEnumTables( &pTables ) ) )  
    {  
        Fatal( "getEnumTables" );  
    }  
    // Do something with table  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../../debugger/debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession--getenumtables.md)