---
title: IDiaSession::findAcceleratorInlineesByName |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: e203e5c2-6563-43fa-be56-3063955043ab
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 240315fed330c72a8fe180056642c9aff0fb96aa
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49864044"
---
# <a name="idiasessionfindacceleratorinlineesbyname"></a>IDiaSession::findAcceleratorInlineesByName
返回与指定为内联函数名称相对应的内嵌帧的符号的枚举。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT findAcceleratorInlineeLinesByName (   
   LPCOLESTR             name,  
   DWORD                 option,  
   IDiaEnumSymbols**     ppResult  
);  
```  
  
#### <a name="parameters"></a>参数  
 `name`  
 [in]要搜索的被内联方函数名称。  
  
 `option`  
 [in]内联搜索帧的时要使用的名称搜索选项对应于`name`。 有关详细信息，请参阅[NameSearchOptions 枚举](../../debugger/debug-interface-access/namesearchoptions.md)。  
  
 `ppResult`  
 [out]一个指向`IDiaEnumSymbols`使用结果初始化的接口指针。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 此函数将搜索仅在加速器存根 （stub） 函数中的内联函数。 它会忽略本机 c + + 过程记录。  
  
## <a name="see-also"></a>请参阅  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)