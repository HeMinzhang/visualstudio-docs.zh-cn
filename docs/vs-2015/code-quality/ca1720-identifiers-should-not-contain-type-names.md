---
title: CA1720： 标识符不应包含类型名称 |Microsoft Docs
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
- CA1720
- IdentifiersShouldNotContainTypeNames
helpviewer_keywords:
- IdentifiersShouldNotContainTypeNames
- CA1720
ms.assetid: c95ee48f-f23a-45f0-ac9e-a3c1ecfabdea
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ec0980d312d4a65a770e63f0a23203a7e95c546f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49862328"
---
# <a name="ca1720-identifiers-should-not-contain-type-names"></a>CA1720：标识符不应包含类型名称
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|IdentifiersShouldNotContainTypeNames|
|CheckId|CA1720|
|类别|Microsoft.Naming|
|是否重大更改|重大|

## <a name="cause"></a>原因
 外部可见成员中的参数的名称包含的数据类型名称。

 或

 外部可见成员的名称包含特定于语言的数据类型名称。

## <a name="rule-description"></a>规则说明
 参数和成员的名称更好地用于进行通信来说明它们应由开发工具提供的类型及其含义。 有关成员的名称，如果必须使用数据类型名称，则使用而不是特定于语言的一个独立于语言的名称。 例如，而不是 C# 类型名称 int，使用独立于语言的数据类型名称，Int32。

 每个离散的标记参数或成员的名称被签入以下特定于语言的数据类型名称，不区分大小写的方式：

- Bool

- WChar

- Int8

- UInt8

- Short

- UShort

- Int

- UInt

- 整数

- UInteger

- Long

- ULong

- 无符号

- 签名

- Float

- float32

- float64

  此外，参数的名称是还会检查以下独立于语言的数据类型名称，不区分大小写的方式：

- 对象

- obj

- Boolean

- Char

- String

- SByte

- Byte

- UByte

- Int16

- UInt16

- Int32

- UInt32

- Int64

- UInt64

- IntPtr

- ptr

- 指针

- UInptr

- UPtr

- UPointer

- Single

- Double

- 十进制

- GUID

## <a name="how-to-fix-violations"></a>如何解决冲突
 **如果针对参数引发的：**

 在参数名的数据类型标识符替换为更好地描述其含义的术语或更通用的词条，如 value。

 **如果触发针对成员：**

 替换为与更好地描述其含义，独立于语言的同等或更通用的词条，如 value 成员的名称的特定于语言的数据类型标识符。

## <a name="when-to-suppress-warnings"></a>何时禁止显示警告
 可能需要偶尔使用的基于类型的参数和成员名称。 但是，对于新的开发，没有已知情况下，则应该禁止显示此规则的警告。 对于以前发布的库，您可能需要禁止显示此规则的警告。

## <a name="related-rules"></a>相关的规则
 [CA1709：标识符的大小写应当正确](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)

 [CA1708：标识符不应仅以大小写进行区分](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

 [CA1707：标识符不应包含下划线](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)

 [CA1719：参数名不应与成员名冲突](../code-quality/ca1719-parameter-names-should-not-match-member-names.md)



