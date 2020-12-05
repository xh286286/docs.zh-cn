---
title: 什么是 F#
description: '了解 F # 编程语言的定义，以及 F # 编程的作用。 了解丰富的数据类型、函数以及它们如何组合在一起。'
ms.date: 08/03/2018
ms.openlocfilehash: a6bad3e1db63c3fe948b5916925d5eb24a18a41c
ms.sourcegitcommit: ecd9e9bb2225eb76f819722ea8b24988fe46f34c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "96739472"
---
# <a name="what-is-f"></a><span data-ttu-id="12047-104">什么是 F\#</span><span class="sxs-lookup"><span data-stu-id="12047-104">What is F\#</span></span>

<span data-ttu-id="12047-105">F # 是一种函数编程语言，可方便编写正确且可维护的代码。</span><span class="sxs-lookup"><span data-stu-id="12047-105">F# is a functional programming language that makes it easy to write correct and maintainable code.</span></span>

<span data-ttu-id="12047-106">F # 编程主要涉及如何定义自动推断和通用化的类型和函数。</span><span class="sxs-lookup"><span data-stu-id="12047-106">F# programming primarily involves defining types and functions that are type-inferred and generalized automatically.</span></span> <span data-ttu-id="12047-107">这样，你的关注点将保留在问题域上并操作其数据，而不是编程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="12047-107">This allows your focus to remain on the problem domain and manipulating its data, rather than the details of programming.</span></span>

```fsharp
open System // Gets access to functionality in System namespace.

// Defines a function that takes a name and produces a greeting.
let getGreeting name = $"Hello, {name}! Isn't F# great?"

[<EntryPoint>]
let main args =
    // Defines a list of names
    let names = [ "Don"; "Julia"; "Xi" ]

    // Prints a greeting for each name!
    names
    |> List.map getGreeting
    |> List.iter (fun greeting -> printfn $"{greeting}")

    0
```

<span data-ttu-id="12047-108">F # 具有许多功能，包括：</span><span class="sxs-lookup"><span data-stu-id="12047-108">F# has numerous features, including:</span></span>

* <span data-ttu-id="12047-109">轻型语法</span><span class="sxs-lookup"><span data-stu-id="12047-109">Lightweight syntax</span></span>
* <span data-ttu-id="12047-110">默认情况下不可变</span><span class="sxs-lookup"><span data-stu-id="12047-110">Immutable by default</span></span>
* <span data-ttu-id="12047-111">类型推理和自动通用化</span><span class="sxs-lookup"><span data-stu-id="12047-111">Type inference and automatic generalization</span></span>
* <span data-ttu-id="12047-112">第一类函数</span><span class="sxs-lookup"><span data-stu-id="12047-112">First-class functions</span></span>
* <span data-ttu-id="12047-113">强大的数据类型</span><span class="sxs-lookup"><span data-stu-id="12047-113">Powerful data types</span></span>
* <span data-ttu-id="12047-114">模式匹配</span><span class="sxs-lookup"><span data-stu-id="12047-114">Pattern matching</span></span>
* <span data-ttu-id="12047-115">异步编程</span><span class="sxs-lookup"><span data-stu-id="12047-115">Async programming</span></span>

