---
title: 中断性变更：CA1831:为字符串使用 AsSpan 而不是基于范围的索引器
description: 了解 .NET 5.0 中启用代码分析规则 CA1831 所致的中断性变更。
ms.date: 08/21/2020
ms.openlocfilehash: 850916b804ae29dba8d2bd05c6e4fb06fe667296
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96437892"
---
# <a name="warning-ca1831-use-asspan-instead-of-range-based-indexers-for-string"></a><span data-ttu-id="ba81f-103">警告 CA1831：为字符串使用 AsSpan 而不是基于范围的索引器</span><span class="sxs-lookup"><span data-stu-id="ba81f-103">Warning CA1831: Use AsSpan instead of Range-based indexers for string</span></span>

<span data-ttu-id="ba81f-104">默认情况下，从 .NET 5.0 开始启用 .NET 代码分析器规则 [CA1831](/visualstudio/code-quality/ca1831)。</span><span class="sxs-lookup"><span data-stu-id="ba81f-104">.NET code analyzer rule [CA1831](/visualstudio/code-quality/ca1831) is enabled, by default, starting in .NET 5.0.</span></span> <span data-ttu-id="ba81f-105">对于在字符串中使用基于 <xref:System.Range> 的索引器，但不打算进行复制的任何代码，都将生成一个生成警告。</span><span class="sxs-lookup"><span data-stu-id="ba81f-105">It produces a build warning for any code where a <xref:System.Range>-based indexer is used on a string, but no copy was intended.</span></span>

## <a name="change-description"></a><span data-ttu-id="ba81f-106">更改说明</span><span class="sxs-lookup"><span data-stu-id="ba81f-106">Change description</span></span>

<span data-ttu-id="ba81f-107">从 .NET 5.0 开始，.NET SDK 包括 [.NET 源代码分析器](../../../../fundamentals/code-analysis/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ba81f-107">Starting in .NET 5.0, the .NET SDK includes [.NET source code analyzers](../../../../fundamentals/code-analysis/overview.md).</span></span> <span data-ttu-id="ba81f-108">默认情况下会启用其中一些规则，包括 [CA1831](/visualstudio/code-quality/ca1831)。</span><span class="sxs-lookup"><span data-stu-id="ba81f-108">Several of these rules are enabled, by default, including [CA1831](/visualstudio/code-quality/ca1831).</span></span> <span data-ttu-id="ba81f-109">如果项目包含违反此规则的代码，并已被配置为将警告视为错误，则此更改可能会中断生成。</span><span class="sxs-lookup"><span data-stu-id="ba81f-109">If your project contains code that violates this rule and is configured to treat warnings as errors, this change could break your build.</span></span>

<span data-ttu-id="ba81f-110">规则 CA1831 查找在字符串中使用基于 <xref:System.Range> 的索引器但不打算进行复制的实例。</span><span class="sxs-lookup"><span data-stu-id="ba81f-110">Rule CA1831 finds instances where a <xref:System.Range>-based indexer is used on a string, but no copy was intended.</span></span> <span data-ttu-id="ba81f-111">如果直接在字符串中使用基于 <xref:System.Range> 的索引器来生成隐式强制转换，则会创建字符串请求部分的不必要副本。</span><span class="sxs-lookup"><span data-stu-id="ba81f-111">If the <xref:System.Range>-based indexer is used directly on a string to produce an implicit cast, then an unnecessary copy of the requested portion of the string is created.</span></span> <span data-ttu-id="ba81f-112">例如：</span><span class="sxs-lookup"><span data-stu-id="ba81f-112">For example:</span></span>

```csharp
ReadOnlySpan<char> slice = str[1..3];
```

<span data-ttu-id="ba81f-113">相反，CA1831 建议在字符串的“范围”上使用基于 <xref:System.Range> 的索引器。</span><span class="sxs-lookup"><span data-stu-id="ba81f-113">CA1831 suggests using the <xref:System.Range>-based indexer on a *span* of the string, instead.</span></span> <span data-ttu-id="ba81f-114">例如：</span><span class="sxs-lookup"><span data-stu-id="ba81f-114">For example:</span></span>

```csharp
ReadOnlySpan<char> slice = str.AsSpan()[1..3];
```

## <a name="version-introduced"></a><span data-ttu-id="ba81f-115">引入的版本</span><span class="sxs-lookup"><span data-stu-id="ba81f-115">Version introduced</span></span>

<span data-ttu-id="ba81f-116">5.0</span><span class="sxs-lookup"><span data-stu-id="ba81f-116">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="ba81f-117">建议操作</span><span class="sxs-lookup"><span data-stu-id="ba81f-117">Recommended action</span></span>

- <span data-ttu-id="ba81f-118">若要更正代码并避免不必要的分配，请在使用基于 <xref:System.Range> 的索引器之前调用 <xref:System.MemoryExtensions.AsSpan(System.String)> 或 <xref:System.MemoryExtensions.AsMemory(System.String)>。</span><span class="sxs-lookup"><span data-stu-id="ba81f-118">To correct your code and avoid unnecessary allocations, call <xref:System.MemoryExtensions.AsSpan(System.String)> or <xref:System.MemoryExtensions.AsMemory(System.String)> before using the <xref:System.Range>-based indexer.</span></span> <span data-ttu-id="ba81f-119">例如：</span><span class="sxs-lookup"><span data-stu-id="ba81f-119">For example:</span></span>

  ```csharp
  ReadOnlySpan<char> slice = str.AsSpan()[1..3];
  ```

- <span data-ttu-id="ba81f-120">如果不想更改代码，则可通过将规则的严重性设置为 `suggestion` 或 `none` 来禁用规则。</span><span class="sxs-lookup"><span data-stu-id="ba81f-120">If you don't want to change your code, you can disable the rule by setting its severity to `suggestion` or `none`.</span></span> <span data-ttu-id="ba81f-121">有关详细信息，请参阅[配置代码分析规则](../../../../fundamentals/code-analysis/configuration-options.md)。</span><span class="sxs-lookup"><span data-stu-id="ba81f-121">For more information, see [Configure code analysis rules](../../../../fundamentals/code-analysis/configuration-options.md).</span></span>

- <span data-ttu-id="ba81f-122">若要完全禁用代码分析，请在项目文件中将 `EnableNETAnalyzers` 设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="ba81f-122">To disable code analysis completely, set `EnableNETAnalyzers` to `false` in your project file.</span></span> <span data-ttu-id="ba81f-123">有关详细信息，请参阅 [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers)。</span><span class="sxs-lookup"><span data-stu-id="ba81f-123">For more information, see [EnableNETAnalyzers](../../../project-sdk/msbuild-props.md#enablenetanalyzers).</span></span>

## <a name="affected-apis"></a><span data-ttu-id="ba81f-124">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="ba81f-124">Affected APIs</span></span>

- <xref:System.Range?displayProperty=fullName>

<!--

### Affected APIs

- `T:System.Range`

### Category

Code analysis

-->
