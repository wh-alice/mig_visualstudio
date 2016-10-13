---
title: "ClickOnce Unmanaged API Reference"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-deployment"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "LaunchApplication [ClickOnce unmanaged]"
  - "ClickOnce, unmanaged APIs"
  - "CleanOnlineAppCache [ClickOnce unmanaged]"
  - "CleanOnlineAppCacheW interface [ClickOnce unmanaged]"
  - "GetDeploymentDataFromManifest [ClickOnce unmanaged]"
ms.assetid: ec002138-4054-456d-bcc1-79ac2f4a4fd7
caps.latest.revision: 6
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
# ClickOnce Unmanaged API Reference
[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] unmanaged public APIs from dfshim.dll.  
  
## CleanOnlineAppCache  
 Cleans or uninstalls all online applications from the [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] application cache.  
  
### Return Value  
 If successful, returns S_OK; otherwise, returns an HRESULT that represents the failure. If a managed exception occurs, returns 0x80020009 (DISP_E_EXCEPTION).  
  
### Remarks  
 Calling CleanOnlineAppCache will start the [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] service if it is not already running.  
  
## GetDeploymentDataFromManifest  
 Retrieves deployment information from the manifest and activation URL.  
  
### Parameters  
  
|Parameter|Description|Type|  
|---------------|-----------------|----------|  
|`pcwzActivationUrl`|A pointer to the `ActivationURL`.|LPCWSTR|  
|`pcwzPathToDeploymentManifest`|A pointer to the `PathToDeploymentManifest`.|LPCWSTR|  
|`pwzApplicationIdentity`|A pointer to a buffer to receive a NULL-terminated string that specifies the full application identity returned.|LPWSTR|  
|`pdwIdentityBufferLength`|A pointer to a DWORD that is the length of the `pwzApplicationIdentity` buffer, in WCHARs. This includes the space for the NULL termination character.|LPDWORD|  
|`pwzProcessorArchitecture`|A pointer to a buffer to receive a NULL-terminated string that specifies the processor architecture of the application deployment, from the manifest.|LPWSTR|  
|`pdwArchitectureBufferLength`|A pointer to a DWORD that is the length of the `pwzProcessorArchitecture` buffer, in WCHARs.|LPDWORD|  
|`pwzApplicationManifestCodebase`|A pointer to a buffer to receive a NULL-terminated string that specifies the codebase of the application manifest, from the manifest.|LPWSTR|  
|`pdwCodebaseBufferLength`|A pointer to a DWORD that is the length of the `pwzApplicationManifestCodebase` buffer, in WCHARs.|LPDWORD|  
|`pwzDeploymentProvider`|A pointer to a buffer to receive a NULL-terminated string that specifies the deployment provider from the manifest, if present. Otherwise, an empty string is returned.|LPWSTR|  
|`pdwProviderBufferLength`|A pointer to a DWORD that is the length of the `pwzProviderBufferLength`.|LPDWORD|  
  
### Return Value  
 If successful, returns S_OK; otherwise, returns an HRESULT that represents the failure. Returns HRESULTFROMWIN32(ERROR_INSUFFICIENT_BUFFER) if a buffer is too small.  
  
### Remarks  
 Pointers must not be null. `pcwzActivationUrl` and `pcwzPathToDeploymentManifest` must not be empty.  
  
 It is the caller's responsibility to clean up the activation URL. For example, adding escape characters where they are needed or removing the query string.  
  
 It is the caller's responsibility to limit the input length. For example, the maximum URL length is 2KB.  
  
## LaunchApplication  
 Launches or installs an application by using a deployment URL.  
  
### Parameters  
  
|Parameter|Description|Type|  
|---------------|-----------------|----------|  
|`deploymentUrl`|A pointer to a NULL-terminated string that contains the URL of the deployment manifest.|LPCWSTR|  
|`data`|Reserved for future use. Must be NULL.|LPVOID|  
|`flags`|Reserved for future use. Must be 0.|DWORD|  
  
### Return Value  
 If successful, returns S_OK; otherwise, returns an HRESULT that represents the failure. If a managed exception occurs, returns 0x80020009 (DISP_E_EXCEPTION).  
  
## See Also  
 \<xref:System.Deployment.Application.DeploymentServiceCom.CleanOnlineAppCache*>