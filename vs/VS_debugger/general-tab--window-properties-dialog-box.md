---
title: "General Tab, Window Properties Dialog Box"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Window Properties dialog box, General Tab"
ms.assetid: 19142c60-9b32-46ba-a556-b62fd77568c1
caps.latest.revision: 4
ms.author: "mikejo"
manager: "ghogen"
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
# General Tab, Window Properties Dialog Box
Use the **General** tab to show information about the selected window. To display the [Window Properties Dialog Box](../VS_debugger/window-properties-dialog-box.md), move the focus to the [Windows View](../VS_debugger/windows-view.md) window. Select any window node in the tree, then choose **Properties** from the **View** menu.  
  
 The following settings are available on the **General** tab:  
  
|Entry|Description|  
|-----------|-----------------|  
|**Window Caption**|The text in the window caption, or text contained in a window if it is a control.|  
|**Window Handle**|The unique ID of this window. Window handle numbers are reused; they identify a window only for the lifetime of that window.|  
|**Window Proc**|The virtual address of the window procedure function for this window. This field also indicates whether this window is a Unicode window, and whether it is subclassed.|  
|**Rectangle**|The bounding rectangle for the window. The size of the rectangle is also displayed. Units are pixels in screen coordinates.|  
|**Restored Rect**|The bounding rectangle for the restored window. The size of the rectangle is also displayed. Restored Rect will differ from Rectangle only when the window is maximized or minimized. Units are pixels in screen coordinates.|  
|**Client Rect**|The bounding rectangle for the window client area. The size of the rectangle is also displayed. Units are pixels relative to the top left of the window client area.|  
|**Instance Handle**|The instance handle of the application. Instance handles are not unique.|  
|**Control ID or Menu Handle**|If the window being displayed is a child window, the Control ID label is displayed. Control ID is an integer that identifies this child window's control ID. If the window being displayed is not a child window, the Menu Handle label is displayed. Menu Handle is an integer that identifies the handle of the menu associated with this window.|  
|**User Data**|Application-specific data that is attached to this window structure.|  
|**Window Bytes**|The number of extra bytes associated with this window. The meaning of these bytes is determined by the application. Expand the list box to see the byte values in DWORD format.|