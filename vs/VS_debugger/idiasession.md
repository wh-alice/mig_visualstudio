---
title: "IDiaSession"
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
  - "IDiaSession interface"
ms.assetid: 69dab9bf-2c68-4f70-9678-3b50fba3e6fa
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
# IDiaSession
Provides a query context for debug symbols.  
  
## Syntax  
  
```  
IDiaSession : IUnknown  
```  
  
## Methods  
 The following table shows the methods of `IDiaSession`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaSession::get_loadAddress](../VS_debugger/idiasession--get_loadaddress.md)|Retrieves the load address for the executable file that corresponds to the symbols in this symbol store. This is the same value that was passed to the `put_loadAddress` method.|  
|[IDiaSession::put_loadAddress](../VS_debugger/idiasession--put_loadaddress.md)|Sets the load address for the executable file that corresponds to the symbols in this symbol store. **Note:**  It is important to call this method when you get an `IDiaSession` object and before you start using the object.|  
|[IDiaSession::get_globalScope](../VS_debugger/idiasession--get_globalscope.md)|Retrieves a reference to the global scope.|  
|[IDiaSession::getEnumTables](../VS_debugger/idiasession--getenumtables.md)|Retrieves an enumerator for all tables contained in the symbol store.|  
|[IDiaSession::getSymbolsByAddr](../VS_debugger/idiasession--getsymbolsbyaddr.md)|Retrieves an enumerator for all named symbols at static locations.|  
|[IDiaSession::findChildren](../VS_debugger/idiasession--findchildren.md)|Retrieves all children of a specified parent identifier that match the name and symbol type.|  
|[IDiaSession::findSymbolByAddr](../VS_debugger/idiasession--findsymbolbyaddr.md)|Retrieves a specified symbol type that contains, or is closest to, a specified address.|  
|[IDiaSession::findSymbolByRVA](../VS_debugger/idiasession--findsymbolbyrva.md)|Retrieves a specified symbol type that contains, or is closest to, a specified relative virtual address (RVA).|  
|[IDiaSession::findSymbolByVA](../VS_debugger/idiasession--findsymbolbyva.md)|Retrieves a specified symbol type that contains, or is closest to, a specified virtual address (VA).|  
|[IDiaSession::findSymbolByToken](../VS_debugger/idiasession--findsymbolbytoken.md)|Retrieves the symbol that contains a specified metadata token.|  
|[IDiaSession::symsAreEquiv](../VS_debugger/idiasession--symsareequiv.md)|Checks to see if two symbols are equivalent.|  
|[IDiaSession::symbolById](../VS_debugger/idiasession--symbolbyid.md)|Retrieves a symbol by its unique identifier.|  
|[IDiaSession::findSymbolByRVAEx](../VS_debugger/idiasession--findsymbolbyrvaex.md)|Retrieves a specified symbol type that contains, or is closest to, a specified relative virtual address and offset.|  
|[IDiaSession::findSymbolByVAEx](../VS_debugger/idiasession--findsymbolbyvaex.md)|Retrieves a specified symbol type that contains, or is closest to, a specified virtual address and offset.|  
|[IDiaSession::findFile](../VS_debugger/idiasession--findfile.md)|Retrieves a source file by compiland and name.|  
|[IDiaSession::findFileById](../VS_debugger/idiasession--findfilebyid.md)|Retrieves a source file by source file identifier.|  
|[IDiaSession::findLines](../VS_debugger/idiasession--findlines.md)|Retrieves line numbers within a specified compiland and source file identifier.|  
|[IDiaSession::findLinesByAddr](../VS_debugger/idiasession--findlinesbyaddr.md)|Retrieves the lines in a specified compiland that contain a specified address.|  
|[IDiaSession::findLinesByRVA](../VS_debugger/idiasession--findlinesbyrva.md)|Retrieves the lines in a specified compiland that contain a specified relative virtual address.|  
|[IDiaSession::findLinesByVA](../VS_debugger/idiasession--findlinesbyva.md)|Finds the line number information for lines contained in a specified address range.|  
|[IDiaSession::findLinesByLinenum](../VS_debugger/idiasession--findlinesbylinenum.md)|Retrieves the lines in a specified compiland by source file and line number.|  
|[IDiaSession::findInjectedSource](../VS_debugger/idiasession--findinjectedsource.md)|Retrieves a source that has been placed into the symbol store by attribute providers or other components of the compilation process.|  
|[IDiaSession::getEnumDebugStreams](../VS_debugger/idiasession--getenumdebugstreams.md)|Retrieves an enumerated sequence of debug data streams.|  
|[IDiaSession::findInlineFramesByAddr](../VS_debugger/idiasession--findinlineframesbyaddr.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a given address.|  
|[IDiaSession::findInlineFramesByRVA](../VS_debugger/idiasession--findinlineframesbyrva.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified relative virtual address (RVA).|  
|[IDiaSession::findInlineFramesByVA](../VS_debugger/idiasession--findinlineframesbyva.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified virtual address (VA).|  
|[IDiaSession::findInlineeLines](../VS_debugger/idiasession--findinlineelines.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, by the specified parent symbol.|  
|[IDiaSession::findInlineeLinesByAddr](../VS_debugger/idiasession--findinlineelinesbyaddr.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, by the specified parent symbol and are contained within the specified address range.|  
|[IDiaSession::findInlineeLinesByRVA](../VS_debugger/idiasession--findinlineelinesbyrva.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, by the specified parent symbol and are contained within the specified relative virtual address (RVA).|  
|[IDiaSession::findInlineeLinesByVA](../VS_debugger/idiasession--findinlineelinesbyva.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, by the specified parent symbol and are contained within the specified virtual address (VA).|  
|[IDiaSession::findInlineeLinesByLinenum](../VS_debugger/idiasession--findinlineelinesbylinenum.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in the specified source file and line number.|  
|[IDiaSession::findInlineesByName](../VS_debugger/idiasession--findinlineesbyname.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all inlined functions that match a specified name.|  
|[IDiaSession::findSymbolsForAcceleratorPointerTag](../VS_debugger/idiasession--findsymbolsforacceleratorpointertag.md)|Returns an enumeration of symbols for the variable that the specified tag value corresponds to in the parent Accelerator stub function.|  
|[IDiaSession::findSymbolsByRVAForAcceleratorPointerTag](../VS_debugger/idiasession--findsymbolsbyrvaforacceleratorpointertag.md)|Given a corresponding tag value, this method returns an enumeration of symbols that are contained in a specified parent Accelerator stub function at a specified relative virtual address.|  
|[IDiaSession::findAcceleratorInlineesByName](../VS_debugger/idiasession--findacceleratorinlineesbyname.md)|Returns an enumeration of symbols for inline frames corresponding to the specified inline function name.|  
|[IDiaSession::findAcceleratorInlineesByLinenum](../VS_debugger/idiasession--findacceleratorinlineesbylinenum.md)|Returns an enumeration of symbols for inline frames that correspond to the specified source location.|  
  
## Remarks  
 It is important to call the [IDiaSession::put_loadAddress](../VS_debugger/idiasession--put_loadaddress.md) method after creating the `IDiaSession` object — and the value passed to the `put_loadAddress` method must be non-zero — for any virtual address (VA) properties of symbols to be accessible. The load address comes from whatever program loaded the executable being debugged. For example, you can call the Win32 function `GetModuleInformation` to retrieve the load address for the executable, given a handle to the executable.  
  
## Example  
 This example shows how to obtain the `IDiaSession` interface as part of a general initialization of the DIA SDK.  
  
```cpp#  
CComPtr<IDiaDataSource> pSource;  
ComPtr<IDiaSession> psession;  
  
void InitializeDIA(const char *szFilename)  
{  
    HRESULT hr = CoCreateInstance( CLSID_DiaSource,  
                                   NULL,  
                                   CLSCTX_INPROC_SERVER,  
                                   __uuidof( IDiaDataSource ),  
                                  (void **) &pSource);  
    if (FAILED(hr))  
    {  
        Fatal("Could not CoCreate CLSID_DiaSource. Register msdia80.dll." );  
    }  
    wchar_t wszFilename[ _MAX_PATH ];  
    mbstowcs( wszFilename,  
              szFilename,  
              sizeof( wszFilename )/sizeof( wszFilename[0] ) );  
    if ( FAILED( pSource->loadDataFromPdb( wszFilename ) ) )  
    {  
        if ( FAILED( pSource->loadDataForExe( wszFilename, NULL, NULL ) ) )  
        {  
            Fatal( "loadDataFromPdb/Exe" );  
        }  
    }  
    if ( FAILED( pSource->openSession( &psession ) ) )  
    {  
        Fatal( "openSession" );  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../VS_debugger/interfaces--debug-interface-access-sdk-.md)   
 [Overview](../VS_debugger/overview--debug-interface-access-sdk-.md)   
 [Exe](../VS_debugger/exe.md)   
 [IDiaAddressMap](../VS_debugger/idiaaddressmap.md)   
 [IDiaDataSource](../VS_debugger/idiadatasource.md)   
 [IDiaDataSource::openSession](../VS_debugger/idiadatasource--opensession.md)   
 [IDiaSymbol::findChildren](../VS_debugger/idiasymbol--findchildren.md)   
 [Querying the .Pdb File](../VS_debugger/querying-the-.pdb-file.md)