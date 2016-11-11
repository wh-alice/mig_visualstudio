---
title: "The property &lt;property name&gt; cannot be deleted because it is participating in the association &lt;association name&gt; | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 389873cc-92dd-48da-bfca-0f6c8e0ae3c2
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
# The property &lt;property name&gt; cannot be deleted because it is participating in the association &lt;association name&gt;
The selected property is set as the **Association Property** for the association between the classes indicated in the error message. Properties cannot be deleted if they are participating in an association between data classes.  
  
 Set the **Association Property** to a different property of the data class to enable successful deletion of the desired property.  
  
### To correct this error  
  
1.  Select the association line on the O/R Designer that connects the data classes indicated in the error message.  
  
2.  Double-click the line to open the **Association Editor** dialog box.  
  
3.  Remove the property from the **Association Properties**.  
  
4.  Try to delete the property again.  
  
## See Also  
 [LINQ to SQL Tools in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [How to: Create an association (relationship) between LINQ to SQL classes (O/R Designer)](../data-tools/how-to-create-an-association-relationship-between-linq-to-sql-classes-o-r-designer.md)   
 [Walkthrough: Creating LINQ to SQL Classes (O-R Designer)](../Topic/Walkthrough:%20Creating%20LINQ%20to%20SQL%20Classes%20\(O-R%20Designer\).md)   
 [LINQ to SQL](http://msdn.microsoft.com/en-us/Library/73d13345-eece-471a-af40-4cc7a2f11655)