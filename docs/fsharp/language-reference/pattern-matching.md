---
title: 模式匹配
description: '了解如何在 F # 中使用模式，以便将数据与逻辑结构进行比较，将数据分解为各个构成部分，或从数据中提取信息。'
ms.date: 11/12/2020
ms.openlocfilehash: e167712b082b7f587e41a78edcaf0a0db9c7294b
ms.sourcegitcommit: 34968a61e9bac0f6be23ed6ffb837f52d2390c85
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "94687800"
---
# <a name="pattern-matching"></a><span data-ttu-id="f07db-103">模式匹配</span><span class="sxs-lookup"><span data-stu-id="f07db-103">Pattern Matching</span></span>

<span data-ttu-id="f07db-104">模式是用于转换输入数据的规则。</span><span class="sxs-lookup"><span data-stu-id="f07db-104">Patterns are rules for transforming input data.</span></span> <span data-ttu-id="f07db-105">它们在整个 F # 语言中使用，以将数据与一个或多个逻辑结构进行比较，将数据分解为各个构成部分，或以各种方式从数据中提取信息。</span><span class="sxs-lookup"><span data-stu-id="f07db-105">They are used throughout the F# language to compare data with a logical structure or structures, decompose data into constituent parts, or extract information from data in various ways.</span></span>

## <a name="remarks"></a><span data-ttu-id="f07db-106">注解</span><span class="sxs-lookup"><span data-stu-id="f07db-106">Remarks</span></span>

<span data-ttu-id="f07db-107">在许多语言构造（如表达式）中使用模式 `match` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-107">Patterns are used in many language constructs, such as the `match` expression.</span></span> <span data-ttu-id="f07db-108">当您处理 `let` 绑定、lambda 表达式和与表达式关联的异常处理程序中的函数的参数时，将使用这些参数 `try...with` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-108">They are used when you are processing arguments for functions in `let` bindings, lambda expressions, and in the exception handlers associated with the `try...with` expression.</span></span> <span data-ttu-id="f07db-109">有关详细信息，请参阅 [Match 表达式](match-expressions.md)、 [let 绑定](./functions/let-bindings.md)、 [Lambda 表达式： `fun` 关键字](./functions/lambda-expressions-the-fun-keyword.md)和 [异常： `try...with` 表达式](./exception-handling/the-try-with-expression.md)。</span><span class="sxs-lookup"><span data-stu-id="f07db-109">For more information, see [Match Expressions](match-expressions.md), [let Bindings](./functions/let-bindings.md), [Lambda Expressions: The `fun` Keyword](./functions/lambda-expressions-the-fun-keyword.md), and [Exceptions: The `try...with` Expression](./exception-handling/the-try-with-expression.md).</span></span>

<span data-ttu-id="f07db-110">例如，在表达式中 `match` ，管道符号 *pattern* 后跟。</span><span class="sxs-lookup"><span data-stu-id="f07db-110">For example, in the `match` expression, the *pattern* is what follows the pipe symbol.</span></span>

```fsharp
match expression with
| pattern [ when condition ] -> result-expression
...
```

<span data-ttu-id="f07db-111">每个模式都充当以某种方式转换输入的规则。</span><span class="sxs-lookup"><span data-stu-id="f07db-111">Each pattern acts as a rule for transforming input in some way.</span></span> <span data-ttu-id="f07db-112">在 `match` 表达式中，将依次检查每个模式，以查看输入数据是否与模式兼容。</span><span class="sxs-lookup"><span data-stu-id="f07db-112">In the `match` expression, each pattern is examined in turn to see if the input data is compatible with the pattern.</span></span> <span data-ttu-id="f07db-113">如果找到匹配项，则执行结果表达式。</span><span class="sxs-lookup"><span data-stu-id="f07db-113">If a match is found, the result expression is executed.</span></span> <span data-ttu-id="f07db-114">如果找不到匹配项，则测试下一个模式规则。</span><span class="sxs-lookup"><span data-stu-id="f07db-114">If a match is not found, the next pattern rule is tested.</span></span> <span data-ttu-id="f07db-115">在 [匹配表达式](match-expressions.md)中说明时，可选的 when *条件* 部分。</span><span class="sxs-lookup"><span data-stu-id="f07db-115">The optional when *condition* part is explained in [Match Expressions](match-expressions.md).</span></span>

