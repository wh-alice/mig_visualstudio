---
title: "Save a dataset as XML"
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
  - "XML [Visual Basic], datasets"
  - "data [Visual Studio], saving as XML"
  - "datasets [Visual Basic], saving as XML"
  - "saving data"
ms.assetid: 68b8327c-ae05-49ff-b9ba-99183e70b52c
caps.latest.revision: 11
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
# Save a dataset as XML
The XML data in a dataset can be accessed by calling the available XML methods  on the dataset. To save the data in XML format, you can call either the <xref:System.Data.DataSet.GetXml*> method or the <xref:System.Data.DataSet.WriteXml*> method of a <xref:System.Data.DataSet>.  
  
 Calling the <xref:System.Data.DataSet.GetXml*> method returns a string that contains the data from all data tables in the dataset that's formatted as XML.  
  
 Calling the <xref:System.Data.DataSet.WriteXml*> method sends the XML-formatted data to a file that  you specify.  
  
### To save the data in a dataset as XML to a variable  
  
-   The <xref:System.Data.DataSet.GetXml*> method returns a <xref:System.String>.This means that you declare a variable of type <xref:System.String> and assign it the results of the <xref:System.Data.DataSet.GetXml*> method.  
  
     [!code[VbRaddataSaving#12](../datatools/codesnippet/VisualBasic/save-a-dataset-as-xml_1.vb)]
[!code[VbRaddataSaving#12](../datatools/codesnippet/CSharp/save-a-dataset-as-xml_1.cs)]  
  
### To save the data in a dataset as XML to a file  
  
-   The <xref:System.Data.DataSet.WriteXml*> method has several overloads. The following code shows how to save the data to a file.Declare a variable and assign it a valid path to save the file to.  
  
     [!code[VbRaddataSaving#13](../datatools/codesnippet/VisualBasic/save-a-dataset-as-xml_2.vb)]
[!code[VbRaddataSaving#13](../datatools/codesnippet/CSharp/save-a-dataset-as-xml_2.cs)]  
  
## See Also  
 [Save data back to the database](../datatools/save-data-back-to-the-database.md)