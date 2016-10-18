---
title: "How to: Change the return type of a DataContext method (O-R Designer)"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: c5b66bff-6dbb-43c0-bffa-317133ca5b9e
caps.latest.revision: 2
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
# How to: Change the return type of a DataContext method (O/R Designer)
The return type of a <xref:System.Data.Linq.DataContext> method (created based on a stored procedure or function) differs depending on where you drop the stored procedure or function in the [!INCLUDE[vs_ordesigner_short](../datatools/includes/vs_ordesigner_short_md.md)]. If you drop an item directly onto an existing entity class, a <xref:System.Data.Linq.DataContext> method that has the return type of the entity class is created (if the schema of the data returned by the stored procedure or function matches the shape of the entity class). If you drop an item onto an empty area of the [!INCLUDE[vs_ordesigner_short](../datatools/includes/vs_ordesigner_short_md.md)], a <xref:System.Data.Linq.DataContext> method that returns an automatically generated type is created. You can change the return type of a <xref:System.Data.Linq.DataContext> method after you add it to the methods pane. To inspect or change the return type of a <xref:System.Data.Linq.DataContext> method, select it and click the **Return Type** property in the **Properties** window.  
  
> [!NOTE]
>  You cannot revert <xref:System.Data.Linq.DataContext> methods that have a return type set to an entity class to return the auto-generated type by using the **Properties** window. To revert a <xref:System.Data.Linq.DataContext> method to return an auto-generated type, you must drag the original database object onto the O/R Designer again.  
  
 [!INCLUDE[note_settings_general](../datatools/includes/note_settings_general_md.md)]  
  
### To change the return type of a DataContext method from the auto-generated type to an entity class  
  
1.  Select the <xref:System.Data.Linq.DataContext> method in the methods pane.  
  
2.  Select **Return Type** in the **Properties** window and then select an available entity class in the **Return Type** list. If the desired entity class is not in the list, add it to or create it in the [!INCLUDE[vs_ordesigner_short](../datatools/includes/vs_ordesigner_short_md.md)] to add it to the list.  
  
3.  Save the .dbml file.  
  
### To change the return type of a DataContext method from an entity class back to the auto-generated type  
  
1.  Select the <xref:System.Data.Linq.DataContext> method in the methods pane and delete it.  
  
2.  Drag the database object from **Server Explorer**/**Database Explorer** onto an empty area of the O/R Designer.  
  
3.  Save the .dbml file.  
  
## See Also  
 [LINQ to SQL Tools in Visual Studio](../datatools/linq-to-sql-tools-in-visual-studio2.md)   
 [LINQ to SQL](../Topic/LINQ%20to%20SQL.md)   
 [DataContext Methods (O/R Designer)](../datatools/datacontext-methods--o-r-designer-.md)   
 [How to: Create DataContext methods mapped to stored procedures and functions (O/R Designer)](../datatools/how-to--create-datacontext-methods-mapped-to-stored-procedures-and-functions--o-r-designer-.md)