<span data-ttu-id="f07db-116">下表显示了支持的模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-116">Supported patterns are shown in the following table.</span></span> <span data-ttu-id="f07db-117">在运行时，将按照表中列出的顺序针对以下每个模式对输入进行测试，并以递归方式应用模式：在代码中显示时，从第一个到最后一个，以及从左到右的每行模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-117">At run time, the input is tested against each of the following patterns in the order listed in the table, and patterns are applied recursively, from first to last as they appear in your code, and from left to right for the patterns on each line.</span></span>

|<span data-ttu-id="f07db-118">名称</span><span class="sxs-lookup"><span data-stu-id="f07db-118">Name</span></span>|<span data-ttu-id="f07db-119">说明</span><span class="sxs-lookup"><span data-stu-id="f07db-119">Description</span></span>|<span data-ttu-id="f07db-120">示例</span><span class="sxs-lookup"><span data-stu-id="f07db-120">Example</span></span>|
|----|-----------|-------|
|<span data-ttu-id="f07db-121">常量模式</span><span class="sxs-lookup"><span data-stu-id="f07db-121">Constant pattern</span></span>|<span data-ttu-id="f07db-122">任何数值、字符或字符串文本、枚举常量或定义的文本标识符</span><span class="sxs-lookup"><span data-stu-id="f07db-122">Any numeric, character, or string literal, an enumeration constant, or a defined literal identifier</span></span>|<span data-ttu-id="f07db-123">`1.0`, `"test"`, `30`, `Color.Red`</span><span class="sxs-lookup"><span data-stu-id="f07db-123">`1.0`, `"test"`, `30`, `Color.Red`</span></span>|
|<span data-ttu-id="f07db-124">标识符模式</span><span class="sxs-lookup"><span data-stu-id="f07db-124">Identifier pattern</span></span>|<span data-ttu-id="f07db-125">可区分联合、异常标签或活动模式用例的 case 值</span><span class="sxs-lookup"><span data-stu-id="f07db-125">A case value of a discriminated union, an exception label, or an active pattern case</span></span>|`Some(x)`<br /><br />`Failure(msg)`|
|<span data-ttu-id="f07db-126">变量模式</span><span class="sxs-lookup"><span data-stu-id="f07db-126">Variable pattern</span></span>|<span data-ttu-id="f07db-127">*identifier*</span><span class="sxs-lookup"><span data-stu-id="f07db-127">*identifier*</span></span>|`a`|
|<span data-ttu-id="f07db-128">`as` 化</span><span class="sxs-lookup"><span data-stu-id="f07db-128">`as` pattern</span></span>|<span data-ttu-id="f07db-129">作为 *标识符* 的 *模式*</span><span class="sxs-lookup"><span data-stu-id="f07db-129">*pattern* as *identifier*</span></span>|`(a, b) as tuple1`|
|<span data-ttu-id="f07db-130">或模式</span><span class="sxs-lookup"><span data-stu-id="f07db-130">OR pattern</span></span>|<span data-ttu-id="f07db-131">*pattern1* &#124; *pattern2*</span><span class="sxs-lookup"><span data-stu-id="f07db-131">*pattern1* &#124; *pattern2*</span></span>|<code>([h] &#124; [h; _])</code>|
|<span data-ttu-id="f07db-132">AND 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-132">AND pattern</span></span>|<span data-ttu-id="f07db-133">*pattern1* &amp;*pattern2*</span><span class="sxs-lookup"><span data-stu-id="f07db-133">*pattern1* &amp; *pattern2*</span></span>|`(a, b) & (_, "test")`|
|<span data-ttu-id="f07db-134">缺点模式</span><span class="sxs-lookup"><span data-stu-id="f07db-134">Cons pattern</span></span>|<span data-ttu-id="f07db-135">*标识符* ：： *list-标识符*</span><span class="sxs-lookup"><span data-stu-id="f07db-135">*identifier* :: *list-identifier*</span></span>|`h :: t`|
|<span data-ttu-id="f07db-136">列表模式</span><span class="sxs-lookup"><span data-stu-id="f07db-136">List pattern</span></span>|<span data-ttu-id="f07db-137">[ *pattern_1*; ...; *pattern_n* ]</span><span class="sxs-lookup"><span data-stu-id="f07db-137">[ *pattern_1*; ... ; *pattern_n* ]</span></span>|`[ a; b; c ]`|
|<span data-ttu-id="f07db-138">数组模式</span><span class="sxs-lookup"><span data-stu-id="f07db-138">Array pattern</span></span>|<span data-ttu-id="f07db-139">[&#124; *pattern_1*; ...; *pattern_n* &#124;]</span><span class="sxs-lookup"><span data-stu-id="f07db-139">[&#124; *pattern_1*; ..; *pattern_n* &#124;]</span></span>|<code>[&#124; a; b; c &#124;]</code>|
|<span data-ttu-id="f07db-140">带括号模式</span><span class="sxs-lookup"><span data-stu-id="f07db-140">Parenthesized pattern</span></span>|<span data-ttu-id="f07db-141"> ( *模式* ) </span><span class="sxs-lookup"><span data-stu-id="f07db-141">( *pattern* )</span></span>|`( a )`|
|<span data-ttu-id="f07db-142">元组模式</span><span class="sxs-lookup"><span data-stu-id="f07db-142">Tuple pattern</span></span>|<span data-ttu-id="f07db-143"> ( *pattern_1*， *pattern_n* ) </span><span class="sxs-lookup"><span data-stu-id="f07db-143">( *pattern_1*, ... , *pattern_n* )</span></span>|`( a, b )`|
|<span data-ttu-id="f07db-144">记录模式</span><span class="sxs-lookup"><span data-stu-id="f07db-144">Record pattern</span></span>|<span data-ttu-id="f07db-145">{ *identifier1*  = *pattern_1*;... ;*identifier_n*  = *pattern_n* }</span><span class="sxs-lookup"><span data-stu-id="f07db-145">{ *identifier1* = *pattern_1*; ... ; *identifier_n* = *pattern_n* }</span></span>|`{ Name = name; }`|
|<span data-ttu-id="f07db-146">通配符模式</span><span class="sxs-lookup"><span data-stu-id="f07db-146">Wildcard pattern</span></span>|<span data-ttu-id="f07db-147">_</span><span class="sxs-lookup"><span data-stu-id="f07db-147">_</span></span>|`_`|
|<span data-ttu-id="f07db-148">模式与类型注释一起</span><span class="sxs-lookup"><span data-stu-id="f07db-148">Pattern together with type annotation</span></span>|<span data-ttu-id="f07db-149">*模式* ： *类型*</span><span class="sxs-lookup"><span data-stu-id="f07db-149">*pattern* : *type*</span></span>|`a : int`|
|<span data-ttu-id="f07db-150">类型测试模式</span><span class="sxs-lookup"><span data-stu-id="f07db-150">Type test pattern</span></span>|<span data-ttu-id="f07db-151">:?</span><span class="sxs-lookup"><span data-stu-id="f07db-151">:?</span></span> <span data-ttu-id="f07db-152">*类型* [作为 *标识符* ]</span><span class="sxs-lookup"><span data-stu-id="f07db-152">*type* [ as *identifier* ]</span></span>|`:? System.DateTime as dt`|
|<span data-ttu-id="f07db-153">Null 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-153">Null pattern</span></span>|<span data-ttu-id="f07db-154">null</span><span class="sxs-lookup"><span data-stu-id="f07db-154">null</span></span>|`null`|
|<span data-ttu-id="f07db-155">Nameof 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-155">Nameof pattern</span></span>|<span data-ttu-id="f07db-156">*nameof expr*</span><span class="sxs-lookup"><span data-stu-id="f07db-156">*nameof expr*</span></span>|`nameof str`|

## <a name="constant-patterns"></a><span data-ttu-id="f07db-157">常量模式</span><span class="sxs-lookup"><span data-stu-id="f07db-157">Constant Patterns</span></span>

<span data-ttu-id="f07db-158">常量模式包括数值、字符和字符串文本、枚举常量 (包含) 的枚举类型名称。</span><span class="sxs-lookup"><span data-stu-id="f07db-158">Constant patterns are numeric, character, and string literals, enumeration constants (with the enumeration type name included).</span></span> <span data-ttu-id="f07db-159">只能将 `match` 具有恒定模式的表达式与其他语言的 case 语句进行比较。</span><span class="sxs-lookup"><span data-stu-id="f07db-159">A `match` expression that has only constant patterns can be compared to a case statement in other languages.</span></span> <span data-ttu-id="f07db-160">如果值相等，则将输入与文本值进行比较并且模式匹配。</span><span class="sxs-lookup"><span data-stu-id="f07db-160">The input is compared with the literal value and the pattern matches if the values are equal.</span></span> <span data-ttu-id="f07db-161">文本的类型必须与输入的类型兼容。</span><span class="sxs-lookup"><span data-stu-id="f07db-161">The type of the literal must be compatible with the type of the input.</span></span>

<span data-ttu-id="f07db-162">下面的示例演示如何使用文本模式，并且还使用变量模式和或模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-162">The following example demonstrates the use of literal patterns, and also uses a variable pattern and an OR pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4801.fs)]

<span data-ttu-id="f07db-163">文本模式的另一个示例是基于枚举常量的模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-163">Another example of a literal pattern is a pattern based on enumeration constants.</span></span> <span data-ttu-id="f07db-164">使用枚举常量时，必须指定枚举类型名称。</span><span class="sxs-lookup"><span data-stu-id="f07db-164">You must specify the enumeration type name when you use enumeration constants.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4802.fs)]

## <a name="identifier-patterns"></a><span data-ttu-id="f07db-165">标识符模式</span><span class="sxs-lookup"><span data-stu-id="f07db-165">Identifier Patterns</span></span>

<span data-ttu-id="f07db-166">如果模式是形成有效标识符的字符串，则标识符的形式决定了模式的匹配方式。</span><span class="sxs-lookup"><span data-stu-id="f07db-166">If the pattern is a string of characters that forms a valid identifier, the form of the identifier determines how the pattern is matched.</span></span> <span data-ttu-id="f07db-167">如果标识符的长度超过一个字符并且以大写字符开头，则编译器将尝试与标识符模式进行匹配。</span><span class="sxs-lookup"><span data-stu-id="f07db-167">If the identifier is longer than a single character and starts with an uppercase character, the compiler tries to make a match to the identifier pattern.</span></span> <span data-ttu-id="f07db-168">此模式的标识符可以是用文本特性标记的值、可区分联合用例、异常标识符或活动模式用例。</span><span class="sxs-lookup"><span data-stu-id="f07db-168">The identifier for this pattern could be a value marked with the Literal attribute, a discriminated union case, an exception identifier, or an active pattern case.</span></span> <span data-ttu-id="f07db-169">如果未找到匹配的标识符，则匹配将失败，并且会将下一个模式规则（变量模式）与输入进行比较。</span><span class="sxs-lookup"><span data-stu-id="f07db-169">If no matching identifier is found, the match fails and the next pattern rule, the variable pattern, is compared to the input.</span></span>

<span data-ttu-id="f07db-170">可区分联合模式可以是简单的命名事例，也可以具有值或包含多个值的元组。</span><span class="sxs-lookup"><span data-stu-id="f07db-170">Discriminated union patterns can be simple named cases or they can have a value, or a tuple containing multiple values.</span></span> <span data-ttu-id="f07db-171">如果有值，则必须指定值的标识符。</span><span class="sxs-lookup"><span data-stu-id="f07db-171">If there is a value, you must specify an identifier for the value.</span></span> <span data-ttu-id="f07db-172">如果是元组，则必须为元组的每个元素提供一个带有标识符的元组模式，或为一个或多个命名联合字段提供字段名称的标识符。</span><span class="sxs-lookup"><span data-stu-id="f07db-172">In the case of a tuple, you must supply a tuple pattern with an identifier for each element of the tuple or an identifier with a field name for one or more named union fields.</span></span> <span data-ttu-id="f07db-173">有关示例，请参阅本节中的代码示例。</span><span class="sxs-lookup"><span data-stu-id="f07db-173">See the code examples in this section for examples.</span></span>

<span data-ttu-id="f07db-174">`option`类型是具有两个用例（和）的可区分联合 `Some` `None` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-174">The `option` type is a discriminated union that has two cases, `Some` and `None`.</span></span> <span data-ttu-id="f07db-175">一个 (`Some`) 有一个值，但是另一个 (`None`) 只是一个命名的事例。</span><span class="sxs-lookup"><span data-stu-id="f07db-175">One case (`Some`) has a value, but the other (`None`) is just a named case.</span></span> <span data-ttu-id="f07db-176">因此， `Some` 需要为与用例关联的值使用变量 `Some` ，但 `None` 必须单独出现。</span><span class="sxs-lookup"><span data-stu-id="f07db-176">Therefore, `Some` needs to have a variable for the value associated with the `Some` case, but `None` must appear by itself.</span></span> <span data-ttu-id="f07db-177">在下面的代码中，将为变量 `var1` 提供通过匹配大小写获得的值 `Some` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-177">In the following code, the variable `var1` is given the value that is obtained by matching to the `Some` case.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4803.fs)]

