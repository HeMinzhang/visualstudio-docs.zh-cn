---
title: 错误： 无法连接到计算机&lt;名称&gt;。 网络上找不到该计算机。 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.remote.dcom_disabled
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- DCOM, unable to connect error
ms.assetid: b584b5db-ef52-45ed-8561-1314da3cc5b8
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d4e2c60723827466942ea02b8881f234e38fa438
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223064"
---
# <a name="error-unable-to-connect-to-the-machine-ltnamegt-the-machine-cannot-be-found-on-the-network"></a>错误： 无法连接到计算机&lt;名称&gt;。 网络上找不到该计算机。
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

如果满足下列某项条件，则会发生此行为：  
  
-   您与远程计算机的连接中断。  
  
-   您在远程计算机上的用户帐户被禁用。  
  
-   您在远程计算机上的密码过期。  
  
### <a name="to-resolve-this-behavior"></a>解决此问题  
  
-   确保本地计算机和远程计算机处于同一个网络中。 若要执行此操作，请使用 Microsoft Windows 资源管理器（或文件资源管理器）尝试访问远程计算机。  
  
     - 和 -  
  
-   确保您用来连接远程计算机的用户帐户是启用的。  
  
     - 和 -  
  
-   确保您用来连接远程计算机的密码是有效的并且尚未过期。  
  
## <a name="see-also"></a>请参阅  
 [设置在设备上的远程工具](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)   
 [调试器设置和准备](../debugger/debugger-settings-and-preparation.md)



