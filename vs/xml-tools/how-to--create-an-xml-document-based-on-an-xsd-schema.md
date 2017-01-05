---
title: "How to: Create an XML Document Based on an XSD Schema"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 193b195f-e918-4c79-a1a1-8096a1433bde
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
# How to: Create an XML Document Based on an XSD Schema
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

The **Generate Sample XML** feature generates a sample XML file based on your XML Schema (XSD) file.  
  
 You can use this option for the following scenarios:  
  
-   To understand the use of various constructs in your schema.  
  
-   To confirm that the schema does what it is intended to do.  
  
 The **Generate Sample XML** feature is only available on global elements, and requires a valid XML schema set.  
  
 This feature typically generates valid XML documents. However, if the schema contains one or more of the following, the sample might not be valid:  
  
-   The `xs:key`, `xs:keyref`, and `xs:unique` identity constraints.  
  
-   `xs:pattern` facets.  
  
-   Enumerations of the `xs:QName` type.  
  
-   `xs:ENTITY`, `xs:ENTITIES`, and `xs:NOTATION` types.  
  
 Also, note that `xs:base64Binary` content will be generated only if enumerations occur in the schema for that type.  
  
### To generate an XML instance document based on the XSD file  
  
1.  Follow the steps in [How to: Create and Edit an XSD Schema File](../xml-tools/how-to--create-and-edit-an-xsd-schema-file.md).  
  
2.  In the [XML Schema Explorer](../xml-tools/xml-schema-explorer.md), right-click the `PurchaseOrder` global element. Select **Generate Sample XML**.  
  
     When you select this option, the PurchaseOrder.xml file with the following sample XML content will be generated and opened in the XML Editor:  
  
    ```  
    <?xml version="1.0" encoding="utf-8"?>  
    <PurchaseOrder OrderDate="1900-01-01" xmlns="http://tempuri.org/PurchaseOrderSchema.xsd">  
      <ShipTo country="US">  
        <name>name1</name>  
        <street>street1</street>  
        <city>city1</city>  
        <state>state1</state>  
        <zip>1</zip>  
      </ShipTo>  
      <ShipTo country="US">  
        <name>name2</name>  
        <street>street2</street>  
        <city>city2</city>  
        <state>state2</state>  
        <zip>-79228162514264337593543950335</zip>  
      </ShipTo>  
      <BillTo country="US">  
        <name>name1</name>  
        <street>street1</street>  
        <city>city1</city>  
        <state>state1</state>  
        <zip>1</zip>  
      </BillTo>  
    </PurchaseOrder>  
    ```  
  
## See Also  
 [Working with XML Data](../xml-tools/working-with-xml-data.md)