---
title: "Cross-Platform Mobile Development Examples"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "tgt-pltfrm-cross-plat"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
ms.assetid: bc384c12-fccc-45d7-9fb9-b90d536aa663
caps.latest.revision: 3
ms.author: "brpeek"
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
# Cross-Platform Mobile Development Examples
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

Several of the templates installed by Visual C++ for Cross-Platform Mobile Development generate complete examples that you can use to learn from. Additionally, the Windows Dev Center has several example applications that you can download and try out in Visual Studio.  
  
-   [hello-jni Android Application Sample](https://code.msdn.microsoft.com/hello-jni-Android-790ab73d)  
  
     This sample is a port of the Android NDK hello-jni application. The sample demonstrates an end-to-end Java Native Interface "Hello World" app. It loads a string from a native method implemented in a shared library, and then displays it in the app.  
  
-   [hello-gl2 Android Application Sample](https://code.msdn.microsoft.com/hello-gl2-Android-3b61896c)  
  
     This sample is a port of the Android NDK hello-gl2 application. The sample demonstrates an end-to-end Java Native Interface Android OpenGL app. It renders a triangle using the OpenGL ES 2.0 shader APIs.  
  
-   [Bitmap Plasma Android Application Sample](https://code.msdn.microsoft.com/Bitmap-Plasma-Android-77ae296a)  
  
     This sample is a port of the Android NDK Bitmap Plasma application. The sample demonstrates an end-to-end Java Native Interface Android OpenGL ES 2.0 application. It demonstrates direct manipulation of Android bitmap pixel buffers to generate a plasma effect.  
  
-   [TwoLibs Android Library Sample](https://code.msdn.microsoft.com/TwoLibs-Android-Library-6396e5c4)  
  
     This sample is a port of the Android NDK TwoLibs sample. It uses both a dynamically loaded shared library, and a static C++ Android native library, that implements a method called from a Java Native Interface app. This sample is a good starting point for developers to understand how to use static/dynamic shared libraries to build an end-to-end JNI Android application with Visual Studio 2015.  
  
-   [Tea Pot Android Application Sample](https://code.msdn.microsoft.com/Tea-Pot-Android-Application-e7c05d73)  
  
     This sample is a port of the Android NDK TeaPot application. The sample demonstrates an end-to-end Java Native Interface Android OpenGL ES 2.0 application.  
  
-   [MoreTeaPots Android Application Sample](https://code.msdn.microsoft.com/MoreTeaPots-Android-a9bd8549)  
  
     This sample is a port of the Android NDK MoreTeaPots application. The sample demonstrates an end-to-end Java Native Interface Android OpenGL application.  
  
-   [test-libstdcpp Android Library Sample](https://code.msdn.microsoft.com/test-libstdcpp-Android-00b548f5)  
  
     This sample is a port of the Android NDK test-libstdc++ sample, specifically for use with Visual Studio 2015. This sample is a good starting point for developers to understand how to use the Standard Library.  
  
 To open one of the examples in Visual Studio, download the zip file and open the **Properties** page of the downloaded file in Explorer. Choose the **Unblock** button then choose **OK**. Extract the contents of the zip file to a convenient location, then open the C++ folder in the extracted sample and open the solution file.  
  
 To build the sample, press F7, or on the menu bar, choose **Build**, **Build Solution**.