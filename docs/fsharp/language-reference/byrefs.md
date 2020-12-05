---
title: Byref
description: '了解 F # 中用于低级别编程的 byref 和 byref 类型。'
ms.date: 11/04/2019
ms.openlocfilehash: ff2c06d8940f7341d5d8b1d942be264bfac586c5
ms.sourcegitcommit: ecd9e9bb2225eb76f819722ea8b24988fe46f34c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "96740310"
---
# <a name="byrefs"></a><span data-ttu-id="e0e9c-103">Byref</span><span class="sxs-lookup"><span data-stu-id="e0e9c-103">Byrefs</span></span>

<span data-ttu-id="e0e9c-104">F # 有两个主要功能区域，用于处理低级别编程的空间：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-104">F# has two major feature areas that deal in the space of low-level programming:</span></span>

* <span data-ttu-id="e0e9c-105">`byref` / `inref` / `outref` 类型为托管指针。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-105">The `byref`/`inref`/`outref` types, which are managed pointers.</span></span> <span data-ttu-id="e0e9c-106">它们对使用情况有限制，因此无法编译在运行时无效的程序。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-106">They have restrictions on usage so that you cannot compile a program that is invalid at run time.</span></span>
* <span data-ttu-id="e0e9c-107">`byref`类似的结构，它是具有类似语义并且与相同的编译时限制的[结构](structures.md) `byref<'T>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-107">A `byref`-like struct, which is a [structure](structures.md) that has similar semantics and the same compile-time restrictions as `byref<'T>`.</span></span> <span data-ttu-id="e0e9c-108">其中一个示例是 <xref:System.Span%601> 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-108">One example is <xref:System.Span%601>.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e9c-109">语法</span><span class="sxs-lookup"><span data-stu-id="e0e9c-109">Syntax</span></span>

```fsharp
// Byref types as parameters
let f (x: byref<'T>) = ()
let g (x: inref<'T>) = ()
let h (x: outref<'T>) = ()

// Calling a function with a byref parameter
let mutable x = 3
f &x

// Declaring a byref-like struct
open System.Runtime.CompilerServices

[<Struct; IsByRefLike>]
type S(count1: int, count2: int) =
    member x.Count1 = count1
    member x.Count2 = count2
```

## <a name="byref-inref-and-outref"></a><span data-ttu-id="e0e9c-110">Byref、inref 和 outref</span><span class="sxs-lookup"><span data-stu-id="e0e9c-110">Byref, inref, and outref</span></span>

<span data-ttu-id="e0e9c-111">有三种形式的 `byref` ：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-111">There are three forms of `byref`:</span></span>

* <span data-ttu-id="e0e9c-112">`inref<'T>`，用于读取基础值的托管指针。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-112">`inref<'T>`, a managed pointer for reading the underlying value.</span></span>
* <span data-ttu-id="e0e9c-113">`outref<'T>`，用于写入基础值的托管指针。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-113">`outref<'T>`, a managed pointer for writing to the underlying value.</span></span>
* <span data-ttu-id="e0e9c-114">`byref<'T>`，用于读取和写入基础值的托管指针。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-114">`byref<'T>`, a managed pointer for reading and writing the underlying value.</span></span>

<span data-ttu-id="e0e9c-115">`byref<'T>`可以在 `inref<'T>` 需要时传递。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-115">A `byref<'T>` can be passed where an `inref<'T>` is expected.</span></span> <span data-ttu-id="e0e9c-116">同样， `byref<'T>` 可以将传递到预期的 `outref<'T>` 位置。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-116">Similarly, a `byref<'T>` can be passed where an `outref<'T>` is expected.</span></span>

## <a name="using-byrefs"></a><span data-ttu-id="e0e9c-117">使用 byref</span><span class="sxs-lookup"><span data-stu-id="e0e9c-117">Using byrefs</span></span>

<span data-ttu-id="e0e9c-118">若要使用 `inref<'T>` ，需要使用以下内容获取指针值 `&` ：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-118">To use a `inref<'T>`, you need to get a pointer value with `&`:</span></span>

```fsharp
open System

let f (dt: inref<DateTime>) =
    printfn $"Now: %O{dt}"

let usage =
    let dt = DateTime.Now
    f &dt // Pass a pointer to 'dt'
```

