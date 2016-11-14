---
title: "Troubleshooting Exceptions: System.Data.NoNullAllowedException | Microsoft Docs"
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
  - "NoNullAllowedException class"
ms.assetid: 1ab87572-007f-4b84-bb13-c3626e7f89cd
caps.latest.revision: 15
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
# Troubleshooting Exceptions: System.Data.NoNullAllowedException
A <xref:System.Data.NoNullAllowedException> exception is thrown when there is an attempt to insert a null value into a column where <xref:System.Data.DataColumn.AllowDBNull%2A> is set to `false`.  
  
## Associated Tips  
 **Check to determine if the value is DBNull before adding it to the column.**  
 If <xref:System.Data.DataColumn.AllowDBNull%2A> is set to `false`, you will not be able to insert a null value. For more information, see <xref:System.DBNull>.  
  
 **Set AllowDBNull to true.**  
 Setting this property to `true` will allow you to inset null values. For more information, see <xref:System.Data.DataColumn.AllowDBNull%2A>.  
  
## Remarks  
 If you use the navigation buttons to move through the records of a database table on a data form, this exception may be thrown with the additional information, "Column 'Column' does not allow nulls." This behavior occurs because the primary key or the "not NULL" column of the database table was not selected in the Data Form Wizard. If the primary key or the "not NULL" column of the database is not selected in the Data Form Wizard when you create the data form, the **Add- Creates a new record** option is not disabled. To work around this problem, select the following columns of the selected table when you add a data form by using the Data Form Wizard: the primary column and a column that does not permit NULLs.  
  
## See Also  
 <xref:System.Data.NoNullAllowedException>   
 <xref:System.Data.DataRowCollection.Add%2A>   
 <xref:System.Data.DataRow.EndEdit%2A>   
 <xref:System.Data.DataRow.ItemArray%2A>   
 <xref:System.Data.DataTable.LoadDataRow%2A>   
 [Use the Exception Assistant](http://msdn.microsoft.com/en-us/Library/e0a78c50-7318-4d54-af51-40c00aea8711)