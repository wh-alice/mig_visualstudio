---
title: "&#39;NonSerialized&#39; attribute will not affect this member because its containing class is not exposed as &#39;Serializable&#39; | Microsoft Docs"
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
  - "vbc30772"
  - "bc30772"
helpviewer_keywords: 
  - "BC30772"
ms.assetid: 1014e944-40c1-4078-8a38-139736ef89da
caps.latest.revision: 9
author: "stevehoag"
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
# &#39;NonSerialized&#39; attribute will not affect this member because its containing class is not exposed as &#39;Serializable&#39;
By default, classes and their members are non-serializable. The <xref:System.NonSerializedAttribute> attribute is only needed if a member of a serializable class should not be serialized.  
  
 **Error ID:** BC30772  
  
### To correct this error  
  
-   Add the <xref:System.SerializableAttribute> attribute to the class.  
  
     —or—  
  
-   Remove the <xref:System.NonSerializedAttribute> attribute from the member.  
  
## See Also  
 <xref:System.NonSerializedAttribute>   
 <xref:System.SerializableAttribute>   
 [NOT IN BUILD: Attributes in Visual Basic](http://msdn.microsoft.com/en-us/620bfc0e-4582-4c8b-8432-ebc5c3dccc22)