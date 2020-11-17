---
title: 内插字符串
description: '了解内插字符串，它是一种特殊形式的字符串，可用于在其中直接嵌入 F # 表达式。'
ms.date: 11/12/2020
ms.openlocfilehash: a49d4e743306fd9bdabb1e019ec4e6c77e0e1f5a
ms.sourcegitcommit: 34968a61e9bac0f6be23ed6ffb837f52d2390c85
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "94688622"
---
# <a name="interpolated-strings"></a><span data-ttu-id="2bb30-103">内插字符串</span><span class="sxs-lookup"><span data-stu-id="2bb30-103">Interpolated strings</span></span>

<span data-ttu-id="2bb30-104">内插字符串是允许您向其中嵌入 F # 表达式的 [字符串](strings.md) 。</span><span class="sxs-lookup"><span data-stu-id="2bb30-104">Interpolated strings are [strings](strings.md) that allow you to embed F# expressions into them.</span></span> <span data-ttu-id="2bb30-105">它们在各种情况下非常有用，其中字符串的值可能根据值或表达式的结果而变化。</span><span class="sxs-lookup"><span data-stu-id="2bb30-105">They are helpful in a wide range of scenarios where the value of a string may change based on the result of a value or expression.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb30-106">语法</span><span class="sxs-lookup"><span data-stu-id="2bb30-106">Syntax</span></span>

```fsharp
$"string-text {expr}"
$"string-text %format-specifier{expr}"
$"""string-text {"embedded string literal"}"""
```

## <a name="remarks"></a><span data-ttu-id="2bb30-107">备注</span><span class="sxs-lookup"><span data-stu-id="2bb30-107">Remarks</span></span>

<span data-ttu-id="2bb30-108">内插字符串使你可以在字符串文本中的 "洞" 中编写代码。</span><span class="sxs-lookup"><span data-stu-id="2bb30-108">Interpolated strings let you write code in "holes" inside of a string literal.</span></span> <span data-ttu-id="2bb30-109">下面是一个基本示例：</span><span class="sxs-lookup"><span data-stu-id="2bb30-109">Here's a basic example:</span></span>

```fsharp
let name = "Phillip"
let age = 30
printfn $"Name: {name}, Age: {age}"

printfn $"I think {3.0 + 0.14} is close to {System.Math.PI}!"
```

<span data-ttu-id="2bb30-110">每个 `{}` 大括号对之间的内容可以是任何 F # 表达式。</span><span class="sxs-lookup"><span data-stu-id="2bb30-110">The contents in between each `{}` brace pair can be any F# expression.</span></span>

<span data-ttu-id="2bb30-111">若要转义 `{}` 大括号对，请编写两个，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2bb30-111">To escape a `{}` brace pair, write two of them like so:</span></span>

```fsharp
let str = $"A pair of braces: {{}}"
// "A pair of braces: {}"
```

## <a name="typed-interpolated-strings"></a><span data-ttu-id="2bb30-112">类型化内插字符串</span><span class="sxs-lookup"><span data-stu-id="2bb30-112">Typed interpolated strings</span></span>

<span data-ttu-id="2bb30-113">内插字符串还可以具有 F # 格式说明符来强制类型 safey。</span><span class="sxs-lookup"><span data-stu-id="2bb30-113">Interpolated strings can also have F# format specifiers to enforce type safey.</span></span>

```fsharp
let name = "Phillip"
let age = 30

printfn $"Name: %s{name}, Age: %d{age}"

// Error: type mismatch
printfn $"Name: %s{age}, Age: %d{name}"
```

<span data-ttu-id="2bb30-114">在上面的示例中，代码错误地传递了 `age` `name` 应为的值，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="2bb30-114">In the previous example, the code mistakenly passes the `age` value where `name` should be, and vice/versa.</span></span> <span data-ttu-id="2bb30-115">因为内插字符串使用格式说明符，所以这是一个编译错误，而不是微妙的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="2bb30-115">Because the interpolated strings use format specifiers, this is a compile error instead of a subtle runtime bug.</span></span>

