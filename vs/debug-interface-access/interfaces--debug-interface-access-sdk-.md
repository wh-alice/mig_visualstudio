---
title: "Interfaces (Debug Interface Access SDK) | testtitle"
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
  - "interfaces [DIA SDK]"
  - "DIA SDK, interfaces"
ms.assetid: 62aee7c3-d314-4272-a32b-b2818f32fab8
caps.latest.revision: 16
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
# Interfaces (Debug Interface Access SDK)
Methods are listed alphabetically under each interface in the table of contents and on the interface page in Vtable order.  
  
## In This Section  
 [IDiaAddressMap](../debug-interface-access/idiaaddressmap.md)  
 Provides control over how the DIA SDK computes virtual and relative virtual addresses for debug objects.  
  
 [IDiaDataSource](../debug-interface-access/idiadatasource.md)  
 Initiates access to a source of debugging symbols.  
  
 [IDiaEnumDebugStreamData](../debug-interface-access/idiaenumdebugstreamdata.md)  
 Provides access to the records in a debug data stream.  
  
 [IDiaEnumDebugStreams](../debug-interface-access/idiaenumdebugstreams.md)  
 Enumerates the various debug streams contained in the data source.  
  
 [IDiaEnumFrameData](../debug-interface-access/idiaenumframedata.md)  
 Enumerates the various frame data elements contained in the data source.  
  
 [IDiaEnumInjectedSources](../debug-interface-access/idiaenuminjectedsources.md)  
 Enumerate the various injected sources contained in the data source.  
  
 [IDiaEnumLineNumbers](../debug-interface-access/idiaenumlinenumbers.md)  
 Enumerates the various line numbers contained in the data source.  
  
 [IDiaEnumSectionContribs](../debug-interface-access/idiaenumsectioncontribs.md)  
 Enumerates the various section contributions contained in the data source.  
  
 [IDiaEnumSegments](../debug-interface-access/idiaenumsegments.md)  
 Enumerates the various segments contained in the data source.  
  
 [IDiaEnumSourceFiles](../debug-interface-access/idiaenumsourcefiles.md)  
 Enumerates the various source files contained in the data source.  
  
 [IDiaEnumStackFrames](../debug-interface-access/idiaenumstackframes.md)  
 Enumerates the various stack frames available.  
  
 [IDiaEnumSymbols](../debug-interface-access/idiaenumsymbols.md)  
 Enumerates the various symbols contained in the data source.  
  
 [IDiaEnumSymbolsByAddr](../debug-interface-access/idiaenumsymbolsbyaddr.md)  
 Enumerates by address the various symbols contained in the data source.  
  
 [IDiaEnumTables](../debug-interface-access/idiaenumtables.md)  
 Enumerates the various tables contained in the data source.  
  
 [IDiaFrameData](../debug-interface-access/idiaframedata.md)  
 Exposes the details of a stack frame.  
  
 [IDiaImageData](../debug-interface-access/idiaimagedata.md)  
 Exposes the details of the base location and memory offsets of the module or image.  
  
 [IDiaInjectedSource](../debug-interface-access/idiainjectedsource.md)  
 Accesses the program source code stored in the DIA data source.  
  
 [IDiaLineNumber](../debug-interface-access/idialinenumber.md)  
 Accesses information that describes the process of mapping from a block of bytes of image text to a source file line number.  
  
 [IDiaLoadCallback](../debug-interface-access/idialoadcallback.md)  
 Receives callbacks from the DIA symbol locating procedure, thus enabling a user interface to report on the progress of the location attempt.  
  
 [IDiaLoadCallback2](../debug-interface-access/idialoadcallback2.md)  
 Receives callbacks from the DIA symbol locating procedure, allowing restrictions to be imposed on the locating process.  
  
 [IDiaPropertyStorage](../debug-interface-access/idiapropertystorage.md)  
 Allows you to read the persistent properties of a DIA property set.  
  
 [IDiaReadExeAtRVACallback](../debug-interface-access/idiareadexeatrvacallback.md)  
 Enables a client application to supply bytes of an executable file as specified by file position.  
  
 [IDiaReadExeAtOffsetCallback](../debug-interface-access/idiareadexeatoffsetcallback.md)  
 Enables a client application to supply bytes of an executable file as specified by a relative virtual address.  
  
 [IDiaSectionContrib](../debug-interface-access/idiasectioncontrib.md)  
 Retrieves data describing a section contribution, that is, a contiguous block of memory contributed to the image by a compiland.  
  
 [IDiaSegment](../debug-interface-access/idiasegment.md)  
 Maps data from the section number to segments of address space.  
  
 [IDiaSession](../debug-interface-access/idiasession.md)  
 Provides a query context for debug symbols.  
  
 [IDiaSourceFile](../debug-interface-access/idiasourcefile.md)  
 Represents a source file.  
  
 [IDiaStackFrame](../debug-interface-access/idiastackframe.md)  
 Exposes the properties of a stack frame.  
  
 [IDiaStackWalker](../debug-interface-access/idiastackwalker.md)  
 Provides methods to do a stack walk using the PDB file.  
  
 [IDiaStackWalkFrame](../debug-interface-access/idiastackwalkframe.md)  
 Maintains stack context between invocations of the [IDiaFrameData::execute](../debug-interface-access/idiaframedata--execute.md) method.  
  
 [IDiaStackWalkHelper](../debug-interface-access/idiastackwalkhelper.md)  
 Facilitates walking the stack using the program debug database (PDB) file.  
  
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)  
 Describes the properties of a symbol instance.  
  
 [IDiaTable](../debug-interface-access/idiatable.md)  
 Enumerates a DIA data source table.  
  
## Related Sections  
 [Enumerations and Structures](../debug-interface-access/enumerations-and-structures.md)  
 Describes the enumerations and structures used by the various interfaces of the DIA SDK.  
  
 [Constants (Debug Interface Access SDK)](../debug-interface-access/constants--debug-interface-access-sdk-.md)  
 Describes the constants available in the DIA SDK.  
  
## See Also  
 [Reference](../debug-interface-access/debug-interface-access-sdk-reference.md)