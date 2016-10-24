---
title: "IDebugBreakpointResolution2::GetBreakpointType"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugBreakpointResolution2::GetBreakpointType"
helpviewer_keywords: 
  - "IDebugBreakpointResolution2::GetBreakpointType"
ms.assetid: 2b707fb9-f703-4c78-91bf-7434f57790a0
caps.latest.revision: 11
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
# IDebugBreakpointResolution2::GetBreakpointType
Gets the type of the breakpoint represented by this resolution.  
  
## Syntax  
  
```cpp#  
HRESULT GetBreakpointType(   
   BP_TYPE* pBPType  
);  
```  
  
```c#  
int GetBreakpointType(   
   out enum_ BP_TYPE pBPType  
);  
```  
  
#### Parameters  
 `pBPType`  
 [out] Returns a value from the [BP_TYPE](../extensibility-debugger-reference/bp_type.md) enumeration that specifies the type of this breakpoint.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code. Returns E_FAIL if the `bpResLocation` field in the associated [BP_RESOLUTION_INFO](../extensibility-debugger-reference/bp_resolution_info.md) structure is not valid.  
  
## Remarks  
 The breakpoint may be a code or a data breakpoint, for example.  
  
## Example  
 The following example shows how to implement this method for a simple `CDebugBreakpointResolution` object that exposes the [IDebugBreakpointResolution2](../extensibility-debugger-reference/idebugbreakpointresolution2.md) interface.  
  
```  
HRESULT CDebugBreakpointResolution::GetBreakpointType(BP_TYPE* pBPType)    
{    
   HRESULT hr;    
  
   if (pBPType)    
   {    
      // Set default BP_TYPE.    
      *pBPType = BPT_NONE;    
  
      // Check if the BPRESI_BPRESLOCATION flag is set in BPRESI_FIELDS.    
      if (IsFlagSet(m_bpResolutionInfo.dwFields, BPRESI_BPRESLOCATION))    
      {    
         // Set the new BP_TYPE.    
         *pBPType = m_bpResolutionInfo.bpResLocation.bpType;    
         hr = S_OK;    
      }    
      else    
      {    
         hr = E_FAIL;    
      }    
   }    
   else    
   {    
      hr = E_INVALIDARG;    
   }    
  
   return hr;    
}    
```  
  
## See Also  
 [IDebugBreakpointResolution2](../extensibility-debugger-reference/idebugbreakpointresolution2.md)   
 [BP_TYPE](../extensibility-debugger-reference/bp_type.md)   
 [BPRESI_FIELDS](../extensibility-debugger-reference/bpresi_fields.md)   
 [BP_RESOLUTION_LOCATION](../extensibility-debugger-reference/bp_resolution_location.md)   
 [BP_RESOLUTION_INFO](../extensibility-debugger-reference/bp_resolution_info.md)