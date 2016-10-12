---
title: "CommentMarkProfile"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "CommentMarkProfile"
  - "CommentMarkProfileA"
ms.assetid: 33ccff45-c33a-4672-b41f-5b317b848cd1
caps.latest.revision: 11
ms.author: "mikejo"
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
# CommentMarkProfile
The `CommentMarkProfile` function inserts a numeric marker and a text string in the .vsp file. For the mark and comment to be inserted, profiling for the thread that contains the `CommentMarkProfile` function must be ON.  
  
## Syntax  
  
```  
PROFILE_COMMAND_STATUS PROFILERAPI CommentMarkProfile(  
                                   long lMarker,   
                                   LPCTSTR szComment);  
```  
  
#### Parameters  
 `lMarker`  
  
 Numeric marker to insert. The marker must greater than or equal to 0 (zero).  
  
 `szComment`  
  
 Pointer to the text string to insert. The string must be less than 256 characters including the NULL terminator.  
  
## Property Value/Return Value  
 The function indicates success or failure by using **PROFILE_COMMAND_STATUS** enumeration. The return value can be one of the following:  
  
|Enumerator|Description|  
|----------------|-----------------|  
|MARK_ERROR_MARKER_RESERVED|The parameter is less than or equal to 0. These values are reserved. The mark and comment are not recorded.|  
|MARK_ERROR_MODE_NEVER|The profiling mode was set to NEVER when the function was called. The mark and comment are not recorded.|  
|MARK_ERROR_MODE_OFF|The profiling mode was set to OFF when the function was called. The mark and comment are not recorded.|  
|MARK_ERROR_NO_SUPPORT|No mark support in this context. The mark and comment are not recorded.|  
|MARK_ERROR_OUTOFMEMORY|Memory was not available to record the event. The mark and comment are not recorded.|  
|MARK_TEXTTOOLONG|The string exceeds the maximum of 256 characters. The comment string is truncated and the mark and comment are recorded.|  
|MARK_OK|MARK_OK is returned to indicate success.|  
  
## Remarks  
 The profiling state for the thread that contains the mark profile function must be on when marks and comments inserted with the VSInstr Mark command or with functions (CommentMarkAtProfile, CommentMarkProfile, or MarkProfile).  
  
 Profile marks are global in scope. For example, a profile mark inserted in one thread can be used to mark the start or end of a data segment in any thread in the .vsp file.  
  
> [!IMPORTANT]
>  CommentMarkProfile method can only be used with instrumentation.  
  
## .NET Framework Equivalent  
 Microsoft.VisualStudio.Profiler.dll  
  
## Function Information  
  
|||  
|-|-|  
|**Header**|Include VSPerf.h|  
|**Library**|Use VSPerf.lib|  
|**Unicode**|Implemented as `CommentMarkProfileW` (Unicode) and `CommentMarkProfileA` (ANSI).|  
  
## Example  
 The following code illustrates the CommentMarkProfile function call. The example assumes the use of Win32 string macros and Unicode compiler settings to determine whether the code calls the [!INCLUDE[vcpransi](../VS_IDE/includes/vcpransi_md.md)] function call.  
  
```  
void ExerciseCommentMarkProfile()  
{  
    // Declare and initalize variables to pass to   
    // CommentMarkProfile.  The values of these   
    // parameters are assigned based on the needs   
    // of the code; and for the sake of simplicity  
    // in this example, the variables are assigned  
    // arbitrary values.  
    long markId = 01;  
    TCHAR * markText = TEXT("Exercising CommentMarkProfile...");  
  
    // Variables used to print output.  
    HRESULT hResult;  
    TCHAR tchBuffer[256];  
  
    // Declare MarkOperationResult Enumerator.    
    // Holds return value from call to CommentMarkProfile.  
    PROFILE_COMMAND_STATUS markResult;  
  
    markResult = CommentMarkProfile(  
        markId,  
        markText);  
  
    // Format and print result.  
    LPCTSTR pszFormat = TEXT("%s %d.\0");  
    TCHAR* pszTxt = TEXT("CommentMarkProfile returned");  
    hResult = StringCchPrintf(tchBuffer, 256, pszFormat,   
        pszTxt, markResult);  
  
#ifdef DEBUG  
    OutputDebugString(tchBuffer);  
#endif  
}  
```  
  
## See Also  
 [Visual Studio Profiler API Reference (Native)](../VS_IDE/visual-studio-profiler-api-reference--native-.md)