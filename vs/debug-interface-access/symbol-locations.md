---
title: "Symbol Locations"
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
  - "LocationType values"
  - "symbols [DIA SDK], locations"
ms.assetid: 7c8cd8fe-169e-4161-9cff-5e9015984add
caps.latest.revision: 7
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
# Symbol Locations
Most symbols have a defined location within the image file. A symbol's location is specified with a value from the [LocationType Enumeration](../debug-interface-access/locationtype.md) enumeration. The symbol may support additional properties depending on its location.  
  
 The following table shows the most commonly used location types and their additional properties.  
  
|Location type|Additional properties|  
|-------------------|---------------------------|  
|`LocIsNull`|none|  
|`LocIsStatic`|[IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)<br /><br /> [IDiaSymbol::get_addressSection](../debug-interface-access/idiasymbol--get_addresssection.md)<br /><br /> [IDiaSymbol::get_relativeVirtualAddress](../debug-interface-access/idiasymbol--get_relativevirtualaddress.md) (if relative virtual addresses are enabled)<br /><br /> [IDiaSymbol::get_virtualAddress](../debug-interface-access/idiasymbol--get_virtualaddress.md) (if the image base has been set to nonzero)|  
|`LocIsTLS`|[IDiaSymbol::get_addressSection](../debug-interface-access/idiasymbol--get_addresssection.md)<br /><br /> [IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)|  
|`LocIsRegRel`|[IDiaSymbol::get_registerId](../debug-interface-access/idiasymbol--get_registerid.md)<br /><br /> [IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|  
|`LocIsThisRel`|[IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|  
|`LocIsEnregistered`|[IDiaSymbol::get_registerId](../debug-interface-access/idiasymbol--get_registerid.md)|  
|`LocIsBitField`|[IDiaSymbol::get_bitPosition](../debug-interface-access/idiasymbol--get_bitposition.md)<br /><br /> [IDiaSymbol::get_length](../debug-interface-access/idiasymbol--get_length.md)<br /><br /> [IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|  
|`LocIsSlot`|[IDiaSymbol::get_slot](../debug-interface-access/idiasymbol--get_slot.md)|  
|`LocIsIlRel`|[IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|  
|`LocInMetaData`|[IDiaSymbol::get_token](../debug-interface-access/idiasymbol--get_token.md)|  
|`LocIsConstant`|[IDiaSymbol::get_value](../debug-interface-access/idiasymbol--get_value.md)|  
  
## See Also  
 [IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)   
 [IDiaSymbol::get_addressSection](../debug-interface-access/idiasymbol--get_addresssection.md)   
 [IDiaSymbol::get_bitPosition](../debug-interface-access/idiasymbol--get_bitposition.md)   
 [IDiaSymbol::get_length](../debug-interface-access/idiasymbol--get_length.md)   
 [IDiaSymbol::get_locationType](../debug-interface-access/idiasymbol--get_locationtype.md)   
 [IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)   
 [IDiaSymbol::get_registerId](../debug-interface-access/idiasymbol--get_registerid.md)   
 [IDiaSymbol::get_relativeVirtualAddress](../debug-interface-access/idiasymbol--get_relativevirtualaddress.md)   
 [IDiaSymbol::get_slot](../debug-interface-access/idiasymbol--get_slot.md)   
 [IDiaSymbol::get_token](../debug-interface-access/idiasymbol--get_token.md)   
 [IDiaSymbol::get_value](../debug-interface-access/idiasymbol--get_value.md)   
 [IDiaSymbol::get_virtualAddress](../debug-interface-access/idiasymbol--get_virtualaddress.md)   
 [LocationType Enumeration](../debug-interface-access/locationtype.md)   
 [Symbols and Symbol Tags](../debug-interface-access/symbols-and-symbol-tags.md)