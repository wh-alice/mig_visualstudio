---
title: "Referenced object has a value of &#39;Nothing&#39; | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30760"
  - "vbc30760"
helpviewer_keywords: 
  - "BC30760"
ms.assetid: 7e792fd8-2880-402b-a908-c89e5b028300
caps.latest.revision: 8
ms.author: "billchi"
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
# Referenced object has a value of &#39;Nothing&#39;
The object being used has the value `Nothing`, but a usable value is expected. `Nothing` is a value that indicates that an object has no value, either because no value has been assigned to it, or it was assigned the value `Nothing`.  
  
 **Error ID:** BC30760  
  
### To correct this error  
  
1.  Check the object to make sure it has been declared within the scope of the procedure where the error occurred.  
  
2.  Verify that the value of the object is being set.  
  
    > [!NOTE]
    >  The value `Nothing` is not the same as zero or an empty string. You can use `IsNothing` to check to see if an object contains the value `Nothing`.  
  
## See Also  
 [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: IsNothing Function](http://msdn.microsoft.com/en-us/5b2a4626-e6a9-49d1-b9b1-fcc6a1302319)