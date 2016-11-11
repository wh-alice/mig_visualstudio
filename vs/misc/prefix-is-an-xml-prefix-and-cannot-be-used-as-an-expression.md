---
title: "&#39;prefix&#39; is an XML prefix and cannot be used as an expression | Microsoft Docs"
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
  - "bc30114"
  - "vbc30114"
helpviewer_keywords: 
  - "BC30114"
ms.assetid: 5cb7c89e-c61b-483a-9369-5285b7cbcf45
caps.latest.revision: 4
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
# &#39;prefix&#39; is an XML prefix and cannot be used as an expression
'prefix' is an XML prefix and cannot be used as an expression. Use the GetXmlNamespace operator to create a namespace object.  
  
 The prefix for an XML namespace that is imported by using the `Imports` statement cannot be used outside an XML literal.  
  
 **Error ID:** BC30114  
  
### To correct this error  
  
-   If you have to refer to part of the imported XML namespace, use the `GetXmlNamespace` operator to retrieve an <xref:System.Xml.Linq.XNamespace> object. Use that object instead of the XML namespace prefix.  
  
-   If you are using the XML namespace prefix to qualify an XML literal, ensure that you are using appropriate syntax for the XML literal.  
  
## See Also  
 [XML Literals](/dotnet/visual-basic/language-reference/xml-literals/index)   
 [Imports Statement (XML Namespace)](/dotnet/visual-basic/language-reference/statements/imports-statement-xml-namespace)   
 [GetXmlNamespace Operator](/dotnet/visual-basic/language-reference/operators/getxmlnamespace-operator)   
 [XML](/dotnet/visual-basic/programming-guide/language-features/xml/index)   
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)