<span data-ttu-id="f07db-178">在下面的示例中， `PersonName` 可区分联合包含字符串的混合和表示可能的名称形式的字符。</span><span class="sxs-lookup"><span data-stu-id="f07db-178">In the following example, the `PersonName` discriminated union contains a mixture of strings and characters that represent possible forms of names.</span></span> <span data-ttu-id="f07db-179">可区分联合的情况为 `FirstOnly` 、 `LastOnly` 和 `FirstLast` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-179">The cases of the discriminated union are `FirstOnly`, `LastOnly`, and `FirstLast`.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4804.fs)]

<span data-ttu-id="f07db-180">对于具有命名字段的可区分联合，使用等号 (=) 提取命名字段的值。</span><span class="sxs-lookup"><span data-stu-id="f07db-180">For discriminated unions that have named fields, you use the equals sign (=) to extract the value of a named field.</span></span> <span data-ttu-id="f07db-181">例如，请考虑使用类似于下面的声明的可区分联合。</span><span class="sxs-lookup"><span data-stu-id="f07db-181">For example, consider a discriminated union with a declaration like the following.</span></span>

```fsharp
type Shape =
    | Rectangle of height : float * width : float
    | Circle of radius : float
```

<span data-ttu-id="f07db-182">您可以使用模式匹配表达式中的命名字段，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f07db-182">You can use the named fields in a pattern matching expression as follows.</span></span>

