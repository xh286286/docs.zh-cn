---
title: 可以为 null 的值类型
description: '了解如何使用可以为 null 的值类型，这种方法表示在 F # 中也可以为 null 的值类型。'
ms.date: 11/19/2020
ms.openlocfilehash: e28cbfc57c5631573f46ac36462517cf011e96d2
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97009633"
---
# <a name="nullable-value-types"></a><span data-ttu-id="e5a0d-103">可以为 null 的值类型</span><span class="sxs-lookup"><span data-stu-id="e5a0d-103">Nullable value types</span></span>

<span data-ttu-id="e5a0d-104">可以 _为 null 的值类型_ `Nullable<'T>` 表示也可以为的任何 [结构](structures.md) 类型 `null` 。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-104">A _nullable value type_ `Nullable<'T>` represents any [struct](structures.md) type that could also be `null`.</span></span> <span data-ttu-id="e5a0d-105">当与库和组件进行交互时，可能会选择将这些类型的类型（如整数）与值相结合，从而 `null` 提高效率。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-105">This is helpful when interacting with libraries and components that may choose to represent these kinds of types, like integers, with a `null` value for efficiency reasons.</span></span> <span data-ttu-id="e5a0d-106">支持此构造的基础类型是 <xref:System.Nullable%601?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-106">The underlying type that backs this construct is <xref:System.Nullable%601?displayProperty=nameWithType>.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a0d-107">语法</span><span class="sxs-lookup"><span data-stu-id="e5a0d-107">Syntax</span></span>

```fsharp
Nullable<'T>
Nullable value
```

## <a name="declare-and-assign-with-values"></a><span data-ttu-id="e5a0d-108">用值声明和赋值</span><span class="sxs-lookup"><span data-stu-id="e5a0d-108">Declare and assign with values</span></span>

<span data-ttu-id="e5a0d-109">声明可为 null 的值类型，就像在 F # 中声明任何类似包装器的类型一样：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-109">Declaring a nullable value type is just like declaring any wrapper-like type in F#:</span></span>

```fsharp
open System

let x = 12
let nullableX = Nullable<int> x
```

<span data-ttu-id="e5a0d-110">你还可以 elide 泛型类型参数，并允许类型推理解决该问题：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-110">You can also elide the generic type parameter and allow type inference to resolve it:</span></span>

```fsharp
open System

let x = 12
let nullableX = Nullable x
```

<span data-ttu-id="e5a0d-111">若要分配给可以为 null 的值类型，还需要是显式的。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-111">To assign to a nullable value type, you'll need to also be explicit.</span></span> <span data-ttu-id="e5a0d-112">对于 F # 定义的可以为 null 的值类型，不存在隐式转换：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-112">There is no implicit conversion for F#-defined nullable value types:</span></span>

```fsharp
open System

let mutable x = Nullable 12
x <- Nullable 13
```

## <a name="assign-null"></a><span data-ttu-id="e5a0d-113">赋值 null</span><span class="sxs-lookup"><span data-stu-id="e5a0d-113">Assign null</span></span>

<span data-ttu-id="e5a0d-114">不能直接分配 `null` 给可以为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-114">You cannot directly assign `null` to a nullable value type.</span></span> <span data-ttu-id="e5a0d-115">`Nullable()`改用：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-115">Use `Nullable()` instead:</span></span>

```fsharp
let mutable a = Nullable 42
a <- Nullable()
```

<span data-ttu-id="e5a0d-116">这是因为不 `Nullable<'T>` 具有 `null` 正确的值。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-116">This is because `Nullable<'T>` does not have `null` as a proper value.</span></span>

## <a name="pass-and-assign-to-members"></a><span data-ttu-id="e5a0d-117">传递并分配给成员</span><span class="sxs-lookup"><span data-stu-id="e5a0d-117">Pass and assign to members</span></span>

<span data-ttu-id="e5a0d-118">使用成员与 F # 值之间的主要区别在于可以在使用成员时隐式推断可以为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-118">A key difference between working with members and F# values is that nullable value types can be implicitly inferred when you're working with members.</span></span> <span data-ttu-id="e5a0d-119">请考虑以下方法，该方法采用可以为 null 的值类型作为输入：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-119">Consider the following method that takes a nullable value type as input:</span></span>

```fsharp
type C() =
    member _.M(x: Nullable<int>) = x.HasValue
    member val NVT = Nullable 12 with get, set

let c = C()
c.M(12)
c.NVT <- 12
```

