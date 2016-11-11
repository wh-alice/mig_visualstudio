---
title: "&#39;&lt;nullconstant&gt;&#39; is not declared | Microsoft Docs"
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
  - "bc30822"
  - "vbc30822"
helpviewer_keywords: 
  - "BC30822"
ms.assetid: dda0e2c1-46a3-4cc4-b36c-0858a5259bac
caps.latest.revision: 13
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
# &#39;&lt;nullconstant&gt;&#39; is not declared
'\<nullconstant>' is not declared. Null constant is no longer supported; use System.DBNull instead.  
  
 A statement uses the `Null` keyword, which is no longer supported in Visual Basic.  
  
 **Error ID:** BC30822  
  
### To correct this error  
  
1.  Use <xref:System.DBNull> instead of `Null`. The following example demonstrates this.  
  
    ```  
    Sub TestDBNull()  
        Dim t As DataTable  
        ' Assume the DataGrid is bound to a DataTable.  
        t = CType(DataGrid1.DataSource, DataTable)  
        Dim r As DataRow  
        r = t.Rows(datagrid1.CurrentCell.RowNumber)  
        r.BeginEdit  
        r(1) = System.DBNull.Value ' Assign DBNull to the record.  
        r.EndEdit  
        r.AcceptChanges  
        If r.IsNull(1) Then  
            MsgBox("")  
        End If  
    End Sub  
    ```  
  
2.  Use the [Nothing](/dotnet/visual-basic/language-reference/nothing) keyword for assignments and comparisons when you use object variables. The following example demonstrates this.  
  
    ```  
    Sub TestNothing()  
        Dim cls As Object  
        ' cls is Nothing if it has not been assigned using the New keyword.  
        If (cls Is Nothing) Then  
            MsgBox("cls is Nothing")  
        End If  
        cls = Nothing ' Assign Nothing to the class variable cls.  
    End Sub  
    ```  
  
## See Also  
 <xref:System.DBNull>   
 [Nothing](/dotnet/visual-basic/language-reference/nothing)   
 [Programming Element Support Changes Summary](http://msdn.microsoft.com/en-us/0483590a-6309-449c-a2fa-effa26a03b95)