```fsharp
let matchShape shape =
    match shape with
    | Rectangle(height = h) -> printfn "Rectangle with length %f" h
    | Circle(r) -> printfn "Circle with radius %f" r
```

<span data-ttu-id="f07db-183">命名字段的使用是可选的，因此在前面的示例中， `Circle(r)` 和 `Circle(radius = r)` 具有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="f07db-183">The use of the named field is optional, so in the previous example, both `Circle(r)` and `Circle(radius = r)` have the same effect.</span></span>

<span data-ttu-id="f07db-184">指定多个字段时，请使用分号 (; ) 作为分隔符。</span><span class="sxs-lookup"><span data-stu-id="f07db-184">When you specify multiple fields, use the semicolon (;) as a separator.</span></span>

```fsharp
match shape with
| Rectangle(height = h; width = w) -> printfn "Rectangle with height %f and width %f" h w
| _ -> ()
```

<span data-ttu-id="f07db-185">使用活动模式可以定义更复杂的自定义模式匹配。</span><span class="sxs-lookup"><span data-stu-id="f07db-185">Active patterns enable you to define more complex custom pattern matching.</span></span> <span data-ttu-id="f07db-186">有关活动模式的详细信息，请参阅 [活动模式](active-patterns.md)。</span><span class="sxs-lookup"><span data-stu-id="f07db-186">For more information about active patterns, see [Active Patterns](active-patterns.md).</span></span>

