---
title: -unsafe（C# 编译器选项）
ms.date: 04/25/2018
f1_keywords:
- /unsafe
helpviewer_keywords:
- -unsafe compiler option [C#]
- unsafe compiler option [C#]
- /unsafe compiler option [C#]
ms.openlocfilehash: 4cfd7c82bc2cbf816164b235642c0647eeb7e5b6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337326"
---
# <a name="-unsafe-c-compiler-options"></a>-unsafe（C# 编译器选项）
-unsafe 编译器选项允许使用[不安全](../../../csharp/language-reference/keywords/unsafe.md)关键字进行编译的代码。  
  
## <a name="syntax"></a>语法  
  
```console  
-unsafe  
```  
  
## <a name="remarks"></a>备注  
 有关不安全代码的详细信息，请参阅[不安全代码和指针](../../../csharp/programming-guide/unsafe-code-pointers/index.md)。  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 开发环境中设置此编译器选项  
  
1. 打开项目的“属性”页。  
  
2. 单击“生成”属性页。  
  
3. 选中“允许不安全代码”复选框。  
  
### <a name="to-add-this-option-in-a-csproj-file"></a>向 csproj 文件添加此选项

打开项目的 csproj 文件，并添加以下元素：

```xml
  <PropertyGroup>
    <AllowUnsafeBlocks>true</AllowUnsafeBlocks>
  </PropertyGroup>
```

 有关如何以编程方式设置此编译器选项的信息，请参阅 <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>。  
  
## <a name="example"></a>示例  
 针对不安全模式编译 `in.cs`：  
  
```console  
csc -unsafe in.cs  
```  
  
## <a name="see-also"></a>请参阅

- [C# 编译器选项](../../../csharp/language-reference/compiler-options/index.md)
- [管理项目和解决方案属性](/visualstudio/ide/managing-project-and-solution-properties)
