---
title: "Visual C++ Structures in Class Designer | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Class Designer [Visual Studio], structures"
ms.assetid: bad18ab6-d956-47a6-a413-811cc26db5f5
caps.latest.revision: 11
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
# Visual C++ Structures in Class Designer
Class Designer supports C++ structures, which are declared with the keyword `struct`. Following is an example:  
  
```  
struct MyStructure  
{  
   char a;  
   int i;  
   long j;  
};  
```  
  
 For more information about using the `struct` type, see [struct](../Topic/struct%20\(C++\).md).  
  
 A C++ structure shape in a class diagram looks and works like a class shape, except that the label reads **Struct** and it has square corners instead of rounded corners.  
  
|Code element|Class Designer view|  
|------------------|-------------------------|  
|`struct StructureName {};`|**StructureName**<br /><br /> Struct|  
  
## See Also  
 [Working with Visual C++ Code (Class Designer)](../ide/working-with-visual-c---code--class-designer-.md)   
 [Classes and Structs](../Topic/Classes%20and%20Structs%20\(C++\).md)   
 [struct](../Topic/struct%20\(C++\).md)