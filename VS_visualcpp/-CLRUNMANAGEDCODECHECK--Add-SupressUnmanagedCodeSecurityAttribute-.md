---
title: "-CLRUNMANAGEDCODECHECK (Add SupressUnmanagedCodeSecurityAttribute)"
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
H1: /CLRUNMANAGEDCODECHECK (Add SupressUnmanagedCodeSecurityAttribute)
ms.assetid: 73abc426-dab0-45e2-be85-0f9a14206cc2
caps.latest.revision: 15
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
# -CLRUNMANAGEDCODECHECK (Add SupressUnmanagedCodeSecurityAttribute)
**/CLRUNMANAGEDCODECHECK** specifies whether the linker will apply <xref:System.Security.SuppressUnmanagedCodeSecurityAttribute?qualifyHint=False> to linker-generated `PInvoke` calls from managed code into native DLLs.  
  
## Syntax  
  
```  
/CLRUNMANAGEDCODECHECK[:NO]  
```  
  
## Remarks  
 By default, the linker applies the SuppressUnmanagedCodeSecurityAttribute to linker-generated `PInvoke` calls. When **/CLRUNMANAGEDCODECHECK** is in effect, SuppressUnmanagedCodeSecurityAttribute is not applied.  
  
 The linker only adds the attribute to objects that are compiled with **/clr** or **/clr:pure**. The linker does not generate `PInvoke` calls in objects compiled with **/clr:safe**. For more information, see [/clr (Common Language Runtime Compilation)](../VS_visualcpp/-clr--Common-Language-Runtime-Compilation-.md).  
  
 A `PInvoke` call is generated by the linker when the linker cannot find a managed symbol to satisfy a reference from a managed caller but can find a native symbol to satisfy that reference. For more information about `PInvoke`, see [Calling Native Functions from Managed Code](../VS_visualcpp/Calling-Native-Functions-from-Managed-Code.md).  
  
 Note that if you use <xref:System.Security.AllowPartiallyTrustedCallersAttribute?qualifyHint=False> in your code, you should explicitly set **/CLRUNMANAGEDCODECHECK**. It is potential security vulnerability if an image contains both the SuppressUnmanagedCodeSecurity and AllowPartiallyTrustedCallers attributes.  
  
 See [Security Optimizations](assetId:///cf255069-d85d-4de3-914a-e4625215a7c0) for more information about the implications of using SuppressUnmanagedCodeSecurityAttribute.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../Topic/How%20to:%20Open%20Project%20Property%20Pages.md).  
  
2.  Expand the **Configuration Properties** node.  
  
3.  Expand the **Linker** node.  
  
4.  Select the **Advanced** property page.  
  
5.  Modify the **CLR Unmanaged Code Check** property.  
  
### To set this linker option programmatically  
  
1.  See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.CLRUnmanagedCodeCheck?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../VS_visualcpp/Setting-Linker-Options.md)   
 [Linker Options](../VS_visualcpp/Linker-Options.md)