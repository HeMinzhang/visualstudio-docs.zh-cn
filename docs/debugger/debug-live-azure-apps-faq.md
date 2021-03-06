---
title: 快照调试常见问题解答 |Microsoft Docs
ms.date: 11/07/2017
ms.technology: vs-ide-debug
ms.topic: reference
helpviewer_keywords:
- debugger
ms.assetid: 944f1eb0-a74b-4d28-ae2b-a370cd869add
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 13b35746a7b0d639d4c954c8ef1a5221973e1abc
ms.sourcegitcommit: 0e5289414d90a314ca0d560c0c3fe9c88cb2217c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/19/2018
ms.locfileid: "39154341"
---
# <a name="frequently-asked-questions-for-snapshot-debugging-in-visual-studio"></a> Visual Studio 中进行快照调试的常见问题

下面是一系列使用快照调试器，调试实时 Azure 应用程序时，可能出现的问题。

#### <a name="what-is-the-performance-cost-of-taking-a-snapshot"></a>什么是创建快照的性能成本？

当快照调试器捕获您的应用程序的快照时，它是创建分支应用的过程和挂起的分支的副本。 当调试快照时，调试针对进程的分支的副本。 此过程，只需 10-20 毫秒，但不复制应用的完整的堆。 相反，它将复制仅页表并页面设置为复制写入。 如果再堆上更改某些应用程序的对象，然后复制到相应页。 因此，每个快照在内存中具有较小的成本 （对于大多数应用程序来说都是几百几千字节为单位）。 

#### <a name="what-happens-if-i-have-a-scaled-out-azure-app-service-multiple-instances-of-my-app"></a>如果我的 Azure 应用服务具有伸缩性 （我的应用程序的多个实例），会发生什么情况？

当您的应用程序拥有多个实例时，获取每个应用实例的快照点。只有符合指定条件的第一个快照点才创建快照。 如果有多个快照点，后续快照来自同一个实例创建的第一个快照。 记录点只将一个实例中的消息发送到输出窗口，此时每一个实例的记录点给应用日志发送消息。 

#### <a name="how-does-the-snapshot-debugger-load-symbols"></a>快照调试程序如何加载符号？

快照调试器要求您为本地或已部署应用程序到 Azure 应用服务匹配符号。 （嵌入式的 Pdb 当前不支持。）快照调试程序将自动从 Azure 应用服务下载符号。 截至 Visual Studio 2017 版本 15.2，部署Azure 应用服务时，同时部署应用程序的符号。

#### <a name="does-the-snapshot-debugger-work-against-release-builds-of-my-application"></a>快照调试器的工作原理与我的应用程序的release版本？

是-快照调试程序旨在针对release版本工作。 当快照点放置在函数中时，该函数被重新编译为debug版本，使其可调试。 快照调试器停止时，函数将返回到其release版本。 

#### <a name="can-logpoints-cause-side-effects-in-my-production-application"></a>记录点可能对在生产应用程序产生负面影响？

否- 任何添加到您的应用程序的日志消息都是经过虚拟评估的。 它们不会在应用程序中产生任何副作用。 但是，某些本机属性可能无法通过记录点访问。 

#### <a name="does-the-snapshot-debugger-work-if-my-server-is-under-load"></a>如果我的服务器是在负载中，快照调试程序是否起作用了？

是的，快照调试可用于在负载下的服务器。 快照调试器不会在服务器的内存过低时捕获快照。

#### <a name="how-do-i-uninstall-the-snapshot-debugger"></a>如何卸载快照调试器？

通过执行以下步骤在应用服务中，可以卸载快照调试器的站点扩展：

1. 通过在 Visual Studio 或 Azure 门户中的云资源管理器，关闭你的应用服务。
1. 导航到你的应用服务 Kudu 站点 (即，yourappservice。**scm**。 azurewebsites.net) 并导航到**站点扩展**。
1. 单击Snapshot Debugger 站点扩展上点击 X，将其删除。

## <a name="see-also"></a>请参阅

[在 Visual Studio 中进行调试](../debugger/index.md)  
[使用快照调试器调试实时 ASP.NET 应用](../debugger/debug-live-azure-applications.md)  
[快照调试疑难解答和已知问题](../debugger/debug-live-azure-apps-troubleshooting.md)
