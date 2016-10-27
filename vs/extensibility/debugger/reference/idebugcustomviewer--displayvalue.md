---
title: "IDebugCustomViewer::DisplayValue"
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
  - "IDebugCustomViewer::DisplayValue"
helpviewer_keywords: 
  - "IDebugCustomViewer::DisplayValue"
ms.assetid: 7a538248-5ced-450e-97cd-13fabe35fb1c
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
# IDebugCustomViewer::DisplayValue
This method is called to display the specified value.  
  
## Syntax  
  
```cpp#  
HRESULT DisplayValue(  
   HWND             hwnd,  
   DWORD            dwID,  
   IUnknown *       pHostServices,  
   IDebugProperty3* pDebugProperty);  
);  
```  
  
```c#  
int DisplayValue(  
   IntPtr          hwnd,   
   uint            dwID,   
   object          pHostServices,   
   IDebugProperty3 pDebugProperty  
);  
```  
  
#### Parameters  
 `hwnd`  
 [in] Parent window  
  
 `dwID`  
 [in] ID for custom viewers that support more than one type.  
  
 `pHostServices`  
 [in] Reserved. Always set to null.  
  
 `pDebugProperty`  
 [in] Interface that can be used to retrieve the value to be displayed.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code.  
  
## Remarks  
 The display is "modal" in that this method will create the necessary window, display the value, wait for input, and close the window, all before returning to the caller. This means the method must handle all aspects of displaying the property's value, from creating a window for output, to waiting for user input, to destroying the window.  
  
 To support changing the value on the given [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) object, you can use the [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3--setvalueasstringwitherror.md) method —if the value can be expressed as a string. Otherwise, it is necessary to create a custom interface—exclusive to the expression evaluator implementing this `DisplayValue` method—on the same object that implements the `IDebugProperty3` interface. This custom interface would supply methods for changing the data of an arbitrary size or complexity.  
  
## See Also  
 [IDebugCustomViewer](../../../extensibility/debugger/reference/idebugcustomviewer.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3--setvalueasstringwitherror.md)