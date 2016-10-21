---
title: "IDiaSymbol | hehe"
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
  - "IDiaSymbol interface"
ms.assetid: 01ad328a-736c-4933-a9f8-c2ded19ddd8c
caps.latest.revision: 30
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
# IDiaSymbol
Describes the properties of a symbol instance.  
  
## Syntax  
  
```  
IDiaSymbol : IUnknown  
```  
  
## Methods in Alphabetical Order  
 The following table shows the methods of `IDiaSymbol`.  
  
> [!NOTE]
>  Symbols will return meaningful data for only some of these methods, depending on the type of symbol. If a method returns `S_OK`, then that method has returned meaningful data.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaSymbol::findChildren](../debug-interface-access/idiasymbol--findchildren.md)|Retrieves all children of the symbol.|  
|[IDiaSymbol::findChildrenEx](../debug-interface-access/idiasymbol--findchildrenex.md)|Retrieves the children of the symbol. This method is the extended version of [IDiaSymbol::findChildren](../debug-interface-access/idiasymbol--findchildren.md).|  
|[IDiaSymbol::findChildrenExByAddr](../debug-interface-access/idiasymbol--findchildrenexbyaddr.md)|Retrieves the children of the symbol that are valid at a specified address.|  
|[IDiaSymbol::findChildrenExByRVA](../debug-interface-access/idiasymbol--findchildrenexbyrva.md)|Retrieves the children of the symbol that are valid at a specified relative virtual address (RVA).|  
|[IDiaSymbol::findChildrenExByVA](../debug-interface-access/idiasymbol--findchildrenexbyva.md)|Retrieves the children of the symbol that are valid at a specified virtual address.|  
|[IDiaSymbol::findInlineFramesByAddr](../debug-interface-access/idiasymbol--findinlineframesbyaddr.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a given address.|  
|[IDiaSymbol::findInlineFramesByRVA](../debug-interface-access/idiasymbol--findinlineframesbyrva.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified relative virtual address (RVA).|  
|[IDiaSymbol::findInlineFramesByVA](../debug-interface-access/idiasymbol--findinlineframesbyva.md)|Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified virtual address (VA).|  
|[IDiaSymbol::findInlineeLines](../debug-interface-access/idiasymbol--findinlineelines.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol.|  
|[IDiaSymbol::findInlineeLinesByAddr](../debug-interface-access/idiasymbol--findinlineelinesbyaddr.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified address range.|  
|[IDiaSymbol::findInlineeLinesByRVA](../debug-interface-access/idiasymbol--findinlineelinesbyrva.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified relative virtual address (RVA).|  
|[IDiaSymbol::findInlineeLinesByVA](../debug-interface-access/idiasymbol--findinlineelinesbyva.md)|Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified virtual address (VA).|  
|[IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag](../debug-interface-access/idiasymbol--findsymbolsbyrvaforacceleratorpointertag.md)|Given a corresponding tag value, this method returns an enumeration of symbols that are contained in this stub function at a specified relative virtual address.|  
|[IDiaSymbol::findSymbolsForAcceleratorPointerTag](../debug-interface-access/idiasymbol--findsymbolsforacceleratorpointertag.md)|Returns the number of accelerator pointer tags in a C++ AMP stub function.|  
|[IDiaSymbol::get_acceleratorPointerTags](../debug-interface-access/idiasymbol--get_acceleratorpointertags.md)|Returns all accelerator pointer tag values that correspond to a C++ AMP accelerator stub function.|  
|[IDiaSymbol::get_access](../debug-interface-access/idiasymbol--get_access.md)|Retrieves the access modifier of a class member.|  
|[IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)|Retrieves the offset part of an address location.|  
|[IDiaSymbol::get_addressSection](../debug-interface-access/idiasymbol--get_addresssection.md)|Retrieves the section part of an address location.|  
|[IDiaSymbol::get_addressTaken](../debug-interface-access/idiasymbol--get_addresstaken.md)|Retrieves a flag indicating whether another symbol references this address.|  
|[IDiaSymbol::get_age](../debug-interface-access/idiasymbol--get_age.md)|Retrieves the age value of a program database.|  
|[IDiaSymbol::get_arrayIndexType](../debug-interface-access/idiasymbol--get_arrayindextype.md)|Retrieves the symbol identifier of the array index type.|  
|[IDiaSymbol::get_arrayIndexTypeId](../debug-interface-access/idiasymbol--get_arrayindextypeid.md)|Retrieves the array index type identifier of the symbol.|  
|[IDiaSymbol::get_backEndMajor](../debug-interface-access/idiasymbol--get_backendmajor.md)|Retrieves the back-end major version number.|  
|[IDiaSymbol::get_backEndMinor](../debug-interface-access/idiasymbol--get_backendminor.md)|Retrieves the back-end minor version number.|  
|[IDiaSymbol::get_backEndBuild](../debug-interface-access/idiasymbol--get_backendbuild.md)|Retrieves the back-end build number.|  
|[IDiaSymbol::get_baseDataOffset](../debug-interface-access/idiasymbol--get_basedataoffset.md)|Retrieves the base data offset.|  
|[IDiaSymbol::get_baseDataSlot](../debug-interface-access/idiasymbol--get_basedataslot.md)|Retrieves the base data slot.|  
|[IDiaSymbol::get_baseSymbol](../debug-interface-access/idiasymbol--get_basesymbol.md)|Retrieves the symbol from which the pointer is based.|  
|[IDiaSymbol::get_baseSymbolId](../debug-interface-access/idiasymbol--get_basesymbolid.md)|Retrieves the symbol ID from which the pointer is based.|  
|[IDiaSymbol::get_baseType](../debug-interface-access/idiasymbol--get_basetype.md)|Retrieves the type tag of a simple type.|  
|[IDiaSymbol::get_bitPosition](../debug-interface-access/idiasymbol--get_bitposition.md)|Retrieves the bit position of a location.|  
|[IDiaSymbol::get_builtInKind](../debug-interface-access/idiasymbol--get_builtinkind.md)|Retrieves a built-in kind of the HLSL type.|  
|[IDiaSymbol::get_callingConvention](../debug-interface-access/idiasymbol--get_callingconvention.md)|Returns an indicator of a method's calling convention.|  
|[IDiaSymbol::get_classParent](../debug-interface-access/idiasymbol--get_classparent.md)|Retrieves a reference to the class parent of the symbol.|  
|[IDiaSymbol::get_classParentId](../debug-interface-access/idiasymbol--get_classparentid.md)|Retrieves the class parent identifier of the symbol.|  
|[IDiaSymbol::get_code](../debug-interface-access/idiasymbol--get_code.md)|Retrieves a flag indicating whether the symbol refers to a code address.|  
|[IDiaSymbol::get_compilerGenerated](../debug-interface-access/idiasymbol--get_compilergenerated.md)|Retrieves a flag indicating whether the symbol was compiler-generated.|  
|[IDiaSymbol::get_compilerName](../debug-interface-access/idiasymbol--get_compilername.md)|Retrieves the name of the compiler used to create the [Compiland](../debug-interface-access/compiland.md).|  
|[IDiaSymbol::get_constructor](../debug-interface-access/idiasymbol--get_constructor.md)|Retrieves a flag indicating whether the user-defined data type has a constructor.|  
|[IDiaSymbol::get_container](../debug-interface-access/idiasymbol--get_container.md)|Retrieves the containing symbol of this symbol.|  
|[IDiaSymbol::get_constType](../debug-interface-access/idiasymbol--get_consttype.md)|Retrieves a flag indicating whether the user-defined data type is constant.|  
|[IDiaSymbol::get_count](../debug-interface-access/idiasymbol--get_count.md)|Retrieves the number of items in a list or array.|  
|[IDiaSymbol::get_countLiveRanges](../debug-interface-access/idiasymbol--get_countliveranges.md)|Retrieves the number of valid address ranges associated with the local symbol.|  
|[IDiaSymbol::get_customCallingConvention](../debug-interface-access/idiasymbol--get_customcallingconvention.md)|Retrieves a flag indicating whether the function uses a custom calling convention.|  
|[IDiaSymbol::get_dataBytes](../debug-interface-access/idiasymbol--get_databytes.md)|Retrieves the data bytes of an OEM symbol.|  
|[IDiaSymbol::get_dataKind](../debug-interface-access/idiasymbol--get_datakind.md)|Retrieves the variable classification of a data symbol.|  
|[IDiaSymbol::get_editAndContinueEnabled](../debug-interface-access/idiasymbol--get_editandcontinueenabled.md)|Retrieves the flag describing the Edit and Continue features of the compiled program or unit.|  
|[IDiaSymbol::get_farReturn](../debug-interface-access/idiasymbol--get_farreturn.md)|Retrieves a flag indicating whether the function uses a far return.|  
|[IDiaSymbol::get_frontEndMajor](../debug-interface-access/idiasymbol--get_frontendmajor.md)|Retrieves the front-end major version number.|  
|[IDiaSymbol::get_frontEndMinor](../debug-interface-access/idiasymbol--get_frontendminor.md)|Retrieves the front-end minor version number.|  
|[IDiaSymbol::get_frontEndBuild](../debug-interface-access/idiasymbol--get_frontendbuild.md)|Retrieves the front-end build number.|  
|[IDiaSymbol::get_function](../debug-interface-access/idiasymbol--get_function.md)|Retrieves a flag indicating whether the public symbol refers to a function.|  
|[IDiaSymbol::get_guid](../debug-interface-access/idiasymbol--get_guid.md)|Retrieves the symbol's GUID.|  
|[IDiaSymbol::get_hasAlloca](../debug-interface-access/idiasymbol--get_hasalloca.md)|Retrieves a flag indicating whether the function contains a call to `alloca`.|  
|[IDiaSymbol::get_hasAssignmentOperator](../debug-interface-access/idiasymbol--get_hasassignmentoperator.md)|Retrieves a flag indicating whether the user-defined data type has any assignment operators defined.|  
|[IDiaSymbol::get_hasCastOperator](../debug-interface-access/idiasymbol--get_hascastoperator.md)|Retrieves a flag indicating whether the user-defined data type has any cast operators defined.|  
|[IDiaSymbol::get_hasDebugInfo](../debug-interface-access/idiasymbol--get_hasdebuginfo.md)|Retrieves a flag indicating whether the compiland contains any debugging information.|  
|[IDiaSymbol::get_hasEH](../debug-interface-access/idiasymbol--get_haseh.md)|Retrieves a flag indicating whether the function has a C++-style exception handler.|  
|[IDiaSymbol::get_hasEHa](../debug-interface-access/idiasymbol--get_haseha.md)|Retrieves a flag indicating whether the function has an asynchronous exception handler.|  
|[IDiaSymbol::get_hasInlAsm](../debug-interface-access/idiasymbol--get_hasinlasm.md)|Retrieves a flag indicating whether the function has inline assembly.|  
|[IDiaSymbol::get_hasLongJump](../debug-interface-access/idiasymbol--get_haslongjump.md)|Retrieves a flag indicating whether the function contains a longjmp command (part of C-style exception handling).|  
|[IDiaSymbol::get_hasManagedCode](../debug-interface-access/idiasymbol--get_hasmanagedcode.md)|Retrieves a flag indicating whether the module contains managed code.|  
|[IDiaSymbol::get_hasNestedTypes](../debug-interface-access/idiasymbol--get_hasnestedtypes.md)|Retrieves a flag indicating whether the user-defined data type has nested type definitions.|  
|[IDiaSymbol::get_hasSecurityChecks](../debug-interface-access/idiasymbol--get_hassecuritychecks.md)|Retrieves a flag indicating whether the function or compiland has security checks compiled in (via the [/GS (Buffer Security Check)](../Topic/-GS%20\(Buffer%20Security%20Check\).md) compiler switch).|  
|[IDiaSymbol::get_hasSEH](../debug-interface-access/idiasymbol--get_hasseh.md)|Retrieves a flag indicating whether the function has Win32-style Structured Exception Handling.|  
|[IDiaSymbol::get_hasSetJump](../debug-interface-access/idiasymbol--get_hassetjump.md)|Retrieves a flag indicating whether the function contains a setjmp command.|  
|[IDiaSymbol::get_indirectVirtualBaseClass](../debug-interface-access/idiasymbol--get_indirectvirtualbaseclass.md)|Retrieves a flag indicating whether the user-defined data type is an indirect virtual base class.|  
|[IDiaSymbol::get_InlSpec](../debug-interface-access/idiasymbol--get_inlspec.md)|Retrieves a flag indicating whether the function has been marked with the inline attribute.|  
|[IDiaSymbol::get_interruptReturn](../debug-interface-access/idiasymbol--get_interruptreturn.md)|Retrieves a flag indicating whether the function has a return from interrupt instruction.|  
|[IDiaSymbol::get_intro](../debug-interface-access/idiasymbol--get_intro.md)|Retrieves a flag indicating whether the function is the base class virtual function.|  
|[IDiaSymbol::get_isAcceleratorGroupSharedLocal](../debug-interface-access/idiasymbol--get_isacceleratorgroupsharedlocal.md)|Retrieves a flag that indicates whether the symbol corresponds to a group shared local variable in code compiled for a C++ AMP Accelerator.|  
|[IDiaSymbol::get_isAcceleratorPointerTagLiveRange](../debug-interface-access/idiasymbol--get_isacceleratorpointertagliverange.md)|Retrieves a flag that indicates whether the symbol corresponds to the *definition range symbol* for the tag component of a pointer variable in code compiled for a C++ AMP Accelerator. The definition range symbol is the location of a variable for a span of addresses.|  
|[IDiaSymbol::get_isAcceleratorStubFunction](../debug-interface-access/idiasymbol--get_isacceleratorstubfunction.md)|Indicates whether the symbol corresponds to a top-level function symbol for a shader compiled for an accelerator that corresponds to a `parallel_for_each` call.|  
|[IDiaSymbol::get_isAggregated](../debug-interface-access/idiasymbol--get_isaggregated.md)|Retrieves a flag indicating whether the data is part of an aggregate of many symbols.|  
|[IDiaSymbol::get_isCTypes](../debug-interface-access/idiasymbol--get_isctypes.md)|Retrieves a flag indicating whether the symbol file contains C types.|  
|[IDiaSymbol::get_isCVTCIL](../debug-interface-access/idiasymbol--get_iscvtcil.md)|Retrieves a flag indicating whether the module was converted from Common Intermediate Language (CIL) to native code.|  
|[IDiaSymbol::get_isDataAligned](../debug-interface-access/idiasymbol--get_isdataaligned.md)|Retrieves a flag indicating whether the elements of a user-defined data type are aligned to a specific boundary.|  
|[IDiaSymbol::get_isHLSLData](../debug-interface-access/idiasymbol--get_ishlsldata.md)|Specifies whether this symbol represents High Level Shader Language (HLSL) data.|  
|[IDiaSymbol::get_isHotpatchable](../debug-interface-access/idiasymbol--get_ishotpatchable.md)|Retrieves a flag indicating whether the module was compiled with the [/hotpatch (Create Hotpatchable Image)](../Topic/-hotpatch%20\(Create%20Hotpatchable%20Image\).md) compiler switch.|  
|[IDiaSymbol::get_isLTCG](../debug-interface-access/idiasymbol--get_isltcg.md)|Retrieves a flag indicating whether the managed compiland was linked with the linker's LTCG.|  
|[IDiaSymbol::get_isMatrixRowMajor](../debug-interface-access/idiasymbol--get_ismatrixrowmajor.md)|Specifies whether the matrix is row major.|  
|[IDiaSymbol::get_isMSILNetmodule](../debug-interface-access/idiasymbol--get_ismsilnetmodule.md)|Retrieves a flag indicating whether the managed compiland is a .netmodule (containing only metadata).|  
|[IDiaSymbol::get_isMultipleInheritance](../debug-interface-access/idiasymbol--get_ismultipleinheritance.md)|Specifies whether the `this` pointer points to a data member with multiple inheritance.|  
|[IDiaSymbol::get_isNaked](../debug-interface-access/idiasymbol--get_isnaked.md)|Retrieves a flag indicating whether the function has the [naked](../Topic/naked%20\(C++\).md) attribute.|  
|[IDiaSymbol::get_isOptimizedAway](../debug-interface-access/idiasymbol--get_isoptimizedaway.md)|Specifies whether the variable is optimized away.|  
|[IDiaSymbol::get_isPointerBasedOnSymbolValue](../debug-interface-access/idiasymbol--get_ispointerbasedonsymbolvalue.md)|Specifies whether the `this` pointer is based on a symbol value.|  
|[IDiaSymbol::get_isPointerToDataMember](../debug-interface-access/idiasymbol--get_ispointertodatamember.md)|Specifies whether this symbol is a pointer to a data member.|  
|[IDiaSymbol::get_isPointerToMemberFunction](../debug-interface-access/idiasymbol--get_ispointertomemberfunction.md)|Specifies whether this symbol is a pointer to a member function.|  
|[IDiaSymbol::get_isReturnValue](../debug-interface-access/idiasymbol--get_isreturnvalue.md)|Specifies whether the variable carries a return value.|  
|[IDiaSymbol::get_isSdl](../debug-interface-access/idiasymbol--get_issdl.md)|Specifies whether the module is compiled with the /SDL option.|  
|[IDiaSymbol::get_isSingleInheritance](../debug-interface-access/idiasymbol--get_issingleinheritance.md)|Specifies whether the `this` pointer points to a data member with single inheritance.|  
|[IDiaSymbol::get_isSplitted](../debug-interface-access/idiasymbol--get_issplitted.md)|Retrieves a flag indicating whether the data has been split into an aggregate of separate symbols.|  
|[IDiaSymbol::get_isStatic](../debug-interface-access/idiasymbol--get_isstatic.md)|Retrieves a flag indicating whether a function or thunk layer is static.|  
|[IDiaSymbol::get_isStripped](../debug-interface-access/idiasymbol--get_isstripped.md)|Retrieves a flag indicating whether private symbols have been stripped from the symbol file.|  
|[IDiaSymbol::get_isVirtualInheritance](../debug-interface-access/idiasymbol--get_isvirtualinheritance.md)|Specifies whether the `this` pointer points to a data member with virtual inheritance.|  
|[IDiaSymbol::get_language](../debug-interface-access/idiasymbol--get_language.md)|Retrieves the language of the source.|  
|[IDiaSymbol::get_length](../debug-interface-access/idiasymbol--get_length.md)|Retrieves the number of bytes of memory used by the object represented by this symbol.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|Retrieves a reference to the lexical parent of the symbol.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|Retrieves the lexical parent identifier of the symbol.|  
|[IDiaSymbol::get_libraryName](../debug-interface-access/idiasymbol--get_libraryname.md)|Retrieves the file name of the library or object file from which the object was loaded.|  
|[IDiaSymbol::get_liveRangeLength](../debug-interface-access/idiasymbol--get_liverangelength.md)|Returns the length of the address range in which the local symbol is valid.|  
|[IDiaSymbol::get_liveRangeStartAddressSection](../debug-interface-access/idiasymbol--get_liverangestartaddresssection.md)|Returns the section part of the starting address range in which the local symbol is valid.|  
|[IDiaSymbol::get_liveRangeStartAddressOffset](../debug-interface-access/idiasymbol--get_liverangestartaddressoffset.md)|Returns the offset part of the starting address range in which the local symbol is valid.|  
|[IDiaSymbol::get_liveRangeStartRelativeVirtualAddress](../debug-interface-access/idiasymbol--get_liverangestartrelativevirtualaddress.md)|Returns the start of the address range in which the local symbol is valid.|  
|[IDiaSymbol::get_locationType](../debug-interface-access/idiasymbol--get_locationtype.md)|Retrieves the location type of a data symbol.|  
|[IDiaSymbol::get_lowerBound](../debug-interface-access/idiasymbol--get_lowerbound.md)|Retrieves the lower bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_lowerBoundId](../debug-interface-access/idiasymbol--get_lowerboundid.md)|Retrieves the symbol identifier of the lower bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_machineType](../debug-interface-access/idiasymbol--get_machinetype.md)|Retrieves the type of the target CPU.|  
|[IDiaSymbol::get_managed](../debug-interface-access/idiasymbol--get_managed.md)|Retrieves a flag that indicating whether the symbol refers to managed code.|  
|[IDiaSymbol::get_memorySpaceKind](../debug-interface-access/idiasymbol--get_memoryspacekind.md)|Retrieves the memory space kind.|  
|[IDiaSymbol::get_msil](../debug-interface-access/idiasymbol--get_msil.md)|Retrieves a flag indicating whether the symbol refers to Microsoft Intermediate Language (MSIL) code.|  
|[IDiaSymbol::get_name](../debug-interface-access/idiasymbol--get_name.md)|Retrieves the name of the symbol.|  
|[IDiaSymbol::get_nested](../debug-interface-access/idiasymbol--get_nested.md)|Retrieves a flag indicating whether the user-defined data type is nested.|  
|[IDiaSymbol::get_noInline](../debug-interface-access/idiasymbol--get_noinline.md)|Retrieves a flag indicating whether the function is marked with the [noinline](../Topic/noinline.md) attribute.|  
|[IDiaSymbol::get_noReturn](../debug-interface-access/idiasymbol--get_noreturn.md)|Retrieves a flag indicating whether the function has been declared with the [noreturn](../Topic/noreturn.md) attribute.|  
|[IDiaSymbol::get_noStackOrdering](../debug-interface-access/idiasymbol--get_nostackordering.md)|Retrieves a flag indicating whether no stack ordering could be done as part of stack buffer checking.|  
|[IDiaSymbol::get_notReached](../debug-interface-access/idiasymbol--get_notreached.md)|Retrieves a flag indicating whether the function or label is never reached.|  
|[IDiaSymbol::get_numberOfAcceleratorPointerTags](../debug-interface-access/idiasymbol--get_numberofacceleratorpointertags.md)|Returns the number of accelerator pointer tags in a C++ AMP stub function.|  
|[IDiaSymbol::get_numberOfModifiers](../debug-interface-access/idiasymbol--get_numberofmodifiers.md)|Retrieves the number of modifiers that are applied to the original type.|  
|[IDiaSymbol::get_numberOfRegisterIndices](../debug-interface-access/idiasymbol--get_numberofregisterindices.md)|Retrieves the number of register indices.|  
|[IDiaSymbol::get_numberOfRows](../debug-interface-access/idiasymbol--get_numberofrows.md)|Retrieves the number of rows in the matrix.|  
|[IDiaSymbol::get_numberOfColumns](../debug-interface-access/idiasymbol--get_numberofcolumns.md)|Retrieves the number of columns in the matrix.|  
|[IDiaSymbol::get_objectFileName](../debug-interface-access/idiasymbol--get_objectfilename.md)|Retrieves the object file name.|  
|[IDiaSymbol::get_objectPointerType](../debug-interface-access/idiasymbol--get_objectpointertype.md)|Retrieves the type of the object pointer for a class method.|  
|[IDiaSymbol::get_oemId](../debug-interface-access/idiasymbol--get_oemid.md)|Retrieves the symbol's `oemId` value.|  
|[IDiaSymbol::get_oemSymbolId](../debug-interface-access/idiasymbol--get_oemsymbolid.md)|Retrieves the symbol's `oemSymbolId` value.|  
|[IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|Retrieves the offset of the symbol location.|  
|[IDiaSymbol::get_optimizedCodeDebugInfo](../debug-interface-access/idiasymbol--get_optimizedcodedebuginfo.md)|Retrieves a flag indicating whether the function or label contains optimized code as well as debug information.|  
|[IDiaSymbol::get_overloadedOperator](../debug-interface-access/idiasymbol--get_overloadedoperator.md)|Retrieves a flag indicating whether the user-defined data type has overloaded operators.|  
|[IDiaSymbol::get_packed](../debug-interface-access/idiasymbol--get_packed.md)|Retrieves a flag indicating whether the user-defined data type is packed.|  
|[IDiaSymbol::get_platform](../debug-interface-access/idiasymbol--get_platform.md)|Retrieves the platform type for which the program or compiland was compiled.|  
|[IDiaSymbol::get_pure](../debug-interface-access/idiasymbol--get_pure.md)|Retrieves a flag that indicating whether the function is pure virtual.|  
|[IDiaSymbol::get_rank](../debug-interface-access/idiasymbol--get_rank.md)|Retrieves the rank of a FORTRAN multidimensional array.|  
|[IDiaSymbol::get_reference](../debug-interface-access/idiasymbol--get_reference.md)|Retrieves a flag indicating whether a pointer type is a reference.|  
|[IDiaSymbol::get_registerId](../debug-interface-access/idiasymbol--get_registerid.md)|Retrieves the register designator of the location.|  
|[IDiaSymbol::get_registerType](../debug-interface-access/idiasymbol--get_registertype.md)|Retrieves the register type.|  
|[IDiaSymbol::get_relativeVirtualAddress](../debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|Retrieves the relative virtual address (RVA) of the location.|  
|[IDiaSymbol::get_restrictedType](../debug-interface-access/idiasymbol--get_restrictedtype.md)|Specifies whether the `this` pointer is flagged as restricted.|  
|[IDiaSymbol::get_samplerSlot](../debug-interface-access/idiasymbol--get_samplerslot.md)|Retrieves the sampler slot.|  
|[IDiaSymbol::get_scoped](../debug-interface-access/idiasymbol--get_scoped.md)|Retrieves a flag indicating whether the user-defined data type appears in a nonglobal lexical scope.|  
|[IDiaSymbol::get_signature](../debug-interface-access/idiasymbol--get_signature.md)|Retrieves the symbol's signature value.|  
|[IDiaSymbol::get_sizeInUdt](../debug-interface-access/idiasymbol--get_sizeinudt.md)|Retrieves the size of a member of a user-defined type.|  
|[IDiaSymbol::get_slot](../debug-interface-access/idiasymbol--get_slot.md)|Retrieves the slot number of the location.|  
|[IDiaSymbol::get_sourceFileName](../debug-interface-access/idiasymbol--get_sourcefilename.md)|Retrieves the file name of the source file.|  
|[IDiaSymbol::getSrcLineOnTypeDefn](../debug-interface-access/idiasymbol--getsrclineontypedefn.md)|Retrieves the source file and line number that indicate where a specified user-defined type is defined.|  
|[IDiaSymbol::get_stride](../debug-interface-access/idiasymbol--get_stride.md)|Retrieves the stride of the matrix or strided array.|  
|[IDiaSymbol::get_subType](../debug-interface-access/idiasymbol--get_subtype.md)|Retrieves the sub type.|  
|[IDiaSymbol::get_subTypeId](../debug-interface-access/idiasymbol--get_subtypeid.md)|Retrieves the sub type ID.|  
|[IDiaSymbol::get_symbolsFileName](../debug-interface-access/idiasymbol--get_symbolsfilename.md)|Retrieves the name of the file from which the symbols were loaded.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|Retrieves the unique symbol identifier.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|Retrieves the symbol type classifier.|  
|[IDiaSymbol::get_targetOffset](../debug-interface-access/idiasymbol--get_targetoffset.md)|Retrieves the offset section of a thunk target.|  
|[IDiaSymbol::get_targetRelativeVirtualAddress](../debug-interface-access/idiasymbol--get_targetrelativevirtualaddress.md)|Retrieves the relative virtual address (RVA) of a thunk target.|  
|[IDiaSymbol::get_targetSection](../debug-interface-access/idiasymbol--get_targetsection.md)|Retrieves the address section of a thunk target.|  
|[IDiaSymbol::get_targetVirtualAddress](../debug-interface-access/idiasymbol--get_targetvirtualaddress.md)|Retrieves the virtual address (VA) of a thunk target.|  
|[IDiaSymbol::get_textureSlot](../debug-interface-access/idiasymbol--get_textureslot.md)|Retrieves the texture slot.|  
|[IDiaSymbol::get_thisAdjust](../debug-interface-access/idiasymbol--get_thisadjust.md)|Retrieves the logical `this` adjustor for the method.|  
|[IDiaSymbol::get_thunkOrdinal](../debug-interface-access/idiasymbol--get_thunkordinal.md)|Retrieves the thunk type of a function.|  
|[IDiaSymbol::get_timeStamp](../debug-interface-access/idiasymbol--get_timestamp.md)|Retrieves the timestamp of the underlying executable file.|  
|[IDiaSymbol::get_token](../debug-interface-access/idiasymbol--get_token.md)|Retrieves the metadata token of a managed function or variable.|  
|[IDiaSymbol::get_type](../debug-interface-access/idiasymbol--get_type.md)|Retrieves a reference to the function signature.|  
|[IDiaSymbol::get_typeId](../debug-interface-access/idiasymbol--get_typeid.md)|Retrieves the type identifier of the symbol.|  
|[IDiaSymbol::get_types](../debug-interface-access/idiasymbol--get_types.md)|Retrieves an array of compiler-specific type values for this symbol.|  
|[IDiaSymbol::get_typeIds](../debug-interface-access/idiasymbol--get_typeids.md)|Retrieves an array of compiler-specific type identifier values for this symbol.|  
|[IDiaSymbol::get_uavSlot](../debug-interface-access/idiasymbol--get_uavslot.md)|Retrieves the uav slot.|  
|[IDiaSymbol::get_udtKind](../debug-interface-access/idiasymbol--get_udtkind.md)|Retrieves the variety of a user-defined type (UDT).|  
|[IDiaSymbol::get_unalignedType](../debug-interface-access/idiasymbol--get_unalignedtype.md)|Retrieves a flag indicating whether the user-defined data type is unaligned.|  
|[IDiaSymbol::get_undecoratedName](../debug-interface-access/idiasymbol--get_undecoratedname.md)|Retrieves the undecorated name for a C++ decorated, or linkage, name.|  
|[IDiaSymbol::get_undecoratedNameEx](../debug-interface-access/idiasymbol--get_undecoratednameex.md)|Extension of the `get_undecoratedName` method that retrieves the undecorated name based on the value of an extension field.|  
|[IDiaSymbol::get_unmodifiedTypeId](../debug-interface-access/idiasymbol--get_unmodifiedtypeid.md)|Retrieves the ID of the original (unmodified) type.|  
|[IDiaSymbol::get_upperBound](../debug-interface-access/idiasymbol--get_upperbound.md)|Retrieves the upper bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_upperBoundId](../debug-interface-access/idiasymbol--get_upperboundid.md)|Retrieves the symbol identifier of the upper bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_value](../debug-interface-access/idiasymbol--get_value.md)|Retrieves the value of a constant.|  
|[IDiaSymbol::get_virtual](../debug-interface-access/idiasymbol--get_virtual.md)|Retrieves a flag indicating whether the function is virtual.|  
|[IDiaSymbol::get_virtualAddress](../debug-interface-access/idiasymbol--get_virtualaddress.md)|Retrieves the virtual address (VA) of the location.|  
|[IDiaSymbol::get_virtualBaseClass](../debug-interface-access/idiasymbol--get_virtualbaseclass.md)|Retrieves a flag indicating whether the user-defined data type is a virtual base class.|  
|[IDiaSymbol::get_virtualBaseDispIndex](../debug-interface-access/idiasymbol--get_virtualbasedispindex.md)|Retrieves the index to the virtual base displacement table.|  
|[IDiaSymbol::get_virtualBaseOffset](../debug-interface-access/idiasymbol--get_virtualbaseoffset.md)|Retrieves the offset in the virtual function table of a virtual function.|  
|[IDiaSymbol::get_virtualBasePointerOffset](../debug-interface-access/idiasymbol--get_virtualbasepointeroffset.md)|Retrieves the offset of the virtual base pointer.|  
|[IDiaSymbol::get_virtualBaseTableType](../debug-interface-access/idiasymbol--get_virtualbasetabletype.md)|Retrieves the type of a virtual base table pointer.|  
|[IDiaSymbol::get_virtualTableShape](../debug-interface-access/idiasymbol--get_virtualtableshape.md)|Retrieves the symbol interface of the type of the virtual table for a user-defined type.|  
|[IDiaSymbol::get_virtualTableShapeId](../debug-interface-access/idiasymbol--get_virtualtableshapeid.md)|Retrieves the virtual table shape identifier of the symbol.|  
|[IDiaSymbol::get_volatileType](../debug-interface-access/idiasymbol--get_volatiletype.md)|Retrieves a flag indicating whether the user-defined data type is volatile.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling one of the following methods:  
  
-   [IDiaEnumSymbols::Item](../debug-interface-access/idiaenumsymbols--item.md)  
  
-   [IDiaEnumSymbols::Next](../debug-interface-access/idiaenumsymbols--next.md)  
  
-   [IDiaEnumSymbolsByAddr::Next](../debug-interface-access/idiaenumsymbolsbyaddr--next.md)  
  
-   [IDiaEnumSymbolsByAddr::Prev](../debug-interface-access/idiaenumsymbolsbyaddr--prev.md)  
  
-   [IDiaEnumSymbolsByAddr::symbolByAddr](../debug-interface-access/idiaenumsymbolsbyaddr--symbolbyaddr.md)  
  
-   [IDiaEnumSymbolsByAddr::symbolByRVA](../debug-interface-access/idiaenumsymbolsbyaddr--symbolbyrva.md)  
  
-   [IDiaEnumSymbolsByAddr::symbolByVA](../debug-interface-access/idiaenumsymbolsbyaddr--symbolbyva.md)  
  
-   [IDiaSession::findSymbolByAddr](../debug-interface-access/idiasession--findsymbolbyaddr.md)  
  
-   [IDiaSession::findSymbolByRVA](../debug-interface-access/idiasession--findsymbolbyrva.md)  
  
-   [IDiaSession::findSymbolByRVAEx](../debug-interface-access/idiasession--findsymbolbyrvaex.md)  
  
-   [IDiaSession::findSymbolByVA](../debug-interface-access/idiasession--findsymbolbyva.md)  
  
-   [IDiaSession::findSymbolByVAEx](../debug-interface-access/idiasession--findsymbolbyvaex.md)  
  
-   [IDiaSession::findSymbolByToken](../debug-interface-access/idiasession--findsymbolbytoken.md)  
  
-   [IDiaSession::symbolById](../debug-interface-access/idiasession--symbolbyid.md)  
  
-   [IDiaStackWalkHelper::symbolForVA](../debug-interface-access/idiastackwalkhelper--symbolforva.md)  
  
-   [IDiaSymbol::get_types](../debug-interface-access/idiasymbol--get_types.md)  
  
## Example  
 This example shows how to display the local variables for a function at a given relative virtual address. It also shows how symbols of different types are related to each other.  
  
> [!NOTE]
>  `CDiaBSTR` is a class that wraps a `BSTR` and automatically handles freeing the string when the instantiation goes out of scope.  
  
```cpp#  
void DumpLocalVars( DWORD rva, IDiaSession *pSession )  
{  
    CComPtr< IDiaSymbol > pBlock;  
    if ( FAILED( psession->findSymbolByRVA( rva, SymTagBlock, &pBlock ) ) )  
    {  
        Fatal( "Failed to find symbols by RVA" );  
    }  
    CComPtr< IDiaSymbol > pscope;  
    for ( ; pBlock != NULL; )  
    {  
        CComPtr< IDiaEnumSymbols > pEnum;  
        // local data search  
        if ( FAILED( pBlock->findChildren( SymTagNull, NULL, nsNone, &pEnum ) ) )  
        {  
            Fatal( "Local scope findChildren failed" );  
        }  
        CComPtr< IDiaSymbol > pSymbol;  
        DWORD tag;  
        DWORD celt;  
        while ( pEnum != NULL &&  
                SUCCEEDED( pEnum->Next( 1, &pSymbol, &celt ) ) &&  
                celt == 1)  
        {  
            pSymbol->get_symTag( &tag );  
            if ( tag == SymTagData )  
            {  
                CDiaBSTR name;  
                DWORD    kind;  
                pSymbol->get_name( &name );  
                pSymbol->get_dataKind( &kind );  
                if ( name != NULL )  
                    wprintf_s( L"\t%s (%s)\n", name, szDataKinds[ kind ] );  
            }  
            else if ( tag == SymTagAnnotation )  
            {  
                CComPtr< IDiaEnumSymbols > pValues;  
                // local data search  
                wprintf_s( L"\tAnnotation:\n" );  
                if ( FAILED( pSymbol->findChildren( SymTagNull, NULL, nsNone, &pValues ) ) )  
                    Fatal( "Annotation findChildren failed" );  
                pSymbol = NULL;  
                while ( pValues != NULL &&  
                        SUCCEEDED( pValues->Next( 1, &pSymbol, &celt ) ) &&  
                        celt == 1 )  
                {  
                    CComVariant value;  
                    if ( pSymbol->get_value( &value ) != S_OK )  
                        Fatal( "No value for annotation data." );  
                    wprintf_s( L"\t\t%ws\n", value.bstrVal );  
                    pSymbol = NULL;  
                }  
            }  
            pSymbol = NULL;  
        }  
        pBlock->get_symTag( &tag );   
        if ( tag == SymTagFunction )    // stop when at function scope  
            break;  
        // move to lexical parent  
        CComPtr< IDiaSymbol > pParent;  
        if ( SUCCEEDED( pBlock->get_lexicalParent( &pParent ) )  
            && pParent != NULL ) {  
            pBlock = pParent;  
        }  
        else  
        {  
            Fatal( "Finding lexical parent failed." );  
        }  
    };  
}  
```  
  
## Requirements  
 `Header:` Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaEnumSymbolsByAddr](../debug-interface-access/idiaenumsymbolsbyaddr.md)   
 [IDiaEnumSymbols](../debug-interface-access/idiaenumsymbols.md)   
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [Class Hierarchy of Symbol Types](../debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [Symbols and Symbol Tags](../debug-interface-access/symbols-and-symbol-tags.md)   
 [Compiland](../debug-interface-access/compiland.md)