<span data-ttu-id="2bb30-116">[纯文本格式](plaintext-formatting.md)中涵盖的所有格式说明符在内插字符串中都有效。</span><span class="sxs-lookup"><span data-stu-id="2bb30-116">All format specifiers covered in [plaintext formatting](plaintext-formatting.md) are valid inside of an interpolated string.</span></span>

## <a name="verbatim-interpolated-strings"></a><span data-ttu-id="2bb30-117">逐字内插字符串</span><span class="sxs-lookup"><span data-stu-id="2bb30-117">Verbatim interpolated strings</span></span>

<span data-ttu-id="2bb30-118">F # 支持带有三个引号的逐字内插字符串，以便可以嵌入字符串文本。</span><span class="sxs-lookup"><span data-stu-id="2bb30-118">F# supports verbatim interpolated strings with triple quotes so that you can embed string literals.</span></span>

```fsharp
let age = 30

printfn $"""Name: {"Phillip"}, Age: %d{age}"""
```

## <a name="aligning-expressions-in-interpolated-strings"></a><span data-ttu-id="2bb30-119">对齐内插字符串中的表达式</span><span class="sxs-lookup"><span data-stu-id="2bb30-119">Aligning expressions in interpolated strings</span></span>

<span data-ttu-id="2bb30-120">您可以使用左对齐或右对齐内插字符串中的表达式 `|` ，并指定多少个空格。</span><span class="sxs-lookup"><span data-stu-id="2bb30-120">You can left-align or right-align expressions inside interpolated strings with `|` and a specification of how many spaces.</span></span> <span data-ttu-id="2bb30-121">下面的内插字符串分别向左和向右对齐7个空格。</span><span class="sxs-lookup"><span data-stu-id="2bb30-121">The following interpolated string aligns the left and right expressions to the left and right, respectively, by 7  spaces.</span></span>

```fsharp
printfn $"""|{"Left",-7}|{"Right",7}|"""
// |Left   |  Right|
```

## <a name="interpolated-strings-and-formattablestring-formatting"></a><span data-ttu-id="2bb30-122">内插字符串和 `FormattableString` 格式设置</span><span class="sxs-lookup"><span data-stu-id="2bb30-122">Interpolated strings and `FormattableString` formatting</span></span>

<span data-ttu-id="2bb30-123">还可以应用符合以下规则的格式 <xref:System.FormattableString> ：</span><span class="sxs-lookup"><span data-stu-id="2bb30-123">You can also apply formatting that adheres to the rules for <xref:System.FormattableString>:</span></span>

```fsharp
let speedOfLight = 299792.458
printfn $"The speed of light is {speedOfLight:N3} km/s."
// "The speed of light is 299,792.458 km/s."
```

<span data-ttu-id="2bb30-124">此外，还可以通过类型注释将内插字符串 typechecked 为 <xref:System.FormattableString> ：</span><span class="sxs-lookup"><span data-stu-id="2bb30-124">Additionally, an interpolated string can also be typechecked as a <xref:System.FormattableString> via a type annotation:</span></span>

```fsharp
let frmtStr = $"The speed of light is {speedOfLight:N3} km/s." : FormattableString
// Type: FormattableString
// The speed of light is 299,792.458 km/s.
```

<span data-ttu-id="2bb30-125">请注意，类型批注必须位于内插字符串表达式本身。</span><span class="sxs-lookup"><span data-stu-id="2bb30-125">Note that the type annotation must be on the interpolated string expression itself.</span></span> <span data-ttu-id="2bb30-126">F # 不会将内插字符串隐式转换为 <xref:System.FormattableString> 。</span><span class="sxs-lookup"><span data-stu-id="2bb30-126">F# does not implicitly convert an interpolated string into a <xref:System.FormattableString>.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bb30-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="2bb30-127">See also</span></span>

* [<span data-ttu-id="2bb30-128">字符串</span><span class="sxs-lookup"><span data-stu-id="2bb30-128">Strings</span></span>](strings.md)
