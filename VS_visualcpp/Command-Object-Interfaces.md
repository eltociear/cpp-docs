---
title: "Command Object Interfaces"
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
ms.assetid: dacff5ae-252c-4f20-9ad7-4e602cc48536
caps.latest.revision: 10
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
# Command Object Interfaces
The command object uses the `IAccessor` interface to specify parameter bindings. The consumer calls `IAccessor::CreateAccessor`, passing it an array of `DBBINDING` structures. `DBBINDING` contains information about the column bindings (such as type and length). The provider receives the structures and determines how the data should be transferred and whether conversions are necessary.  
  
 The `ICommandText` interface provides a way to specify a text command. The `ICommandProperties` interface handles all the command properties.  
  
## See Also  
 [OLE DB Provider Template Architecture](../VS_visualcpp/OLE-DB-Provider-Template-Architecture.md)