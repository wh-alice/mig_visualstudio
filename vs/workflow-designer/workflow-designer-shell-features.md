---
title: "Workflow Designer Shell Features"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "WFDShellFeatures.UI"
ms.assetid: 14bfe312-9592-408e-92ce-e98585ad16e7
caps.latest.revision: 6
ms.author: "erikre"
manager: "erikre"
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
# Workflow Designer Shell Features
[!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)] is composed of three major UI areas: the designer surface, the breadcrumb bar above it and the shell below it. The breadcrumb bar, positioned at the top of the screen, is used to display the list of ancestors of the current root activity. [!INCLUDE[crdefault](../code-quality/includes/crdefault_md.md)][How to: Use Breadcrumb Navigation](../workflow-designer/how-to--use-breadcrumb-navigation.md). The designer surface, positioned at the center of the screen, is used to compose workflows. The shell, positioned at the bottom of the screen, contains a number of buttons for managing the current view.  
  
## Shell Features  
 The shell has buttons on the right side of the bar that you can use to zoom in or out of your workflow, fit the contents of your workflow to the size of your screen, and show or hide the overview map. You can also zoom in or out of a workflow using the keyboard shortcuts CTRL++ and CTRL+-.  
  
## Overview Map  
 The overview map displays a small version of the entire activity at the current breadcrumb root, including all of its children and all of their expanded children. There is a viewport, a rectangle with an orange border, which highlights the portion of the activity currently displayed inside the editor. Dragging the rectangle around the overview map scrolls the workflow designer and changes the view of the editor.  
  
> [!NOTE]
>  The [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] user interface is virtualized. The activity designers are rendered only when required. If a portion of the workflow has never been drawn on the designer surface, that portion appears as white on the overview map. Scrolling around the overview map completely draws the workflow.  
  
## Copying or Saving Workflows as Images  
 Workflows can be copied in bitmap format or saved in bitmap or vector format. Copying or saving an image provides a way to export a view of entire activity at the current breadcrumb root, including all of its children and all of their expanded children to another program.  
  
 To copy as image, right-click anywhere in the designer and select **Copy as Image**. To save as image, right-click anywhere in the designer and select **Save as Image**. Workflows can be saved in JPG, PNG, GIF, or XPS format. The format is selected on the **Save As** dialog box in the **Save as Type:** drop down list box at the bottom of the window.  
  
## Fonts and Colors  
 The fonts used in [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] inside [!INCLUDE[vs2010](../code-quality/includes/vs2010_md.md)] are controlled by the environment font. The colors displayed in [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] change if you are using a high contrast color scheme for your operating system theme. You must restart [!INCLUDE[vs2010](../code-quality/includes/vs2010_md.md)] after making a change to the font or color settings before the changes take effect in [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)].