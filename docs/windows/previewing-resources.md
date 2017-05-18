---
title: "Previewing Resources | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology:  
  - "cpp-windows"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.resvw.resource.previewing"
  - "vs.resvw.resource.previewing"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "resources [Visual Studio], viewing"
  - "resource previews"
  - "code, viewing"
ms.assetid: d6abda66-0e2b-4ac3-a59a-a57b8c6fb70b
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
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
# Previewing Resources
Previewing your resources allows you to view graphical resource without opening them. Previewing is also useful for executables after you've compiled them because the resource identifiers change to numbers. Since these numeric identifiers often don't provide enough information, previewing the resources helps you quickly identify them.  
  
 You can preview the visual layout of the following resource types:  
  
-   Bitmap  
  
-   Dialog  
  
-   Icon  
  
-   Menu  
  
-   Cursor  
  
-   Toolbar  
  
 The visual preview function does not apply to Accelerator, Manifest, String Table, and Version Information resources.  
  
### To preview resources  
  
1.  In [Resource View](../windows/resource-view-window.md) or a document window, select your resource, for example, IDD_ABOUTBOX.  
  
     **Note** If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../windows/how-to-create-a-resource-script-file.md).  
  
2.  In the [Properties window](/visualstudio/ide/reference/properties-window), click the **Property Pages** button.  
  
     \- or -  
  
3.  On the **View** menu, click **Property Pages**.  
  
     The Property Page for the resource opens displaying a preview of that resource. You can then use the Up and Down arrow keys to navigate the tree control in Resource View or the document window. The Property Page will stay open and show any resource that has focus and is able to be previewed.  
  
 For information on adding resources to managed projects, please see [Resources in Desktop Apps](https://msdn.microsoft.com/library/f45fce5x.aspx) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resource strings to properties, see [Creating Resource Files for Desktop Apps](https://msdn.microsoft.com/library/xbx3z216.aspx). For information on globalization and localization of resources in managed apps, see [Globalizing and Localizing .NET Framework Applications](https://msdn.microsoft.com/library/h6270d0z.aspx).  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [How to: Open a Resource Script File Outside of a Project (Standalone)](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)   
 [Resource Editors](../windows/resource-editors.md)
