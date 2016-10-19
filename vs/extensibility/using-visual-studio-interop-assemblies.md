---
title: "Using Visual Studio Interop Assemblies"
ms.custom: ""
ms.date: "10/18/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Visual Studio, interop assemblies"
  - "interop assemblies, Visual Studio"
  - "managed VSPackages, interop assemblies"
ms.assetid: 1043eb95-4f0d-4861-be21-2a25395b3b3c
caps.latest.revision: 33
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
# Using Visual Studio Interop Assemblies
Visual Studio interop assemblies allow managed applications to access the COM interfaces that provide Visual Studio extensibility. There are some differences between straight COM interfaces and their interop versions. For example, HRESULTs are generally represented as int values and need to be handled in the same way as exceptions, and parameters (especially out parameters) are treated differently.  
  
## Handling HRESULTs Returned to Managed Code from COM  
 When you call a COM interface from managed code, examine the HRESULT value and throw an exception if required. The <xref:Microsoft.VisualStudio.ErrorHandler> class contains the <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure*> method, which throws a COM exception, depending on the value of the HRESULT passed to it.  
  
 By default, <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure*> throws an exception whenever it is passed an HRESULT that has a value less than zero. In cases where such HRESULTs are acceptable values and no exception should be thrown, the values of additional HRESULTS should be passed to <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure*> after the values are tested. If the HRESULT being tested matches any HRESULT values explicitly passed to <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure*>, no exception is thrown.  
  