<span data-ttu-id="e0e9c-119">若要使用或写入指针 `outref<'T>` `byref<'T>` ，还必须使您获取指向的指针的值 `mutable` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-119">To write to the pointer by using an `outref<'T>` or `byref<'T>`, you must also make the value you grab a pointer to `mutable`.</span></span>

```fsharp
open System

let f (dt: byref<DateTime>) =
    printfn $"Now: %O{dt}"
    dt <- DateTime.Now

// Make 'dt' mutable
let mutable dt = DateTime.Now

// Now you can pass the pointer to 'dt'
f &dt
```

<span data-ttu-id="e0e9c-120">如果只是编写指针而不是读取它，请考虑使用 `outref<'T>` 而不是 `byref<'T>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-120">If you are only writing the pointer instead of reading it, consider using `outref<'T>` instead of `byref<'T>`.</span></span>

### <a name="inref-semantics"></a><span data-ttu-id="e0e9c-121">Inref 语义</span><span class="sxs-lookup"><span data-stu-id="e0e9c-121">Inref semantics</span></span>

<span data-ttu-id="e0e9c-122">请考虑以下代码：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-122">Consider the following code:</span></span>

```fsharp
let f (x: inref<SomeStruct>) = x.SomeField
```

<span data-ttu-id="e0e9c-123">从语义上说，这意味着：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-123">Semantically, this means the following:</span></span>

* <span data-ttu-id="e0e9c-124">指针的刀柄 `x` 只能用它来读取值。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-124">The holder of the `x` pointer may only use it to read the value.</span></span>
* <span data-ttu-id="e0e9c-125">获取到 `struct` 嵌套在中的字段 `SomeStruct` 的任何指针都具有给定的类型 `inref<_>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-125">Any pointer acquired to `struct` fields nested within `SomeStruct` are given type `inref<_>`.</span></span>

<span data-ttu-id="e0e9c-126">以下情况也成立：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-126">The following is also true:</span></span>

* <span data-ttu-id="e0e9c-127">不意味着其他线程或别名没有写入访问权限 `x` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-127">There is no implication that other threads or aliases do not have write access to `x`.</span></span>
* <span data-ttu-id="e0e9c-128">这并不是不可变的，因为这是不可 `SomeStruct` 变的 `x` `inref` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-128">There is no implication that `SomeStruct` is immutable by virtue of `x` being an `inref`.</span></span>

<span data-ttu-id="e0e9c-129">但是，对于 **不可变的** F # 值类型，指针将 `this` 推断为 `inref` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-129">However, for F# value types that **are** immutable, the `this` pointer is inferred to be an `inref`.</span></span>

<span data-ttu-id="e0e9c-130">所有这些规则一起表示指针的持有者 `inref` 可能不会修改所指向的内存的即时内容。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-130">All of these rules together mean that the holder of an `inref` pointer may not modify the immediate contents of the memory being pointed to.</span></span>

### <a name="outref-semantics"></a><span data-ttu-id="e0e9c-131">Outref 语义</span><span class="sxs-lookup"><span data-stu-id="e0e9c-131">Outref semantics</span></span>

<span data-ttu-id="e0e9c-132">的用途 `outref<'T>` 是指示只应将指针写入。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-132">The purpose of `outref<'T>` is to indicate that the pointer should only be written to.</span></span> <span data-ttu-id="e0e9c-133">意外， `outref<'T>` 不管名称如何，都允许读取基础值。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-133">Unexpectedly, `outref<'T>` permits reading the underlying value despite its name.</span></span> <span data-ttu-id="e0e9c-134">这是为了实现兼容性。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-134">This is for compatibility purposes.</span></span> <span data-ttu-id="e0e9c-135">在语义上， `outref<'T>` 与不同 `byref<'T>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-135">Semantically, `outref<'T>` is no different than `byref<'T>`.</span></span>

### <a name="interop-with-c"></a><span data-ttu-id="e0e9c-136">与 C 互操作\#</span><span class="sxs-lookup"><span data-stu-id="e0e9c-136">Interop with C\#</span></span>

<span data-ttu-id="e0e9c-137">`in ref` `out ref` 除返回外，c # 还支持和关键字 `ref` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-137">C# supports the `in ref` and `out ref` keywords, in addition to `ref` returns.</span></span> <span data-ttu-id="e0e9c-138">下表显示 F # 如何解释 c # 发出的内容：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-138">The following table shows how F# interprets what C# emits:</span></span>

