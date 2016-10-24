---
title: "IDiaStackFrame"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "IDiaStackFrame interface"
ms.assetid: 486d25b8-a590-41c1-bdb5-faff3ae35632
caps.latest.revision: 16
ms.author: "mikejo"
manager: "ghogen"
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
# IDiaStackFrame
Exposes the properties of a stack frame.  
  
## Syntax  
  
```  
IDiaStackFrame : IUnknown  
```  
  
## Methods in Vtable Order  
 The following are methods supported by this interface:  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaStackFrame::get_allocatesBasePointer](../debug-interface-access/idiastackframe--get_allocatesbasepointer.md)|Retrieves a flag indicating that the base pointer is allocated for code in this address range. This method is deprecated.|  
|[IDiaStackFrame::get_base](../debug-interface-access/idiastackframe--get_base.md)|Retrieves the address base of the frame.|  
|[IDiaStackFrame::get_cplusplusExceptionHandling](../debug-interface-access/idiastackframe--get_cplusplusexceptionhandling.md)|Retrieves a flag indicating that C++ exception handling is in effect.|  
|[IDiaStackFrame::get_functionStart](../debug-interface-access/idiastackframe--get_functionstart.md)|Retrieves a flag indicating that the block contains the entry point of a function.|  
|[IDiaStackFrame::get_lengthLocals](../debug-interface-access/idiastackframe--get_lengthlocals.md)|Retrieves the number of bytes of local variables pushed on the stack.|  
|[IDiaStackFrame::get_lengthParams](../debug-interface-access/idiastackframe--get_lengthparams.md)|Retrieves the number of bytes of parameters pushed on the stack.|  
|[IDiaStackFrame::get_lengthProlog](../debug-interface-access/idiastackframe--get_lengthprolog.md)|Retrieves the number of bytes of prologue code in the block|  
|[IDiaStackFrame::get_lengthSavedRegisters](../debug-interface-access/idiastackframe--get_lengthsavedregisters.md)|Retrieves the number of bytes of saved registers pushed on the stack.|  
|[IDiaStackFrame::get_localsBase](../debug-interface-access/idiastackframe--get_localsbase.md)|Retrieves the address base of the locals.|  
|[IDiaStackFrame::get_maxStack](../debug-interface-access/idiastackframe--get_maxstack.md)|Retrieves the maximum number of bytes pushed on the stack in the frame.|  
|[IDiaStackFrame::get_rawLVarInstanceValue](../debug-interface-access/idiastackframe--get_rawlvarinstancevalue.md)|Retrieves the value of the specified local variable as raw bytes.|  
|[IDiaStackFrame::get_registerValue](../debug-interface-access/idiastackframe--get_registervalue.md)|Retrieves the value of a specified register.|  
|[IDiaStackFrame::get_returnAddress](../debug-interface-access/idiastackframe--get_returnaddress.md)|Retrieves the return address of the frame.|  
|[IDiaStackFrame::get_size](../debug-interface-access/idiastackframe--get_size.md)|Retrieves the size of the frame in bytes.|  
|[IDiaStackFrame::get_systemExceptionHandling](../debug-interface-access/idiastackframe--get_systemexceptionhandling.md)|Retrieves a flag indicating that system exception handling is in effect.|  
|[IDiaStackFrame::get_type](../debug-interface-access/idiastackframe--get_type.md)|Retrieves the frame type.|  
  
## Remarks  
 A stack frame is an abstraction of a function call during its execution.  
  
## Notes for Callers  
 Obtain this interface by calling the [IDiaEnumStackFrames::Next](../debug-interface-access/idiaenumstackframes--next.md) method. See the [IDiaEnumStackFrames](../debug-interface-access/idiaenumstackframes.md) interface for an example on obtaining the `IDiaStackFrame` interface.  
  
## Example  
 This example displays various attributes of a stack frame.  
  
```cpp#  
void PrintStackFrame(IDiaStackFrame* pFrame)  
{  
    if (pFrame != NULL)  
    {  
        ULONGLONG bottom = 0;  
        ULONGLONG top    = 0;  
  
        if (pFrame->get_base(&bottom) == S_OK &&  
            pFrame->get_registerValue( CV_REG_ESP, &top ) == S_OK )  
        {  
             printf("range = 0x%08I64x - 0x%08I64x\n", bottom, top);  
        }  
  
        ULONGLONG returnAddress = 0;  
        if (pFrame->get_returnAddress(&returnAddress) == S_OK)  
        {  
             printf("return address = 0x%08I64x\n", returnAddress);  
        }  
  
        DWORD lengthFrame     = 0;  
        DWORD lengthLocals    = 0;  
        DWORD lengthParams    = 0;  
        DWORD lengthProlog    = 0;  
        DWORD lengthSavedRegs = 0;  
        if (pFrame->get_size(&lengthFrame) == S_OK &&  
            pFrame->get_lengthLocals(&lengthLocals) == S_OK &&  
            pFrame->get_lengthParams(&lengthParams) == S_OK &&  
            pFrame->get_lengthProlog(&lengthProlog) == S_OK &&  
            pFrame->get_lengthSavedRegisters(&lengthSavedRegs) == S_OK)  
        {  
            printf("stack frame size          = 0x%08lx bytes\n", lengthFrame);  
            printf("length of locals          = 0x%08lx bytes\n", lengthLocals);  
            printf("length of parameters      = 0x%08lx bytes\n", lengthParams);  
            printf("length of prolog          = 0x%08lx bytes\n", lengthProlog);  
            printf("length of saved registers = 0x%08lx bytes\n", lengthSavedRegs);  
        }  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaEnumStackFrames](../debug-interface-access/idiaenumstackframes.md)   
 [IDiaEnumStackFrames::Next](../debug-interface-access/idiaenumstackframes--next.md)   
 [IDiaStackWalkFrame](../debug-interface-access/idiastackwalkframe.md)