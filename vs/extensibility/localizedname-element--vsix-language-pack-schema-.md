---
title: "LocalizedName Element (VSIX Language Pack Schema)"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 57b7f502-3b04-42d9-90d5-f57772a7c757
caps.latest.revision: 7
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# LocalizedName Element (VSIX Language Pack Schema)
Required. The localized name of the extension to be installed.  
  
## Syntax  
  
```  
<Name>Localized name of the extension</Name>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|None||  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|None||  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[VSIX LanguagePack Element](../extensibility/vsixlanguagepack-element--vsix-language-pack-schema-.md)|Required. Provides the root element for a VSIX language pack.|  
  
## Text Value  
 Required. The name of the language pack in the target language.  
  
## Element Information  
  
|||  
|-|-|  
|Namespace|http://schemas.microsoft.com/developer/vsx-schema-lp/2010|  
|Schema Name|VSIX Language Pack Schema|  
|Validation File|VSIXLanguagePackSchema.xsd|  
|Can be Empty|Not applicable|  
  
## See Also  
 [VSX Language Pack Schema Reference](../extensibility/vsx-language-pack-schema-reference.md)   
 [Localizing VSIX Packages](../extensibility/localizing-vsix-packages.md)   
 [VSIX Extension Schema 1.0 Reference](assetId:///76e410ec-b1fb-4652-ac98-4a4c52e09a2b)