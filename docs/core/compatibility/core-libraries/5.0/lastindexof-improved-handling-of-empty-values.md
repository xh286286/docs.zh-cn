---
title: 中断性变更：LastIndexOf 改进了对空搜索字符串的处理
description: 了解核心 .NET 库中的以下 .NET 5.0 中断性变更：在搜索零长度子字符串时，LastIndexOf 和相关 API 现在返回正确的值。
ms.date: 11/01/2020
ms.openlocfilehash: 6d1a676eb2b9ed3de6a745db27d53bd43560a32f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759091"
---
# <a name="lastindexof-has-improved-handling-of-empty-search-strings"></a><span data-ttu-id="00d66-103">LastIndexOf 改进了对空搜索字符串的处理</span><span class="sxs-lookup"><span data-stu-id="00d66-103">LastIndexOf has improved handling of empty search strings</span></span>

<span data-ttu-id="00d66-104">在较大字符串中搜索零长度（或零长度等效项）子字符串时，<xref:System.String.LastIndexOf%2A?displayProperty=nameWithType> 和相关 API 现在返回正确的值。</span><span class="sxs-lookup"><span data-stu-id="00d66-104"><xref:System.String.LastIndexOf%2A?displayProperty=nameWithType> and related APIs now return correct values when searching for a zero-length (or zero-length equivalent) substring within a larger string.</span></span>

## <a name="change-description"></a><span data-ttu-id="00d66-105">更改描述</span><span class="sxs-lookup"><span data-stu-id="00d66-105">Change description</span></span>

<span data-ttu-id="00d66-106">在 .NET Framework 和 .NET Core 1.0-3.1 中，当调用方搜索零长度子字符串时，<xref:System.String.LastIndexOf%2A?displayProperty=nameWithType> 和相关 API 可能会返回不正确的值。</span><span class="sxs-lookup"><span data-stu-id="00d66-106">In .NET Framework and .NET Core 1.0 - 3.1, <xref:System.String.LastIndexOf%2A?displayProperty=nameWithType> and related APIs might return an incorrect value when the caller searches for a zero-length substring.</span></span>

```csharp
Console.WriteLine("Hello".LastIndexOf("")); // prints '4' (incorrect)

ReadOnlySpan<char> span = "Hello";
Console.WriteLine(span.LastIndexOf("")); // prints '0' (incorrect)
```

<span data-ttu-id="00d66-107">从 .NET 5.0 开始，这些 API 将返回 `LastIndexOf` 的正确值。</span><span class="sxs-lookup"><span data-stu-id="00d66-107">Starting with .NET 5.0, these APIs return the correct value for `LastIndexOf`.</span></span>

```csharp
Console.WriteLine("Hello".LastIndexOf("")); // prints '5' (correct)

ReadOnlySpan<char> span = "Hello";
Console.WriteLine(span.LastIndexOf("")); // prints '5' (correct)
```

<span data-ttu-id="00d66-108">在这些示例中，`5` 为正确答案，因为 `"Hello".Substring(5)` 和 `"Hello".AsSpan().Slice(5)` 均生成一个空字符串，该字符串完全等同于所查找的空子字符串。</span><span class="sxs-lookup"><span data-stu-id="00d66-108">In these examples, `5` is the correct answer because `"Hello".Substring(5)` and `"Hello".AsSpan().Slice(5)` both produce an empty string, which is trivially equal to the empty substring that is sought.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="00d66-109">更改原因</span><span class="sxs-lookup"><span data-stu-id="00d66-109">Reason for change</span></span>

<span data-ttu-id="00d66-110">此更改是围绕 .NET 5 字符串处理的整体 bug 修复工作的一部分。</span><span class="sxs-lookup"><span data-stu-id="00d66-110">This change was part of an overall bug fixing effort around string handling for .NET 5.</span></span> <span data-ttu-id="00d66-111">它还有助于统一 Windows 和非 Windows 平台的行为。</span><span class="sxs-lookup"><span data-stu-id="00d66-111">It also helps unify our behavior between Windows and non-Windows platforms.</span></span> <span data-ttu-id="00d66-112">有关详细信息，请参阅 [dotnet/runtime#13383](https://github.com/dotnet/runtime/issues/13383) 和 [dotnet/runtime##13382](https://github.com/dotnet/runtime/issues/13382)。</span><span class="sxs-lookup"><span data-stu-id="00d66-112">For more information, see [dotnet/runtime#13383](https://github.com/dotnet/runtime/issues/13383) and [dotnet/runtime##13382](https://github.com/dotnet/runtime/issues/13382).</span></span>

## <a name="version-introduced"></a><span data-ttu-id="00d66-113">引入的版本</span><span class="sxs-lookup"><span data-stu-id="00d66-113">Version introduced</span></span>

<span data-ttu-id="00d66-114">5.0</span><span class="sxs-lookup"><span data-stu-id="00d66-114">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="00d66-115">建议操作</span><span class="sxs-lookup"><span data-stu-id="00d66-115">Recommended action</span></span>

<span data-ttu-id="00d66-116">你不必执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="00d66-116">You don't need to take any action.</span></span> <span data-ttu-id="00d66-117">.NET 5.0 运行时自动提供新行为。</span><span class="sxs-lookup"><span data-stu-id="00d66-117">The .NET 5.0 runtime provides the new behaviors automatically.</span></span>

<span data-ttu-id="00d66-118">没有用于还原旧行为的兼容性开关。</span><span class="sxs-lookup"><span data-stu-id="00d66-118">There is no compatibility switch to restore the old behavior.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="00d66-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="00d66-119">Affected APIs</span></span>

- <xref:System.String.LastIndexOf%2A?displayProperty=fullName>
- <xref:System.Globalization.CompareInfo.LastIndexOf%2A?displayProperty=fullName>
- <xref:System.MemoryExtensions.LastIndexOf%2A?displayProperty=fullName>

<!--

### Category

Core .NET libraries

### Affected APIs

- `Overload:System.String.LastIndexOf`
- `Overload:System.Globalization.CompareInfo.LastIndexOf`
- `Overload:System.MemoryExtensions.LastIndexOf`

-->
