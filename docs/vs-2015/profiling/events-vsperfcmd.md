---
title: Events (VSPerfCmd) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: eb139327-4783-4f2a-874c-efad377a7be4
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b67fbdb021cb39edd8899d537db368c18a6421ff
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49215262"
---
# <a name="events-vsperfcmd"></a>Events (VSPerfCmd)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe“Events”选项控制 Windows 事件跟踪 (ETW) 日志记录。 会将 ETW 数据保存到独立于探查器数据文件的 .etl 文件中。 可以使用 [VSPerfReport](../profiling/vsperfreport.md) /summary:etw 命令在报告中查看这些数据。  
  
 在调用 VSPerfCmd Shutdown 命令停止分析之前，可以随时调用“Events”选项。  
  
## <a name="syntax"></a>语法  
  
```  
VSPerfCmd.exe /events {On|Off} {Guid|ProviderName} [,Flags[,Level]  
```  
  
#### <a name="parameters"></a>参数  
 On&#124;Off  
 开始或停止收集事件数据。  
  
 `Guid`  
 提供程序控件的 GUID。  
  
 `ProviderName`  
 向 Windows Management Instrumentation (WMI) 注册的提供程序的名称。  
  
 `Flags`  
 以“0x”为前缀的十六进制标志值，由事件提供程序定义。  
  
 `Level`  
 指定收集的数据量。 `Level` 由事件提供程序定义。  
  
 “Events”选项将以下内核关键字识别为提供程序名称：  
  
 **Process**  
 进程事件  
  
 **线程**  
 线程事件  
  
 **Image**  
 映像加载和卸载事件  
  
 **Disk**  
 磁盘 I/O 事件  
  
 **文件**  
 文件 I/O 事件  
  
 **Hardfault**  
 硬页面错误  
  
 **Pagefault**  
 软页错误  
  
 **Network**  
 网络事件  
  
 **Registry**  
 注册表访问事件  
  
 请注意，内核提供程序只能处于启用状态。 在监视器关闭之前，既不能禁用它，也不能修改它的标志。  
  
## <a name="remarks"></a>备注  
  
> [!NOTE]
>  启用 CLR ETW 事件后，跟踪视图报告中还将收集额外的启动数据。 若要将启动事件从报告中排除，请使用以下命令：  
  
```  
C:\<path>VSPerfCmd -events on, \".NET Common Language Runtime\", 0x7fffffff, 5  
```  
  
> [!IMPORTANT]
>  如果不排除启动事件，则由于这些事件未在托管对象格式 (MOF) 文件中列出，它们将在报告中显示为 GUID。 有关详细信息，请参阅 Microsoft 网站上的此页面：[托管对象格式 (MOF) 文件示例](http://go.microsoft.com/fwlink/?linkid=37118)。  
  
## <a name="see-also"></a>请参阅  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [分析独立应用程序](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [分析 ASP.NET Web 应用程序](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [分析服务](../profiling/command-line-profiling-of-services.md)



