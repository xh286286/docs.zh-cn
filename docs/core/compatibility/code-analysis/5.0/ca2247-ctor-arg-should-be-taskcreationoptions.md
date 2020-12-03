---
title: 中断性变更：CA2247:TaskCompletionSource 构造函数的参数应为 TaskCreationOptions 值
description: 了解 .NET 5.0 中启用代码分析规则 CA2247 所致的中断性变更。
ms.date: 09/03/2020
ms.openlocfilehash: 323fd5a05da4dfeb68ef75d88d5d293ba01c8ade
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759169"
---
# <a name="warning-ca2247-argument-to-taskcompletionsource-constructor-should-be-taskcreationoptions-value"></a><span data-ttu-id="33ef7-103">警告 CA2247：TaskCompletionSource 构造函数的参数应为 TaskCreationOptions 值</span><span class="sxs-lookup"><span data-stu-id="33ef7-103">Warning CA2247: Argument to TaskCompletionSource constructor should be TaskCreationOptions value</span></span>

<span data-ttu-id="33ef7-104">从 .NET 5.0 开始，默认启用 .NET 代码分析器规则 [CA2247](/visualstudio/code-quality/ca2247)。</span><span class="sxs-lookup"><span data-stu-id="33ef7-104">.NET code analyzer rule [CA2247](/visualstudio/code-quality/ca2247) is enabled, by default, starting in .NET 5.0.</span></span> <span data-ttu-id="33ef7-105">关于对 <xref:System.Threading.Tasks.TaskCompletionSource%601> 构造函数的调用（该函数传递类型为 <xref:System.Threading.Tasks.TaskContinuationOptions> 的参数），它会生成一个生成警告。</span><span class="sxs-lookup"><span data-stu-id="33ef7-105">It produces a build warning for calls to the <xref:System.Threading.Tasks.TaskCompletionSource%601> constructor that pass an argument of type <xref:System.Threading.Tasks.TaskContinuationOptions>.</span></span>

## <a name="change-description"></a><span data-ttu-id="33ef7-106">更改说明</span><span class="sxs-lookup"><span data-stu-id="33ef7-106">Change description</span></span>

<span data-ttu-id="33ef7-107">从 .NET 5.0 开始，.NET SDK 包括 [.NET 源代码分析器](../../../../fundamentals/code-analysis/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="33ef7-107">Starting in .NET 5.0, the .NET SDK includes [.NET source code analyzers](../../../../fundamentals/code-analysis/overview.md).</span></span> <span data-ttu-id="33ef7-108">其中一些规则会默认启用，包括 [CA2247](/visualstudio/code-quality/ca2247)。</span><span class="sxs-lookup"><span data-stu-id="33ef7-108">Several of these rules are enabled, by default, including [CA2247](/visualstudio/code-quality/ca2247).</span></span> <span data-ttu-id="33ef7-109">如果项目包含违反此规则的代码，并已被配置为将警告视为错误，则此更改可能会中断生成。</span><span class="sxs-lookup"><span data-stu-id="33ef7-109">If your project contains code that violates this rule and is configured to treat warnings as errors, this change could break your build.</span></span>

<span data-ttu-id="33ef7-110">规则 CA2247 会查找对 <xref:System.Threading.Tasks.TaskCompletionSource%601> 构造函数的调用，这些调用传递类型为 <xref:System.Threading.Tasks.TaskContinuationOptions> 的参数。</span><span class="sxs-lookup"><span data-stu-id="33ef7-110">Rule CA2247 finds calls to the <xref:System.Threading.Tasks.TaskCompletionSource%601> constructor that pass an argument of type <xref:System.Threading.Tasks.TaskContinuationOptions>.</span></span> <span data-ttu-id="33ef7-111"><xref:System.Threading.Tasks.TaskCompletionSource%601> 类型具有一个接受 <xref:System.Threading.Tasks.TaskCreationOptions> 值的构造函数和一个接受 <xref:System.Object> 的构造函数。</span><span class="sxs-lookup"><span data-stu-id="33ef7-111">The <xref:System.Threading.Tasks.TaskCompletionSource%601> type has a constructor that accepts a <xref:System.Threading.Tasks.TaskCreationOptions> value, and another constructor that accepts an <xref:System.Object>.</span></span> <span data-ttu-id="33ef7-112">如果意外传递了 <xref:System.Threading.Tasks.TaskContinuationOptions> 值（而不是 <xref:System.Threading.Tasks.TaskCreationOptions> 值），则在运行时调用带有 <xref:System.Object> 参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="33ef7-112">If you accidentally pass a <xref:System.Threading.Tasks.TaskContinuationOptions> value instead of a <xref:System.Threading.Tasks.TaskCreationOptions> value, the constructor with the <xref:System.Object> parameter is called at run time.</span></span> <span data-ttu-id="33ef7-113">代码将编译并运行，但没有预期行为。</span><span class="sxs-lookup"><span data-stu-id="33ef7-113">Your code will compile and run but won't have the intended behavior.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="33ef7-114">引入的版本</span><span class="sxs-lookup"><span data-stu-id="33ef7-114">Version introduced</span></span>

<span data-ttu-id="33ef7-115">5.0</span><span class="sxs-lookup"><span data-stu-id="33ef7-115">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="33ef7-116">建议操作</span><span class="sxs-lookup"><span data-stu-id="33ef7-116">Recommended action</span></span>

- <span data-ttu-id="33ef7-117">将 <xref:System.Threading.Tasks.TaskContinuationOptions> 参数替换为相应的 <xref:System.Threading.Tasks.TaskCreationOptions> 值。</span><span class="sxs-lookup"><span data-stu-id="33ef7-117">Replace the <xref:System.Threading.Tasks.TaskContinuationOptions> argument with the corresponding <xref:System.Threading.Tasks.TaskCreationOptions> value.</span></span> <span data-ttu-id="33ef7-118">请勿禁止显示此警告，因为它几乎总是突出显示代码中的 bug。</span><span class="sxs-lookup"><span data-stu-id="33ef7-118">Do not suppress this warning, since it almost always highlights a bug in your code.</span></span> <span data-ttu-id="33ef7-119">有关详细信息，请参阅 [CA2247](/visualstudio/code-quality/ca2247)。</span><span class="sxs-lookup"><span data-stu-id="33ef7-119">For more information, see [CA2247](/visualstudio/code-quality/ca2247).</span></span>

- <span data-ttu-id="33ef7-120">若要完全禁用代码分析，请在项目文件中将 `EnableNETAnalyzers` 设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="33ef7-120">To disable code analysis completely, set `EnableNETAnalyzers` to `false` in your project file.</span></span> <span data-ttu-id="33ef7-121">有关详细信息，请参阅 [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers)。</span><span class="sxs-lookup"><span data-stu-id="33ef7-121">For more information, see [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers).</span></span>

## <a name="affected-apis"></a><span data-ttu-id="33ef7-122">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="33ef7-122">Affected APIs</span></span>

- <xref:System.Threading.Tasks.TaskCompletionSource%601.%23ctor(System.Object)>

<!--

### Affected APIs

- ``M:System.Threading.Tasks.TaskCompletionSource`1.#ctor(System.Object)``

### Category

Code analysis

-->
