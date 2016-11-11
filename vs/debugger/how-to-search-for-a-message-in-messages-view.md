---
title: "How to: Search for a Message in Messages View | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Message Search dialog box"
  - "Messages view"
  - "messages, searching for"
ms.assetid: 732b7ccc-54ea-41db-823b-2b96e3e4083e
caps.latest.revision: 5
author: "mikejo5000"
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
# How to: Search for a Message in Messages View
You can search for a specific message in Messages view by using its handle, type, or message ID as search criteria. Any one of these — or a combination — will be valid search criteria. The initial direction of the search can also be specified. The fields in the dialog box are preloaded with the attributes of the message currently selected.  
  
### To search for a message in Messages view  
  
1.  Arrange your windows so that Spy++ and an active [Messages View](../debugger/messages-view.md) window are visible.  
  
2.  From the **Search** menu, choose **Find Message**.  
  
     The [Message Search Dialog Box](../debugger/message-search-dialog-box.md) opens.  
  
3.  Drag the **Finder Tool** over the desired window. As you drag the tool, the **Message Search** dialog box displays details on the selected window.  
  
     – or –  
  
     If you have the handle of the window whose messages you want to examine, type it into the **Handle** text box.  
  
     – or –  
  
     If you know the message type and/or message ID you want, select them from the **Type** and **Message** dropdown menus, and clear the **Handle** text box.  
  
4.  Clear any fields for which you do not want to specify values.  
  
    > [!TIP]
    >  To reduce screen clutter, select the **Hide Spy** option. This option conceals the main Spy++ window, leaving only the **Find Window** dialog box visible on top of your other applications. The Spy++ main window is restored when you click **OK** or **Cancel**, or when you clear the **Hide Spy++** option.  
  
5.  Choose **Up** or **Down** for the initial direction of the search.  
  
6.  Click **OK**.  
  
 If a matching message is found, it is highlighted in the Messages view window. See [Messages View](../debugger/messages-view.md).