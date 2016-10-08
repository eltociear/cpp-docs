---
title: "Dialog Data Exchange Functions for OLE Controls"
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
ms.assetid: 7ef1f288-ff65-40d4-aad2-5497bc00bb27
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
# Dialog Data Exchange Functions for OLE Controls
This topic lists the DDX_OC functions used to exchange data between a property of an OLE control in a dialog box, form view, or control view object and a data member of the dialog box, form view, or control view object.  
  
### DDX_OC Functions  
  
|||  
|-|-|  
|[DDX_OCBool](../Topic/DDX_OCBool.md)|Manages the transfer of                             **BOOL** data between a property of an OLE control and a                             **BOOL** data member.|  
|[DDX_OCBoolRO](../Topic/DDX_OCBoolRO.md)|Manages the transfer of                             **BOOL** data between a read-only property of an OLE control and a                             **BOOL** data member.|  
|[DDX_OCColor](../Topic/DDX_OCColor.md)|Manages the transfer of                             **OLE_COLOR** data between a property of an OLE control and an                             **OLE_COLOR** data member.|  
|[DDX_OCColorRO](../Topic/DDX_OCColorRO.md)|Manages the transfer of                             **OLE_COLOR** data between a read-only property of an OLE control and an                             **OLE_COLOR** data member.|  
|[DDX_OCFloat](../Topic/DDX_OCFloat.md)|Manages the transfer of                             **float** (or                             **double**) data between a property of an OLE control and a                             **float** (or                             **double**) data member.|  
|[DDX_OCFloatRO](../Topic/DDX_OCFloatRO.md)|Manages the transfer of                             **float** (or                             **double**) data between a read-only property of an OLE control and a                             **float** (or                             **double**) data member.|  
|[DDX_OCInt](../Topic/DDX_OCInt.md)|Manages the transfer of                             `int` (or                             **long**) data between a property of an OLE control and an                             `int` (or                             **long**) data member.|  
|[DDX_OCIntRO](../Topic/DDX_OCIntRO.md)|Manages the transfer of                             `int` (or                             **long**) data between a read-only property of an OLE control and an                             `int` (or                             **long**) data member.|  
|[DDX_OCShort](../Topic/DDX_OCShort.md)|Manages the transfer of                             **short** data between a property of an OLE control and a                             **short** data member.|  
|[DDX_OCShortRO](../Topic/DDX_OCShortRO.md)|Manages the transfer of                             **short** data between a read-only property of an OLE control and a                             **short** data member.|  
|[DDX_OCText](../Topic/DDX_OCText.md)|Manages the transfer of                             **CString** data between a property of an OLE control and a                             **CString** data member.|  
|[DDX_OCTextRO](../Topic/DDX_OCTextRO.md)|Manages the transfer of                             **CString** data between a read-only property of an OLE control and a                             **CString** data member.|  
  
##  <a name="ddx_ocbool"></a>  DDX_OCBool  
 The                 `DDX_OCBool` function manages the transfer of                 **BOOL** data between a property of an OLE control in a dialog box, form view, or control view object and a                 **BOOL** data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCBool(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   BOOL&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocboolro"></a>  DDX_OCBoolRO  
 The                 `DDX_OCBoolRO` function manages the transfer of                 **BOOL** data between a read-only property of an OLE control in a dialog box, form view, or control view object and a                 **BOOL** data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCBoolRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   BOOL&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_occolor"></a>  DDX_OCColor  
 The                 `DDX_OCColor` function manages the transfer of                 **OLE_COLOR** data between a property of an OLE control in a dialog box, form view, or control view object and a                 **OLE_COLOR** data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCColor(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   OLE_COLOR&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_occolorro"></a>  DDX_OCColorRO  
 The                 `DDX_OCColorRO` function manages the transfer of                 **OLE_COLOR** data between a read-only property of an OLE control in a dialog box, form view, or control view object and a                 **OLE_COLOR** data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCColorRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   OLE_COLOR &   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocfloat"></a>  DDX_OCFloat  
 The                 `DDX_OCFloat` function manages the transfer of                 **float** (or                 **double**) data between a property of an OLE control in a dialog box, form view, or control view object and a                 **float** (or                 **double**) data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCFloat(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   float&   
value  
);  
void AFXAPI DDX_OCFloat(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   double&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocfloatro"></a>  DDX_OCFloatRO  
 The                 `DDX_OCFloatRO` function manages the transfer of                 **float** (or                 **double**) data between a read-only property of an OLE control in a dialog box, form view, or control view object and a                 **float** (or                 **double**) data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCFloatRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   float&   
value  
);  
void AFXAPI DDX_OCFloatRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   double&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocint"></a>  DDX_OCInt  
 The                 `DDX_OCInt` function manages the transfer of                 `int` (or                 **long**) data between a property of an OLE control in a dialog box, form view, or control view object and a                 `int` (or                 **long**) data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCInt(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   int&   
value  
);  
void AFXAPI DDX_OCInt(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   long&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocintro"></a>  DDX_OCIntRO  
 The                 `DDX_OCIntRO` function manages the transfer of                 `int` (or                 **long**) data between a read-only property of an OLE control in a dialog box, form view, or control view object and a                 `int` (or                 **long**) data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCIntRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   int&   
value  
);  
void AFXAPI DDX_OCIntRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   long&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocshort"></a>  DDX_OCShort  
 The                 `DDX_OCShort` function manages the transfer of short data between a property of an OLE control in a dialog box, form view, or control view object and a short data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCShort(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   short&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_ocshortro"></a>  DDX_OCShortRO  
 The                 `DDX_OCShortRO` function manages the transfer of short data between a read-only property of an OLE control in a dialog box, form view, or control view object and a short data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCShortRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   short&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_octext"></a>  DDX_OCText  
 The                 **DDX_OCText** function manages the transfer of                 **CString** data between a property of an OLE control in a dialog box, form view, or control view object and a                 **CString** data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCText(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   CString&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 **CDataExchange** object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
##  <a name="ddx_octextro"></a>  DDX_OCTextRO  
 The                 `DDX_OCTextRO` function manages the transfer of                 `CString` data between a read-only property of an OLE control in a dialog box, form view, or control view object and a                 `CString` data member of the dialog box, form view, or control view object.  
  
```  
  
void AFXAPI DDX_OCTextRO(  
   CDataExchange*   
pDX  
,  
   int   
nIDC  
,  
   DISPID   
dispid  
,  
   CString&   
value  
);  
  
```  
  
### Parameters  
 `pDX`  
 A pointer to a                                 `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an OLE control in the dialog box, form view, or control view object.  
  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 *value*  
 A reference to a member variable of the dialog box, form view or control view object with which data is exchanged.  
  
### Remarks  
 For more information about DDX, see                         [Dialog Data Exchange and Validation](../VS_visualcpp/Dialog-Data-Exchange-and-Validation.md).  
  
## See Also  
 [Macros and Globals](../VS_visualcpp/MFC-Macros-and-Globals.md)