---
title: DEBUG_ADDRESS |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- DEBUG_ADDRESS
helpviewer_keywords:
- DEBUG_ADDRESS structure
ms.assetid: 79f5e765-9aac-4b6e-82ef-bed88095e9ba
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1d5851fd9fe7224d060b1454a7123b98f77216b4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49813474"
---
# <a name="debugaddress"></a>DEBUG_ADDRESS
此结构表示地址。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct _tagDEBUG_ADDRESS {  
   ULONG32             ulAppDomainID;  
   GUID                guidModule;  
   _mdToken            tokClass;  
   DEBUG_ADDRESS_UNION addr;  
} DEBUG_ADDRESS;  
```  
  
```csharp  
public struct DEBUG_ADDRESS {  
   public uint                ulAppDomainID;  
   public Guid                guidModule;  
   public int                 tokClass;  
   public DEBUG_ADDRESS_UNION addr;  
}  
```  
  
## <a name="terms"></a>术语  
 ulAppDomainID  
 进程 id。  
  
 guidModule  
 包含此地址的模块的 GUID。  
  
 tokClass  
 确定类或类型的地址，此标记。  
  
> [!NOTE]
>  此值是特定于符号提供程序，因此具有以外的其他任何常规含义为类类型的标识符。  
  
 Addr  
 一个[DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)结构，其中包含描述单个地址类型的结构的并集。 值`addr`。`dwKind` 来自[ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)枚举，其中介绍了如何解释并集。  
  
## <a name="remarks"></a>备注  
 此结构传递给[GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)要填充的方法。  
  
 **警告 [c + +]**  
  
 如果`addr.dwKind`是`ADDRESS_KIND_METADATA_LOCAL`; 如果`addr.addr.addrLocal.pLocal`不为空值，则必须调用`Release`上标记的指针：  
  
```  
if (addr.dwKind == ADDRESS_KIND_METADATA_LOCAL &&  addr.addr.addrLocal.pLocal != NULL)  
{  
    addr.addr.addrLocal.pLocal->Release();  
}  
```  
  
## <a name="requirements"></a>要求  
 标头： sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [结构和联合](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)   
 [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)