|<span data-ttu-id="e0e9c-139">C # 构造</span><span class="sxs-lookup"><span data-stu-id="e0e9c-139">C# construct</span></span>|<span data-ttu-id="e0e9c-140">F # 推导</span><span class="sxs-lookup"><span data-stu-id="e0e9c-140">F# infers</span></span>|
|------------|---------|
|<span data-ttu-id="e0e9c-141">`ref` 返回值</span><span class="sxs-lookup"><span data-stu-id="e0e9c-141">`ref` return value</span></span>|`outref<'T>`|
|<span data-ttu-id="e0e9c-142">`ref readonly` 返回值</span><span class="sxs-lookup"><span data-stu-id="e0e9c-142">`ref readonly` return value</span></span>|`inref<'T>`|
|<span data-ttu-id="e0e9c-143">`in ref` 参数</span><span class="sxs-lookup"><span data-stu-id="e0e9c-143">`in ref` parameter</span></span>|`inref<'T>`|
|<span data-ttu-id="e0e9c-144">`out ref` 参数</span><span class="sxs-lookup"><span data-stu-id="e0e9c-144">`out ref` parameter</span></span>|`outref<'T>`|

<span data-ttu-id="e0e9c-145">下表显示 F # 发出的内容：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-145">The following table shows what F# emits:</span></span>

|<span data-ttu-id="e0e9c-146">F # 构造</span><span class="sxs-lookup"><span data-stu-id="e0e9c-146">F# construct</span></span>|<span data-ttu-id="e0e9c-147">发出的构造</span><span class="sxs-lookup"><span data-stu-id="e0e9c-147">Emitted construct</span></span>|
|------------|-----------------|
|<span data-ttu-id="e0e9c-148">`inref<'T>` 参数</span><span class="sxs-lookup"><span data-stu-id="e0e9c-148">`inref<'T>` argument</span></span>|<span data-ttu-id="e0e9c-149">`[In]` 参数上的属性</span><span class="sxs-lookup"><span data-stu-id="e0e9c-149">`[In]` attribute on argument</span></span>|
|<span data-ttu-id="e0e9c-150">`inref<'T>` 返回</span><span class="sxs-lookup"><span data-stu-id="e0e9c-150">`inref<'T>` return</span></span>|<span data-ttu-id="e0e9c-151">`modreq` 值的属性</span><span class="sxs-lookup"><span data-stu-id="e0e9c-151">`modreq` attribute on value</span></span>|
|<span data-ttu-id="e0e9c-152">`inref<'T>` 在抽象槽或实现中</span><span class="sxs-lookup"><span data-stu-id="e0e9c-152">`inref<'T>` in abstract slot or implementation</span></span>|<span data-ttu-id="e0e9c-153">`modreq` 参数或返回</span><span class="sxs-lookup"><span data-stu-id="e0e9c-153">`modreq` on argument or return</span></span>|
|<span data-ttu-id="e0e9c-154">`outref<'T>` 参数</span><span class="sxs-lookup"><span data-stu-id="e0e9c-154">`outref<'T>` argument</span></span>|<span data-ttu-id="e0e9c-155">`[Out]` 参数上的属性</span><span class="sxs-lookup"><span data-stu-id="e0e9c-155">`[Out]` attribute on argument</span></span>|

### <a name="type-inference-and-overloading-rules"></a><span data-ttu-id="e0e9c-156">类型推理和重载规则</span><span class="sxs-lookup"><span data-stu-id="e0e9c-156">Type inference and overloading rules</span></span>

<span data-ttu-id="e0e9c-157">`inref<'T>`在以下情况下，类型由 F # 编译器推断：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-157">An `inref<'T>` type is inferred by the F# compiler in the following cases:</span></span>

1. <span data-ttu-id="e0e9c-158">具有特性的 .NET 参数或返回类型 `IsReadOnly` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-158">A .NET parameter or return type that has an `IsReadOnly` attribute.</span></span>
2. <span data-ttu-id="e0e9c-159">`this`结构类型上没有可变字段的指针。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-159">The `this` pointer on a struct type that has no mutable fields.</span></span>
3. <span data-ttu-id="e0e9c-160">派生自另一个指针的内存位置的地址 `inref<_>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-160">The address of a memory location derived from another `inref<_>` pointer.</span></span>

<span data-ttu-id="e0e9c-161">当使用的是隐式地址时 `inref` ，具有类型的参数的重载 `SomeType` 优先于具有类型的参数的重载 `inref<SomeType>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-161">When an implicit address of an `inref` is being taken, an overload with an argument of type `SomeType` is preferred to an overload with an argument of type `inref<SomeType>`.</span></span> <span data-ttu-id="e0e9c-162">例如：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-162">For example:</span></span>

