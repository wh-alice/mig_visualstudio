---
title: "Item Metadata in Task Batching | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "batching [MSBuild]"
  - "MSBuild, batching"
  - "task batching [MSBuild]"
  - "MSBuild, task batching"
ms.assetid: 31e480f8-fe4d-4633-8c54-8ec498e2306d
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
# Item Metadata in Task Batching
[!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)] has the ability to divide item lists into different categories, or batches, based on item metadata, and run a task one time with each batch. It can be confusing to understand exactly what items are being passed with which batch. This topic covers the following common scenarios that involve batching.  
  
-   Dividing an item list into batches  
  
-   Dividing several item lists into batches  
  
-   Batching one item at a time  
  
-   Filtering item lists  
  
 For more information on batching with [!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)], see [Batching](../reference/msbuild-batching.md).  
  
## Dividing an Item list into Batches  
 Batching allows you to divide an item list into different batches based on item metadata, and pass each of the batches into a task separately. This is useful for building satellite assemblies.  
  
 The following example shows how to divide an item list into batches based on item metadata. The `ExampColl` item list is divided into three batches based on the `Number` item metadata. The presence of `%(ExampColl.Number)`in the `Text` attribute notifies [!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)] that batching should be performed. The `ExampColl` item list is divided into three batches based on the `Number` metadata, and each batch is passed separately into the task.  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <ExampColl Include="Item1">  
            <Number>1</Number>  
        </ExampColl>  
        <ExampColl Include="Item2">  
            <Number>2</Number>  
        </ExampColl>  
        <ExampColl Include="Item3">  
            <Number>3</Number>  
        </ExampColl>  
        <ExampColl Include="Item4">  
            <Number>1</Number>  
        </ExampColl>  
        <ExampColl Include="Item5">  
            <Number>2</Number>  
        </ExampColl>  
        <ExampColl Include="Item6">  
            <Number>3</Number>  
        </ExampColl>  
    </ItemGroup>  
  
    <Target Name="ShowMessage">  
        <Message  
            Text = "Number: %(ExampColl.Number) -- Items in ExampColl: @(ExampColl)"/>  
    </Target>  
  
</Project>  
```  
  
 The [Message Task](../reference/message-task.md) task displays the following information:  
  
 `Number: 1 -- Items in ExampColl: Item1;Item4`  
  
 `Number: 2 -- Items in ExampColl: Item2;Item5`  
  
 `Number: 3 -- Items in ExampColl: Item3;Item6`  
  
## Dividing Several Item lists into Batches  
 [!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)] can divide multiple item lists into batches based on the same metadata. This makes it easy to divide different item lists into batches to build multiple assemblies. For example, you could have an item list of .cs files divided into an application batch and an assembly batch, and an item list of resource files divided into an application batch and an assembly batch. You could then use batching to pass these item lists into one task and build both the application and the assembly.  
  
> [!NOTE]
>  If an item list being passed into a task contains no items with the referenced metadata, every item in that item list is passed into every batch.  
  
 The following example shows how to divide multiple item list into batches based on item metadata. The `ExampColl` and `ExampColl2` item lists are each divided into three batches based on the `Number` item metadata. The presence of `%(Number)`in the `Text` attribute notifies [!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)] that batching should be performed. The `ExampColl` and `ExampColl2` item lists are divided into three batches based on the `Number` metadata, and each batch is passed separately into the task.  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
  
        <ExampColl Include="Item1">  
            <Number>1</Number>  
        </ExampColl>  
        <ExampColl Include="Item2">  
            <Number>2</Number>  
        </ExampColl>  
        <ExampColl Include="Item3">  
            <Number>3</Number>  
        </ExampColl>  
  
        <ExampColl2 Include="Item4">  
            <Number>1</Number>  
        </ExampColl2>  
        <ExampColl2 Include="Item5">  
            <Number>2</Number>  
        </ExampColl2>  
        <ExampColl2 Include="Item6">  
            <Number>3</Number>  
        </ExampColl2>  
  
    </ItemGroup>  
  
    <Target Name="ShowMessage">  
        <Message  
            Text = "Number: %(Number) -- Items in ExampColl: @(ExampColl) ExampColl2: @(ExampColl2)"/>  
    </Target>  
  
</Project>  
```  
  
 The [Message Task](../reference/message-task.md) task displays the following information:  
  
 `Number: 1 -- Items in ExampColl: Item1 ExampColl2: Item4`  
  
 `Number: 2 -- Items in ExampColl: Item2 ExampColl2: Item5`  
  
 `Number: 3 -- Items in ExampColl: Item3 ExampColl2: Item6`  
  
