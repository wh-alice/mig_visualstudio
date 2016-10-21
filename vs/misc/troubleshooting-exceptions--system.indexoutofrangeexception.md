---
title: "Troubleshooting Exceptions: System.IndexOutOfRangeException | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "IndexOutOfRangeException class"
ms.assetid: 9e28623c-93fc-4111-a0cb-c380e0b5de0c
caps.latest.revision: 25
ms.author: "mblome"
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
# Troubleshooting Exceptions: System.IndexOutOfRangeException
An <xref:System.IndexOutOfRangeException> exception is thrown when an attempt is made to access an element of an array or collection with an index that is outside the bounds of the array or less than zero.  
  
## Associated Tips  
 **Make sure that the maximum index on a list is less than the list size**  
 The maximum index on a list must be less than the list size.  
  
 **Make sure the index is not a negative number.**  
 This exception will be thrown if the index is less than zero.  
  
 **Make sure data column names are correct.**  
 This exception may be thrown if the data column name being supplied to the <xref:System.Data.DataView.Sort*?displayProperty=fullName> property is not valid. For more information, see the <xref:System.Data.DataView> class.  
  
## Example  
  
### Description  
 The following example uses a `Try…Catch` block to trap the `IndexOutOfRangeException` when index `i` is outside the array bounds, 0 to 3. The example displays the following:  
  
 `Element at index 0: 3`  
  
 `Element at index 2: 5`  
  
 `Element at index -1: IndexOutOfRangeException caught`  
  
 `Element at index 4: IndexOutOfRangeException caught`  
  
### Code  
  
```vb#  
Module Module1  
  
    Sub Main()  
        ' The first two tests will display the value of the array element.  
        IndexTest(0)  
        IndexTest(2)  
        ' The following two calls will display the information that  
        ' an IndexOutOfRangeException was caught.  
        IndexTest(-1)  
        IndexTest(4)  
    End Sub  
  
    Sub IndexTest(ByVal i As Integer)  
        Dim testArray() As Integer = {3, 4, 5, 6}  
        Console.Write("Element at index {0}: ", i)  
        Try  
            Console.WriteLine(testArray(i))  
        Catch ex As IndexOutOfRangeException  
            Console.WriteLine("IndexOutOfRangeException caught")  
        End Try  
    End Sub  
  
End Module  
```  
  
## See Also  
 <xref:System.IndexOutOfRangeException>   
 [Use the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)