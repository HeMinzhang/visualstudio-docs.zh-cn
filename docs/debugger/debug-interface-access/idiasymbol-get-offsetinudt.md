---
title: 'Idiasymbol:: Get_offsetinudt |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_offsetInUdt method
ms.assetid: 442f20d9-9d6a-44a1-83fb-c3f8c14b6c97
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 48b13de8a9d1680ae4e2a6a94a4fda120a74a18e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49911416"
---
# <a name="idiasymbolgetoffsetinudt"></a>IDiaSymbol::get_offsetInUdt
检索到用户定义类型 (UDT) 的用户定义的类型中的成员开始的偏移量。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT get_offsetInUdt(   
   DWORD* pRetVal)  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRetVal`  
 [out]返回以字节为单位的符号位置的偏移量。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回`S_FALSE`或错误代码。  
  
> [!NOTE]
>  返回值为`S_FALSE`表示该属性不是可用于符号。  
  
## <a name="remarks"></a>备注  
 仅在优化版本中的本地记录中使用此函数。  
  
## <a name="requirements"></a>要求  
 标头： Dia2.h  
  
 库： diaguids.lib  
  
 DLL: msdia100.dll  
  
## <a name="see-also"></a>请参阅  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)