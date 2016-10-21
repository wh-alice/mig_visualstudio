---
title: "The property &lt;property name&gt; cannot be deleted"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 55873f74-7834-4ec1-8815-eeeb65618d87
caps.latest.revision: 2
ms.author: "mblome"
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
# The property &lt;property name&gt; cannot be deleted
The property \<property name> cannot be deleted because it is set as the Discriminator Property for the inheritance between \<class name> and \<class name>  
  
 The selected property is set as the **Discriminator Property** for the inheritance between the classes indicated in the error message. Properties cannot be deleted if they are participating in the inheritance configuration between data classes.  
  
 Set the **Discriminator Property** to a different property of the data class to enable successful deletion of the desired property.  
  
### To correct this error  
  
1.  In the O/R Designer, select the inheritance line that connects the data classes indicated in the error message.  
  
2.  Set the **Discriminator** Property to a different property.  
  
3.  Try to delete the property again.  
  
## See Also  
 [How to: Configure inheritance by using the O/R Designer](../data-tools/how-to--configure-inheritance-by-using-the-o-r-designer.md)   
 [Data class inheritance (O/R Designer)](../data-tools/data-class-inheritance--o-r-designer-.md)   
 [Walkthrough: Creating LINQ to SQL Classes by Using Single-Table Inheritance (O/R Designer)](../data-tools/63bc6328-e0df-4655-9ce3-5ff74dbf69a4.md)