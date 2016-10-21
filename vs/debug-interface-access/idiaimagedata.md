---
title: "IDiaImageData | hehe"
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
  - "IDiaImageData interface"
ms.assetid: b696f350-fc08-4352-9287-a15e87512c1e
caps.latest.revision: 9
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
# IDiaImageData
Exposes the details of the base location and memory offsets of the module or image.  
  
## Syntax  
  
```  
IDiaImageData : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaImageData`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaImageData::get_relativeVirtualAddress](../debug-interface-access/idiaimagedata--get_relativevirtualaddress.md)|Retrieves the location in virtual memory of the module relative to the application.|  
|[IDiaImageData::get_virtualAddress](../debug-interface-access/idiaimagedata--get_virtualaddress.md)|Retrieves the location in virtual memory of the image.|  
|[IDiaImageData::get_imageBase](../debug-interface-access/idiaimagedata--get_imagebase.md)|Retrieves the memory location where the image should be based.|  
  
## Remarks  
 Some debug streams (XDATA, PDATA) contain copies of data also stored in the image. These stream data objects can be queried for the `IDiaImageData` interface. See the "Notes for Callers" section in this topic for details.  
  
## Notes for Callers  
 Obtain this interface by calling `QueryInterface` on an [IDiaEnumDebugStreamData](../debug-interface-access/idiaenumdebugstreamdata.md) object. Note that not all debug streams support the `IDiaImageData` interface. For example, currently only the XDATA and PDATA streams support the `IDiaImageData` interface.  
  
## Example  
 This example searches all of the debug streams for any stream that supports the `IDiaImageData` interface. If such a stream is found, some information about that stream is displayed.  
  
```cpp#  
void ShowImageData(IDiaSession *pSession)  
{  
    if (pSession != NULL)  
    {  
        CComPtr<IDiaEnumDebugStreams> pStreamsList;  
        HRESULT hr;  
  
        hr = pSession->getEnumDebugStreams(&pStreamsList);  
        if (SUCCEEDED(hr))  
        {  
            LONG numStreams = 0;  
            hr = pStreamsList->get_Count(&numStreams);  
            if (SUCCEEDED(hr))  
            {  
                ULONG fetched = 0;  
                for (LONG i = 0; i < numStreams; i++)  
                {  
                    CComPtr<IDiaEnumDebugStreamData> pStream;  
                    hr = pStreamsList->Next(1,&pStream,&fetched);  
                    if (fetched == 1)  
                    {  
                        CComPtr<IDiaImageData> pImageData;  
                        hr = pStream->QueryInterface(__uuidof(IDiaImageData),  
                                                     (void **)&pImageData);  
                        if (SUCCEEDED(hr))  
                        {  
                            CComBSTR name;  
                            hr = pStream->get_name(&name);  
                            if (SUCCEEDED(hr))  
                            {  
                                wprintf(L"Stream %s:\n",(BSTR)name);  
                            }  
                            else  
                            {  
                                wprintf(L"Failed to get name of stream\n");  
                            }  
  
                            ULONGLONG imageBase = 0;  
                            if (pImageData->get_imageBase(&imageBase) == S_OK)  
                            {  
                                wprintf(L"  image base = 0x%0I64x\n",imageBase);  
                            }  
  
                            DWORD relVA = 0;  
                            if (pImageData->get_relativeVirtualAddress(&relVA) == S_OK)  
                            {  
                                wprintf(L"  relative virtual address = 0x%08lx\n",relVA);  
                            }  
  
                            ULONGLONG va = 0;  
                            if (pImageData->get_virtualAddress(&va) == S_OK)  
                            {  
                                wprintf(L"  virtual address = 0x%0I64x\n", va);  
                            }  
                        }  
                    }  
                }  
            }  
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
 [IDiaEnumDebugStreamData](../debug-interface-access/idiaenumdebugstreamdata.md)