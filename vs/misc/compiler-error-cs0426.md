---
title: "Compiler Error CS0426"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0426"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0426"
ms.assetid: 62df0deb-3624-436e-9691-ebe3ee1fc31f
caps.latest.revision: 8
ms.author: "wiwagn"
manager: "wpickett"
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
# Compiler Error CS0426
The type name 'identifier' does not exist in the type 'type'  
  
 This error occurs when you reference a type nested within another type, but no such nested type exists. This can occur if you mistype the name of the nested type. Check the spelling of the names used, and verify that the enclosing type has the expected member.  
  
 The following sample generates CS0426 because class C has no nested type A:  
  
```  
// CS0426.cs  
  
class C  
{  
    // No nested types are declared.     
}  
  
class D  
{  
   public static void Main()  
   {  
       C c = new C();  
       // Attempt to reference a nested type A:  
       C.A a; // CS0426 because no such type C.A  
   }  
}  
```  
  
## See Also  
 [Classes and Structs](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)