<span data-ttu-id="f07db-187">标识符为异常的情况在异常处理程序上下文的模式匹配中使用。</span><span class="sxs-lookup"><span data-stu-id="f07db-187">The case in which the identifier is an exception is used in pattern matching in the context of exception handlers.</span></span> <span data-ttu-id="f07db-188">有关异常处理中的模式匹配的信息，请参阅 [异常： `try...with` 表达式](./exception-handling/the-try-with-expression.md)。</span><span class="sxs-lookup"><span data-stu-id="f07db-188">For information about pattern matching in exception handling, see [Exceptions: The `try...with` Expression](./exception-handling/the-try-with-expression.md).</span></span>

## <a name="variable-patterns"></a><span data-ttu-id="f07db-189">变量模式</span><span class="sxs-lookup"><span data-stu-id="f07db-189">Variable Patterns</span></span>

<span data-ttu-id="f07db-190">变量模式将匹配的值分配给一个变量名称，该变量可在符号右侧的执行表达式中使用 `->` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-190">The variable pattern assigns the value being matched to a variable name, which is then available for use in the execution expression to the right of the `->` symbol.</span></span> <span data-ttu-id="f07db-191">变量模式单独与任何输入匹配，但变量模式通常显示在其他模式内，因此可以将更复杂的结构（例如元组和数组）分解为变量。</span><span class="sxs-lookup"><span data-stu-id="f07db-191">A variable pattern alone matches any input, but variable patterns often appear within other patterns, therefore enabling more complex structures such as tuples and arrays to be decomposed into variables.</span></span>

<span data-ttu-id="f07db-192">下面的示例演示元组模式内的变量模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-192">The following example demonstrates a variable pattern within a tuple pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4805.fs)]

## <a name="as-pattern"></a><span data-ttu-id="f07db-193">as 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-193">as Pattern</span></span>

