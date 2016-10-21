---
title: "Edit data in datasets | hehe"
ms.custom: ""
ms.date: "10/18/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "aspx"
helpviewer_keywords: 
  - "datasets [Visual Basic], editing data"
  - "data [Visual Studio], editing in datasets"
ms.assetid: 50d5c580-fbf7-408f-be70-e63ac4f4d0eb
caps.latest.revision: 15
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
# Edit data in datasets
You edit data in data tables much like you edit the data in a table in any database. The process can include inserting, updating, and deleting records in the table. In a data-bound form, you can specify which fields are user-editable. In those cases, the data-binding infrastructure handles all the change tracking so that the changes can be sent back to the database later. If you programmatically make edits to data, and you intend to send those changes back to the database, you must use the objects and methods that do the change tracking for you.  
  
 In addition to changing the actual data, you can also query a <xref:System.Data.DataTable> to return specific rows of data. For example, you might query for individual rows, specific versions of rows (original and proposed),  rows that have changed, or rows that have errors.  
  
## To edit rows in a dataset  
 To edit an existing row in a <xref:System.Data.DataTable>, you need to locate the <xref:System.Data.DataRow> you want to edit, and then assign the updated values to the desired columns.  
  
 If you don't know the index of the row you want to edit, use the `FindBy` method to search by the primary key:  
  
 [!code[VbRaddataEditing#3](../data-tools/codesnippet/CSharp/edit-data-in-datasets_1.cs)]
[!code[VbRaddataEditing#3](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_1.vb)]  
  
 If you know the row index, you can access and edits rows as follows:  
  
 [!code[VbRaddataEditing#5](../data-tools/codesnippet/CSharp/edit-data-in-datasets_2.cs)]
[!code[VbRaddataEditing#5](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_2.vb)]  
  
## To insert new rows into a dataset  
 Applications that use data-bound controls typically add new records through the **Add New** button on a [BindingNavigator Control](../Topic/BindingNavigator%20Control%20\(Windows%20Forms\).md).  
  
 To manually add new records to a dataset, create a new data row by calling the method on the DataTable. Then add the row to the <xref:System.Data.DataRow> collection (<xref:System.Data.DataTable.Rows*>) of the <xref:System.Data.DataTable>:  
  
 [!code[VbRaddataEditing#1](../data-tools/codesnippet/CSharp/edit-data-in-datasets_3.cs)]
[!code[VbRaddataEditing#1](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_3.vb)]  
  
 In order to retain the information that the dataset needs to send updates to the data source, use the <xref:System.Data.DataRow.Delete*> method to remove rows in a data table. For example, if your application uses a TableAdapter (or <xref:System.Data.Common.DataAdapter>), the TableAdapter's `Update` method deletes rows in the database that have a <xref:System.Data.DataRow.RowState*> of <xref:System.Data.DataRowState>.  
  
 If your application does not need to send updates back to a data source, then it's possible to remove records by directly accessing the data row collection (<xref:System.Data.DataRowCollection.Remove*>).  
  
#### To delete records from a data table  
  
-   Call the <xref:System.Data.DataRow.Delete*> method of a <xref:System.Data.DataRow>.  
  
     This method doesn't physically remove the record. Instead, it marks the record for deletion.  
  
    > [!NOTE]
    >  If you get the count property of a <xref:System.Data.DataRowCollection>, the resulting count includes records that have been marked for deletion. To get an accurate count of records that aren't marked for deletion, you can loop through the collection looking at the <xref:System.Data.DataRow.RowState*> property of each record. (Records marked for deletion have a <xref:System.Data.DataRow.RowState*> of <xref:System.Data.DataRowState>.) Alternatively, you can create a data view of a dataset that filters based on row state and get the count property from there.  
  
     The following example shows how to call the <xref:System.Data.DataRow.Delete*> method to mark the first row in the `Customers` table as deleted:  
  
     [!code[VbRaddataEditing#8](../data-tools/codesnippet/CSharp/edit-data-in-datasets_4.cs)]
[!code[VbRaddataEditing#8](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_4.vb)]  
  
## Determine if there are changed rows  
 When changes are made to records in a dataset, information about those changes is stored until you commit them. You commit the changes  when you call the `AcceptChanges` method of a dataset or data table, or when you call the `Update` method of a TableAdapter or data adapter.  
  
 Changes are tracked two ways in each data row:  
  
-   Each data row contains information related to it's <xref:System.Data.DataRow.RowState*> (for example, <xref:System.Data.DataRowState>, <xref:System.Data.DataRowState>, <xref:System.Data.DataRowState>, or <xref:System.Data.DataRowState>).  
  
-   Each changed data row contains multiple versions of that row (<xref:System.Data.DataRowVersion>), the original version (before changes), and the current version (after changes). During the period when a change is pending (the time when you can respond to the <xref:System.Data.DataTable.RowChanging> event), a third version — the proposed version— is available as well. For more information, see [How to: Get Specific Versions of a DataRow](../data-tools/how-to--get-specific-versions-of-a-datarow.md).  
  
 The <xref:System.Data.DataSet.HasChanges*> method of a dataset returns `true` if changes have been made in the dataset. After determining that changed rows exist, you can call the `GetChanges` method of a <xref:System.Data.DataSet> or <xref:System.Data.DataTable> to return a set of changed rows. For more information, see [How to: Retrieve Changed Rows](../Topic/How%20to:%20Retrieve%20Changed%20Rows.md).  
  
#### To determine if changes have been made to any rows  
  
-   Call the <xref:System.Data.DataSet.HasChanges*> method of a dataset to check for changed rows.  
  
     The following example shows how to check the return value from the <xref:System.Data.DataSet.HasChanges*> method to detect whether there are any changed rows in a dataset named `NorthwindDataset1`:  
  
     [!code[VbRaddataEditing#12](../data-tools/codesnippet/CSharp/edit-data-in-datasets_5.cs)]
[!code[VbRaddataEditing#12](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_5.vb)]  
  
## Determine the type of changes  
 You can also check to see what type of changes were made in a dataset by passing a value from the <xref:System.Data.DataRowState> enumeration to the <xref:System.Data.DataSet.HasChanges*> method.  
  
#### To determine what type of changes have been made to a row  
  
-   Pass a <xref:System.Data.DataRowState> value to the <xref:System.Data.DataSet.HasChanges*> method.  
  
     The following example shows how to check a dataset named `NorthwindDataset1` to determine if any new rows have been added to it:  
  
     [!code[VbRaddataEditing#13](../data-tools/codesnippet/CSharp/edit-data-in-datasets_6.cs)]
[!code[VbRaddataEditing#13](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_6.vb)]  
  
## To locate rows that have errors  
 When working with individual columns and rows of data, you might encounter errors. You can check the `HasErrors` property to determine if errors exist in a <xref:System.Data.DataSet>, <xref:System.Data.DataTable>, or <xref:System.Data.DataRow>.  
  
1.  Check the `HasErrors` property to see if there are any errors in the dataset.  
  
2.  If the `HasErrors` property is `true`, iterate through the collections of tables, and then the through the rows, to find the row with the error.  
  
     [!code[VbRaddataEditing#23](../data-tools/codesnippet/CSharp/edit-data-in-datasets_7.cs)]
[!code[VbRaddataEditing#23](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_7.vb)]