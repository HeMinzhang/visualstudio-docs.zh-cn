---
title: IManagedAddin::Load
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords: ''
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: d1ea659d59e780beba3949e7cae363affa312c17
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2018
ms.locfileid: "35671729"
---
# <a name="imanagedaddinload"></a>IManagedAddin::Load
  在加载托管 VSTO 外接程序时调用。  
  
## <a name="syntax"></a>语法  
  
```csharp
HRESULT Load([in] BSTR bstrManifestURL,   
             [in] IDispatch *pdispApplication);  
```  
  
### <a name="parameters"></a>参数  
  
|参数|描述|  
|---------------|-----------------|  
|*bstrManifestURL*|VSTO 外接程序清单的完整路径。|  
|*pdispApplication*|指向表示主机应用程序加载 VSTO 外接程序 IDispatch 指针。|  
  
## <a name="return-value"></a>返回值  
 HRESULT 值，指示方法是否已成功完成。  
  
## <a name="remarks"></a>备注  
 清单是一个文件（通常是 XML 文件），提供用于帮助加载 VSTO 外接程序的信息。 例如，加载 VSTO 外接程序时，清单可以指定 VSTO 外接程序程序集的位置以及要实例化的入口点类。  
  
 *BstrManifestURL*参数包含的值`Manifest`下的项**HKEY_CURRENT_USER\Software\Microsoft\Office\\_\<应用程序名称>_ \Addins\\_\<外接程序 ID >_**  VSTO 外接程序的注册表项。 有关详细信息，请参阅[IManagedAddin 接口](../vsto/imanagedaddin-interface.md)。  
  
 实现 [IManagedAddIn::Load](../vsto/imanagedaddin-load.md) 方法以执行各项任务，例如为正在加载的 VSTO 外接程序配置应用程序域和安全策略。  
  
## <a name="see-also"></a>请参阅  
 [IManagedAddin Interface](../vsto/imanagedaddin-interface.md)   
 [IManagedAddin::Unload](../vsto/imanagedaddin-unload.md)  
  
  