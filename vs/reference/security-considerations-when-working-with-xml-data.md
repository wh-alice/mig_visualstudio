---
title: "Security Considerations when Working with XML Data | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fce2b708-1aef-454f-be59-52b76f359351
caps.latest.revision: 2
ms.author: "kempb"
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
# Security Considerations when Working with XML Data
This topic discusses security issues that you need to know about when working with the XML Editor or the XSLT debugger.  
  
## XML Editor  
 The XML Editor is based on the Visual Studio Text Editor. It relies on the <xref:System.Xml> and <xref:System.Xml.Xsl> classes to handle many of the XML processes.  
  
-   XSLT transformations are executed in a new application domain. The XSLT transformations are *sandboxed*; that is, the code access security policy of your computer is used to determine the restricted permissions based on where the XSLT style sheet is located. For example, style sheets from an Internet location have the most restricted permissions, whereas style sheets copied to your hard drive run with Full Trust.  
  
-   The <xref:System.Xml.Xsl.XslCompiledTransform> class is used to compile the XSLT to Microsoft intermediate language for faster performance during execution.  
  
-   Schemas that point to an external location in the catalog file are automatically downloaded when the XML Editor first loads. The <xref:System.Xml.Schema.XmlSchemaSet> class is used to compile the schemas. The catalog file that ships with the XML Editor does not have links to any external schemas. The user has to explicitly add a reference to the external schema before the XML Editor downloads the schema file. HTTP downloading can be disabled via the **Miscellaneous Tools Options** page for the XML Editor.  
  
-   The XML Editor uses the <xref:System.Net> classes to download schemas  
  
## XSLT Debugger  
 The XSLT debugger utilizes the Visual Studio managed debug engine and classes from the <xref:System.Xml> and <xref:System.Xml.Xsl> namespace.  
  
-   The XSLT debugger runs each XSLT transformation in a sandboxed application domain. The code access security policy of your computer is used to determine the restricted permissions based on where the XSLT style sheet is located. For example, style sheets from an Internet location have the most restricted permissions, whereas style sheets copied to your hard drive run with Full Trust.  
  
-   The XSLT style sheet is compiled using the <xref:System.Xml.Xsl.XslCompiledTransform> class.  
  
-   The XSLT expression evaluator is loaded by the managed debug engine. The managed debug engine assumes that all code is run from the user's local computer. Accordingly, the <xref:System.Xml.Xsl.XslCompiledTransform> class downloads the XSLT file to the user's local computer. The possibility that an elevation in execution privilege could occur is mitigated by executing all XSLT transformations in a new application domain with restricted permissions  
  
## See Also  
 [Application Domains](http://msdn.microsoft.com/en-us/39e57d07-a740-4cd4-ae82-e119ea3856c1)