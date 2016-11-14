---
title: "Troubleshooting Exceptions: System.Net.Sockets.SocketException | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "SocketException class"
ms.assetid: 89e8194d-83b0-450f-91f5-548e5c13944d
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Troubleshooting Exceptions: System.Net.Sockets.SocketException
A <xref:System.Net.Sockets.SocketException> exception is thrown by the <xref:System.Net.Sockets.Socket> and <xref:System.Net.Dns> classes when an error occurs with the network.  
  
## Associated Tips  
 **Check the Errorcode property to determine why the socket error occurred.**  
 The default constructor for the <xref:System.Net.Sockets.SocketException> class sets the <xref:System.Net.Sockets.SocketException.ErrorCode%2A> property to the last operating-system socket error that occurred.  
  
## See Also  
 <xref:System.Net.Sockets.SocketException>   
 [Use the Exception Assistant](http://msdn.microsoft.com/en-us/Library/e0a78c50-7318-4d54-af51-40c00aea8711)   
 [Using Secure Sockets Layer](http://msdn.microsoft.com/en-us/Library/6e4289e6-d1b7-4e82-ab0d-e83e3b6063ed)