---
title: THREADSTATE |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- THREADSTATE
helpviewer_keywords:
- THREADSTATE enumeration
ms.assetid: 62efdd7c-25b1-4fd3-9d06-ac1830a418a9
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1bc74c4b893cd7eb9aa389af31780c1b9cc8d35c
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2018
ms.locfileid: "51817303"
---
# <a name="threadstate"></a>THREADSTATE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

指定线程的状态。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
enum enum_THREADSTATE {   
   THREADSTATE_RUNNING = 0x0001,  
   THREADSTATE_STOPPED = 0x0002,  
   THREADSTATE_FRESH   = 0x0003,  
   THREADSTATE_DEAD    = 0x0004,  
   THREADSTATE_FROZEN  = 0x0005  
};  
typedef DWORD THREADSTATE;  
```  
  
```csharp  
public enum enum_THREADSTATE {   
   THREADSTATE_RUNNING = 0x0001,  
   THREADSTATE_STOPPED = 0x0002,  
   THREADSTATE_FRESH   = 0x0003,  
   THREADSTATE_DEAD    = 0x0004,  
   THREADSTATE_FROZEN  = 0x0005  
};  
```  
  
## <a name="members"></a>成员  
 THREADSTATE_RUNNING  
 指示该线程正在运行。  
  
 THREADSTATE_STOPPED  
 指示该线程已因断点而停止。  
  
 THREADSTATE_FRESH  
 指示线程已创建但尚未运行代码。  
  
 THREADSTATE_DEAD  
 指示线程出现故障。  
  
 THREADSTATE_FROZEN  
 指示该线程已冻结 （可以执行任何执行）。  
  
## <a name="remarks"></a>备注  
 用于`dwThreadState`字段[THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)结构。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [枚举](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)

