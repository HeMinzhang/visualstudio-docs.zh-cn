---
title: IDebugProcess3 |Microsoft Docs
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
- IDebugProcess3
helpviewer_keywords:
- IDebugProcess3 interface
ms.assetid: 7bd6b952-cf34-4e66-b8f6-d472dac3748f
caps.latest.revision: 25
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a5392329892c564608ab9649e29f1ff2bd2b1044
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49269697"
---
# <a name="idebugprocess3"></a>IDebugProcess3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

此接口表示正在运行的进程和其程序。 此接口作为替换多个方法中存在[IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)接口。 它提供对在过程中的所有程序控制。  
  
> [!NOTE]
>  [继续](../../../extensibility/debugger/reference/idebugprogram2-continue.md)， [Execute](../../../extensibility/debugger/reference/idebugprogram2-execute.md)，和[步骤](../../../extensibility/debugger/reference/idebugprogram2-step.md)方法已弃用，应不再使用。 使用相应的方法上`IDebugProcess3`改为接口。  
  
## <a name="syntax"></a>语法  
  
```  
IDebugProcess3 : IDebugProcess2  
```  
  
## <a name="notes-for-implementers"></a>实施者的说明  
 此接口由自定义端口提供程序作为一个组管理程序实现。 当程序作为一个组管理时，可以控制其执行和表达式计算器为建立一种语言。 此接口必须由端口提供程序实现。  
  
## <a name="notes-for-callers"></a>调用方的说明  
 此接口称为主要由会话调试管理器 (SDM) 以便与一组在此过程中标识的程序进行交互。  
  
 调用[QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3)上[IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)接口，以获得此接口。  
  
## <a name="methods-in-vtable-order"></a>Vtable 顺序中的方法  
 除了继承的方法之外[IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)，`IDebugProcess3`实现以下方法。  
  
|方法|描述|  
|------------|-----------------|  
|[Continue](../../../extensibility/debugger/reference/idebugprocess3-continue.md)|将继续执行或逐步执行过程。|  
|[Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)|开始执行的进程。|  
|[Step](../../../extensibility/debugger/reference/idebugprocess3-step.md)|步骤转发一个指令或在过程中的语句。|  
|[GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md)|获取进程已启动用于调试的原因。|  
|[SetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-sethostingprocesslanguage.md)|设置宿主的语言，以便调试引擎可以加载适当的表达式计算器。|  
|[GetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-gethostingprocesslanguage.md)|检索当前为此过程设置的语言。|  
|[DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)|此过程中禁用编辑并继续 (ENC)。<br /><br /> 自定义端口提供程序不实现此方法 (它应始终返回`E_NOTIMPL`)。|  
|[GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)|此过程获取 ENC 状态。<br /><br /> 自定义端口提供程序不实现此方法 (它应始终返回`E_NOTIMPL`)。|  
|[GetEngineFilter](../../../extensibility/debugger/reference/idebugprocess3-getenginefilter.md)|检索可用的调试引擎的唯一标识符的数组。|  
  
## <a name="requirements"></a>要求  
 标头： Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [核心接口](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)

