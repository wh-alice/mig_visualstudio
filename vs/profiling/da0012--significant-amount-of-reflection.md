---
title: "DA0012: Significant amount of Reflection"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.performance.rules.DAReflection"
  - "vs.performance.12"
  - "vs.performance.rules.DA0012"
  - "vs.performance.DA0011"
ms.assetid: c92a1d76-21fa-426e-8b1b-a3c08e9bcbca
caps.latest.revision: 13
ms.author: "mikejo"
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
# DA0012: Significant amount of Reflection
|||  
|-|-|  
|Rule Id|DA0012|  
|Category|.NET Framework Usage|  
|Profiling methods|Sampling|  
|Message|You may be using Reflection excessively. It is an expensive operation.|  
|Rule type|Warning|  
  
## Cause  
 Calls to the System.Reflection methods such as InvokeMember and GetMember or to Type methods such as MemberInvoke are a significant proportion of the profiling data. When possible, consider replacing these methods with early binding to the methods of dependent assemblies.  
  
## Rule Description  
 Reflection is a flexible facility of the .NET Framework that can be used to perform late binding of your application to a dependent run-time Assembly or to create and dynamically execute new types during run-time. However, these techniques can decrease performance if they are used frequently or called in tight loops.  
  
 For more information, see the [Reflection and Late Binding](http://go.microsoft.com/fwlink/?LinkId=177826) section of Chapter 5 — Improving Managed Code Performance in the Improving .NET Application Performance and Scalability volume of the Microsoft Patterns and Practices library on MSDN.  
  
## How to Investigate a Warning  
 Double-click the message in the Errors List window to navigate to the [Function Details View](../profiling/function-details-view.md) of the profiling data. Examine the calling functions of the System.Type or System.Reflection method to find the sections of the program that make the most frequent use of .NET Reflection APIs. Avoid using methods that return metadata. When the performance of your application is critical, you might need to avoid using late binding and creating types dynamically at run-time.