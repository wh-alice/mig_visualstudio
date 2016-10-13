---
title: "Overview of Domain-Specific Language Tools"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Domain-Specific Language"
ms.assetid: 50d93ea2-8c88-4522-853b-40ab194953db
caps.latest.revision: 54
ms.author: "awills"
manager: "kamrani"
---
# Overview of Domain-Specific Language Tools
Domain-Specific Language Tools (DSL Tools), which are hosted in [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)], let you design a domain-specific language and then generate everything that users must have to create models that are based on the language.  
  
 The following tools are included in DSL Tools:  
  
-   A project wizard that uses different solution templates to help you start developing your domain-specific language.  
  
-   A graphical designer for creating and editing your domain-specific language definition.  
  
-   A validation engine that makes sure that the domain-specific language definition is well-formed, and displays errors and warnings if there are problems.  
  
-   A code generator that takes a domain-specific language definition as input and produces source code as output.  
  
## The DSL Tools Solution  
 The Domain-Specific Designer Wizard provides the following solution templates:  
  
-   Task Flow  
  
-   Class Diagrams  
  
-   Minimal Language  
  
-   Component Models  
  
-   Minimal WPF  
  
-   Minimal Windows.Forms  
  
-   DSL Library  
  
 For more information, see [Choosing a Domain-Specific Language Solution Template](../modeling/choosing-a-domain-specific-language-solution-template.md).  
  
 The wizard creates a [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] solution that has the following projects:  
  
-   Dsl  
  
     The Dsl project defines the domain-specific language and its editing and processing tools.  
  
-   **DslPackage**  
  
     The DslPackage project determines how the language tools integrate with [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)].  
  
## The DSL Tools Graphical Interface  
 You can use the DSL Tools graphical interface to add elements and relationships to your domain-specific language. After you have added the elements, you can define their appearance by mapping them to shapes, customizing colors, and adding decorators. You can also add the elements to the toolbox.  
  
## Validation in DSL Tools  
 Dsl provides one level of validation to make sure that the domain model meets the basic requirements for code generation. Typically, when you create your own domain-specific language, you would add your own validation to express your business logic rules. For more information about custom validation, see [Validation in a Domain-Specific Language](../modeling/validation-in-a-domain-specific-language.md).  
  
 We recommend that you validate your domain-specific language often when you are designing it. If your domain-specific language has validation errors, you cannot generate source code. The process of generating source code from the templates is performed by clicking **Transform All Templates** in the toolbar of Solution Explorer. Whenever you modify the language definition, also make sure to **Transform All Templates**. For more information, see [How to: Create a Domain-Specific Language Solution](../modeling/how-to--create-a-domain-specific-language-solution.md).  
  
## Customization of DSL Tools  
 You can provide additional code to refine the behavior of the model and to define constraints over your language. If required, you can make significant changes by modifying the text templates.  
  
## Distributing Your DSL Solution  
 DSL Tools generates a package that is hosted in [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)]. The package displays a toolbox, a DSL explorer, and other UI elements that let users create models by using your domain-specific language.  
  
 When you build and run the DSL Tools solution in [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)], a second instance of [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] shows you how your domain-specific language looks to the user of the language. After you verify that everything works correctly, you can distribute the `.vsix` file that you will find in the build folder of the DslPackage project. This file can be used to install the DSL as a [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] extension on other computers.  For more information, see [Deploying Domain-Specific Language Solutions](../modeling/deploying-domain-specific-language-solutions.md).  
  
## See Also  
 [The Experimental Instance](../extensibility/the-experimental-instance.md)   
 [Domain-Specific Language Tools Glossary](http://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)