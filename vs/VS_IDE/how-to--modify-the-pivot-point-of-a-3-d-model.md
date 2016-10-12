---
title: "How to: Modify the Pivot Point of a 3-D Model"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: c20b4ec8-29f5-4ca5-bc39-d4548ca6f573
caps.latest.revision: 14
ms.author: "mithom"
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
# How to: Modify the Pivot Point of a 3-D Model
This document demonstrates how to use the Model Editor to modify the *pivot point* of a 3-D model. The pivot point is the point in space that defines the mathematical center of the object for rotation and scaling.  
  
 This document demonstrates this activity:  
  
-   Modifying the pivot point of an object  
  
## Modifying the pivot point of a 3-D model  
 You can redefine the origin of a 3-D model by modifying its pivot point.  
  
 Make sure that the **Properties** window and the **Toolbox** are displayed.  
  
#### To modify the pivot point of a 3-D model  
  
1.  Begin with an existing 3-D model, such as the one that's described in [How to: Create a Basic 3-D Model](../VS_IDE/how-to--create-a-basic-3-d-model.md).  
  
2.  Enter pivot mode. On the **Model Editor Mode** toolbar, choose the **Pivot Mode** button to activate pivot mode. A box appears around the **Pivot Mode** button to indicate that the Model Editor is now in pivot mode. In pivot mode, operations such as translation affect the pivot point of the object instead of the structure of the object in world-space.  
  
3.  Modify the pivot point of the object. In **Select** mode, select the object, and then on the **Model Viewer** toolbar, choose the **Translate** tool. A box that represents the pivot point appears on the design surface. Move the box to modify the pivot point of the object.  
  
     By moving the box, you can move the pivot point in all three dimensions. To translate the pivot point along one axis, move the arrow that corresponds to that axis. The box and arrows change to a yellow color to indicate the axis that's affected by the translation.  
  
     You can also specify the pivot point by using the **Pivot Translation** property in the **Properties** window.  
  
    > [!TIP]
    >  You can view the effect of the new pivot point by rotating the object. To rotate it, use the **Rotate** tool or modify the **Rotation** property.  
  
 Here's a model that has a modified pivot point:  
  
 ![A model of a house that has a modified pivot point](../VS_IDE/media/digit-modified-model.png "Digit-Modified-Model")  
  
## See Also  
 [How to: Create a Basic 3-D Model](../VS_IDE/how-to--create-a-basic-3-d-model.md)   
 [Model Editor](../VS_IDE/model-editor.md)