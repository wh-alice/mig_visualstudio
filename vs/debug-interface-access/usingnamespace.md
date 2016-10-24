---
title: "UsingNameSpace | testtitle"
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
  - "UsingNamespace symbol tag"
ms.assetid: e8e1beb5-7cb9-43b4-9ff4-760d5f91ea2d
caps.latest.revision: 17
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
# UsingNameSpace
Some symbols might be referred to by namespace, and would subsequently be identified by a `SymTagUsingNameSpace` tag.  
  
> [!NOTE]
>  The UsingNamespace symbol tag appears only in managed code.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, block, or function.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Namespace name.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagNameSpace` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../debug-interface-access/lexical-hierarchy-of-symbol-types.md)