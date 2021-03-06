---
title: stackalloc 关键字 - C# 参考
ms.custom: seodec18
ms.date: 04/12/2018
f1_keywords:
- stackalloc_CSharpKeyword
- stackalloc
helpviewer_keywords:
- stackalloc keyword [C#]
ms.openlocfilehash: 61a27e777a1919a2a6fc5140a311835a8f3daba9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59480802"
---
# <a name="stackalloc-c-reference"></a>stackalloc（C# 参考）

使用 `stackalloc` 关键字在堆栈上分配内存块。

```csharp
Span<int> block = stackalloc int[100];
```

将分配的块分配给 <xref:System.Span%601?displayName=nameWithType>（而不是 `int*`），可以在安全块中实现堆栈分配。 不需要 `unsafe` 上下文。

## <a name="remarks"></a>备注

此关键字仅在局部变量初始值设定项中有效。 以下代码导致编译器错误。

```csharp
int* block;
// The following assignment statement causes compiler errors. You
// can use stackalloc only when declaring and initializing a local
// variable.
block = stackalloc int[100];
Span<int> span;
// The following assignment statement causes compiler errors. You
// can use stackalloc only when declaring and initializing a local
// variable.
span = stackalloc int[100];
```

自 C# 7.3 起，可以对 `stackalloc` 数组使用数组初始值设定项语法。 以下所有声明都声明了一个包含三个元素的数组，这三个元素的值为整数 `1`、`2` 和 `3`。 第二个初始化将内存分配到 <xref:System.ReadOnlySpan%601>，指明无法修改内存。

```csharp
// Valid starting with C# 7.3
Span<int> first = stackalloc int[3] { 1, 2, 3 };
ReadOnlySpan<int> second = stackalloc int[] { 1, 2, 3 };
Span<int> third = stackalloc[] { 1, 2, 3 };
```

当涉及指针类型时，`stackalloc` 需要 [unsafe](unsafe.md) 上下文。 有关详细信息，请参阅[不安全代码和指针](../../programming-guide/unsafe-code-pointers/index.md)。

`stackalloc` 就像 C 运行时库中的 [_alloca](/cpp/c-runtime-library/reference/alloca)。

## <a name="examples"></a>示例

下面的示例计算并显示 Fibonacci 序列中的前 20 个数字。 每个数字是前两个数字的总和。 在此代码中，在堆栈上分配足够大的可包含 20 个 `int` 类型元素的内存块，而不是在堆上分配。 块的地址存储在 `Span` `fib` 中。 此内存不受垃圾回收的限制，因此不必对其进行单边锁定（使用 [fixed](fixed-statement.md)）。 内存块的生存期受到定义此内存块的方法的生存期的限制。 在方法返回之前，无法释放内存。

[!code-csharp[csrefKeywordsOperator#15](~/samples/snippets/csharp/keywords/StackAllocExamples.cs#1)]

下面的示例将 `stackalloc` 整数数组初始化为位掩码，其中每个元素内都有一个位集。 下面展示了自 C# 7.3 起新增的初始值设定项语法：

[!code-csharp[csrefKeywordsOperator#15](~/samples/snippets/csharp/keywords/StackAllocExamples.cs#2)]

## <a name="security"></a>安全性

应尽可能使用 <xref:System.Span%601> 或 <xref:System.ReadOnlySpan%601>，因为不安全代码的安全性低于安全替代项。 即使与指针一起使用，使用 `stackalloc` 也会在公共语言运行时 (CLR) 中自动启用缓冲区溢出检测功能。 如果检测到缓冲区溢出，则将尽快终止进程，以便将执行恶意代码的可能性降到最低。

## <a name="c-language-specification"></a>C# 语言规范

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>请参阅

- [C# 参考](../index.md)
- [C# 编程指南](../../programming-guide/index.md)
- [C# 关键字](index.md)
- [运算符关键字](operator-keywords.md)
- [不安全代码和指针](../../programming-guide/unsafe-code-pointers/index.md)
