---
title: 中断性变更：CA2014:请勿在循环中使用 stackalloc
description: 了解 .NET 5.0 中启用代码分析规则 CA2014 所致的中断性变更。
ms.date: 09/03/2020
ms.openlocfilehash: 7ad6203c0edd930bbbe43cdb8df0413cba833d8e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759065"
---
# <a name="warning-ca2014-do-not-use-stackalloc-in-loops"></a><span data-ttu-id="e063e-103">警告 CA2014：请勿在循环中使用 stackalloc</span><span class="sxs-lookup"><span data-stu-id="e063e-103">Warning CA2014: Do not use stackalloc in loops</span></span>

<span data-ttu-id="e063e-104">从 .NET 5.0 开始，默认启用 .NET 代码分析器规则 [CA2014](/visualstudio/code-quality/ca2014)。</span><span class="sxs-lookup"><span data-stu-id="e063e-104">.NET code analyzer rule [CA2014](/visualstudio/code-quality/ca2014) is enabled, by default, starting in .NET 5.0.</span></span> <span data-ttu-id="e063e-105">对于在循环内使用 [stackalloc](../../../../csharp/language-reference/operators/stackalloc.md) 表达式的任何 C# 代码，它都会生成一个生成警告。</span><span class="sxs-lookup"><span data-stu-id="e063e-105">It produces a build warning for any C# code where a [stackalloc](../../../../csharp/language-reference/operators/stackalloc.md) expression is used inside a loop.</span></span>

## <a name="change-description"></a><span data-ttu-id="e063e-106">更改说明</span><span class="sxs-lookup"><span data-stu-id="e063e-106">Change description</span></span>

<span data-ttu-id="e063e-107">从 .NET 5.0 开始，.NET SDK 包括 [.NET 源代码分析器](../../../../fundamentals/code-analysis/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e063e-107">Starting in .NET 5.0, the .NET SDK includes [.NET source code analyzers](../../../../fundamentals/code-analysis/overview.md).</span></span> <span data-ttu-id="e063e-108">其中一些规则会默认启用，包括 [CA2014](/visualstudio/code-quality/ca2014)。</span><span class="sxs-lookup"><span data-stu-id="e063e-108">Several of these rules are enabled, by default, including [CA2014](/visualstudio/code-quality/ca2014).</span></span> <span data-ttu-id="e063e-109">如果项目包含违反此规则的代码，并已被配置为将警告视为错误，则此更改可能会中断生成。</span><span class="sxs-lookup"><span data-stu-id="e063e-109">If your project contains code that violates this rule and is configured to treat warnings as errors, this change could break your build.</span></span>

<span data-ttu-id="e063e-110">规则 CA2014 会查找在循环中使用 [stackalloc 表达式](../../../../csharp/language-reference/operators/stackalloc.md)的 C# 代码。</span><span class="sxs-lookup"><span data-stu-id="e063e-110">Rule CA2014 looks for C# code where a [stackalloc expression](../../../../csharp/language-reference/operators/stackalloc.md) is used inside a loop.</span></span> <span data-ttu-id="e063e-111">[stackalloc](../../../../csharp/language-reference/operators/stackalloc.md) 从当前堆栈帧中分配内存。</span><span class="sxs-lookup"><span data-stu-id="e063e-111">[stackalloc](../../../../csharp/language-reference/operators/stackalloc.md) allocates memory from the current stack frame.</span></span> <span data-ttu-id="e063e-112">在当前方法调用返回之前，不会释放内存，这可能导致堆栈溢出。</span><span class="sxs-lookup"><span data-stu-id="e063e-112">The memory isn't released until the current method call returns, which can lead to stack overflows.</span></span> <span data-ttu-id="e063e-113">因为无法捕获堆栈溢出异常，应用将在发生堆栈溢出时终止。</span><span class="sxs-lookup"><span data-stu-id="e063e-113">Because you can't catch stack overflow exceptions, the app will terminate in case of stack overflow.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="e063e-114">引入的版本</span><span class="sxs-lookup"><span data-stu-id="e063e-114">Version introduced</span></span>

<span data-ttu-id="e063e-115">5.0</span><span class="sxs-lookup"><span data-stu-id="e063e-115">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="e063e-116">建议操作</span><span class="sxs-lookup"><span data-stu-id="e063e-116">Recommended action</span></span>

- <span data-ttu-id="e063e-117">不要在循环内使用 [stackalloc](../../../../csharp/language-reference/operators/stackalloc.md)。</span><span class="sxs-lookup"><span data-stu-id="e063e-117">Avoid using [stackalloc](../../../../csharp/language-reference/operators/stackalloc.md) inside loops.</span></span> <span data-ttu-id="e063e-118">在循环外分配内存块，然后在循环内重用它。</span><span class="sxs-lookup"><span data-stu-id="e063e-118">Allocate the memory block outside the loop and reuse it inside the loop.</span></span> <span data-ttu-id="e063e-119">有关详细信息，请参阅 [CA2014](/visualstudio/code-quality/ca2014)。</span><span class="sxs-lookup"><span data-stu-id="e063e-119">For more information, see [CA2014](/visualstudio/code-quality/ca2014).</span></span>

- <span data-ttu-id="e063e-120">若要完全禁用代码分析，请在项目文件中将 `EnableNETAnalyzers` 设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="e063e-120">To disable code analysis completely, set `EnableNETAnalyzers` to `false` in your project file.</span></span> <span data-ttu-id="e063e-121">有关详细信息，请参阅 [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers)。</span><span class="sxs-lookup"><span data-stu-id="e063e-121">For more information, see [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers).</span></span>

## <a name="affected-apis"></a><span data-ttu-id="e063e-122">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="e063e-122">Affected APIs</span></span>

<span data-ttu-id="e063e-123">无法通过 API 分析检测到。</span><span class="sxs-lookup"><span data-stu-id="e063e-123">Not detectable via API analysis.</span></span>

<!--

### Affected APIs

Not detectable via API analysis.

### Category

Code analysis

-->
