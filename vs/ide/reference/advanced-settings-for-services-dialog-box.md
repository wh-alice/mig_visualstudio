---
title: "Advanced Settings for Services Dialog Box | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.ProjectPropertiesAdvancedServices"
helpviewer_keywords: 
  - "Advanced Settings for Services dialog box"
ms.assetid: 6dde4a2d-85e1-4275-aa55-24b84111be91
caps.latest.revision: 14
author: "kempb"
ms.author: "kempb"
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
# Advanced Settings for Services Dialog Box
Client application services provide simplified access to [!INCLUDE[ajax_current_short](../../ide/reference/includes/ajax_current_short_md.md)] login, roles, and profile services from Windows Forms and Windows Presentation Foundation (WPF) applications. You can use the **Services** page in the **Project Designer** to configure client application services. For more information about the **Services** page, see [Services Page, Project Designer](../../ide/reference/services-page-project-designer.md).  
  
 Use the **Advanced Settings for Services** dialog box of the **Services** page in the **Project Designer** to configure advanced settings for client application services. By using these settings, you can override some default application service behaviors to enable less common scenarios. For more information, see [Client Application Services](http://msdn.microsoft.com/en-us/Library/1487d8df-089e-4f21-abfb-a791a652b58e).  
  
 To access the **Advanced Settings for Services** dialog box, select a project node in **Solution Explorer**, and then click **Properties** on the **Project** menu. When the **Project Designer** appears, click the **Services** tab, and then click the **Advanced** button. This button will be disabled until you enable client application services.  
  
## Task List  
 [How to: Configure Client Application Services](http://msdn.microsoft.com/en-us/Library/34a8688a-a32c-40d3-94be-c8e610c6a4e8)  
  
 [How to: Work Offline with Client Application Services](http://msdn.microsoft.com/en-us/f792cb16-8520-4a0f-9dc9-07bfbc454e38)  
  
## UIElement List  
 **Save password hash locally to enable offline login**  
 Specifies whether an encrypted form of the user's password will be cached locally to enable the user to log in when the application is in offline mode. For more information, see [How to: Work Offline with Client Application Services](http://msdn.microsoft.com/en-us/f792cb16-8520-4a0f-9dc9-07bfbc454e38). This option is selected by default.  
  
 **Require users to log on again whenever the server cookie expires**  
 Specifies whether previously authenticated users are automatically reauthenticated when your application accesses the roles or profile service and the server authentication cookie has expired. Select this option to deny access to the application services and require explicit reauthentication after the cookie expires. This is useful for applications deployed in public locations to make sure that users who leave the application running after use will not remain authenticated indefinitely. This option is cleared by default.  
  
 **Role service cache timeout**  
 Specifies the amount of time the client role provider will use cached role values instead of accessing the roles service. Set this time interval to a small value when roles are updated frequently or to a larger value when roles are updated infrequently. The default value is one day.  
  
 The role provider accesses the cached role values or the roles service when you call the <xref:System.Web.Security.RolePrincipal.IsInRole%2A> method. To programmatically clear the cache and force this method to access the remote service, call the <xref:System.Web.ClientServices.Providers.ClientRoleProvider.ResetCache%2A> method.  
  
 **Use custom connection string**  
 Specifies whether the client service providers will use a custom data store for the local cache. By default, the service providers will use the local file system for the cache. Selecting this option will automatically populate the text box with a default connection string. You can keep the default connection string to automatically generate and use a SQL Server Compact Edition database, or you can specify a connection string to an existing SQL Server database. For more information, see [How to: Configure Client Application Services](http://msdn.microsoft.com/en-us/Library/34a8688a-a32c-40d3-94be-c8e610c6a4e8). This option is cleared by default.  
  
## See Also  
 [Client Application Services](http://msdn.microsoft.com/en-us/Library/1487d8df-089e-4f21-abfb-a791a652b58e)   
 [Services Page, Project Designer](../../ide/reference/services-page-project-designer.md)   
 [How to: Configure Client Application Services](http://msdn.microsoft.com/en-us/Library/34a8688a-a32c-40d3-94be-c8e610c6a4e8)   
 [How to: Work Offline with Client Application Services](http://msdn.microsoft.com/en-us/f792cb16-8520-4a0f-9dc9-07bfbc454e38)