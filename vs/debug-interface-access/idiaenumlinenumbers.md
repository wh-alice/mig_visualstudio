---
title: "IDiaEnumLineNumbers"
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
  - "IDiaEnumLineNumbers interface"
ms.assetid: cdf07b4f-19e4-4dcd-8af8-c2dbca586a7c
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
# IDiaEnumLineNumbers
Enumerates the various line numbers contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumLineNumbers : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumLineNumbers`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumLineNumbers::get__NewEnum](../debug-interface-access/idiaenumlinenumbers--get__newenum.md)|Retrieves the [IEnumVARIANT Interface](http://msdn.microsoft.com/en-us/139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumLineNumbers::get_Count](../debug-interface-access/idiaenumlinenumbers--get_count.md)|Retrieves the number of line numbers.|  
|[IDiaEnumLineNumbers::Item](../debug-interface-access/idiaenumlinenumbers--item.md)|Retrieves a line number by means of an index.|  
|[IDiaEnumLineNumbers::Next](../debug-interface-access/idiaenumlinenumbers--next.md)|Retrieves a specified number of line numbers in the enumeration sequence.|  
|[IDiaEnumLineNumbers::Skip](../debug-interface-access/idiaenumlinenumbers--skip.md)|Skips a specified number of line numbers in an enumeration sequence.|  
|[IDiaEnumLineNumbers::Reset](../debug-interface-access/idiaenumlinenumbers--reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumLineNumbers::Clone](../debug-interface-access/idiaenumlinenumbers--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 This interface is obtained by calling one of the following methods in the [IDiaSession](../debug-interface-access/idiasession.md) interface:  
  
-   [IDiaSession::findLines](../debug-interface-access/idiasession--findlines.md)  
  
-   [IDiaSession::findLinesByAddr](../debug-interface-access/idiasession--findlinesbyaddr.md)  
  
-   [IDiaSession::findLinesByRVA](../debug-interface-access/idiasession--findlinesbyrva.md)  
  
-   [IDiaSession::findLinesByVA](../debug-interface-access/idiasession--findlinesbyva.md)  
  
-   [IDiaSession::findLinesByLinenum](../debug-interface-access/idiasession--findlinesbylinenum.md)  
  
## Example  
 This example shows how to obtain the `IDiaEnumLineNumbers` interface from a session. In this case, the example shows how to get the line number enumeration for a function (represented by `pSymbol`). For a more complete example of using line numbers, see the [IDiaLineNumber](../debug-interface-access/idialinenumber.md) interface.  
  
```cpp#  
void dumpFunctionLines( IDiaSymbol* pSymbol, IDiaSession* pSession )  
{  
    ULONGLONG length = 0;  
    DWORD isect = 0;  
    DWORD offset = 0;  
    pSymbol->get_addressSection( &isect );  
    pSymbol->get_addressOffset( &offset );  
    pSymbol->get_length( &length );  
    if ( isect != 0 && length > 0 )  
    {  
        CComPtr< IDiaEnumLineNumbers > pLines;  
        if ( SUCCEEDED( pSession->findLinesByAddr(  
                                      isect,  
                                      offset,  
                                      static_cast<DWORD>( length ),  
                                      &pLines )  
                      )  
           )  
        {  
            // Do something with the enumeration  
        }  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [IDiaSession::findLinesByLinenum](../debug-interface-access/idiasession--findlinesbylinenum.md)   
 [IDiaSession::findLinesByRVA](../debug-interface-access/idiasession--findlinesbyrva.md)   
 [IDiaSession::findLinesByVA](../debug-interface-access/idiasession--findlinesbyva.md)   
 [IDiaSession::findLines](../debug-interface-access/idiasession--findlines.md)   
 [IDiaSession::findLinesByAddr](../debug-interface-access/idiasession--findlinesbyaddr.md)