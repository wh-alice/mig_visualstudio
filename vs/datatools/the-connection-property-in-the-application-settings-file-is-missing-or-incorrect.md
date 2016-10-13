---
title: "The connection property in the Application Settings file is missing or incorrect"
ms.custom: na
ms.date: "10/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 77724510-ff59-4d43-b933-a0434e1ac597
caps.latest.revision: 4
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
# The connection property in the Application Settings file is missing or incorrect
The connection property in the Application Settings file is missing or incorrect. The connection string from the .dbml file has been used in its place.  
  
 The .dbml file contains a reference to a connection string in the application settings file that cannot be found. This message is informational; the connection string setting will be created when **OK** is clicked.  
  
### To respond to this message  
  
-   Click **OK**. The connection information that is contained in the .dbml file is added to application settings.  
  
## See Also  
 [LINQ to SQL Tools in Visual Studio](../datatools/linq-to-sql-tools-in-visual-studio2.md)   
 [Walkthrough: Creating LINQ to SQL Classes (O-R Designer)](../Topic/Walkthrough:%20Creating%20LINQ%20to%20SQL%20Classes%20\(O-R%20Designer\).md)   
 [NIB: How to: Add or Remove Application Settings](http://msdn.microsoft.com/a233965c-126d-46ab-add4-efb758f576f4)   
 [LINQ to SQL](../Topic/LINQ%20to%20SQL.md)