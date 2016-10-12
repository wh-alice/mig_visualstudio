---
title: "Troubleshooting Exceptions: System.ServiceModel.Persistence.InstanceNotFoundException"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "InstanceNotFoundException exception"
  - "System.ServiceModel.Persistence.InstanceNotFoundException exception"
ms.assetid: e3905352-dff0-41d4-b970-8e1b26d85a83
caps.latest.revision: 6
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
# Troubleshooting Exceptions: System.ServiceModel.Persistence.InstanceNotFoundException
An \<xref:System.ServiceModel.Persistence.InstanceNotFoundException> exception is thrown under the following circumstances:  
  
-   An operation is performed on a durable service instance that has been marked for completion.  
  
-   A persistence provider created by a \<xref:System.ServiceModel.Persistence.SqlPersistenceProviderFactory> attempts to lock, unlock, or otherwise process state data that is not found in the database.  
  
## See Also  
 \<xref:System.ServiceModel.Persistence.InstanceNotFoundException>   
 [Use the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)