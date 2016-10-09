---
title: "Lexical Hierarchy of Symbol Types"
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
  - "symbols [DIA SDK], type hierarchies"
ms.assetid: 912da653-ddfe-45a4-84aa-64281283739a
caps.latest.revision: 15
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
# Lexical Hierarchy of Symbol Types
The following table shows the symbol types in the lexical hierarchy.  
  
## Symbol Types  
  
|Symbol type|Description|  
|-----------------|-----------------|  
|[Annotation](../VS_debugger/annotation.md)|Specifies an annotated location in program code.|  
|[Block](../VS_debugger/block.md)|Specifies nested scopes in functions.|  
|`Compiland`|Specifies a `compiland` linked to the .exe file.|  
|[CompilandDetails](../VS_debugger/compilanddetails.md)|Specifies compiland data that may require loading additional compiland details and thus incur run-time overhead to retrieve.|  
|[CompilandEnv](../VS_debugger/compilandenv.md)|Specifies any additional environment variables significant to the compilation of the compiland.|  
|[Custom (Debug Interface Access SDK)](../VS_debugger/custom--debug-interface-access-sdk-.md)|Specifies a user-defined symbol.|  
|[Data (Debug Interface Access SDK)](../VS_debugger/data--debug-interface-access-sdk-.md)|Specifies such variables as parameters, local variables, global variables, and class members.|  
|[Exe](../VS_debugger/exe.md)|Specifies the global scope of the data; corresponds to an entire .exe or .dll file.|  
|[FuncDebugEnd](../VS_debugger/funcdebugend.md)|Specifies a function that has a defined point at which debugging is to end.|  
|[FuncDebugStart](../VS_debugger/funcdebugstart.md)|Specifies a function that has a defined point at which debugging is to begin.|  
|[Function (Debug Interface Access SDK)](../VS_debugger/function--debug-interface-access-sdk-.md)|Specifies a function.|  
|[Label (Debug Interface Access SDK)](../VS_debugger/label--debug-interface-access-sdk-.md)|Specifies a location in program code.|  
|[PublicSymbol](../VS_debugger/publicsymbol.md)|Specifies an external symbol that appears when building the executable program.|  
|[Thunk](../VS_debugger/thunk.md)|Specifies a `thunk`.|  
|[UsingNameSpace](../VS_debugger/usingnamespace.md)|Specifies a `namespace`identifier.|  
  
> [!NOTE]
>  Additional symbol properties may be available depending on the symbol type. These properties are listed in the individual symbol topics.  
  
## See Also  
 [Class Hierarchy of Symbol Types](../VS_debugger/class-hierarchy-of-symbol-types.md)   
 [IDiaSymbol::get_symTag](../VS_debugger/idiasymbol--get_symtag.md)   
 [Symbols and Symbol Tags](../VS_debugger/symbols-and-symbol-tags.md)   
 [SymTagEnum Enumeration](../VS_debugger/symtagenum.md)