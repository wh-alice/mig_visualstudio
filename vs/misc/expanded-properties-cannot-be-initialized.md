---
title: "Expanded properties cannot be initialized"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc36714"
  - "bc36714"
helpviewer_keywords: 
  - "BC36714"
ms.assetid: ba9408f3-e606-4749-8372-987999f405f5
caps.latest.revision: 4
ms.author: "shoag"
manager: "wpickett"
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
# Expanded properties cannot be initialized
An auto-implemented property can be initialized as part of its declaration, but an expanded property cannot be.  
  
 **Error ID:** BC36714  
  
### To correct this error  
  
-   Either use an auto-implemented property or remove the initialization from the property declaration.  
  
## Example  
 The following examples show both auto-implemented and expanded properties. Auto-implemented properties can be initialized by using assignment or a `New` clause, but expanded properties cannot be.  
  
```vb#  
Class AutoImplementedExample  
    ' An auto-implemented property can be assigned an initial value.  
    Property IDNum As Integer = 33542  
    ' An auto-implemented property can be initialized with New.  
    Property Name As New String("Don Hall")  
End Class  
  
Class ExpandedExample  
    ' Attempting to expand an initialized auto-implemented property  
    ' causes this error.  
    'Property IDNum As Integer = 33542  
    '    Get  
    '    End Get  
    '    Set(ByVal value As Integer)  
    '    End Set  
    'End Property  
  
    ' Instead, you can assign the initial value to the backing field.  
    Private _IDNum As Integer = 33542  
    Property IDNum As Integer  
        Get  
        End Get  
        Set(ByVal value As Integer)  
        End Set  
    End Property  
End Class  
```  
  
## See Also  
 [Auto-Implemented Properties](../Topic/Auto-Implemented%20Properties%20\(Visual%20Basic\).md)   
 [How to: Create a Property](../Topic/How%20to:%20Create%20a%20Property%20\(Visual%20Basic\).md)   
 [Property Procedures](../Topic/Property%20Procedures%20\(Visual%20Basic\).md)