---
title: 中断性变更：CA2015:请勿为派生自 MemoryManager<T> 的类型定义终结器
description: 了解 .NET 5.0 中启用代码分析规则 CA2015 所致的中断性变更。
ms.date: 09/03/2020
ms.openlocfilehash: 5d0ba0546b5a72363559f23713c8af4bb4e26e48
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759064"
---
# <a name="warning-ca2015-do-not-define-finalizers-for-types-derived-from-memorymanagert"></a><span data-ttu-id="37bfe-103">警告 CA2015：请勿为派生自 MemoryManager\<T> 的类型定义终结器</span><span class="sxs-lookup"><span data-stu-id="37bfe-103">Warning CA2015: Do not define finalizers for types derived from MemoryManager\<T></span></span>

<span data-ttu-id="37bfe-104">从 .NET 5.0 开始，默认启用 .NET 代码分析器规则 [CA2015](/visualstudio/code-quality/ca2015)。</span><span class="sxs-lookup"><span data-stu-id="37bfe-104">.NET code analyzer rule [CA2015](/visualstudio/code-quality/ca2015) is enabled, by default, starting in .NET 5.0.</span></span> <span data-ttu-id="37bfe-105">对于派生自定义终结器的 <xref:System.Buffers.MemoryManager%601> 的任何类型，它都会生成一个生成警告。</span><span class="sxs-lookup"><span data-stu-id="37bfe-105">It produces a build warning for any types that derive from <xref:System.Buffers.MemoryManager%601> that define a finalizer.</span></span>

## <a name="change-description"></a><span data-ttu-id="37bfe-106">更改说明</span><span class="sxs-lookup"><span data-stu-id="37bfe-106">Change description</span></span>

<span data-ttu-id="37bfe-107">从 .NET 5.0 开始，.NET SDK 包括 [.NET 源代码分析器](../../../../fundamentals/code-analysis/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="37bfe-107">Starting in .NET 5.0, the .NET SDK includes [.NET source code analyzers](../../../../fundamentals/code-analysis/overview.md).</span></span> <span data-ttu-id="37bfe-108">其中一些规则会默认启用，包括 [CA2015](/visualstudio/code-quality/ca2015)。</span><span class="sxs-lookup"><span data-stu-id="37bfe-108">Several of these rules are enabled, by default, including [CA2015](/visualstudio/code-quality/ca2015).</span></span> <span data-ttu-id="37bfe-109">如果项目包含违反此规则的代码，并已被配置为将警告视为错误，则此更改可能会中断生成。</span><span class="sxs-lookup"><span data-stu-id="37bfe-109">If your project contains code that violates this rule and is configured to treat warnings as errors, this change could break your build.</span></span>

<span data-ttu-id="37bfe-110">派生自定义终结器的 <xref:System.Buffers.MemoryManager%601> 的规则 CA2015 标记类型。</span><span class="sxs-lookup"><span data-stu-id="37bfe-110">Rule CA2015 flags types that derive from <xref:System.Buffers.MemoryManager%601> that define a finalizer.</span></span> <span data-ttu-id="37bfe-111">将终结器添加到派生自 <xref:System.Buffers.MemoryManager%601> 的类型可能表明存在 bug。</span><span class="sxs-lookup"><span data-stu-id="37bfe-111">Adding a finalizer to a type that derives from <xref:System.Buffers.MemoryManager%601> is likely an indication of a bug.</span></span> <span data-ttu-id="37bfe-112">这表明在 <xref:System.Span%601> 中获得的本机资源正在被清除，同时 <xref:System.Span%601> 可能仍在使用该资源。</span><span class="sxs-lookup"><span data-stu-id="37bfe-112">It suggests that a native resource that could have been obtained in a <xref:System.Span%601> is getting cleaned up, potentially while it's still in use by the <xref:System.Span%601>.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="37bfe-113">引入的版本</span><span class="sxs-lookup"><span data-stu-id="37bfe-113">Version introduced</span></span>

<span data-ttu-id="37bfe-114">5.0</span><span class="sxs-lookup"><span data-stu-id="37bfe-114">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="37bfe-115">建议操作</span><span class="sxs-lookup"><span data-stu-id="37bfe-115">Recommended action</span></span>

- <span data-ttu-id="37bfe-116">删除终结器定义。</span><span class="sxs-lookup"><span data-stu-id="37bfe-116">Remove the finalizer definition.</span></span> <span data-ttu-id="37bfe-117">有关详细信息，请参阅 [CA2015](/visualstudio/code-quality/ca2015)。</span><span class="sxs-lookup"><span data-stu-id="37bfe-117">For more information, see [CA2015](/visualstudio/code-quality/ca2015).</span></span>

- <span data-ttu-id="37bfe-118">若要完全禁用代码分析，请在项目文件中将 `EnableNETAnalyzers` 设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="37bfe-118">To disable code analysis completely, set `EnableNETAnalyzers` to `false` in your project file.</span></span> <span data-ttu-id="37bfe-119">有关详细信息，请参阅 [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers)。</span><span class="sxs-lookup"><span data-stu-id="37bfe-119">For more information, see [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers).</span></span>

## <a name="affected-apis"></a><span data-ttu-id="37bfe-120">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="37bfe-120">Affected APIs</span></span>

<span data-ttu-id="37bfe-121">无法通过 API 分析检测到。</span><span class="sxs-lookup"><span data-stu-id="37bfe-121">Not detectable via API analysis.</span></span>

<!--

### Affected APIs

Not detectable via API analysis.

### Category

Code analysis

-->
