---
title: shell 命令 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- tools.shell
helpviewer_keywords:
- exe files
- Shell command
- Tools.Shell command
- executables, running from Visual Studio
- .exe files
- Shell, launching exe files
- Visual Studio, executables from
ms.assetid: 737fda23-b852-45c4-a9fe-41cbce6ba70f
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5f760e449921a45f7ad22a3d81376bca432fe24a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49242211"
---
# <a name="shell-command"></a>shell 命令
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
从 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] 内启动可执行程序。  
  
## <a name="syntax"></a>语法  
  
```  
Tools.Shell [/command] [/output] [/dir:folder] path [args]  
```  
  
## <a name="arguments"></a>自变量  
 `path`  
 必须的。 要执行的文件或要打开的文档的路径和文件名。 如果在环境变量 PATH 的某个目录中没有指定的文件，则必须使用完整路径。  
  
 `args`  
 可选。 要传递给被调用的程序的任何参数。  
  
## <a name="switches"></a>开关  
 /commandwindow [或] /command [或] /c [或] /cmd  
 可选。 指定在“命令”窗口中显示可执行文件的输出。  
  
 /dir:`folder` [或] /d:`folder`  
 可选。 指定程序运行时要设置的工作目录。  
  
 /outputwindow [或] /output [或] /out [或] /o  
 可选。 指定在“输出”窗口中显示可执行文件的输出。  
  
## <a name="remarks"></a>备注  
 必须在 `Tools.Shell` 之后立即指定 /dir /o /c 开关。 可执行文件的名称之后指定的任何内容都会作为命令行参数传递给它。  
  
 可以使用预定义的别名 `Shell` 替换 `Tools.Shell`。  
  
> [!CAUTION]
>  如果 `path` 参数提供了目录路径和文件名，则应该将整个路径名引在原义引号 (""") 中，如下所示：  
  
```  
Tools.Shell """C:\Program Files\SomeFile.exe"""  
```  
  
 `Shell` 处理器将三个为一组的每组双引号 (""") 解释为一个双引号字符。 因此，上述示例实际上将以下路径字符串传递给 `Shell` 命令：  
  
```  
"C:\Program Files\SomeFile.exe"  
```  
  
> [!CAUTION]
>  如果未将路径字符串引在文本引号 (""") 中，Windows 将只使用第一个空格前的字符串部分。 例如，如果上面的路径字符串引用不正确，则 Windows 将查找 C:\ 根目录中的名为“Program”的文件。 如果 C:\Program.exe 可执行文件实际可用，则即使是由非法篡改安装的，Windows 也会尝试执行该程序，而不执行所需的“c:\Program Files\SomeFile.exe”程序。  
  
## <a name="example"></a>示例  
 以下命令使用 xcopy.exe 将文件 `MyText.txt` 复制到 `Text` 文件夹。 xcopy.exe 的输出同时显示在“命令”窗口和“输出”窗口中。  
  
```  
>Tools.Shell /o /c xcopy.exe c:\MyText.txt c:\Text\MyText.txt  
```  
  
## <a name="see-also"></a>请参阅  
 [Visual Studio 命令](../../ide/reference/visual-studio-commands.md)   
 [“命令”窗口](../../ide/reference/command-window.md)   
 [“输出”窗口](../../ide/reference/output-window.md)   
 [“查找/命令”框](../../ide/find-command-box.md)   
 [Visual Studio Command Aliases](../../ide/reference/visual-studio-command-aliases.md)



