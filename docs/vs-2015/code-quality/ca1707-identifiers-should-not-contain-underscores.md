---
title: CA1707： 标识符不应包含下划线 |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IdentifiersShouldNotContainUnderscores
- CA1707
helpviewer_keywords:
- CA1707
- IdentifiersShouldNotContainUnderscores
ms.assetid: 5fb539ef-c304-4323-90c0-b14386da9774
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0aeea5c113ebebe33d4c371fed1a5c46da4e735e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49211063"
---
# <a name="ca1707-identifiers-should-not-contain-underscores"></a>CA1707：标识符不应包含下划线
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio 2017 的最新文档，请参阅[CA1707： 标识符不应包含下划线](https://docs.microsoft.com/visualstudio/code-quality/ca1707-identifiers-should-not-contain-underscores)docs.microsoft.com 上。  
  
|||  
|-|-|  
|TypeName|IdentifiersShouldNotContainUnderscores|  
|CheckId|CA1707|  
|类别|Microsoft.Naming|  
|是否重大更改|-对程序集引发时中断<br /><br /> 无间断-类型参数上发生|  
  
## <a name="cause"></a>原因  
 标识符名称包含下划线 (_) 字符。  
  
## <a name="rule-description"></a>规则说明  
 按照约定，标识符名称不包含下划线 (_) 字符。 此规则检查命名空间、 类型、 成员和参数。  
  
 命名约定提供了通用的外观对于库面向公共语言运行时。 这会减少所需的新软件库，并会增加客户信心库由必须在托管代码中开发的专业知识的人学习曲线。  
  
## <a name="how-to-fix-violations"></a>如何解决冲突  
 从名称中删除所有下划线字符。  
  
## <a name="when-to-suppress-warnings"></a>何时禁止显示警告  
 不禁止显示此规则发出的警告。  
  
## <a name="related-rules"></a>相关的规则  
 [CA1709：标识符的大小写应当正确](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)  
  
 [CA1708：标识符不应仅以大小写进行区分](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