<span data-ttu-id="f07db-194">`as`模式是一个附加了子句的模式 `as` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-194">The `as` pattern is a pattern that has an `as` clause appended to it.</span></span> <span data-ttu-id="f07db-195">`as`子句将匹配的值绑定到可在表达式的执行表达式中使用的名称， `match` 或者，如果在绑定中使用此模式，则会将 `let` 该名称作为绑定添加到本地范围。</span><span class="sxs-lookup"><span data-stu-id="f07db-195">The `as` clause binds the matched value to a name that can be used in the execution expression of a `match` expression, or, in the case where this pattern is used in a `let` binding, the name is added as a binding to the local scope.</span></span>

<span data-ttu-id="f07db-196">下面的示例使用 `as` 模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-196">The following example uses an `as` pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4806.fs)]

## <a name="or-pattern"></a><span data-ttu-id="f07db-197">或模式</span><span class="sxs-lookup"><span data-stu-id="f07db-197">OR Pattern</span></span>

<span data-ttu-id="f07db-198">当输入数据可以匹配多个模式，并且您想要执行与结果相同的代码时，可以使用或模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-198">The OR pattern is used when input data can match multiple patterns, and you want to execute the same code as a result.</span></span> <span data-ttu-id="f07db-199">或模式两边的类型必须兼容。</span><span class="sxs-lookup"><span data-stu-id="f07db-199">The types of both sides of the OR pattern must be compatible.</span></span>

<span data-ttu-id="f07db-200">下面的示例演示了或模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-200">The following example demonstrates the OR pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4807.fs)]

## <a name="and-pattern"></a><span data-ttu-id="f07db-201">AND 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-201">AND Pattern</span></span>

<span data-ttu-id="f07db-202">和模式要求输入匹配两种模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-202">The AND pattern requires that the input match two patterns.</span></span> <span data-ttu-id="f07db-203">和模式两边的类型必须兼容。</span><span class="sxs-lookup"><span data-stu-id="f07db-203">The types of both sides of the AND pattern must be compatible.</span></span>

<span data-ttu-id="f07db-204">下面的示例类似于 `detectZeroTuple` 本主题后面的元组模式部分中所示的示例，但这两个 `var1` 和 `var2` 都是使用和模式作为值获取的。</span><span class="sxs-lookup"><span data-stu-id="f07db-204">The following example is like `detectZeroTuple` shown in the Tuple Pattern section later in this topic, but here both `var1` and `var2` are obtained as values by using the AND pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4808.fs)]

## <a name="cons-pattern"></a><span data-ttu-id="f07db-205">缺点模式</span><span class="sxs-lookup"><span data-stu-id="f07db-205">Cons Pattern</span></span>

<span data-ttu-id="f07db-206">缺点模式用于将列表分解为第一个元素、 *头* 以及包含剩余元素（ *尾部*）的列表。</span><span class="sxs-lookup"><span data-stu-id="f07db-206">The cons pattern is used to decompose a list into the first element, the *head*, and a list that contains the remaining elements, the *tail*.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4809.fs)]

## <a name="list-pattern"></a><span data-ttu-id="f07db-207">列表模式</span><span class="sxs-lookup"><span data-stu-id="f07db-207">List Pattern</span></span>

<span data-ttu-id="f07db-208">列表模式使列表可分解为多个元素。</span><span class="sxs-lookup"><span data-stu-id="f07db-208">The list pattern enables lists to be decomposed into a number of elements.</span></span> <span data-ttu-id="f07db-209">列表模式本身只能匹配特定数量的元素的列表。</span><span class="sxs-lookup"><span data-stu-id="f07db-209">The list pattern itself can match only lists of a specific number of elements.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4810.fs)]

## <a name="array-pattern"></a><span data-ttu-id="f07db-210">数组模式</span><span class="sxs-lookup"><span data-stu-id="f07db-210">Array Pattern</span></span>

<span data-ttu-id="f07db-211">数组模式类似于列表模式，可用于分解特定长度的数组。</span><span class="sxs-lookup"><span data-stu-id="f07db-211">The array pattern resembles the list pattern and can be used to decompose arrays of a specific length.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4811.fs)]

## <a name="parenthesized-pattern"></a><span data-ttu-id="f07db-212">带括号模式</span><span class="sxs-lookup"><span data-stu-id="f07db-212">Parenthesized Pattern</span></span>

