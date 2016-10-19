---
title: "Error: The Web Server Has Been Locked Down and Is Blocking the DEBUG Verb"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.error.webdbg_debug_verb_blocked"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "debugger, Web application errors"
ms.assetid: 9c8c4812-17db-484d-9c1b-ffd9e3bfef5a
caps.latest.revision: 10
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
# Error: The Web Server Has Been Locked Down and Is Blocking the DEBUG Verb
Stepping into a Web application or XML Web service failed because the IIS lockdown tool has been run and URLScan has been installed and activated. This condition blocks IIS from receiving the DEBUG verb.  
  
 URLScan is a security tool that works in conjunction with the IIS Lockdown Tool to give IIS Web site administrators the ability to turn off unnecessary features and restrict the type of HTTP requests that the server will process. By blocking specific HTTP requests, the URLScan security tool prevents potentially harmful requests from reaching the server and causing damage.  
  
 If your application is running on IIS 6.0 on Windows Server 2003, you need not run the IIS Lockdown tool because IIS 6.0 provides the same functionality.  
  
### To enable debugging on a Web server with URLScan installed  
  
1.  Locate the Urlscan.ini file. Normally, you will find it in a directory that looks something like this:  
  
     C:\WINNT\System32\Inetsrv\urlscan  
  
2.  Create a copy of the file, and name it **Urlscan.old**.  
  
3.  Open the original copy of the Urlscan.ini file using Notepad or the text editor of your choice.  
  
4.  In Urlscan.ini, locate the [AllowVerbs] section. Add DEBUG to the [AllowVerbs] section. If you see ;DEBUG in the [AllowVerbs] section, remove the semicolon to uncomment the verb.  
  
5.  Locate the [DenyVerbs] section. If DEBUG appears in the [DenyVerbs] section, remove it.  
  
6.  Save the file.  
  
7.  Restart the server or restart IIS.  
  
## See Also  
 [Debugging Web Applications: Errors and Troubleshooting](../debugger/debugging-web-applications--errors-and-troubleshooting.md)   
 [Error: The Web Server Could Not Find the Requested Resource](../debugger/error--the-web-server-could-not-find-the-requested-resource.md)