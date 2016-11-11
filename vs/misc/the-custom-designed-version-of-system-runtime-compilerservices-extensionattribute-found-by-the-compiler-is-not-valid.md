---
title: "The custom-designed version of &#39;System.Runtime.CompilerServices.ExtensionAttribute&#39; found by the compiler is not valid | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc36558"
  - "bc36558"
helpviewer_keywords: 
  - "BC36558"
ms.assetid: f47d310a-95fd-4340-bda2-21262c217dbb
caps.latest.revision: 16
author: "stevehoag"
ms.author: "shoag"
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
# The custom-designed version of &#39;System.Runtime.CompilerServices.ExtensionAttribute&#39; found by the compiler is not valid
The custom-designed version of 'System.Runtime.CompilerServices.ExtensionAttribute' found by the compiler is not valid. Its attribute usage flags must be set to allow assemblies, classes, and methods.  
  
 The custom-designed version of <xref:System.Runtime.CompilerServices.ExtensionAttribute?displayProperty=fullName> that the compiler found does not set its attribute usage flags to enable application of the attribute to assemblies, methods, and classes. Application to at least those three program elements is required.  
  
 **Error ID:** BC36558  
  
### To correct this error  
  
-   Change the attribute definition to enable the attribute to apply at least to assemblies, methods, and classes, as shown in the following examples.  
  
-   Use <xref:System.Runtime.CompilerServices.ExtensionAttribute?displayProperty=fullName> instead of the custom-designed version.  
  
## Example  
 The following example uses the `AttributeUsage` attribute to specify which program elements the new version of `ExtensionAttribute` can apply to. The example specifies three members of the `AttributeTargets` enumeration: `Assembly`, `Class`, and `Method`. The omission of any one of these elements will cause this error.  
  
```  
Namespace System.Runtime.CompilerServices  
    <AttributeUsage(AttributeTargets.Assembly Or _  
        AttributeTargets.Class Or AttributeTargets.Method)>  
    Class ExtensionAttribute  
        Inherits System.Attribute  
        ' Definitions of methods, fields, and properties.  
    End Class  
End Namespace  
```  
  
 Alternatively, you could allow `ExtensionAttribute` to apply to all program elements by using the `All` member of `AttributeTargets`.  
  
```  
<AttributeUsage(AttributeTargets.All)>  
```  
  
 Deleting the `AttributeUsage` line, as shown in the following code, produces the same result.  
  
```  
Namespace System.Runtime.CompilerServices  
    Class ExtensionAttribute  
        Inherits System.Attribute  
        ' Definitions of methods, fields, and properties.  
    End Class  
End Namespace  
```  
  
## See Also  
 <xref:System.Runtime.CompilerServices.ExtensionAttribute>   
 [NOT IN BUILD: Attributes Overview in Visual Basic](http://msdn.microsoft.com/en-us/0d0cff64-892d-4f57-83bd-bef388553d4f)   
 [NOT IN BUILD: Custom Attributes in Visual Basic](http://msdn.microsoft.com/en-us/d72d8a5c-8f64-4614-b15b-cad66845d047)   
 [Extension Methods](/dotnet/visual-basic/language-reference/procedures/extension-methods)   
 [NOT IN BUILD: How to: Define Your Own Attributes](http://msdn.microsoft.com/en-us/039609c4-ec43-4f44-945f-aa3b5b535c6a)   
 [Writing Custom Attributes](http://msdn.microsoft.com/en-us/Library/97216f69-bde8-49fd-ac40-f18c500ef5dc)