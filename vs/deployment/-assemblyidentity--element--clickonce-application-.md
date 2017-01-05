---
title: "&lt;assemblyIdentity&gt; Element (ClickOnce Application)"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-deployment"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "urn:schemas-microsoft-com:asm.v2#assemblyIdentity"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "<assemblyIdentity> element [ClickOnce application manifest]"
ms.assetid: f48e9531-efac-4d11-8166-f63a5ece1ac5
caps.latest.revision: 20
ms.author: "shoag"
manager: "wpickett"
translation.priority.ht: 
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
# &lt;assemblyIdentity&gt; Element (ClickOnce Application)
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

Identifies the application deployed in a [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] deployment.  
  
## Syntax  
  
```  
  
      <assemblyIdentity   
   name  
   version  
   publicKeyToken  
   processorArchitecture  
   language  
/>  
```  
  
## Elements and Attributes  
 The `assemblyIdentity` element is required. It contains no child elements and has the following attributes.  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Name`|Required. Identifies the name of the application.<br /><br /> If `Name` contains special characters, such as single or double quotes, the application may fail to activate.|  
|`Version`|Required. Specifies the version number of the application in the following format: `major.minor.build.revision`|  
|`publicKeyToken`|Optional. Specifies a 16-character hexadecimal string that represents the last 8 bytes of the `SHA-1` hash value of the public key under which the application or assembly is signed. The public key that is used to sign the catalog must be 2048 bits or greater.<br /><br /> Although signing an assembly is recommended but optional, this attribute is required. If an assembly is unsigned, you should copy a value from a self-signed assembly or use a "dummy" value of all zeros.|  
|`processorArchitecture`|Required. Specifies the processor. The valid values are `msil` for all processors, `x86` for 32-bit Windows, `IA64` for 64-bit Windows, and `Itanium` for Intel 64-bit Itanium processors.|  
|`language`|Required. Identifies the two part language codes (for example, `en-US`) of the assembly. This element is in the `asmv2` namespace. If unspecified, the default is `neutral`.|  
  
## Examples  
  
### Description  
 The following code example illustrates an `assemblyIdentity` element in a [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] application manifest. This code example is part of a larger example provided in [ClickOnce Application Manifest](../deployment/clickonce-application-manifest.md).  
  
### Code  
  
```  
<asmv1:assemblyIdentity   
  name="My Application Deployment.exe"   
  version="1.0.0.0"   
  publicKeyToken="43cb1e8e7a352766"   
  language="neutral"   
  processorArchitecture="x86"   
  type="win32" />  
```  
  
## See Also  
 [ClickOnce Application Manifest](../deployment/clickonce-application-manifest.md)   
 [\<assemblyIdentity> Element](../deployment/-assemblyidentity--element--clickonce-deployment-.md)