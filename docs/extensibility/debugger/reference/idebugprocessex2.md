---
title: IDebugProcessEx2 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProcessEx2
helpviewer_keywords:
- IDebugProcessEx2 interface
ms.assetid: 44e309ba-1d6f-499b-aa7e-9b34858a6d57
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7fa10fb5ebe2f9a78d44997c29ae51bc02e2c842
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49934933"
---
# <a name="idebugprocessex2"></a>IDebugProcessEx2
此接口允许的会话调试管理器 (SDM) 通知过程将附加到或与进程分离。  
  
## <a name="syntax"></a>语法  
  
```  
IDebugProcessEx2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 自定义端口提供程序在与相同的对象上实现此接口[IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)接口以便：  
  
- 支持跟踪的会话连接到的进程  
  
- 支持自动附加跨多个调试引擎  
  
  如果还选择能自定义端口供应商可以实现此接口。  
  
## <a name="notes-for-callers"></a>调用方的说明  
  
-   SDM 调用[QueryInterface](/cpp/atl/queryinterface)上`IDebugProcess2`接口，以获得此接口。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 下表显示的方法`IDebugProcessEx2`。  
  
|方法|描述|  
|------------|-----------------|  
|[附加](../../../extensibility/debugger/reference/idebugprocessex2-attach.md)|通知会话现在正在调试的进程的进程。|  
|[分离](../../../extensibility/debugger/reference/idebugprocessex2-detach.md)|通知该过程在会话不再调试进程。|  
|[AddImplicitProgramNodes](../../../extensibility/debugger/reference/idebugprocessex2-addimplicitprogramnodes.md)|将添加一系列的调试引擎的程序节点。|  
  
## <a name="remarks"></a>备注  
 此接口是专用 SDM 和进程之间。  
  
## <a name="requirements"></a>要求  
 标头： Portpriv.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)