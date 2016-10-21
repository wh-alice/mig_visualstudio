---
title: "NAME_MATCH | hehe"
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
  - "NAME_MATCH"
helpviewer_keywords: 
  - "NAME_MATCH enumeration"
ms.assetid: 3842c417-a3c9-4259-a05f-52b64b829ef6
caps.latest.revision: 8
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
# NAME_MATCH
Selects the case option for matching names.  
  
## Syntax  
  
```cpp#  
typedef enum {   
   nmNone            = 0,  
   nmCaseSensitive   = 1,  
   nmCaseInsensitive = 2  
} NAME_MATCH;  
```  
  
```c#  
public enum NameMatchOptions {   
   nmNone            = 0,  
   nmCaseSensitive   = 1,  
   nmCaseInsensitive = 2  
}  
```  
  
## Members  
 nmNone  
 No options are specified.  
  
 nmCaseSensitive  
 Indicates that names to be matched are case-sensitive.  
  
 nmCaseInsensitive  
 Indicates that names to be matched are not case-sensitive.  
  
## Remarks  
 Passed as an argument to the following methods:  
  
-   [GetTypeByName](../extensibility-debugger-reference/idebugsymbolprovider--gettypebyname.md)  
  
-   [GetClassTypeByName](../extensibility-debugger-reference/idebugsymbolprovider--getclasstypebyname.md)  
  
-   [EnumFields](../extensibility-debugger-reference/idebugcontainerfield--enumfields.md)  
  
-   [GetMethodFieldsByName](../extensibility-debugger-reference/idebugsymbolprovider--getmethodfieldsbyname.md)  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../extensibility-debugger-reference/enumerations--visual-studio-debugging-.md)   
 [GetTypeByName](../extensibility-debugger-reference/idebugsymbolprovider--gettypebyname.md)   
 [GetClassTypeByName](../extensibility-debugger-reference/idebugsymbolprovider--getclasstypebyname.md)   
 [EnumFields](../extensibility-debugger-reference/idebugcontainerfield--enumfields.md)   
 [GetMethodFieldsByName](../extensibility-debugger-reference/idebugsymbolprovider--getmethodfieldsbyname.md)