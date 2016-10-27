---
title: "IDiaLineNumber"
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
  - "IDiaLineNumber interface"
ms.assetid: 1071f7d0-1f8c-4384-933f-c49c7eb930bd
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
# IDiaLineNumber
Accesses information that describes the process of mapping from a block of bytes of image text to a source file line number.  
  
## Syntax  
  
```  
IDiaLineNumber : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaLineNumber`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaLineNumber::get_compiland](../../debugger/debug-interface-access/idialinenumber--get_compiland.md)|Retrieves a reference to the symbol for the compiland that contributed the bytes of image text.|  
|[IDiaLineNumber::get_sourceFile](../../debugger/debug-interface-access/idialinenumber--get_sourcefile.md)|Retrieves a reference to the source file object.|  
|[IDiaLineNumber::get_lineNumber](../../debugger/debug-interface-access/idialinenumber--get_linenumber.md)|Retrieves the line number in the source file.|  
|[IDiaLineNumber::get_lineNumberEnd](../../debugger/debug-interface-access/idialinenumber--get_linenumberend.md)|Retrieves the one-based source line number where the statement or expression ends.|  
|[IDiaLineNumber::get_columnNumber](../../debugger/debug-interface-access/idialinenumber--get_columnnumber.md)|Retrieves the column number where the expression or statement begins.|  
|[IDiaLineNumber::get_columnNumberEnd](../../debugger/debug-interface-access/idialinenumber--get_columnnumberend.md)|Retrieves the column number where the expression or statement ends.|  
|[IDiaLineNumber::get_addressSection](../../debugger/debug-interface-access/idialinenumber--get_addresssection.md)|Retrieves the section part of the memory address where a block begins.|  
|[IDiaLineNumber::get_addressOffset](../../debugger/debug-interface-access/idialinenumber--get_addressoffset.md)|Retrieves the offset part of the memory address where a block begins.|  
|[IDiaLineNumber::get_relativeVirtualAddress](../../debugger/debug-interface-access/idialinenumber--get_relativevirtualaddress.md)|Retrieves the image relative virtual address (RVA) of a block.|  
|[IDiaLineNumber::get_virtualAddress](../../debugger/debug-interface-access/idialinenumber--get_virtualaddress.md)|Retrieves the virtual address (VA) of a block.|  
|[IDiaLineNumber::get_length](../../debugger/debug-interface-access/idialinenumber--get_length.md)|Retrieves the number of bytes in a block.|  
|[IDiaLineNumber::get_sourceFileId](../../debugger/debug-interface-access/idialinenumber--get_sourcefileid.md)|Retrieves a unique source file identifier for the source file that contributed this line.|  
|[IDiaLineNumber::get_statement](../../debugger/debug-interface-access/idialinenumber--get_statement.md)|Retrieves a flag indicating that this line information describes the beginning of a statement in the program source.|  
|[IDiaLineNumber::get_compilandId](../../debugger/debug-interface-access/idialinenumber--get_compilandid.md)|Retrieves the unique identifier for the compiland that contributed this line.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling the [IDiaEnumLineNumbers::Item](../../debugger/debug-interface-access/idiaenumlinenumbers--item.md) or [IDiaEnumLineNumbers::Next](../../debugger/debug-interface-access/idiaenumlinenumbers--next.md) methods.  
  
## Example  
 The following function displays line numbers used in a function (represented by `pSymbol`).  
  
```cpp#  
void dumpFunctionLines( IDiaSymbol* pSymbol, IDiaSession* pSession )  
{  
    ULONGLONG length = 0;  
    DWORD     isect  = 0;  
    DWORD     offset = 0;  
  
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
                                      &pLines)  
                      )  
           )  
        {  
            CComPtr< IDiaLineNumber > pLine;  
            DWORD celt      = 0;  
            bool  firstLine = true;  
  
            while ( SUCCEEDED( pLines->Next( 1, &pLine, &celt ) ) &&  
                    celt == 1 )  
            {  
                DWORD offset;  
                DWORD seg;  
                DWORD linenum;  
                CComPtr< IDiaSymbol >     pComp;  
                CComPtr< IDiaSourceFile > pSrc;  
  
                pLine->get_compiland( &pComp );  
                pLine->get_sourceFile( &pSrc );  
                pLine->get_addressSection( &seg );  
                pLine->get_addressOffset( &offset );  
                pLine->get_lineNumber( &linenum );  
                printf( "\tline %d at 0x%x:0x%x\n", linenum, seg, offset );  
                pLine = NULL;  
                if ( firstLine )  
                {  
                    // sanity check  
                    CComPtr< IDiaEnumLineNumbers > pLinesByLineNum;  
                    if ( SUCCEEDED( pSession->findLinesByLinenum(  
                                                  pComp,  
                                                  pSrc,  
                                                  linenum,  
                                                  0,  
                                                  &pLinesByLineNum)  
                                  )  
                       )  
                    {  
                        CComPtr< IDiaLineNumber > pLine;  
                        DWORD celt;  
                        while ( SUCCEEDED( pLinesByLineNum->Next( 1, &pLine, &celt ) ) &&  
                                celt == 1 )  
                        {  
                            DWORD offset;  
                            DWORD seg;  
                            DWORD linenum;  
  
                            pLine->get_addressSection( &seg );  
                            pLine->get_addressOffset( &offset );  
                            pLine->get_lineNumber( &linenum );  
                            printf( "\t\tfound line %d at 0x%x:0x%x\n", linenum, seg, offset );  
                            pLine = NULL;  
                       }  
                    }  
                    firstLine = false;  
                }  
            }  
        }  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../../debugger/debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaEnumLineNumbers::Item](../../debugger/debug-interface-access/idiaenumlinenumbers--item.md)   
 [IDiaEnumLineNumbers::Next](../../debugger/debug-interface-access/idiaenumlinenumbers--next.md)