<span data-ttu-id="f07db-213">括号可以围绕模式分组，以实现所需的关联性。</span><span class="sxs-lookup"><span data-stu-id="f07db-213">Parentheses can be grouped around patterns to achieve the desired associativity.</span></span> <span data-ttu-id="f07db-214">在下面的示例中，括号用于控制和模式与缺点模式之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="f07db-214">In the following example, parentheses are used to control associativity between an AND pattern and a cons pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4812.fs)]

## <a name="tuple-pattern"></a><span data-ttu-id="f07db-215">元组模式</span><span class="sxs-lookup"><span data-stu-id="f07db-215">Tuple Pattern</span></span>

<span data-ttu-id="f07db-216">元组模式与元组格式的输入匹配，并通过对元组中的每个位置使用模式匹配变量，将元组分解为其构成元素。</span><span class="sxs-lookup"><span data-stu-id="f07db-216">The tuple pattern matches input in tuple form and enables the tuple to be decomposed into its constituent elements by using pattern matching variables for each position in the tuple.</span></span>

<span data-ttu-id="f07db-217">下面的示例演示元组模式，还使用文本模式、变量模式和通配符模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-217">The following example demonstrates the tuple pattern and also uses literal patterns, variable patterns, and the wildcard pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4813.fs)]

## <a name="record-pattern"></a><span data-ttu-id="f07db-218">记录模式</span><span class="sxs-lookup"><span data-stu-id="f07db-218">Record Pattern</span></span>

<span data-ttu-id="f07db-219">记录模式用于分解记录，以便提取字段的值。</span><span class="sxs-lookup"><span data-stu-id="f07db-219">The record pattern is used to decompose records to extract the values of fields.</span></span> <span data-ttu-id="f07db-220">模式不必引用记录的所有字段;所有省略的字段不会参与匹配，也不会被提取。</span><span class="sxs-lookup"><span data-stu-id="f07db-220">The pattern does not have to reference all fields of the record; any omitted fields just do not participate in matching and are not extracted.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4814.fs)]

## <a name="wildcard-pattern"></a><span data-ttu-id="f07db-221">通配符模式</span><span class="sxs-lookup"><span data-stu-id="f07db-221">Wildcard Pattern</span></span>

<span data-ttu-id="f07db-222">通配符模式由下划线 () 字符表示， `_` 并与变量模式相同，只是丢弃输入，而不是分配给变量。</span><span class="sxs-lookup"><span data-stu-id="f07db-222">The wildcard pattern is represented by the underscore (`_`) character and matches any input, just like the variable pattern, except that the input is discarded instead of assigned to a variable.</span></span> <span data-ttu-id="f07db-223">通配符模式通常用在其他模式内作为值的占位符，而在该符号右侧的表达式中不需要这些值 `->` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-223">The wildcard pattern is often used within other patterns as a placeholder for values that are not needed in the expression to the right of the `->` symbol.</span></span> <span data-ttu-id="f07db-224">通配符模式还经常用于模式列表的末尾，以匹配任何不匹配的输入。</span><span class="sxs-lookup"><span data-stu-id="f07db-224">The wildcard pattern is also frequently used at the end of a list of patterns to match any unmatched input.</span></span> <span data-ttu-id="f07db-225">本主题中的许多代码示例演示了通配符模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-225">The wildcard pattern is demonstrated in many code examples in this topic.</span></span> <span data-ttu-id="f07db-226">有关示例，请参阅前面的代码。</span><span class="sxs-lookup"><span data-stu-id="f07db-226">See the preceding code for one example.</span></span>

## <a name="patterns-that-have-type-annotations"></a><span data-ttu-id="f07db-227">具有类型批注的模式</span><span class="sxs-lookup"><span data-stu-id="f07db-227">Patterns That Have Type Annotations</span></span>

<span data-ttu-id="f07db-228">模式可以具有类型批注。</span><span class="sxs-lookup"><span data-stu-id="f07db-228">Patterns can have type annotations.</span></span> <span data-ttu-id="f07db-229">它们的行为与其他类型注释和其他类型注释类似。</span><span class="sxs-lookup"><span data-stu-id="f07db-229">These behave like other type annotations and guide inference like other type annotations.</span></span> <span data-ttu-id="f07db-230">在模式中的类型批注前后需要括号。</span><span class="sxs-lookup"><span data-stu-id="f07db-230">Parentheses are required around type annotations in patterns.</span></span> <span data-ttu-id="f07db-231">下面的代码演示具有类型批注的模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-231">The following code shows a pattern that has a type annotation.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4815.fs)]

## <a name="type-test-pattern"></a><span data-ttu-id="f07db-232">类型测试模式</span><span class="sxs-lookup"><span data-stu-id="f07db-232">Type Test Pattern</span></span>

