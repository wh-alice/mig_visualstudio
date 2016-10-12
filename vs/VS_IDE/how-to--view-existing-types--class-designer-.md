---
title: "How to: View Existing Types (Class Designer)"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.classdesigner.CannotShowBaseType"
helpviewer_keywords: 
  - "types [Visual Studio], visualizing"
  - "types [Visual Studio], class diagrams"
  - "class diagrams, types"
ms.assetid: de110a4e-5b51-4a40-9dee-615df4d8f999
caps.latest.revision: 27
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
# How to: View Existing Types (Class Designer)
To see an existing type and its members, add its shape to a class diagram.  
  
 You can see local and referenced types. A local type exists in the currently open project and is read/write. A referenced type exists in another project or in a referenced assembly and is read-only.  
  
 To design new types on class diagrams, see [How to: Create Types by using Class Designer](../VS_IDE/how-to--create-types-by-using-class-designer.md).  
  
### To see types in a project on a class diagram  
  
1.  From a project in Solution Explorer, open an existing class diagram (.cd) file. Or if no class diagram exists, add a new class diagram to the project. See [How to: Add Class Diagrams to Projects (Class Designer)](../VS_IDE/how-to--add-class-diagrams-to-projects--class-designer-.md).  
  
2.  From the project in Solution Explorer, drag a source code file to the class diagram.  
  
    > [!WARNING]
    >  If your solution has a project that shares code across multiple apps, you can drag files or code to a class diagram only from these sources:  
    >   
    >  -   The app project that contains the diagram  
    > -   A shared project that was imported by the app project  
    > -   A referenced project  
    > -   An assembly  
  
     Shapes representing the types defined in the source code file appear on the diagram at the position where you dragged the file.  
  
 You can also view types in the project by dragging one or more types from the project node in Class View to the class diagram.  
  
> [!TIP]
>  If Class View is not open, open Class View from the **View** menu. For more information about Class View, see [Viewing Classes and Their Members](assetId:///71e9e8f3-261a-4e0c-87bf-5ec48b8bf333).  
  
 To display types at default locations on the diagram, select one or more types in Class View, right-click the selected types, and choose **View Class Diagram**.  
  
> [!NOTE]
>  If a closed class diagram containing the type already exists in the project, the class diagram opens to display the type shape. However, if no class diagram containing the type exists in the project, Class Designer creates a new class diagram in the project and opens it to display the type.  
  
 When you first display a type on the diagram, its shape appears collapsed by default. You can expand the shape to view its contents.  
  
### To display the contents of a project in a class diagram  
  
1.  In Solution Explorer or Class View, right-click the project and choose **View**, then choose **View Class Diagram**.  
  
     An auto-populated Class Diagram is created.  
  
## See Also  
 [How to: View Inheritance Between Types (Class Designer)](../VS_IDE/how-to--view-inheritance-between-types--class-designer-.md)   
 [How to: Customize Class Diagrams (Class Designer)](../VS_IDE/how-to--customize-class-diagrams--class-designer-.md)   
 [Viewing Types and Relationships (Class Designer)](../VS_IDE/viewing-types-and-relationships--class-designer-.md)