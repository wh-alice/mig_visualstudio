---
title: "Lexical Hierarchy of Symbol Types | testtitle"
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
|[Annotation](../debug-interface-access/annotation.md)|Specifies an annotated location in program code.|  
|[Block](../debug-interface-access/block.md)|Specifies nested scopes in functions.|  
|`Compiland`|Specifies a `compiland` linked to the .exe file.|  
|[CompilandDetails](../debug-interface-access/compilanddetails.md)|Specifies compiland data that may require loading additional compiland details and thus incur run-time overhead to retrieve.|  
|[CompilandEnv](../debug-interface-access/compilandenv.md)|Specifies any additional environment variables significant to the compilation of the compiland.|  
|[Custom (Debug Interface Access SDK)](../debug-interface-access/custom--debug-interface-access-sdk-.md)|Specifies a user-defined symbol.|  
|[Data (Debug Interface Access SDK)](../debug-interface-access/data--debug-interface-access-sdk-.md)|Specifies such variables as parameters, local variables, global variables, and class members.|  
|[Exe](../debug-interface-access/exe.md)|Specifies the global scope of the data; corresponds to an entire .exe or .dll file.|  
|[FuncDebugEnd](../debug-interface-access/funcdebugend.md)|Specifies a function that has a defined point at which debugging is to end.|  
|[FuncDebugStart](../debug-interface-access/funcdebugstart.md)|Specifies a function that has a defined point at which debugging is to begin.|  
|[Function (Debug Interface Access SDK)](../debug-interface-access/function--debug-interface-access-sdk-.md)|Specifies a function.|  
|[Label (Debug Interface Access SDK)](../debug-interface-access/label--debug-interface-access-sdk-.md)|Specifies a location in program code.|  
|[PublicSymbol](../debug-interface-access/publicsymbol.md)|Specifies an external symbol that appears when building the executable program.|  
|[Thunk](../debug-interface-access/thunk.md)|Specifies a `thunk`.|  
|[UsingNameSpace](../debug-interface-access/usingnamespace.md)|Specifies a `namespace`identifier.|  
  
> [!NOTE]
>  Additional symbol properties may be available depending on the symbol type. These properties are listed in the individual symbol topics.  
  
## See Also  
 [Class Hierarchy of Symbol Types](../debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)   
 [Symbols and Symbol Tags](../debug-interface-access/symbols-and-symbol-tags.md)   
 [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md)