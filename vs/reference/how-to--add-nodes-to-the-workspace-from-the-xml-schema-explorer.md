---
title: "How to: Add Nodes to the Workspace from the XML Schema Explorer"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 3b5a5749-9693-4b29-b0c2-8e07e0e55514
caps.latest.revision: 3
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
# How to: Add Nodes to the Workspace from the XML Schema Explorer
This topic explains how to add nodes to the [XML Schema Designer workspace](../reference/xml-schema-designer-workspace.md) from the XML Schema Explorer. This can be achieved by dragging and dropping nodes from the XML Schema Explorer onto an XSD Designer view, or by using the XML Schema Explorer's context menu. You can also add nodes that are highlighted as a result of a search performed by the XML Schema Explorer. For more information, see [How to: Add Schema Set Search Result Nodes to the Workspace](../reference/how-to--add-schema-set-search-result-nodes-to-the-workspace.md).  
  
> [!NOTE]
>  Only global nodes can be added to the [XML Schema Designer Workspace](../reference/xml-schema-designer-workspace.md).  
  
### To add nodes through the XML Explorer Context Menu  
  
1.  Follow the steps in [How to: Create and Edit an XSD Schema File](../reference/how-to--create-and-edit-an-xsd-schema-file.md).  
  
2.  Right click on the `PurchaseOrderType` node in the a XSD Explorer. Select **Show in Graph View**.  
  
     The `purchaseOrderType` node appears on the design surface of the Graph View.  
  
### To drag and drop a node on to a view  
  
1.  Right click on the `PurchaseOrderType` node in the Graph View. Select **Show in XML Schema Explorer**.  
  
     The node is highlighted in the XML Schema Explorer.  
  
2.  Right click on the `PurchaseOrderType` node in the XML Schema Explorer and select **Show All References**.  
  
     The `purchaseOrder` node is highlighted.  
  
3.  Drag the `purchaseOrder` node on to the Graph View.  
  
     The `purchaseOrder` node and the `PurchaseOrderType` node appear next to each other on the design surface of the Graph View. Because the two nodes are realted (the `purchaseOrder` element is of the `PurchaseOrderType` type), an arrow is drawn between them.  
  
### To add nodes using the Schema Explorer search capability  
  
1.  Type "purchaseOrder" in the search text box of the [XML Explorer](../reference/xml-schema-explorer.md) toolbar and click on the search button.  
  
     ![XML Schema Explorer Keyword Search](../reference/media/schemaexplorersearch.gif "SchemaExplorerSearch")  
  
     The search results are highlighted in the XML Schema Explorer and marked by ticks on the vertical scroll bar.  
  
2.  Add the search results to the workspace by clicking the **Add highlighted nodes to Workspace** button on the summary results pane.  
  
     ![XML Schema Explorer Search Result](../reference/media/schemaexplorersearchresult.gif "SchemaExplorerSearchResult")  
  
     The `purchaseOrder` node and the `PurchaseOrderType` node appear next to each other on the design surface of the [Graph View](../reference/graph-view.md). Because the two nodes are related (the `purchaseOrder` element is of the `PurchaseOrderType` type), an arrow is drawn between them.  
  
## See Also  
 [XML Schema Explorer](../reference/xml-schema-explorer.md)