```fsharp
type C() =
    static member M(x: System.DateTime) = x.AddDays(1.0)
    static member M(x: inref<System.DateTime>) = x.AddDays(2.0)
    static member M2(x: System.DateTime, y: int) = x.AddDays(1.0)
    static member M2(x: inref<System.DateTime>, y: int) = x.AddDays(2.0)

let res = System.DateTime.Now
let v =  C.M(res)
let v2 =  C.M2(res, 4)
```

<span data-ttu-id="e0e9c-163">在这两种情况下，将解析重载， `System.DateTime` 而不是重载 `inref<System.DateTime>` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-163">In both cases, the overloads taking `System.DateTime` are resolved rather than the overloads taking `inref<System.DateTime>`.</span></span>

## <a name="byref-like-structs"></a><span data-ttu-id="e0e9c-164">类似 Byref 的结构</span><span class="sxs-lookup"><span data-stu-id="e0e9c-164">Byref-like structs</span></span>

<span data-ttu-id="e0e9c-165">除了 `byref` / `inref` / `outref` 三个，还可以定义自己的结构，这些结构可以遵循 `byref` 类似的语义。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-165">In addition to the `byref`/`inref`/`outref` trio, you can define your own structs that can adhere to `byref`-like semantics.</span></span> <span data-ttu-id="e0e9c-166">这是通过属性完成的 <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> ：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-166">This is done with the <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> attribute:</span></span>

```fsharp
open System
open System.Runtime.CompilerServices

[<IsByRefLike; Struct>]
type S(count1: Span<int>, count2: Span<int>) =
    member x.Count1 = count1
    member x.Count2 = count2
```

<span data-ttu-id="e0e9c-167">`IsByRefLike` 不意味着 `Struct` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-167">`IsByRefLike` does not imply `Struct`.</span></span> <span data-ttu-id="e0e9c-168">这两者都必须存在于类型上。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-168">Both must be present on the type.</span></span>

<span data-ttu-id="e0e9c-169">`byref`F # 中的 "like" 结构是堆栈绑定值类型。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-169">A "`byref`-like" struct in F# is a stack-bound value type.</span></span> <span data-ttu-id="e0e9c-170">永远不会在托管堆上分配。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-170">It is never allocated on the managed heap.</span></span> <span data-ttu-id="e0e9c-171">`byref`类似的结构可用于实现高性能编程，因为它是针对生存期和非捕获的一组强检查强制实施的。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-171">A `byref`-like struct is useful for high-performance programming, as it is enforced with set of strong checks about lifetime and non-capture.</span></span> <span data-ttu-id="e0e9c-172">规则如下：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-172">The rules are:</span></span>

* <span data-ttu-id="e0e9c-173">它们可用作函数参数、方法参数、局部变量、方法返回。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-173">They can be used as function parameters, method parameters, local variables, method returns.</span></span>
* <span data-ttu-id="e0e9c-174">它们不能是类或普通结构的静态成员或实例成员。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-174">They cannot be static or instance members of a class or normal struct.</span></span>
* <span data-ttu-id="e0e9c-175">不能通过任何闭包构造 (`async` 方法或 lambda 表达式来捕获它们) 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-175">They cannot be captured by any closure construct (`async` methods or lambda expressions).</span></span>
* <span data-ttu-id="e0e9c-176">它们不能用作泛型参数。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-176">They cannot be used as a generic parameter.</span></span>

<span data-ttu-id="e0e9c-177">最后一点对于 F # 管道样式编程至关重要，因为它 `|>` 是一个参数化其输入类型的泛型函数。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-177">This last point is crucial for F# pipeline-style programming, as `|>` is a generic function that parameterizes its input types.</span></span> <span data-ttu-id="e0e9c-178">此限制可能会 `|>` 在将来为宽松，因为它是内联的，不会对其主体中的非内联泛型函数进行任何调用。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-178">This restriction may be relaxed for `|>` in the future, as it is inline and does not make any calls to non-inlined generic functions in its body.</span></span>

