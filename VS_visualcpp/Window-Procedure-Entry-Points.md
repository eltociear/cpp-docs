---
title: "Window Procedure Entry Points"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a6b46a7f-6e42-45f2-9ae6-82e19fc57148
caps.latest.revision: 7
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# Window Procedure Entry Points
To protect MFC window procedures, a module static links with a special window procedure implementation. The linkage occurs automatically when the module is linked with MFC. This window procedure uses the `AFX_MANAGE_STATE` macro to properly set the effective module state, then it calls **AfxWndProc**, which in turn delegates to the `WindowProc` member function of the appropriate `CWnd`-derived object.  
  
## See Also  
 [Managing the State Data of MFC Modules](../VS_visualcpp/Managing-the-State-Data-of-MFC-Modules.md)