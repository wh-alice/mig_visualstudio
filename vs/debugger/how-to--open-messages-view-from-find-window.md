---
title: "How to: Open Messages View from Find Window | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Messages View in Spy++, opening"
  - "opening Messages View in Spy++"
ms.assetid: 601a193e-432a-417b-9406-6fec9e401264
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
# How to: Open Messages View from Find Window
You might find it convenient to use the **Find Window** dialog box to select a target window, and then open a Messages view of that window.  
  
### To open a Messages view window using the Find Window dialog box  
  
1.  Arrange your windows so that both Spy++ and the target window are visible.  
  
2.  From the **Spy** menu, choose **Find Window**.  
  
     The [Find Window Dialog Box](../debugger/find-window-dialog-box.md) opens.  
  
3.  From the **Windows** tab, drag the **Finder Tool** over the target window. As you drag the tool, the **Find Window** dialog box displays details on the selected window.  
  
     – or –  
  
     If you have the handle of the window you want to examine (for example, copied from the debugger), you can type it into the **Handle** text box.  
  
4.  Under **Show**, select **Messages**.  
  
5.  Press **OK**.  
  
     A blank [Messages View](../debugger/messages-view.md) window opens, and a **Messages** menu is added to the Spy++ toolbar.  
  
6.  From the **Messages** menu, choose **Logging Options**.  
  
     The [Message Options Dialog Box](../debugger/message-options-dialog-box.md) opens.  
  
7.  Select the options for the messages you want to display.  
  
8.  Press **OK** to begin logging messages.  
  
     Depending upon the options selected, messages begin streaming into the active Messages view window.  
  
9. When you have enough messages, choose **Stop Logging** from the **Messages** menu.