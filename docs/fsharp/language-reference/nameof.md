---
title: Nameof
description: 了解 nameof 运算符，它是一项元编程功能，可用于在源代码中生成任何符号的名称。
ms.date: 11/12/2020
ms.openlocfilehash: 9947d7172d1b73db5c181297ec8b1131382e1f5e
ms.sourcegitcommit: 34968a61e9bac0f6be23ed6ffb837f52d2390c85
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "94688626"
---
# <a name="nameof"></a><span data-ttu-id="ec6c1-103">Nameof</span><span class="sxs-lookup"><span data-stu-id="ec6c1-103">Nameof</span></span>

<span data-ttu-id="ec6c1-104">`nameof`表达式生成一个字符串常量，该常量与 source 中几乎任何 F # 构造的源中的名称匹配。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-104">The `nameof` expression produces a string constant that matches the name in source for nearly any F# construct in source.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec6c1-105">语法</span><span class="sxs-lookup"><span data-stu-id="ec6c1-105">Syntax</span></span>

```fsharp
nameof symbol
nameof<'TGeneric>
```

## <a name="remarks"></a><span data-ttu-id="ec6c1-106">备注</span><span class="sxs-lookup"><span data-stu-id="ec6c1-106">Remarks</span></span>

<span data-ttu-id="ec6c1-107">`nameof` 通过解析传递给它的符号，并生成该符号的名称，因为它是在源代码中声明的。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-107">`nameof` works by resolving the symbol passed to it and produces the name of that symbol as it is declared in your source code.</span></span> <span data-ttu-id="ec6c1-108">这在各种情况下非常有用，例如日志记录，并可防止日志记录在源代码中发生更改。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-108">This is useful in various scenarios, such as logging, and protects your logging against changes in source code.</span></span>

```fsharp
let months =
    [
        "January"; "February"; "March"; "April";
        "May"; "June"; "July"; "August"; "September";
        "October"; "November"; "December"
    ]

let lookupMonth month =
    if (month > 12 || month < 1) then
        invalidArg (nameof month) ($"Value passed in was %d{month}.")

    months.[month-1]

printfn "%s" (lookupMonth 12)
printfn "%s" (lookupMonth 1)
printfn "%s" (lookupMonth 13)
```

<span data-ttu-id="ec6c1-109">最后一行将引发异常，并 `"month"` 将显示在错误消息中。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-109">The last line will throw an exception and `"month"` will be shown in the error message.</span></span>

<span data-ttu-id="ec6c1-110">你可以创建几乎每个 F # 构造的名称：</span><span class="sxs-lookup"><span data-stu-id="ec6c1-110">You can take a name of nearly every F# construct:</span></span>

```fsharp
module M =
    let f x = nameof x

printfn $"{(M.f 12)]}"
printfn $"{(nameof M)}"
printfn $"{(nameof M.f)}"
```

<span data-ttu-id="ec6c1-111">`nameof` 不是第一类函数，因此不能使用。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-111">`nameof` is not a first-class function and cannot be used as such.</span></span> <span data-ttu-id="ec6c1-112">这意味着不能对其进行部分应用，并且无法通过 F # 管道运算符将值通过管道传递给它。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-112">That means it cannot be partially applied and values cannot be piped into it via F# pipeline operators.</span></span>

## <a name="nameof-on-operators"></a><span data-ttu-id="ec6c1-113">运算符上的 Nameof</span><span class="sxs-lookup"><span data-stu-id="ec6c1-113">Nameof on operators</span></span>

<span data-ttu-id="ec6c1-114">F # 中的运算符可通过两种方式使用：作为运算符文本本身，或表示已编译的窗体的符号。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-114">Operators in F# can be used in two ways, as an operator text itself, or a symbol representing the compiled form.</span></span> <span data-ttu-id="ec6c1-115">`nameof` 运算符上的将生成运算符的名称，因为它是在源中声明的。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-115">`nameof` on an operator will produce the name of the operator as it is declared in source.</span></span> <span data-ttu-id="ec6c1-116">若要获取已编译的名称，请在源中使用编译的名称：</span><span class="sxs-lookup"><span data-stu-id="ec6c1-116">To get the compiled name, use the compiled name in source:</span></span>

```fsharp
nameof(+) // "+"
nameof op_Addition // "op_Addition"
```

## <a name="nameof-on-generics"></a><span data-ttu-id="ec6c1-117">泛型上的 Nameof</span><span class="sxs-lookup"><span data-stu-id="ec6c1-117">Nameof on generics</span></span>

<span data-ttu-id="ec6c1-118">您还可以采用泛型类型参数的名称，但语法不同：</span><span class="sxs-lookup"><span data-stu-id="ec6c1-118">You can also take a name of a generic type parameter, but the syntax is different:</span></span>

```fsharp
let f<'a> () = nameof<'a>
f() // "a"
```

<span data-ttu-id="ec6c1-119">`nameof<'TGeneric>` 将采用源中定义的符号名称，而不是在调用站点替换的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-119">`nameof<'TGeneric>` will take the name of the symbol as defined in source, not the name of the type substituted at a call site.</span></span>

<span data-ttu-id="ec6c1-120">语法不同的原因在于与和等其他 F # 内部运算符对齐 `typeof<>` `typedefof<>` 。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-120">The reason why the syntax is different is to align with other F# intrinsic operators like `typeof<>` and `typedefof<>`.</span></span> <span data-ttu-id="ec6c1-121">这使 F # 对于作用于泛型类型的运算符和源中的任何其他内容都保持一致。</span><span class="sxs-lookup"><span data-stu-id="ec6c1-121">This makes F# consistent with respect to operators that act on generic types and anything else in source.</span></span>

## <a name="nameof-in-pattern-matching"></a><span data-ttu-id="ec6c1-122">模式匹配中的 Nameof</span><span class="sxs-lookup"><span data-stu-id="ec6c1-122">Nameof in pattern matching</span></span>

<span data-ttu-id="ec6c1-123">[ `nameof` 模式](pattern-matching.md#nameof-pattern)允许 `nameof` 在模式匹配表达式中使用，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ec6c1-123">The [`nameof` pattern](pattern-matching.md#nameof-pattern) lets you use `nameof` in a pattern match expression like so:</span></span>

```fsharp
let f (str: string) =
    match str with
    | nameof str -> "It's 'str'!"
    | _ -> "It is not 'str'!"

f "str" // matches
f "asdf" // does not match
```