<span data-ttu-id="12047-116">[F # 语言参考](./language-reference/index.md)中记录了一组完整的功能。</span><span class="sxs-lookup"><span data-stu-id="12047-116">A full set of features are documented in the [F# language reference](./language-reference/index.md).</span></span>

## <a name="rich-data-types"></a><span data-ttu-id="12047-117">丰富的数据类型</span><span class="sxs-lookup"><span data-stu-id="12047-117">Rich data types</span></span>

<span data-ttu-id="12047-118">数据类型（如 [记录](./language-reference/records.md) 和可 [区分联合](./language-reference/discriminated-unions.md) ）允许您表示复杂的数据和域。</span><span class="sxs-lookup"><span data-stu-id="12047-118">Data types such as [Records](./language-reference/records.md) and [Discriminated Unions](./language-reference/discriminated-unions.md) let you represent complex data and domains.</span></span>

```fsharp
// Group data with Records
type SuccessfulWithdrawal =
    { Amount: decimal
      Balance: decimal }

type FailedWithdrawal =
    { Amount: decimal
      Balance: decimal
      IsOverdraft: bool }

// Use discriminated unions to represent data of 1 or more forms
type WithdrawalResult =
    | Success of SuccessfulWithdrawal
    | InsufficientFunds of FailedWithdrawal
    | CardExpired of System.DateTime
    | UndisclosedFailure
```

<span data-ttu-id="12047-119">F # 记录和可区分联合默认情况下为非 null、不可变和可比较，因此它们非常易于使用。</span><span class="sxs-lookup"><span data-stu-id="12047-119">F# records and discriminated unions are non-null, immutable, and comparable by default, making them very easy to use.</span></span>

## <a name="enforced-correctness-with-functions-and-pattern-matching"></a><span data-ttu-id="12047-120">使用函数和模式匹配强制实现的正确性</span><span class="sxs-lookup"><span data-stu-id="12047-120">Enforced correctness with functions and pattern matching</span></span>

<span data-ttu-id="12047-121">F # 函数在实践中易于声明和强大。</span><span class="sxs-lookup"><span data-stu-id="12047-121">F# functions are easy to declare and powerful in practice.</span></span> <span data-ttu-id="12047-122">与 [模式匹配](./language-reference/pattern-matching.md)一起使用时，它们允许您定义由编译器强制执行的行为。</span><span class="sxs-lookup"><span data-stu-id="12047-122">When combined with [pattern matching](./language-reference/pattern-matching.md), they allow you to define behavior whose correctness is enforced by the compiler.</span></span>

```fsharp
// Returns a WithdrawalResult
let withdrawMoney amount = // Implementation elided

let handleWithdrawal amount =
    let w = withdrawMoney amount

    // The F# compiler enforces accounting for each case!
    match w with
    | Success s -> printfn "Successfully withdrew %f{s.Amount}"
    | InsufficientFunds f -> printfn "Failed: balance is %f{f.Balance}"
    | CardExpired d -> printfn "Failed: card expired on {d}"
    | UndisclosedFailure -> printfn "Failed: unknown :("
```

<span data-ttu-id="12047-123">F # 函数也是第一类，这意味着它们可以作为参数传递，并从其他函数返回。</span><span class="sxs-lookup"><span data-stu-id="12047-123">F# functions are also first-class, meaning they can be passed as parameters and returned from other functions.</span></span>

## <a name="functions-to-define-operations-on-objects"></a><span data-ttu-id="12047-124">用于定义对象操作的函数</span><span class="sxs-lookup"><span data-stu-id="12047-124">Functions to define operations on objects</span></span>

<span data-ttu-id="12047-125">F # 完全支持对象，当你需要混合数据和功能时，它们是有用的数据类型。</span><span class="sxs-lookup"><span data-stu-id="12047-125">F# has full support for objects, which are useful data types when you need to blend data and functionality.</span></span> <span data-ttu-id="12047-126">F # 函数用于处理对象。</span><span class="sxs-lookup"><span data-stu-id="12047-126">F# functions are used to manipulate objects.</span></span>

```fsharp
type Set<'T when 'T: comparison>(elements: seq<'T>) =
    member s.IsEmpty = // Implementation elided
    member s.Contains (value) =// Implementation elided
    member s.Add (value) = // Implementation elided
    // ...
    // Further Implementation elided
    // ...
    interface IEnumerable<‘T>
    interface IReadOnlyCollection<‘T>

module Set =
    let isEmpty (set: Set<'T>) = set.IsEmpty

    let contains element (set: Set<'T>) = set.Contains(element)

    let add value (set: Set<'T>) = set.Add(value)
```

<span data-ttu-id="12047-127">不是编写面向对象的代码，在 F # 中，你通常会编写将对象视为函数的另一个数据类型的代码。</span><span class="sxs-lookup"><span data-stu-id="12047-127">Rather than writing code that is object-oriented, in F#, you will often write code that treats objects as another data type for functions to manipulate.</span></span> <span data-ttu-id="12047-128">[泛型接口](./language-reference/interfaces.md)、[对象表达式](./language-reference/object-expressions.md)和明智使用[成员](./language-reference/members/index.md)等功能在较大的 F # 程序中很常见。</span><span class="sxs-lookup"><span data-stu-id="12047-128">Features such as [generic interfaces](./language-reference/interfaces.md), [object expressions](./language-reference/object-expressions.md), and judicious use of [members](./language-reference/members/index.md) are common in larger F# programs.</span></span>

## <a name="next-steps"></a><span data-ttu-id="12047-129">后续步骤</span><span class="sxs-lookup"><span data-stu-id="12047-129">Next steps</span></span>

<span data-ttu-id="12047-130">若要详细了解更多 F # 功能，请查看 [f # 教程](tour.md)。</span><span class="sxs-lookup"><span data-stu-id="12047-130">To learn more about a larger set of F# features, check out the [F# Tour](tour.md).</span></span>
