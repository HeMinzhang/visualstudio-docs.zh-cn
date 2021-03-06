---
title: IEnumDebugThreads2 |Microsoft Docs
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
- IEnumDebugThreads2
helpviewer_keywords:
- IEnumDebugThreads2
ms.assetid: 1854f078-3b49-42c2-b65b-33e3b506fd63
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: aff3103d122063277b2f935d2cb6f30353434ae6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49269082"
---
# <a name="ienumdebugthreads2"></a>IEnumDebugThreads2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此界面枚举当前调试会话中运行的线程。  
  
## <a name="syntax"></a>语法  
  
```  
IEnumDebugThreads2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 调试引擎 (DE) 实现此接口来表示在程序中的主题的列表。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 调用[EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md)获取表示的进程中运行的所有程序中的所有线程列表的此接口。 调用[EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md)获取表示在程序中运行的线程的列表的此接口。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 下表显示的方法`IEnumDebugThreads2`。  
  
|方法|描述|  
|------------|-----------------|  
|[下一篇](../../../extensibility/debugger/reference/ienumdebugthreads2-next.md)|检索指定的数目的枚举序列中的线程。|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugthreads2-skip.md)|将跳过指定的数目的枚举序列中的线程。|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugthreads2-reset.md)|将枚举序列重置到开头。|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugthreads2-clone.md)|创建包含相同枚举状态与当前的枚举器。|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugthreads2-getcount.md)|获取一个枚举器中的线程数。|  
  
## <a name="remarks"></a>备注  
 Visual Studio 通常将获取此接口，以更新**线程**窗口以及关于获取列表中，在第一个线程，以便调用[Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)，[继续](../../../extensibility/debugger/reference/idebugprocess3-continue.md)，和[步骤](../../../extensibility/debugger/reference/idebugprocess3-step.md)。  
  
## <a name="requirements"></a>要求  
 标头： msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprocess2-enumthreads.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md)   
 [步骤](../../../extensibility/debugger/reference/idebugprocess3-step.md)   
 [继续](../../../extensibility/debugger/reference/idebugprocess3-continue.md)   
 [Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)

