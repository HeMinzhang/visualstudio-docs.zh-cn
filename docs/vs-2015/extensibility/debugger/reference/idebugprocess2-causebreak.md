---
title: IDebugProcess2::CauseBreak |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugProcess2::CauseBreak
helpviewer_keywords:
- IDebugProcess2::CauseBreak
ms.assetid: efda8865-2319-4d53-90bf-6d9d74cd5195
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9d50452e234ea56631c1c77eabff372a63f01e4d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47480644"
---
# <a name="idebugprocess2causebreak"></a>IDebugProcess2::CauseBreak
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[IDebugProcess2::CauseBreak](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprocess2-causebreak)。  
  
下一步，它是程序在此过程中运行代码的请求中断并发送[IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)事件对象。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT CauseBreak(   
   void  
);  
```  
  
```csharp  
int CauseBreak();  
```  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="see-also"></a>请参阅  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