## Batching One Item at a Time  
 Batching can also be performed on well-known item metadata that is assigned to every item upon creation. This guarantees that every item in a collection will have some metadata to use for batching. The `Identity` metadata value is unique for every item, and is useful for dividing every item in an item list into a separate batch. For a complete list of well-known item metadata, see [Well-known Item Metadata](../reference/msbuild-well-known-item-metadata.md).  
  
 The following example shows how to batch each item in an item list one at a time. Because the `Identity` metadata value of every item is unique, the `ExampColl` item list is divided into six batches, each batch containing one item of the item list. The presence of `%(Identity)`in the `Text` attribute notifies [!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)] that batching should be performed.  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
  
        <ExampColl Include="Item1"/>  
        <ExampColl Include="Item2"/>  
        <ExampColl Include="Item3"/>  
        <ExampColl Include="Item4"/>  
        <ExampColl Include="Item5"/>  
        <ExampColl Include="Item6"/>  
  
    </ItemGroup>  
  
    <Target Name="ShowMessage">  
        <Message  
            Text = "Identity: "%(Identity)" -- Items in ExampColl: @(ExampColl)"/>  
    </Target>  
  
</Project>  
```  
  
 The [Message Task](../reference/message-task.md) task displays the following information:  
  
```  
Identity: "Item1" -- Items in ExampColl: Item1  
Identity: "Item2" -- Items in ExampColl: Item2  
Identity: "Item3" -- Items in ExampColl: Item3  
Identity: "Item4" -- Items in ExampColl: Item4  
Identity: "Item5" -- Items in ExampColl: Item5  
Identity: "Item6" -- Items in ExampColl: Item6  
```  
  
## Filtering Item lists  
 Batching can be used to filter out certain items from an item list before passing it to a task. For example, filtering on the `Extension` well-known item metadata value allows you to run a task on only files with a specific extension.  
  
 The following example shows how to divide an item list into batches based on item metadata, and then filter those batches when they are passed into a task. The `ExampColl` item list is divided into three batches based on the `Number` item metadata. The `Condition` attribute of the task specifies that only batches with a `Number` item metadata value of `2` will be passed into the task  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
  
        <ExampColl Include="Item1">  
            <Number>1</Number>  
        </ExampColl>  
        <ExampColl Include="Item2">  
            <Number>2</Number>  
        </ExampColl>  
        <ExampColl Include="Item3">  
            <Number>3</Number>  
        </ExampColl>  
        <ExampColl Include="Item4">  
            <Number>1</Number>  
        </ExampColl>  
        <ExampColl Include="Item5">  
            <Number>2</Number>  
        </ExampColl>  
        <ExampColl Include="Item6">  
            <Number>3</Number>  
        </ExampColl>  
  
    </ItemGroup>  
  
    <Target Name="Exec">  
        <Message  
            Text = "Items in ExampColl: @(ExampColl)"  
            Condition="'%(Number)'=='2'"/>  
    </Target>  
  
</Project>  
```  
  
 The [Message Task](../reference/message-task.md) task displays the following information:  
  
```  
Items in ExampColl: Item2;Item5  
```  
  
## See Also  
 [Well-known Item Metadata](../reference/msbuild-well-known-item-metadata.md)   
 [Item Element (MSBuild)](../reference/item-element--msbuild-.md)   
 [ItemMetadata Element (MSBuild)](../reference/itemmetadata-element--msbuild-.md)   
 [Batching](../reference/msbuild-batching.md)   
 [MSBuild Concepts](../reference/msbuild-concepts.md)   
 [MSBuild Reference](../reference/msbuild-reference.md)