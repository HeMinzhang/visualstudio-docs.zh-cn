---
title: '&lt;param&gt; (JavaScript) |Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- <param> JavaScript XML tag
- param JavaScript XML tag
ms.assetid: 2c4e0167-c1dd-4e54-83f1-c437856bddc1
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b1178fc6ff2cb5b4664930eaa70fd3de5ebed0f5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49949066"
---
# <a name="ltparamgt-javascript"></a>&lt;param&gt; (JavaScript)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

在函数或方法中指定的参数的文档信息。  
  
## <a name="syntax"></a>语法  
  
```  
<param name="parameterName" type="ParameterType"  
    integer="true|false" domElement="true|false"  
    mayBeNull="true|false" elementType="ArrayElementType"  
    elementInteger="true|false" elementDomElement="true|false"  
    elementMayBeNull="true|false" locid="descriptionID"  
    parameterArray="true|false" optional="true|false"  
    value="code">description  
</param>  
```  
  
#### <a name="parameters"></a>参数  
 `name`  
 必须的。 参数的名称。  
  
 `type`  
 可选。 参数的数据类型。 类型可以是以下值之一：  
  
- ECMAScript 语言键入在 ECMAScript 5 规范中，如`Number`和`Object`。  
  
- DOM 对象，例如`HTMLElement`， `Window`，和`Document`。  
  
- JavaScript 构造函数。  
  
  `integer`  
  可选。 如果`type`是`Number`，指定参数是否为整数。 设置为`true`以指示该参数是一个整数; 否则，将设置为`false`。 Visual Studio 不使用此属性以提供 IntelliSense 信息。  
  
  `domElement`  
  可选。 此属性已弃用;`type`特性将优先于此属性。 此属性指定有案可稽的参数是否为 DOM 元素。 设置为`true`来指定该参数是一个 DOM 元素; 否则，将设置为`false`。 如果`type`未设置属性和`domElement`设置为`true`，IntelliSense 将有案可稽的参数视为`HTMLElement`执行语句完成时。  
  
  `mayBeNull`  
  可选。 指定是否可以设置有案可稽的参数为 null。 设置为`true`若要指示参数可设置为 null; 否则为将设置为`false`。 默认值为 `false`。 Visual Studio 不使用此属性以提供 IntelliSense 信息。  
  
  `elementType`  
  可选。 如果`type`是`Array`，此属性指定数组中元素的类型。  
  
  `elementInteger`  
  可选。 如果`type`是`Array`并`elementType`是`Number`，此属性指定数组中的元素是否为整数。 设置为`true`来指示数组中的元素都是整数; 否则，将设置为`false`。 Visual Studio 不使用此属性以提供 IntelliSense 信息。  
  
  `elementDomElement`  
  可选。 此属性已弃用;`elementType`特性将优先于此属性。 如果`type`是`Array`，此属性指定数组中的元素是否 DOM 元素。 设置为`true`来指定元素的 DOM 元素; 否则，将设置为`false`。 如果`elementType`未设置属性和`elementDomElement`设置为`true`，IntelliSense 将作为数组中的每个元素`HTMLElement`执行语句完成时。  
  
  `elementMayBeNull`  
  可选。 如果`type`是`Array`，指定是否可以设置数组中的元素为 null。 设置为`true`若要指示为 null; 否则为，可以设置数组中的元素，将设置为`false`。 默认值为 `false`。 Visual Studio 不使用此属性以提供 IntelliSense 信息。  
  
  `locid`  
  可选。 有关参数的本地化信息的标识符。 该标识符是任一成员 ID 或其对应于`name`属性在 OpenAjax 元数据定义消息绑定中的值。 标识符类型取决于中指定的格式[ \<loc >](../ide/loc-javascript.md)元素。  
  
  `parameterArray`  
  可选。 指定是否可以在函数调用中，类似于重复中支持参数重复有案可稽的参数`String.format`函数。 设置为`true`若要指示该参数可重复; 否则为将设置为`false`。 Visual Studio 不使用此属性以提供 IntelliSense 信息。  
  
  `optional`  
  可选。 指定是否有案可稽的参数是可选调用的函数中。 设置为`true`若要指示该参数是可选的; 否则为将设置为`false`。  
  
  `value`  
  可选。 指定应将使用由评估 IntelliSense 而不是函数代码本身的代码。 可以使用此属性是未定义的参数类型时提供类型信息。 例如，可以使用`value=’1’`将参数类型为数字。  
  
  `description`  
  可选。 参数的说明。  
  
## <a name="remarks"></a>备注  
 所需的唯一属性是`name`。 所有其他属性是可选的。  
  
 元素用于进行批注的函数，如[\<摘要 >](../ide/summary-javascript.md)， [ \<param >](../ide/param-javascript.md)，以及[\<返回 >](../ide/returns-javascript.md)，必须放置在任何语句之前在函数体。  
  
 如果有多个`<param>`元素具有相同的名称，其中一个`<param>`使用元素和冗余元素将被忽略。 确定使用哪个元素的行为未定义。 如果`name`引用不存在参数，将忽略该元素。  
  
## <a name="example"></a>示例  
 下面的代码示例演示如何使用`<param>`元素。  
  
```javascript  
function areaFunction(radiusParam)  
{  
    /// <summary>Determines the area of a circle when provided a radius parameter.</summary>  
    /// <param name="radiusParam" type="Number">The radius of the circle.</param>  
    /// <returns type="Number">The area.</returns>  
    var areaVal;  
    areaVal = Math.PI * radiusParam * radiusParam;  
    return areaVal;  
}  
  
// Uses of <param> with the value attribute.  
  
function calculate(a) {  
    /// <param name='a' value='1'/>  
    a.    // Completion list for a Number.  
}  
  
function calculate(a) {  
    /// <param name='a' value='{x:0,y:0}'/>  
    a.    // x and y appear in the completion list.  
}  
  
```  
  
## <a name="see-also"></a>请参阅  
 [XML 文档注释](../ide/xml-documentation-comments-javascript.md)



