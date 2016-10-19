---
title: "How to: Use the Modules Window"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.modules"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "debugger, Modules window"
  - "Modules window"
  - "executable files, displaying while debugging"
  - "debugging [Visual Studio], displaying modules"
  - "DLLs, displaying while debugging"
  - "modules, displaying"
ms.assetid: d840fdca-b035-4452-b652-72580c831896
caps.latest.revision: 36
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
# How to: Use the Modules Window
> [!NOTE]
>  This feature is not available for SQL or script debugging.  
  
 The **Modules** window lists the DLLs and EXE that are used by your program and shows relevant information for each.  
  
### To display the Modules window in break mode or in run mode  
  
-   On the **Debug** menu, choose **Windows**, and then click **Modules**.  
  
     By default, the **Modules** window sorts modules by load order. However, you can choose to sort by any column.  
  
### To sort by any column  
  
-   Click the button at the top of the column.  
  
     You can load symbols or specify a symbol path from the **Modules** window by using the shortcut menu.  
  
## Loading Symbols  
 In the **Modules** window, you can see which modules have debugging symbols loaded. This information appears in the **Symbol Status** column. If the status says **Skipped loadingCannot find or open the PDB file**, or **Loading disabled by include/exclude setting**, you can direct the debugger to download symbols from the Microsoft public symbol servers or to load symbols from a symbol directory on your computer. For more information, see [Specify Symbol (.pdb) and Source Files](../debugger/specify-symbol--.pdb--and-source-files-in-the-visual-studio-debugger.md)  
  
#### To load symbols manually  
  
1.  In the **Modules** window, right-click a module for which symbols have not loaded.  
  
2.  Point to **Load Symbols From** and then click **Microsoft Symbol Servers** or **Symbol Path**.  
  
#### To change symbol load settings  
  
1.  In the **Modules** window, right-click any module.  
  
2.  Click **Symbol Settings**.  
  
     You can now change the symbol load settings, as described in [Specify symbol locations and loading behavior](../debugger/specify-symbol--.pdb--and-source-files-in-the-visual-studio-debugger.md#BKMK_Specify_symbol_locations_and_loading_behavior). Changes do not take effect until you restart the debugging session.  
  
#### To change symbol load behavior for a specific module  
  
1.  In the **Modules** window, right-click the module.  
  
2.  Point to **Automatic Symbol Load Settings** and then click **Always Load Manually** or **Default**. Changes do not take effect until you restart the debugging session.  
  
## See Also  
 [Breaking Execution](http://msdn.microsoft.com/en-us/30fc4643-f337-4651-b1ff-f2de2c098d40)   
 [Viewing Data in the Debugger](../debugger/viewing-data-in-the-debugger.md)   
 [Specify Symbol (.pdb) and Source Files](../debugger/specify-symbol--.pdb--and-source-files-in-the-visual-studio-debugger.md)