---
title: with 表达式 - C# 参考
description: 了解执行 C# 记录的非破坏性转变的 with 表达式
ms.date: 11/12/2020
f1_keywords:
- with_CSharpKeyword
helpviewer_keywords:
- with expression [C#]
- with operator [C#]
ms.openlocfilehash: 8412dfe8663703d3b201fe98b5f4752da1b344cf
ms.sourcegitcommit: f99115e12a5eb75638abe45072e023a3ce3351ac
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2020
ms.locfileid: "94556707"
---
# <a name="with-expression-c-reference"></a><span data-ttu-id="4c3cb-103">with 表达式（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="4c3cb-103">with expression (C# reference)</span></span>

<span data-ttu-id="4c3cb-104">`with` 表达式在 C# 9.0 及更高版本中可用，使用修改的特定属性和字段生成其[记录](../../whats-new/csharp-9.md#record-types)操作数的副本：</span><span class="sxs-lookup"><span data-stu-id="4c3cb-104">Available in C# 9.0 and later, a `with` expression produces a copy of its [record](../../whats-new/csharp-9.md#record-types) operand with the specified properties and fields modified:</span></span>

:::code language="csharp" source="snippets/with-expression/BasicExample.cs" :::

<span data-ttu-id="4c3cb-105">如上一个示例所示，你可以使用[对象初始值设定项](../../programming-guide/classes-and-structs/object-and-collection-initializers.md)语法来指定要修改的成员及其新值。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-105">As the preceding example shows, you use [object initializer](../../programming-guide/classes-and-structs/object-and-collection-initializers.md) syntax to specify what members to modify and their new values.</span></span> <span data-ttu-id="4c3cb-106">在 `with` 表达式中，左侧操作数必须为记录类型。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-106">In a `with` expression, a left-hand operand must be of a record type.</span></span>

<span data-ttu-id="4c3cb-107">`with` 表达式的结果与表达式的操作数具有相同的运行时类型，如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="4c3cb-107">The result of a `with` expression has the same runtime type as the expression's operand, as the following example shows:</span></span>

:::code language="csharp" source="snippets/with-expression/InheritanceExample.cs" :::

<span data-ttu-id="4c3cb-108">对于引用类型成员，在复制记录时仅复制对实例的引用。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-108">In case of a reference-type member, only the reference to an instance is copied when a record is copied.</span></span> <span data-ttu-id="4c3cb-109">副本和原始记录都具有对同一引用类型实例的访问权限。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-109">Both the copy and original record have access to the same reference-type instance.</span></span> <span data-ttu-id="4c3cb-110">以下示例演示了该行为：</span><span class="sxs-lookup"><span data-stu-id="4c3cb-110">The following example demonstrates that behavior:</span></span>

:::code language="csharp" source="snippets/with-expression/ExampleWithReferenceType.cs" :::

<span data-ttu-id="4c3cb-111">任何记录类型都具有复制构造函数。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-111">Any record type has the *copy constructor*.</span></span> <span data-ttu-id="4c3cb-112">这是一个包含记录类型的单个参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-112">That is a constructor with a single parameter of the containing record type.</span></span> <span data-ttu-id="4c3cb-113">它将参数的状态复制到新的记录实例。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-113">It copies the state of its argument to a new record instance.</span></span> <span data-ttu-id="4c3cb-114">在评估 `with` 表达式时，将调用复制构造函数，以基于原始记录实例化新记录实例化。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-114">At evaluation of a `with` expression, the copy constructor gets called to instantiate a new record instance based on an original record.</span></span> <span data-ttu-id="4c3cb-115">之后，新实例将根据指定的修改进行更新。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-115">After that, the new instance gets updated according to the specified modifications.</span></span> <span data-ttu-id="4c3cb-116">默认情况下，复制构造函数是隐式的，即编译器生成的。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-116">By default, the copy constructor is implicit, that is, compiler-generated.</span></span> <span data-ttu-id="4c3cb-117">如果需要自定义记录复制语义，请显式声明具有所需行为的复制构造函数。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-117">If you need to customize the record copy semantics, explicitly declare a copy constructor with the desired behavior.</span></span> <span data-ttu-id="4c3cb-118">下面的示例使用显式复制构造函数更新前面的示例。</span><span class="sxs-lookup"><span data-stu-id="4c3cb-118">The following example updates the preceding example with an explicit copy constructor.</span></span> <span data-ttu-id="4c3cb-119">复制记录时，新的复制行为是复制列表项而不是列表引用：</span><span class="sxs-lookup"><span data-stu-id="4c3cb-119">The new copy behavior is to copy list items instead of a list reference when a record is copied:</span></span>

:::code language="csharp" source="snippets/with-expression/UserDefinedCopyConstructor.cs" :::

## <a name="c-language-specification"></a><span data-ttu-id="4c3cb-120">C# 语言规范</span><span class="sxs-lookup"><span data-stu-id="4c3cb-120">C# language specification</span></span>

<span data-ttu-id="4c3cb-121">有关详细信息，请参阅[记录功能建议说明](~/_csharplang/proposals/csharp-9.0/records.md)的以下部分：</span><span class="sxs-lookup"><span data-stu-id="4c3cb-121">For more information, see the following sections of the [records feature proposal note](~/_csharplang/proposals/csharp-9.0/records.md):</span></span>

- [<span data-ttu-id="4c3cb-122">`with`表达式</span><span class="sxs-lookup"><span data-stu-id="4c3cb-122">`with` expression</span></span>](~/_csharplang/proposals/csharp-9.0/records.md#with-expression)
- [<span data-ttu-id="4c3cb-123">复制和克隆成员</span><span class="sxs-lookup"><span data-stu-id="4c3cb-123">Copy and Clone members</span></span>](~/_csharplang/proposals/csharp-9.0/records.md#copy-and-clone-members)

## <a name="see-also"></a><span data-ttu-id="4c3cb-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4c3cb-124">See also</span></span>

- [<span data-ttu-id="4c3cb-125">C# 参考</span><span class="sxs-lookup"><span data-stu-id="4c3cb-125">C# reference</span></span>](../index.md)
- [<span data-ttu-id="4c3cb-126">C# 运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="4c3cb-126">C# operators and expressions</span></span>](index.md)
