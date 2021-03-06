---
title: "IDiaSession::findAcceleratorInlineesByName | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
ms.assetid: e203e5c2-6563-43fa-be56-3063955043ab
caps.latest.revision: 6
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# IDiaSession::findAcceleratorInlineesByName
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDiaSession::findAcceleratorInlineesByName](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/idiasession-findacceleratorinlineesbyname).  
  
Returns an enumeration of symbols for inline frames corresponding to the specified inline function name.  
  
## Syntax  
  
```cpp#  
HRESULT findAcceleratorInlineeLinesByName (   
   LPCOLESTR             name,  
   DWORD                 option,  
   IDiaEnumSymbols**     ppResult  
);  
```  
  
#### Parameters  
 `name`  
 [in] The inlinee function name to be searched.  
  
 `option`  
 [in] The name search options to be used when searching for inline frames that correspond to `name`. For more information, see [NameSearchOptions Enumeration](../../debugger/debug-interface-access/namesearchoptions.md).  
  
 `ppResult`  
 [out] A pointer to an `IDiaEnumSymbols` interface pointer that is initialized with the result.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This function searches for inlinees only within Accelerator stub functions. It ignores native C++ procedure records.  
  
## See Also  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



