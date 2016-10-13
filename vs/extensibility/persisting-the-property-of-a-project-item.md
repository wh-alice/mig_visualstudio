---
title: "Persisting the Property of a Project Item"
ms.custom: na
ms.date: "10/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "properties, adding to a project item"
  - "project items, adding properties"
ms.assetid: d7a0f2b0-d427-4d49-9536-54edfb37c0f3
caps.latest.revision: 7
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# Persisting the Property of a Project Item
You may want to persist a property you add to a project item, such as the author of a source file. You can do this by storing the property in the project file.  
  
 The first step to persist a property in a project file is to obtain the hierarchy of the project as an \<xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> interface. You can obtain this interface either by using Automation or by using \<xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection>. Once you obtain the interface, you can use it to determine which project item is currently selected. Once you have the project item ID, you can use \<xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute*> to add the property.  
  
 In the following procedures, you persist the VsPkg.cs property `Author` with the value `Tom` in the project file.  
  
### To obtain the project hierarchy with the DTE object  
  
1.  Add the following code to your VSPackage:  
  
    ```c#  
    EnvDTE.DTE dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));  
    EnvDTE.Project project = dte.Solution.Projects.Item(1);  
  
    string uniqueName = project.UniqueName;  
    IVsSolution solution = (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));  
    IVsHierarchy hierarchy;  
    solution.GetProjectOfUniqueName(uniqueName, out hierarchy);  
    ```  
  
### To persist the project item property with the DTE object  
  
1.  Add the following code to the code given in the method in the previous procedure:  
  
    ```c#  
    IVsBuildPropertyStorage buildPropertyStorage =   
        hierarchy as IVsBuildPropertyStorage;  
    if (buildPropertyStorage != null)  
    {  
        uint itemId;  
        string fullPath = (string)project.ProjectItems.Item(  
            "VsPkg.cs").Properties.Item("FullPath").Value;  
        hierarchy.ParseCanonicalName(fullPath, out itemId);  
        buildPropertyStorage.SetItemAttribute(itemId, "Author", "Tom");  
    }  
    ```  
  
### To obtain the project hierarchy using IVsMonitorSelection  
  
1.  Add the following code to your VSPackage:  
  
    ```c#  
    IVsHierarchy hierarchy = null;  
    IntPtr hierarchyPtr = IntPtr.Zero;  
    IntPtr selectionContainer = IntPtr.Zero;  
    uint itemid;  
  
    // Retrieve shell interface in order to get current selection  
    IVsMonitorSelection monitorSelection =     Package.GetGlobalService(typeof(SVsShellMonitorSelection)) as     IVsMonitorSelection;  
    if (monitorSelection == null)  
        throw new InvalidOperationException();  
  
    try  
    {  
        // Get the current project hierarchy, project item, and selection container for the current selection  
        // If the selection spans multiple hierachies, hierarchyPtr is Zero  
        IVsMultiItemSelect multiItemSelect = null;  
        ErrorHandler.ThrowOnFailure(  
            monitorSelection.GetCurrentSelection(  
                out hierarchyPtr, out itemid,   
                out multiItemSelect, out selectionContainer));  
  
        // We only care if there is only one node selected in the tree  
        if (!(itemid == VSConstants.VSITEMID_NIL ||   
            hierarchyPtr == IntPtr.Zero ||  
            multiItemSelect != null ||  
            itemid == VSConstants.VSITEMID_SELECTION))  
        {  
            hierarchy = Marshal.GetObjectForIUnknown(hierarchyPtr)  
                as IVsHierarchy;  
        }  
    }  
    finally  
    {  
        if (hierarchyPtr != IntPtr.Zero)  
            Marshal.Release(hierarchyPtr);  
        if (selectionContainer != IntPtr.Zero)  
            Marshal.Release(selectionContainer);  
    }  
    ```  
  
2.  
  
### To persist the selected project item property, given the project hierarchy  
  
1.  Add the following code to the code given in the method in the previous procedure:  
  
    ```  
    IVsBuildPropertyStorage buildPropertyStorage =   
        hierarchy as IVsBuildPropertyStorage;  
    if (buildPropertyStorage != null)  
    {  
        buildPropertyStorage.SetItemAttribute(itemId, "Author", "Tom");  
    }  
    ```  
  
### To verify that the property is persisted  
  
1.  Start [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] and then open or create a solution.  
  
2.  Select the project item VsPkg.cs in **Solution Explorer**.  
  
3.  Use a breakpoint or otherwise determine that your VSPackage is loaded and that SetItemAttribute runs.  
  
    > [!NOTE]
    >  You can autoload a VSPackage in the UI context \<xref:Microsoft.VisualStudio.VSConstants.UICONTEXT_SolutionExists>. For more information, see [Loading VSPackages](../extensibility/loading-vspackages.md).  
  
4.  Close [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] and then open the project file in Notepad. You should see the \<Author> tag with the value Tom, as follows:  
  
    ```  
    <Compile Include="VsPkg.cs">  
        <Author>Tom</Author>  
    </Compile>  
    ```  
  
## See Also  
 [Custom Tools](../extensibility/custom-tools.md)