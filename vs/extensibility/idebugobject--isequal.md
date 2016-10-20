---
title: "IDebugObject::IsEqual | Microsoft Docs"
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
  - "IDebugObject::IsEqual"
helpviewer_keywords: 
  - "IDebugObject::IsEqual method"
ms.assetid: 4b76e663-ef2e-41ff-9be1-bf26d666a34a
caps.latest.revision: 9
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
# IDebugObject::IsEqual
Compares an object with this object.  
  
## Syntax  
  
```cpp#  
HRESULT IsEqual(   
   IDebugObject* pObject,  
   BOOL*         pfIsEqual  
);  
```  
  
```c#  
int IsEqual(  
   IDebugObject pObject,  
   out int      pfIsEqual  
);  
```  
  
#### Parameters  
 `pObject`  
 [in] An [IDebugObject](../extensibility/idebugobject.md) object representing the object to compare to.  
  
 `pfIsEqual`  
 [out] Returns non-zero (`TRUE`) if the values of the objects are equal; otherwise, returns zero (`FALSE`).  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Typically, this method can compare the addresses of the values represented by the `pObject` parameter and this [IDebugObject](../extensibility/idebugobject.md) object; if the addresses are equal, then the objects can be considered equal.  
  
## See Also  
 [IDebugObject](../extensibility/idebugobject.md)