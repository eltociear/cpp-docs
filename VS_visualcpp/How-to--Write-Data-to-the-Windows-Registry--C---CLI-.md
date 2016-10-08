---
title: "How to: Write Data to the Windows Registry (C++-CLI)"
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
H1: How to: Write Data to the Windows Registry (C++/CLI)
ms.assetid: 3d40b978-4baa-4779-bfe3-47e2917b757f
caps.latest.revision: 9
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
# How to: Write Data to the Windows Registry (C++-CLI)
The following code example uses the <xref:Microsoft.Win32.Registry.CurrentUser?qualifyHint=False> key to create a writable instance of the <xref:Microsoft.Win32.RegistryKey?qualifyHint=False> class corresponding to the **Software** key. The <xref:Microsoft.Win32.RegistryKey.CreateSubKey?qualifyHint=False> method is then used to create a new key and add to key/value pairs.  
  
## Example  
  
### Code  
  
```  
// registry_write.cpp  
// compile with: /clr  
using namespace System;  
using namespace Microsoft::Win32;  
  
int main()  
{  
   // The second OpenSubKey argument indicates that  
   // the subkey should be writable.   
   RegistryKey^ rk;  
   rk  = Registry::CurrentUser->OpenSubKey("Software", true);  
   if (!rk)  
   {  
      Console::WriteLine("Failed to open CurrentUser/Software key");  
      return -1;  
   }  
  
   RegistryKey^ nk = rk->CreateSubKey("NewRegKey");  
   if (!nk)  
   {  
      Console::WriteLine("Failed to create 'NewRegKey'");  
      return -1;  
   }  
  
   String^ newValue = "NewValue";  
   try  
   {  
      nk->SetValue("NewKey", newValue);  
      nk->SetValue("NewKey2", 44);  
   }  
   catch (Exception^)  
   {  
      Console::WriteLine("Failed to set new values in 'NewRegKey'");  
      return -1;  
   }  
  
   Console::WriteLine("New key created.");  
   Console::Write("Use REGEDIT.EXE to verify ");  
   Console::WriteLine("'CURRENTUSER/Software/NewRegKey'\n");  
   return 0;  
}  
```  
  
## Remarks  
 You can use the .NET Framework to access the registry with the <xref:Microsoft.Win32.Registry?qualifyHint=False> and [RegistryKey](https://msdn.microsoft.com/en-us/library/microsoft.win32.registrykey.aspx) classes, which are both defined in the <xref:Microsoft.Win32?qualifyHint=False> namespace. The **Registry** class is a container for static instances of the <xref:Microsoft.Win32.RegistryKey?qualifyHint=False> class. Each instance represents a root registry node. The instances are <xref:Microsoft.Win32.Registry.ClassesRoot?qualifyHint=False>, <xref:Microsoft.Win32.Registry.CurrentConfig?qualifyHint=False>, <xref:Microsoft.Win32.Registry.CurrentUser?qualifyHint=False>, <xref:Microsoft.Win32.Registry.LocalMachine?qualifyHint=False>, and <xref:Microsoft.Win32.Registry.Users?qualifyHint=False>.  
  
## See Also  
 [How to: Read Data from the Windows Registry (C++/CLI)](../VS_visualcpp/How-to--Read-Data-from-the-Windows-Registry--C---CLI-.md)   
 [.NET Programming with C++/CLI (Visual C++)](../VS_visualcpp/.NET-Programming-with-C---CLI--Visual-C---.md)