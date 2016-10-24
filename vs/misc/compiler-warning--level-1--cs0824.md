---
title: "Compiler Warning (level 1) CS0824 | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0824"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0824"
ms.assetid: ad643bb7-51b2-455b-a9f3-2bd4588d2c5d
caps.latest.revision: 8
ms.author: "billchi"
manager: "douge"
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
# Compiler Warning (level 1) CS0824
Constructor 'name' is marked external.  
  
 A constructor may be marked as extern. However, the compiler cannot verify that the constructor actually exists. Therefore the warning is generated.  
  
### To remove this warning  
  
1.  Use a pragma warning directive to ignore it.  
  
2.  Move the constructor inside the type.  
  
## Example  
 The following code generates CS0824:  
  
```  
// cs0824.cs  
public class C  
{  
    extern C(); // CS0824  
    public static int Main()  
    {  
        return 1;  
    }  
}  
```  
  
## See Also  
 [extern](../Topic/extern%20\(C%23%20Reference\).md)   
 [#pragma warning](../Topic/%23pragma%20warning%20\(C%23%20Reference\).md)