---
title: 将控件绑定到 Visual Studio 中的数据
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- data, displaying
- data sources, displaying data
- Data Sources window
- dislaying data
ms.assetid: be8b6623-86a6-493e-ab7a-050de4661fd6
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: ca43b4daea5c5bb95a0752eeae93814d234e9a62
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49923012"
---
# <a name="bind-controls-to-data-in-visual-studio"></a>将控件绑定到 Visual Studio 中的数据
通过将数据绑定到控件，可以向应用程序的用户显示数据。 可以通过将项从创建这些数据绑定控件**数据源**窗口拖到设计图面上或在 Visual Studio 中的图面上的控件。

 本主题描述可用于创建数据绑定控件的数据源。 它还描述了数据绑定中涉及的一些常规任务。 有关如何创建数据绑定控件的更多具体详细信息，请参阅[绑定 Windows 窗体控件添加到 Visual Studio 中的数据](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)并[控件添加到 Visual Studio 中的数据绑定 WPF](../data-tools/bind-wpf-controls-to-data-in-visual-studio.md)。

## <a name="data-sources"></a>数据源
 在数据绑定的上下文中，数据源表示可绑定到您的用户界面的内存中的数据。 在实践中，数据源可以是实体框架类、 数据集、 封装.NET 代理对象、 LINQ to SQL 类或任何.NET 对象或集合中的服务终结点。 某些数据源，可以通过将项从创建数据绑定控件**数据源**窗口中，而其他数据源不能。 下表显示了支持的数据源。


| 数据源 | 中的拖放支持**Windows 窗体设计器** | 中的拖放支持**WPF 设计器** | 中的拖放支持**Silverlight 设计器** |
| - | - | - | - |
| 数据集 | 是 | 是 | 否 |
| 实体数据模型 | 是<sup>1</sup> | 是 | 是 |
| LINQ to SQL 类 | 否<sup>2</sup> | 否<sup>2</sup> | 否<sup>2</sup> |
| 服务 (包括[!INCLUDE[ssAstoria](../data-tools/includes/ssastoria_md.md)]，WCF 服务和 web 服务) | 是 | 是 | 是 |
| 对象 | 是 | 是 | 是 |
| SharePoint | 是 | 是 | 是 |

 1. 生成模型使用**实体数据模型**向导中，然后将这些对象拖到设计器。

 2. LINQ to SQL 类不显示在**数据源**窗口。 不过，你可以添加基于 LINQ to SQL 类的新对象数据源，然后将这些对象拖到设计器来创建数据绑定控件。 有关详细信息，请参阅[演练： 创建 LINQ to SQL 类 （O-R 设计器）](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)。

## <a name="data-sources-window"></a>“数据源”窗口
 数据源形式提供给你的项目中的项**数据源**窗口。 此窗口可见，或从可访问**视图**菜单中，当窗体设计图面是您的项目中的活动窗口。 可以将项从此窗口来创建绑定到基础数据的控件，还可以通过右键单击配置数据源。

 ![“数据源”窗口](../data-tools/media/raddata-data-sources-window.png)

 将出现在每种数据类型**数据源**窗口中，默认值创建一个控件时将项拖动到设计器。 中的项拖之前**数据源**窗口中，你可以创建的控件。 有关详细信息，请参阅[设置从数据源窗口中拖动时创建的控件](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md)。

## <a name="tasks-involved-in-binding-controls-to-data"></a>控件绑定到数据中涉及的任务
 下表列出了一些最常见的任务所需执行将控件绑定到数据。

|任务|详细信息|
|----------| - |
|打开**数据源**窗口。|在编辑器中打开设计图面，然后选择**视图** > **数据源**。|
|将数据源添加到你的项目。|[添加新数据源](../data-tools/add-new-data-sources.md)|
|设置中的项拖时创建的控件**数据源**到设计器窗口。|[设置从“数据源”窗口中拖动时要创建的控件](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md)|
|修改与中的项相关联的控件列表**数据源**窗口。|[向“数据源”窗口添加自定义控件](../data-tools/add-custom-controls-to-the-data-sources-window.md)|
|创建数据绑定控件。|[在 Visual Studio 中将 Windows 窗体控件绑定到数据](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)<br /><br /> [在 Visual Studio 中将 WPF 控件绑定到数据](../data-tools/bind-wpf-controls-to-data-in-visual-studio.md)|
|将绑定到对象或集合。|[Visual Studio 中的绑定对象](../data-tools/bind-objects-in-visual-studio.md)|
|在 UI 中显示的数据进行筛选。|[在 Windows 窗体应用程序中对数据进行筛选和排序](../data-tools/filter-and-sort-data-in-a-windows-forms-application.md)|
|自定义控件的标题。|[自定义 Visual Studio 创建数据绑定控件的标题的方式](../data-tools/customize-how-visual-studio-creates-captions-for-data-bound-controls.md)|

## <a name="see-also"></a>请参阅

- [适用于 NET 的 Visual Studio Data Tools](../data-tools/visual-studio-data-tools-for-dotnet.md)
- [Windows 窗体数据绑定](/dotnet/framework/winforms/windows-forms-data-binding)