<span data-ttu-id="f07db-233">类型测试模式用于将输入与类型进行匹配。</span><span class="sxs-lookup"><span data-stu-id="f07db-233">The type test pattern is used to match the input against a type.</span></span> <span data-ttu-id="f07db-234">如果输入类型与在模式中指定的类型) 的 (或派生类型匹配，则匹配成功。</span><span class="sxs-lookup"><span data-stu-id="f07db-234">If the input type is a match to (or a derived type of) the type specified in the pattern, the match succeeds.</span></span>

<span data-ttu-id="f07db-235">下面的示例演示了类型测试模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-235">The following example demonstrates the type test pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4816.fs)]

<span data-ttu-id="f07db-236">如果只检查标识符是否为特定的派生类型，则不需要 `as identifier` 模式的一部分，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="f07db-236">If you're only checking if an identifier is of a particular derived type, you don't need the `as identifier` part of the pattern, as shown in the following example:</span></span>

```fsharp
type A() = class end
type B() = inherit A()
type C() = inherit A()

let m (a: A) =
    match a with
    | :? B -> printfn "It's a B"
    | :? C -> printfn "It's a C"
    | _ -> ()
```

## <a name="null-pattern"></a><span data-ttu-id="f07db-237">Null 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-237">Null Pattern</span></span>

<span data-ttu-id="f07db-238">Null 模式匹配可以在使用允许 null 值的类型时显示的 null 值。</span><span class="sxs-lookup"><span data-stu-id="f07db-238">The null pattern matches the null value that can appear when you are working with types that allow a null value.</span></span> <span data-ttu-id="f07db-239">与 .NET Framework 代码互操作时，经常使用 Null 模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-239">Null patterns are frequently used when interoperating with .NET Framework code.</span></span> <span data-ttu-id="f07db-240">例如，.NET API 的返回值可能是表达式的输入 `match` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-240">For example, the return value of a .NET API might be the input to a `match` expression.</span></span> <span data-ttu-id="f07db-241">您可以根据返回值是否为 null 以及返回值的其他特征来控制程序流。</span><span class="sxs-lookup"><span data-stu-id="f07db-241">You can control program flow based on whether the return value is null, and also on other characteristics of the returned value.</span></span> <span data-ttu-id="f07db-242">可以使用 null 模式来防止空值传播到程序的其余部分。</span><span class="sxs-lookup"><span data-stu-id="f07db-242">You can use the null pattern to prevent null values from propagating to the rest of your program.</span></span>

<span data-ttu-id="f07db-243">下面的示例使用 null 模式和变量模式。</span><span class="sxs-lookup"><span data-stu-id="f07db-243">The following example uses the null pattern and the variable pattern.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-2/snippet4817.fs)]

## <a name="nameof-pattern"></a><span data-ttu-id="f07db-244">Nameof 模式</span><span class="sxs-lookup"><span data-stu-id="f07db-244">Nameof pattern</span></span>

<span data-ttu-id="f07db-245">`nameof`当某个字符串的值等于关键字后面的表达式时，该模式与字符串匹配 `nameof` 。</span><span class="sxs-lookup"><span data-stu-id="f07db-245">The `nameof` pattern matches against a string when its value is equal to the expression that follows the `nameof` keyword.</span></span> <span data-ttu-id="f07db-246">例如：</span><span class="sxs-lookup"><span data-stu-id="f07db-246">for example:</span></span>

```fsharp
let f (str: string) =
    match str with
    | nameof str -> "It's 'str'!"
    | _ -> "It is not 'str'!"

f "str" // matches
f "asdf" // does not match
```

<span data-ttu-id="f07db-247">有关 [`nameof`](nameof.md) 可获取名称的信息，请参阅运算符。</span><span class="sxs-lookup"><span data-stu-id="f07db-247">See the [`nameof`](nameof.md) operator for information on what you can take a name of.</span></span>

## <a name="see-also"></a><span data-ttu-id="f07db-248">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f07db-248">See also</span></span>

- [<span data-ttu-id="f07db-249">Match 表达式</span><span class="sxs-lookup"><span data-stu-id="f07db-249">Match Expressions</span></span>](match-expressions.md)
- [<span data-ttu-id="f07db-250">活动模式</span><span class="sxs-lookup"><span data-stu-id="f07db-250">Active Patterns</span></span>](active-patterns.md)
- [<span data-ttu-id="f07db-251">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="f07db-251">F# Language Reference</span></span>](index.md)
