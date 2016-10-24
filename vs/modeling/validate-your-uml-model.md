---
title: "Validate your UML model | testtitle"
ms.custom: ""
ms.date: "10/21/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "UML, constraints"
  - "UML, validation"
ms.assetid: deed5092-c11d-4431-a801-1e866a103075
caps.latest.revision: 10
ms.author: "ahomer"
manager: "douge"
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
# Validate your UML model
Some of the UML models that you can draw in Visual Studio might be considered invalid in your project. For example, you might require that a use case must always be linked to a sequence diagram that has lifelines representing the use case's actors. You can install or define *constraints* that help your team to conform to requirements such as this. Constraints can be applied when the user saves or opens a model, and can be invoked by menu command.  
  
 No constraints are provided with [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], because they depend on how your team interprets and uses UML models. But you can define your own constraints, and install constraints that are defined by other users. To learn how to define constraints and package them for distribution, see [Define validation constraints for UML models](../modeling/define-validation-constraints-for-uml-models.md).  
  
## Invoking Validation  
 When you have installed a validation extension, the constraints it provides may be applied in the following cases. Some constraints are set to apply in only some of these cases.  
  
-   **Validation command.** To invoke validation at any time, click **Validate UML Model** on the **Architecture** menu.  
  
    > [!NOTE]
    >  The command will appear only if validation constraints are installed.  
  
-   **On saving a model.** Validation constraints may be applied when you save the model. The purpose of these constraints is to help make sure that you do not save a model that is invalid according to your project's interpretation.  
  
     If there are errors, you will be asked whether you still want to save the model. You can choose to correct the errors, or to save the model anyway.  
  
-   **On opening a model.** When you open a model, validation methods can be applied to restore error messages that existed when you saved the model. Errors can also be introduced by inconsistencies between the changes that are made by users who are working on different parts of a model. For more information, see [Share models and exporting diagrams](../modeling/share-models-and-exporting-diagrams.md).  
  
 Validation errors are reported in the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] errors window.  
  
 To select in a diagram the elements that are incorrect, double-click the error. This works only if the incorrect elements are visible in an open diagram.  
  
## Installing Validation Constraints  
 Constraints are packaged within [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Extension (VSIX) files. Typically, a set of constraints will be part of an extension that also contains other definitions such as menu commands, profiles, and toolbox items.  
  
#### To install a Visual Studio Extension  
  
1.  Double-click the **.vsix** file in Windows Explorer (or File Explorer).  
  
2.  Restart any instance of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] that is already running.  
  
## Disabling and Uninstalling Validation Constraints  
 When you want to work with a model to which the constraints do not apply, you can temporarily disable the extension that contains them. In this way, you can work with different kinds of model at different times, by enabling and disabling different extensions.  
  
#### To disable or uninstall a Visual Studio Extension  
  
1.  On the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] **Tools** menu, click **Extensions and Updates**.  
  
2.  Alongside the extension, click **Disable** to temporarily disable the extension. You can re-enable it later by returning to the **Extensions and Updates** window.  
  
     \- or -  
  
     Click **Uninstall** to remove the extension.  
  
3.  Restart [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
## See Also  
 [Define validation constraints for UML models](../modeling/define-validation-constraints-for-uml-models.md)   
 [Create models for your app](../modeling/create-models-for-your-app.md)   
 [Use models in your development process](../modeling/use-models-in-your-development-process.md)