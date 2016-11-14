---
title: "The selected connection uses an unsupported database provider | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4d25dfa1-8fa4-4529-9b90-973bc2ec2993
caps.latest.revision: 3
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
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
# The selected connection uses an unsupported database provider
This message appears when you drag items that do not use the .NET Framework Data Provider for SQL Server from **Server Explorer**/**Database Explorer** onto the [LINQ to SQL Tools in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md).  
  
 The [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)] supports only data connections that use the .NET Framework Provider for SQL Server. Only connections to Microsoft SQL Server or Microsoft SQL Server Database File are valid.  
  
### To correct this error  
  
-   Add only items from data connections that use the .NET Framework Data Provider for SQL Server to the [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)].  
  
## See Also  
 <xref:System.Data.SqlClient>   
 [Connecting to Data in Visual Studio](../data-tools/connecting-to-data-in-visual-studio.md)   
 [.NET Framework Data Providers](http://msdn.microsoft.com/en-us/Library/03a9fc62-2d24-491a-9fe6-d6bdb6dcb131)   
 [Walkthrough: Creating LINQ to SQL Classes (O-R Designer)](http://msdn.microsoft.com/en-us/Library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [Creating Data Applications](../data-tools/creating-data-applications.md)