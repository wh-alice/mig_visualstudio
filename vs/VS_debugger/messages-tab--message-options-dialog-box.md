---
title: "Messages Tab, Message Options Dialog Box"
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
  - "message options, Messages"
ms.assetid: fb9fa211-e82c-40a5-9e4b-ba8de07313c0
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
# Messages Tab, Message Options Dialog Box
Use the **Messages** tab to select which message types to list in [Messages View](../VS_debugger/messages-view.md), and to specify message search criteria. To display the [Message Options Dialog Box](../VS_debugger/message-options-dialog-box.md), choose **Log Messages** from the **Spy** menu.  
  
 Typically, you first select **Message Groups**, and then fine-tune the selection by selecting individual **Messages to View**. The **All** button selects all message types, and the **None** button clears all types.  
  
 The following settings are available on the **Messages** tab:  
  
 **Messages to View**  
 Select specific messages for viewing. When you create a new Messages window, it can display all messages. When you filter messages from the **Messages** tab, that filter only applies to new messages, not messages that have already been displayed in the Windows view.  
  
 **Message Groups**  
 Select message groups for viewing. The available groups include:  
  
-   WM_USER: with a code greater than or equal to WM_USER  
  
-   Registered: registered with the **RegisterWindowMessage** call  
  
-   Unknown: unknown messages in the range 0 to (WM_USER – 1)  
  
 Note that these **Message Groups** do not map to specific entries under **Messages To View**. When you select a group, the selection is applied directly to the message stream.  
  
 A grayed check box within **Message Groups** indicates that the **Messages To View** list box has been modified for messages in that group; not all of the message types in that group are selected.  
  
 **Save Settings as Default**  
 Save the current settings for later use as message search options. These settings are also saved when exiting Spy++.