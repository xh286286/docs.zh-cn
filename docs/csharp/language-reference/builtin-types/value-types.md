---
description: 了解 C# 中的值类型、种类以及内置值类型
title: 值类型 - C# 参考
ms.date: 01/22/2020
f1_keywords:
- cs.valuetypes
helpviewer_keywords:
- value types [C#]
- types [C#], value types
- C# language, value types
ms.assetid: 471eb994-2958-49d5-a6be-19b4313f80a3
ms.openlocfilehash: 64c9e9eba2495531cfef8a603d53fb21c95c87a4
ms.sourcegitcommit: 9d525bb8109216ca1dc9e39c149d4902f4b43da5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/04/2020
ms.locfileid: "96599390"
---
# <a name="value-types-c-reference"></a><span data-ttu-id="588f9-103">值类型（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="588f9-103">Value types (C# reference)</span></span>

<span data-ttu-id="588f9-104">值类型和[引用类型](../keywords/reference-types.md)是 C# 类型的两个主要类别。</span><span class="sxs-lookup"><span data-stu-id="588f9-104">*Value types* and [reference types](../keywords/reference-types.md) are the two main categories of C# types.</span></span> <span data-ttu-id="588f9-105">值类型的变量包含类型的实例。</span><span class="sxs-lookup"><span data-stu-id="588f9-105">A variable of a value type contains an instance of the type.</span></span> <span data-ttu-id="588f9-106">它不同于引用类型的变量，后者包含对类型实例的引用。</span><span class="sxs-lookup"><span data-stu-id="588f9-106">This differs from a variable of a reference type, which contains a reference to an instance of the type.</span></span> <span data-ttu-id="588f9-107">默认情况下，在[分配](../operators/assignment-operator.md)中，通过将实参传递给方法并返回方法结果来复制变量值。</span><span class="sxs-lookup"><span data-stu-id="588f9-107">By default, on [assignment](../operators/assignment-operator.md), passing an argument to a method, and returning a method result, variable values are copied.</span></span> <span data-ttu-id="588f9-108">对于值类型变量，会复制相应的类型实例。</span><span class="sxs-lookup"><span data-stu-id="588f9-108">In the case of value-type variables, the corresponding type instances are copied.</span></span> <span data-ttu-id="588f9-109">以下示例演示了该行为：</span><span class="sxs-lookup"><span data-stu-id="588f9-109">The following example demonstrates that behavior:</span></span>

[!code-csharp[copy of values](snippets/shared/ValueTypes.cs#ValueTypeCopied)]

<span data-ttu-id="588f9-110">如前面的示例所示，对值类型变量的操作只影响存储在变量中的值类型实例。</span><span class="sxs-lookup"><span data-stu-id="588f9-110">As the preceding example shows, operations on a value-type variable affect only that instance of the value type, stored in the variable.</span></span>

<span data-ttu-id="588f9-111">如果值类型包含引用类型的数据成员，则在复制值类型实例时，只会复制对引用类型实例的引用。</span><span class="sxs-lookup"><span data-stu-id="588f9-111">If a value type contains a data member of a reference type, only the reference to the instance of the reference type is copied when a value-type instance is copied.</span></span> <span data-ttu-id="588f9-112">副本和原始值类型实例都具有对同一引用类型实例的访问权限。</span><span class="sxs-lookup"><span data-stu-id="588f9-112">Both the copy and original value-type instance have access to the same reference-type instance.</span></span> <span data-ttu-id="588f9-113">以下示例演示了该行为：</span><span class="sxs-lookup"><span data-stu-id="588f9-113">The following example demonstrates that behavior:</span></span>

[!code-csharp[shallow copy](snippets/shared/ValueTypes.cs#ShallowCopy)]

> [!NOTE]
> <span data-ttu-id="588f9-114">若要使代码更不易出错、更可靠，请定义并使用不可变的值类型。</span><span class="sxs-lookup"><span data-stu-id="588f9-114">To make your code less error-prone and more robust, define and use immutable value types.</span></span> <span data-ttu-id="588f9-115">本文仅为演示目的使用可变值类型。</span><span class="sxs-lookup"><span data-stu-id="588f9-115">This article uses mutable value types only for demonstration purposes.</span></span>

## <a name="kinds-of-value-types-and-type-constraints"></a><span data-ttu-id="588f9-116">值类型的种类以及类型约束</span><span class="sxs-lookup"><span data-stu-id="588f9-116">Kinds of value types and type constraints</span></span>

<span data-ttu-id="588f9-117">值类型可以是以下种类之一：</span><span class="sxs-lookup"><span data-stu-id="588f9-117">A value type can be one of the two following kinds:</span></span>

- <span data-ttu-id="588f9-118">[结构类型](struct.md)，用于封装数据和相关功能</span><span class="sxs-lookup"><span data-stu-id="588f9-118">a [structure type](struct.md), which encapsulates data and related functionality</span></span>
- <span data-ttu-id="588f9-119">[枚举类型](enum.md)，由一组命名常数定义，表示一个选择或选择组合</span><span class="sxs-lookup"><span data-stu-id="588f9-119">an [enumeration type](enum.md), which is defined by a set of named constants and represents a choice or a combination of choices</span></span>

<span data-ttu-id="588f9-120">[可为 null 值类型](nullable-value-types.md) `T?` 表示其基础值类型 `T` 的所有值及额外的 [null](../keywords/null.md) 值。</span><span class="sxs-lookup"><span data-stu-id="588f9-120">A [nullable value type](nullable-value-types.md) `T?` represents all values of its underlying value type `T` and an additional [null](../keywords/null.md) value.</span></span> <span data-ttu-id="588f9-121">不能将 `null` 分配给值类型的变量，除非它是可为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="588f9-121">You cannot assign `null` to a variable of a value type, unless it's a nullable value type.</span></span>

<span data-ttu-id="588f9-122">你可使用 [`struct` 约束](../../programming-guide/generics/constraints-on-type-parameters.md)指定类型参数为不可为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="588f9-122">You can use the [`struct` constraint](../../programming-guide/generics/constraints-on-type-parameters.md) to specify that a type parameter is a non-nullable value type.</span></span> <span data-ttu-id="588f9-123">结构类型和枚举类型都满足 `struct` 约束。</span><span class="sxs-lookup"><span data-stu-id="588f9-123">Both structure and enumeration types satisfy the `struct` constraint.</span></span> <span data-ttu-id="588f9-124">从 C# 7.3 开始，你可以在基类约束中使用 `System.Enum`（称为[枚举约束](../../programming-guide/generics/constraints-on-type-parameters.md#enum-constraints)），以指定类型参数为枚举类型。</span><span class="sxs-lookup"><span data-stu-id="588f9-124">Beginning with C# 7.3, you can use `System.Enum` in a base class constraint (that is known as the [enum constraint](../../programming-guide/generics/constraints-on-type-parameters.md#enum-constraints)) to specify that a type parameter is an enumeration type.</span></span>

## <a name="built-in-value-types"></a><span data-ttu-id="588f9-125">内置值类型</span><span class="sxs-lookup"><span data-stu-id="588f9-125">Built-in value types</span></span>

<span data-ttu-id="588f9-126">C# 提供以下内置值类型，也称为“简单类型”：</span><span class="sxs-lookup"><span data-stu-id="588f9-126">C# provides the following built-in value types, also known as *simple types*:</span></span>

- [<span data-ttu-id="588f9-127">整型数值类型</span><span class="sxs-lookup"><span data-stu-id="588f9-127">Integral numeric types</span></span>](integral-numeric-types.md)
- [<span data-ttu-id="588f9-128">浮点型数值类型</span><span class="sxs-lookup"><span data-stu-id="588f9-128">Floating-point numeric types</span></span>](floating-point-numeric-types.md)
- <span data-ttu-id="588f9-129">[bool](bool.md)，表示布尔值</span><span class="sxs-lookup"><span data-stu-id="588f9-129">[bool](bool.md) that represents a Boolean value</span></span>
- <span data-ttu-id="588f9-130">[char](char.md)，表示 Unicode UTF-16 字符</span><span class="sxs-lookup"><span data-stu-id="588f9-130">[char](char.md) that represents a Unicode UTF-16 character</span></span>

<span data-ttu-id="588f9-131">所有简单值都是结构类型，它们与其他结构类型的不同之处在于，它们允许特定的额外操作：</span><span class="sxs-lookup"><span data-stu-id="588f9-131">All simple types are structure types and differ from other structure types in that they permit certain additional operations:</span></span>

- <span data-ttu-id="588f9-132">可以使用文字为简单类型提供值。</span><span class="sxs-lookup"><span data-stu-id="588f9-132">You can use literals to provide a value of a simple type.</span></span> <span data-ttu-id="588f9-133">例如，`'A'` 是类型 `char` 的文本，`2001` 是类型 `int` 的文本。</span><span class="sxs-lookup"><span data-stu-id="588f9-133">For example, `'A'` is a literal of the type `char` and `2001` is a literal of the type `int`.</span></span>

- <span data-ttu-id="588f9-134">可以使用 [const](../keywords/const.md) 关键字声明简单类型的常数。</span><span class="sxs-lookup"><span data-stu-id="588f9-134">You can declare constants of the simple types with the [const](../keywords/const.md) keyword.</span></span> <span data-ttu-id="588f9-135">不能具有其他结构类型的常数。</span><span class="sxs-lookup"><span data-stu-id="588f9-135">It's not possible to have constants of other structure types.</span></span>

- <span data-ttu-id="588f9-136">常数表达式的操作数都是简单类型的常数，在编译时进行评估。</span><span class="sxs-lookup"><span data-stu-id="588f9-136">Constant expressions, whose operands are all constants of the simple types, are evaluated at compile time.</span></span>

<span data-ttu-id="588f9-137">从 C# 7.0 开始，C# 支持[值元组](value-tuples.md)。</span><span class="sxs-lookup"><span data-stu-id="588f9-137">Beginning with C# 7.0, C# supports [value tuples](value-tuples.md).</span></span> <span data-ttu-id="588f9-138">值元组是值类型，而不是简单类型。</span><span class="sxs-lookup"><span data-stu-id="588f9-138">A value tuple is a value type, but not a simple type.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="588f9-139">C# 语言规范</span><span class="sxs-lookup"><span data-stu-id="588f9-139">C# language specification</span></span>

<span data-ttu-id="588f9-140">有关更多信息，请参阅 [C# 语言规范](~/_csharplang/spec/introduction.md)的以下部分：</span><span class="sxs-lookup"><span data-stu-id="588f9-140">For more information, see the following sections of the [C# language specification](~/_csharplang/spec/introduction.md):</span></span>

- [<span data-ttu-id="588f9-141">值类型</span><span class="sxs-lookup"><span data-stu-id="588f9-141">Value types</span></span>](~/_csharplang/spec/types.md#value-types)
- [<span data-ttu-id="588f9-142">简单类型</span><span class="sxs-lookup"><span data-stu-id="588f9-142">Simple types</span></span>](~/_csharplang/spec/types.md#simple-types)
- [<span data-ttu-id="588f9-143">变量</span><span class="sxs-lookup"><span data-stu-id="588f9-143">Variables</span></span>](~/_csharplang/spec/variables.md)

## <a name="see-also"></a><span data-ttu-id="588f9-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="588f9-144">See also</span></span>

- [<span data-ttu-id="588f9-145">C# 参考</span><span class="sxs-lookup"><span data-stu-id="588f9-145">C# reference</span></span>](../index.md)
- <xref:System.ValueType?displayProperty=nameWithType>
- [<span data-ttu-id="588f9-146">引用类型</span><span class="sxs-lookup"><span data-stu-id="588f9-146">Reference types</span></span>](../keywords/reference-types.md)