<span data-ttu-id="e0e9c-179">尽管这些规则对使用进行了严格的限制，但这样做可确保以安全的方式满足高性能计算的承诺。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-179">Although these rules strongly restrict usage, they do so to fulfill the promise of high-performance computing in a safe manner.</span></span>

## <a name="byref-returns"></a><span data-ttu-id="e0e9c-180">Byref 返回</span><span class="sxs-lookup"><span data-stu-id="e0e9c-180">Byref returns</span></span>

<span data-ttu-id="e0e9c-181">可以生成和使用来自 F # 函数或成员的 Byref 返回。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-181">Byref returns from F# functions or members can be produced and consumed.</span></span> <span data-ttu-id="e0e9c-182">使用 `byref` 返回方法时，会隐式取消引用该值。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-182">When consuming a `byref`-returning method, the value is implicitly dereferenced.</span></span> <span data-ttu-id="e0e9c-183">例如：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-183">For example:</span></span>

```fsharp
let squareAndPrint (data : byref<int>) =
    let squared = data*data    // data is implicitly dereferenced
    printfn $"%d{squared}"
```

<span data-ttu-id="e0e9c-184">若要返回值 byref，则包含值的变量的生存期必须长于当前范围。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-184">To return a value byref, the variable that contains the value must live longer than the current scope.</span></span>
<span data-ttu-id="e0e9c-185">此外，若要返回 byref，请使用 `&value` (其中，值是生存时间比当前范围) 长的变量。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-185">Also, to return byref, use `&value` (where value is a variable that lives longer than the current scope).</span></span>

```fsharp
let mutable sum = 0
let safeSum (bytes: Span<byte>) =
    for i in 0 .. bytes.Length - 1 do
        sum <- sum + int bytes.[i]
    &sum  // sum lives longer than the scope of this function.
```

<span data-ttu-id="e0e9c-186">若要避免隐式取消引用（如通过多个链式调用传递引用），请使用 `&x` (，其中 `x` 是) 值。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-186">To avoid the implicit dereference, such as passing a reference through multiple chained calls, use `&x` (where `x` is the value).</span></span>

<span data-ttu-id="e0e9c-187">还可以直接分配给返回 `byref` 。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-187">You can also directly assign to a return `byref`.</span></span> <span data-ttu-id="e0e9c-188">请考虑以下 (高命令式) 程序：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-188">Consider the following (highly imperative) program:</span></span>

```fsharp
type C() =
    let mutable nums = [| 1; 3; 7; 15; 31; 63; 127; 255; 511; 1023 |]

    override _.ToString() = String.Join(' ', nums)

    member _.FindLargestSmallerThan(target: int) =
        let mutable ctr = nums.Length - 1

        while ctr > 0 && nums.[ctr] >= target do ctr <- ctr - 1

        if ctr > 0 then &nums.[ctr] else &nums.[0]

[<EntryPoint>]
let main argv =
    let c = C()
    printfn $"Original sequence: %O{c}"

    let v = &c.FindLargestSmallerThan 16

    v <- v*2 // Directly assign to the byref return

    printfn $"New sequence:      %O{c}"

    0 // return an integer exit code
```

<span data-ttu-id="e0e9c-189">以下是输出：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-189">This is the output:</span></span>

```console
Original sequence: 1 3 7 15 31 63 127 255 511 1023
New sequence:      1 3 7 30 31 63 127 255 511 1023
```

## <a name="scoping-for-byrefs"></a><span data-ttu-id="e0e9c-190">Byref 的作用域</span><span class="sxs-lookup"><span data-stu-id="e0e9c-190">Scoping for byrefs</span></span>

<span data-ttu-id="e0e9c-191">`let`绑定值的引用不能超过其定义的范围。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-191">A `let`-bound value cannot have its reference exceed the scope in which it was defined.</span></span> <span data-ttu-id="e0e9c-192">例如，不允许以下操作：</span><span class="sxs-lookup"><span data-stu-id="e0e9c-192">For example, the following is disallowed:</span></span>

```fsharp
let test2 () =
    let x = 12
    &x // Error: 'x' exceeds its defined scope!

let test () =
    let x =
        let y = 1
        &y // Error: `y` exceeds its defined scope!
    ()
```

<span data-ttu-id="e0e9c-193">这会阻止你获取不同的结果，具体取决于你是否编译了优化。</span><span class="sxs-lookup"><span data-stu-id="e0e9c-193">This prevents you from getting different results depending on if you compile with optimizations or not.</span></span>
