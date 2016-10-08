---
title: "_com_error::Source"
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
ms.topic: language-reference
ms.assetid: 55353741-fabc-4b0c-9787-b5a69bb189f2
caps.latest.revision: 6
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
# _com_error::Source
**Microsoft Specific**  
  
 Calls **IErrorInfo::GetSource** function.  
  
## Syntax  
  
```  
  
_bstr_t Source() const;  
  
```  
  
## Return Value  
 Returns the result of **IErrorInfo::GetSource** for the **IErrorInfo** object recorded within the `_com_error` object. The resulting BSTR is encapsulated in a `_bstr_t` object. If no **IErrorInfo** is recorded, it returns an empty `_bstr_t`.  
  
## Remarks  
 Any failure while calling the **IErrorInfo::GetSource** method is ignored.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_error Class](../VS_visualcpp/_com_error-Class.md)