> [!NOTE]
>  The <xref:Microsoft.VisualStudio.VSConstants> class contains constants for common HRESULTS, for example, <xref:Microsoft.VisualStudio.VSConstants.S_OK> and <xref:Microsoft.VisualStudio.VSConstants.E_NOTIMPL>, and [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] HRESULTS, for example, <xref:Microsoft.VisualStudio.VSConstants.VS_E_INCOMPATIBLEDOCDATA> and <xref:Microsoft.VisualStudio.VSConstants.VS_E_UNSUPPORTEDFORMAT>. <xref:Microsoft.VisualStudio.VSConstants> also provides the <xref:Microsoft.VisualStudio.ErrorHandler.Succeeded*> and <xref:Microsoft.VisualStudio.ErrorHandler.Failed*> methods, which correspond to the SUCCEEDED and FAILED macros in COM.  
  
 For example, consider the following function call, in which <xref:Microsoft.VisualStudio.VSConstants.E_NOTIMPL> is an acceptable return value but any other HRESULT less than zero represents an error.  
  
 [!code[VSSDKHRESULTInformation#1](../extensibility/codesnippet/VisualBasic/using-visual-studio-interop-assemblies_1.vb)]
[!code[VSSDKHRESULTInformation#1](../extensibility/codesnippet/CSharp/using-visual-studio-interop-assemblies_1.cs)]  
  
 If there are more than one acceptable return values, additional HRESULT values can just be appended to the list in the call to <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure*>.  
  
 [!code[VSSDKHRESULTInformation#2](../extensibility/codesnippet/VisualBasic/using-visual-studio-interop-assemblies_2.vb)]
[!code[VSSDKHRESULTInformation#2](../extensibility/codesnippet/CSharp/using-visual-studio-interop-assemblies_2.cs)]  
  
## Returning HRESULTS to COM from Managed Code  
 If no exception occurs, managed code returns <xref:Microsoft.VisualStudio.VSConstants.S_OK> to the COM function that called it. COM interop supports common exceptions that are strongly typed in managed code. For example, a method that receives an unacceptable `null` argument throws an <xref:System.ArgumentNullException>.  
  
 If you are not certain which exception to throw, but you know the HRESULT you want to return to COM, you can use the <xref:System.Runtime.InteropServices.Marshal.ThrowExceptionForHR*> method to throw an appropriate exception. This works even with a nonstandard error, for example, <xref:Microsoft.VisualStudio.VSConstants.VS_E_INCOMPATIBLEDOCDATA>. <xref:System.Runtime.InteropServices.Marshal.ThrowExceptionForHR*> attempts to map the HRESULT passed to it to a strongly typed exception. If it cannot, it throws a generic COM exception instead. The ultimate result is that the HRESULT you pass to <xref:System.Runtime.InteropServices.Marshal.ThrowExceptionForHR*> from managed code is returned to the COM function that called it.  
  
> [!NOTE]
>  Exceptions compromise performance and are intended to indicate abnormal program conditions. Conditions that occur often should be handled inline, instead of a thrown exception.  
  
## IUnknown parameters passed as Type void**  
 Look for [out] parameters that are defined as type `void **` in the COM interface, but that are defined as `[``iid_is``]` in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly method prototype.  
  
 Sometimes, a COM interface generates an `IUnknown` object, and the COM interface then passes it as type `void **`. These interfaces are especially important because if the variable is defined as [out] in the IDL, then the `IUnknown` object is reference-counted with the `AddRef` method. A memory leak occurs if the object is not handled correctly.  
  
> [!NOTE]
>  An `IUnknown` object created by the COM interface and returned in an [out] variable causes a memory leak if it is not explicitly released.  
  
 Managed methods that handle such objects should treat <xref:System.IntPtr> as a pointer to an `IUnknown` object, and call the <xref:System.Runtime.InteropServices.Marshal.GetObjectForIUnknown*> method to obtain the object. The caller should then cast the return value to whatever type is appropriate. When the object is no longer needed, call <xref:System.Runtime.InteropServices.Marshal.Release*> to release it.  
  
 Following is an example of calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.QueryViewInterface*> method and handling the `IUnknown` object correctly:  
  
```  
MyClass myclass;  
Object object;  
IntPtr pObj;  
Guid iid = Typeof(MyClass).Guid;  
int hr = windowFrame.QueryViewInterface(ref iid, out pObj);     
if (NativeMethods.Succeeded(hr))   
{  
    try   
    {  
        object = Marshal.GetObjectForIUnknown(pObj);  
        myclass = object;  
    }  
    finally   
    {  
        Marshal.Release(pObj);  
    }  
}  
else   
{  
    // error calling QueryViewInterface  
}  
```  
  
> [!NOTE]
>  The following methods are known to pass `IUnknown` object pointers as type <xref:System.IntPtr>. Handle them as described in this section.  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CreateProject*>  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory.InitializeForOwner*>  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetNestedHierarchy*>  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolution.CreateProject*>  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.QueryViewInterface*>  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfg2.get_CfgType*>  
  
## Optional [out] Parameters  
 Look for parameters that are defined as an [out] data type (`int`, `object`, and so on) in the COM interface, but that are defined as arrays of the same data type in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly method prototype.  
  
 Some COM interfaces, such as <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetCfgs*>, treat [out] parameters as optional. If an object is not required, these COM interfaces return a `null` pointer as the value of that parameter instead of creating the [out] object. This is by design. For these interfaces, `null` pointers are assumed as part of the correct behavior of the VSPackage, and no error is returned.  
  
 Because the CLR does not allow the value of an [out] parameter to be `null`, part of the designed behavior of these interfaces is not directly available within managed code. The [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly methods for affected interfaces work around the issue by defining the relevant parameters as arrays because the CLR allows the passing of `null` arrays.  
  
 Managed implementations of these methods should put a `null` array into the parameter when there is nothing to be returned. Otherwise, create a one-element array of the correct type and put the return value in the array.  
  
 Managed methods that receive information from interfaces with optional [out] parameters receive the parameter as an array. Just examine the value of the first element of the array. If it is not `null`, treat the first element as if it were the original parameter.  
  
## Passing Constants in Pointer Parameters  
 Look for parameters that are defined as [in] pointers in the COM interface, but that are defined as a <xref:System.IntPtr> type in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly method prototype.  
  
 A similar issue occurs when a COM interface passes a special value, such as 0, -1, or –2, instead of an object pointer. Unlike [!INCLUDE[vcprvc](../codequality/includes/vcprvc_md.md)], the CLR does not allow constants to be cast as objects. Instead, the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly defines the parameter as a <xref:System.IntPtr> type.  
  
 Managed implementations of these methods should take advantage of the fact that the <xref:System.IntPtr> class has both `int` and `void *` constructors to create an <xref:System.IntPtr> from either an object or an integer constant, as appropriate.  
  
 Managed methods that receive <xref:System.IntPtr> parameters of this type should use the <xref:System.IntPtr> type conversion operators to handle the results. First convert the <xref:System.IntPtr> to `int` and test it against relevant integer constants. If no values match, convert it to an object of the required type and continue.  
  
 For examples of this, see <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor*> and <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenSpecificEditor*>.  
  
## OLE Return Values Passed as [out] Parameters  
 Look for methods that have a `retval` return value in the COM interface, but that have an `int` return value and an additional [out] array parameter in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly method prototype. It should be clear that these methods require special handling because the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly method prototypes have one more parameter than the COM interface methods.  
  
 Many COM interfaces that deal with OLE activity send information about OLE status back to the calling program stored in the `retval` return value of the interface. Instead of using a return value, the corresponding [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assembly methods send the information back to the calling program stored in an [out] array parameter.  
  
 Managed implementations of these methods should create a single-element array of the same type as the [out] parameter and put it in the parameter. The value of the array element should be the same as the appropriate COM `retval`.  
  
 Managed methods that call interfaces of this type should pull the first element out of the [out] array. This element can be treated as if it were a `retval` return value from the corresponding COM interface.  
  
## See Also  
 [Interoperating with Unmanaged Code](../Topic/Interoperating%20with%20Unmanaged%20Code.md)