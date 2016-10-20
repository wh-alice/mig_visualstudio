---
title: "Attribute &#39;System.Runtime.InteropServices.DefaultCharSetAttribute&#39; is not supported in this version | Microsoft Docs"
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
  - "bc32510"
  - "vbc32510"
helpviewer_keywords: 
  - "BC32510"
ms.assetid: e2eec233-6e0b-4f2f-a801-b0274e579c0e
caps.latest.revision: 7
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
# Attribute &#39;System.Runtime.InteropServices.DefaultCharSetAttribute&#39; is not supported in this version
The <xref:System.Runtime.InteropServices.DefaultCharSetAttribute?displayProperty=fullName> attribute allows you to specify the character set to be used in marshaled strings. Its value takes a member of the <xref:System.Runtime.InteropServices.CharSet?displayProperty=fullName> enumeration.  
  
 The current version of [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] does not support this attribute. Support is possible in future versions.  
  
 **Error ID:** BC32510  
  
### To correct this error  
  
-   Use each [Declare Statement](../Topic/Declare%20Statement.md) to specify the character set for the external procedure it is declaring. The following example illustrates this.  
  
    ```  
    Ansi Declare Function GetUserName Lib "advapi32.dll" _  
        (ByVal lpBuffer As String, ByRef nSize As Integer) As Integer  
    Unicode Declare Sub externalProc Lib "projectlib.dll" _  
        (ByVal arg As Double)  
    ```  
  
     If you do not specify the character set in the `Declare` statement, it defaults to ANSI.  
  
## See Also  
 <xref:System.Runtime.InteropServices.DefaultCharSetAttribute>   
 <xref:System.Runtime.InteropServices.CharSet>   
 [NOT IN BUILD: Attributes in Visual Basic](http://msdn.microsoft.com/en-us/620bfc0e-4582-4c8b-8432-ebc5c3dccc22)   
 [Declare Statement](../Topic/Declare%20Statement.md)