---
title: "Event &#39;&lt;eventname&gt;&#39; implicitly declares &#39;&lt;membername&gt;&#39;, which conflicts with a member in the base &lt;type&gt; &#39;&lt;classname&gt;&#39;, and so the event should be declared &#39;Shadows&#39; | Microsoft Docs"
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
  - "bc40012"
  - "vbc40012"
helpviewer_keywords: 
  - "BC40012"
ms.assetid: 5f14e8bd-a227-4115-af99-cd2b6fe4dc0e
caps.latest.revision: 10
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
# Event &#39;&lt;eventname&gt;&#39; implicitly declares &#39;&lt;membername&gt;&#39;, which conflicts with a member in the base &lt;type&gt; &#39;&lt;classname&gt;&#39;, and so the event should be declared &#39;Shadows&#39;
An event is declared with a name that combines to form an implicit member with the same name as a member of the base class. For example, if you declare an event named `Event1`, the compiler generates the implicit procedures `add_Event1` and `remove_Event1`. If the base class has a member with one of these names, the event in this class should shadow the base class member.  
  
 This message is a warning. `Shadows` is assumed by default. For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC40012  
  
### To correct this error  
  
1.  To hide the base class member, add the `Shadows` keyword to the event declaration.  
  
2.  If you do not intend to hide the base class member, change the name of the event.  
  
## See Also  
 [Event Statement](/dotnet/visual-basic/language-reference/statements/event-statement)   
 [Shadows](/dotnet/visual-basic/language-reference/modifiers/shadows)   
 [Shadowing in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/declared-elements/shadowing)