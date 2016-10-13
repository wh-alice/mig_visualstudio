---
title: "XML Document Properties, Properties Window"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 9dbb34d9-02ea-4201-b445-c98a0eb0d6db
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
# XML Document Properties, Properties Window
The **Properties** window provides basic information about the document that is active in the XML Editor. The properties that are available vary depending on the type of XML document that is currently active.  
  
> [!NOTE]
>  All XML document properties are saved in the solution. As a result, you do not have to reenter these values the next time you open the solution.  
  
 **Encoding**  
 The character encoding for the file. Changing this property also changes the encoding attribute on the XML declaration, and vice versa. The new encoding will be used to encode the file when you save the file.  
  
 **Input**  
 The input document associated with the XSLT style sheet. It is used by the **ShowXSLT Output** command. A document can be selected using the browse (**...**) button.  
  
 This property is visible only when an XSLT file is currently active in the Editor window.  
  
 **Output**  
 The file that is generated when transforming an XML document.  
  
 If a file is not specified, a default file name is generated based on the `method` attribute on the `xsl:output` element which determines the file extension. The default file is located in the current user's temporary directory.  
  
 **Schemas**  
 The schemas to use for validation. The button opens the **XSD Schemas** dialog box, which can be used to select the schemas to use.  
  
 You can also enter the path to the schemas. If multiple schemas are specified, each schema path must be enclosed in double quotes.  
  
 **Stylesheet**  
 The XSLT file that is used to transform the document when the **Show XSLT Output** command is used. If this field is blank when the **Show XSLT Output** command is used, the editor uses the value provided in the `xml-stylesheet` processing instruction of the document, or it prompts you for the filename.  
  
 When editing an XSLT file, this property can be used to specify that a different style sheet should be used when the **Show XSLT Output** or **Debug XSLT** command is selected. For example, you may want to do this when you are editing a style sheet that is included in a parent style sheet.  
  
## See Also  
 [XML Editor](../reference/xml-editor.md)   
 [XML Editor Components](../reference/xml-editor-components.md)