<span data-ttu-id="e5a0d-120">在上面的示例中，可以将传递 `12` 给方法 `M` 。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-120">In the previous example, you can pass `12` to the method `M`.</span></span> <span data-ttu-id="e5a0d-121">你还可以分配 `12` 给 auto 属性 `NVT` 。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-121">You can also assign `12` to the auto property `NVT`.</span></span> <span data-ttu-id="e5a0d-122">如果可以将输入构造为可以为 null 的值类型并且它与目标类型匹配，则 F # 编译器将隐式转换此类调用或分配。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-122">If the input can be constructed as a nullable value type and it matches the target type, the F# compiler will implicitly convert such calls or assignments.</span></span>

## <a name="examine-a-nullable-value-type-instance"></a><span data-ttu-id="e5a0d-123">检查可以为 null 的值类型实例</span><span class="sxs-lookup"><span data-stu-id="e5a0d-123">Examine a nullable value type instance</span></span>

<span data-ttu-id="e5a0d-124">与 [选项](options.md)不同，后者是表示可能值的通用构造，可以为 null 的值类型不与模式匹配一起使用。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-124">Unlike [Options](options.md), which are a generalized construct for representing a possible value, nullable value types are not used with pattern matching.</span></span> <span data-ttu-id="e5a0d-125">相反，您需要使用 [`if`](conditional-expressions-if-then-else.md) 表达式并检查 `HasValue` 属性。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-125">Instead, you need to use an [`if`](conditional-expressions-if-then-else.md) expression and check the `HasValue` property.</span></span>

<span data-ttu-id="e5a0d-126">若要获取基础值，请在 `Value` 检查后使用属性 `HasValue` ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-126">To get the underlying value, use the `Value` property after a `HasValue` check, like so:</span></span>

```fsharp
open System

let a = Nullable 42

if a.HasValue then
    printfn $"{a} is {a.Value}"
else
    printfn $"{a} has no value."
```

## <a name="nullable-operators"></a><span data-ttu-id="e5a0d-127">可以为 null 的运算符</span><span class="sxs-lookup"><span data-stu-id="e5a0d-127">Nullable operators</span></span>

<span data-ttu-id="e5a0d-128">对可以为 null 的值类型（例如算术或比较）的操作，可能需要使用 [可以为 null 的运算符](symbol-and-operator-reference/nullable-operators.md)。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-128">Operations on nullable value types, such as arithmetic or comparison, can require the use of [nullable operators](symbol-and-operator-reference/nullable-operators.md).</span></span>

<span data-ttu-id="e5a0d-129">可以使用命名空间中的转换运算符从一个可为 null 的值类型转换为另一个值类型 `FSharp.Linq` ：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-129">You can convert from one nullable value type to another using conversion operators from the `FSharp.Linq` namespace:</span></span>

```fsharp
open System
open FSharp.Linq

let nullableInt = Nullable 10
let nullableFloat = Nullable.float nullableInt
```

<span data-ttu-id="e5a0d-130">你还可以使用适当的不可为 null 的运算符转换为基元类型，如果该类型没有值，则会产生异常：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-130">You can also use an appropriate non-nullable operator to convert to a primitive type, risking an exception if it has no value:</span></span>

```fsharp
open System
open FSharp.Linq

let nullableInt = Nullable 10
let nullableFloat = Nullable.float nullableInt

printfn $"value is %f{float nullableFloat}"
```

<span data-ttu-id="e5a0d-131">你还可以使用可以为 null 的运算符作为检查和的 `HasValue` 简短 `Value` 操作：</span><span class="sxs-lookup"><span data-stu-id="e5a0d-131">You can also use nullable operators as a short-hand for checking `HasValue` and `Value`:</span></span>

```fsharp
open System
open FSharp.Linq

let nullableInt = Nullable 10
let nullableFloat = Nullable.float nullableInt

let isBigger = nullableFloat ?> 1.0
let isBiggerLongForm = nullableFloat.HasValue && nullableFloat.Value > 1.0
```

<span data-ttu-id="e5a0d-132">`?>`如果左侧是可以为 null 的，则比较检查是否可以为 null，并且仅在其具有值时才会成功。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-132">The `?>` comparison checks if the left-hand side is nullable and only succeeds if it has a value.</span></span> <span data-ttu-id="e5a0d-133">它与其后的行等效。</span><span class="sxs-lookup"><span data-stu-id="e5a0d-133">It is equivalent to the line that follows it.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5a0d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e5a0d-134">See also</span></span>

- [<span data-ttu-id="e5a0d-135">结构</span><span class="sxs-lookup"><span data-stu-id="e5a0d-135">Structures</span></span>](structures.md)
- [<span data-ttu-id="e5a0d-136">F # 选项</span><span class="sxs-lookup"><span data-stu-id="e5a0d-136">F# Options</span></span>](options.md)
