---
title: "-DEBUGTYPE (Debug Info Options) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology:  
  - "cpp-tools"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "/debugtype"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "/DEBUGTYPE linker option"
  - "DEBUGTYPE linker option"
  - "-DEBUGTYPE linker option"
ms.assetid: 1ddcb718-7fec-4f92-a319-3f70f04fe742
caps.latest.revision: 2
author: "corob-msft"
ms.author: "corob"
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
# /DEBUGTYPE (Debug Info Options)
The /DEBUGTYPE option specifies the types of debugging information generated by the /DEBUG option.  
  
```  
/DEBUGTYPE:[CV | PDATA | FIXUP]  
```  
  
## Arguments  
 CV  
 Tells the linker to emit debug information for symbols, line numbers, and other object compilation information in the PDB file. By default, this option is enabled when **/DEBUG** is specified and **/DEBUGTYPE** is not specified.  
  
 PDATA  
 Tells the linker to add .pdata and .xdata entries to the debug stream information in the PDB file. By default, this option is enabled when both the **/DEBUG** and **/DRIVER** options are specified. If **/DEBUGTYPE:PDATA** is specified by itself, the linker automatically includes debugging symbols in the PDB file. If **/DEBUGTYPE:PDATA,FIXUP** is specified, the linker does not include debugging symbols in the PDB file.  
  
 FIXUP  
 Tells the linker to add relocation table entries to the debug stream information in the PDB file. By default, this option is enabled when both the **/DEBUG** and **/PROFILE** options are specified. If **/DEBUGTYPE:FIXUP** or **/DEBUGTYPE:FIXUP,PDATA** is specified, the linker does not include debugging symbols in the PDB file.  
  
 Arguments to **/DEBUGTYPE** may be combined in any order by separating them with a comma. The **/DEBUGTYPE** option and its arguments are not case sensitive.  
  
## Remarks  
 Use the **/DEBUGTYPE** option to specify inclusion of relocation table data or .pdata and .xdata header information in the debugging stream. This causes the linker to include information about user-mode code that is visible in a kernel debugger when breaking in kernel-mode code. To make debugging symbols available when **FIXUP** is specified, include the **CV** argument.  
  
 To debug code in user mode, which is typical for applications, the **/DEBUGTYPE** option isn't needed. By default, the compiler switches that specify debugging output ([/Z7, /Zi, /ZI](../../build/reference/z7-zi-zi-debug-information-format.md)) emit all the information needed by the Visual Studio debugger. Use **/DEBUGTYPE:PDATA** or **/DEBUGTYPE:CV,PDATA,FIXUP** to debug code that combines user-mode and kernel-mode components, such as a configuration app for a device driver. For more information about kernel mode debuggers, see [Debugging Tools for Windows (WinDbg, KD, CDB, NTSD)](http://go.microsoft.com/fwlink/p?LinkID=285651)  
  
## See Also  
 [/DEBUG (Generate Debug Info)](../../build/reference/debug-generate-debug-info.md)   
 [/DRIVER (Windows NT Kernel Mode Driver)](../../build/reference/driver-windows-nt-kernel-mode-driver.md)   
 [/PROFILE (Performance Tools Profiler)](../../build/reference/profile-performance-tools-profiler.md)   
 [Debugging Tools for Windows (WinDbg, KD, CDB, NTSD)](http://go.microsoft.com/fwlink/p?LinkID=285651)