---
title: 中断性变更：Blazor：JSObjectReference 和 JSInProcessObjectReference 类型已更改为 internal
description: 了解 ASP.NET Core 5.0 中的以下中断性变更：Blazor：JSObjectReference 和 JSInProcessObjectReference 类型已更改为 internal
author: scottaddie
ms.author: scaddie
ms.date: 10/01/2020
ms.openlocfilehash: 43a66d204f8309dc5afc57d099b2201c477cc3ad
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759143"
---
# <a name="blazor-jsobjectreference-and-jsinprocessobjectreference-types-changed-to-internal"></a><span data-ttu-id="1ed55-103">Blazor：JSObjectReference 和 JSInProcessObjectReference 类型已更改为 internal</span><span class="sxs-lookup"><span data-stu-id="1ed55-103">Blazor: JSObjectReference and JSInProcessObjectReference types changed to internal</span></span>

<span data-ttu-id="1ed55-104">ASP.NET Core 5.0 RC1 中引入的新的 `Microsoft.JSInterop.JSObjectReference` 和 `Microsoft.JSInterop.JSInProcessObjectReference` 类型已被标记为 `internal`。</span><span class="sxs-lookup"><span data-stu-id="1ed55-104">The new `Microsoft.JSInterop.JSObjectReference` and `Microsoft.JSInterop.JSInProcessObjectReference` types introduced in ASP.NET Core 5.0 RC1 have been marked as `internal`.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="1ed55-105">引入的版本</span><span class="sxs-lookup"><span data-stu-id="1ed55-105">Version introduced</span></span>

<span data-ttu-id="1ed55-106">5.0 RC2</span><span class="sxs-lookup"><span data-stu-id="1ed55-106">5.0 RC2</span></span>

## <a name="old-behavior"></a><span data-ttu-id="1ed55-107">旧行为</span><span class="sxs-lookup"><span data-stu-id="1ed55-107">Old behavior</span></span>

<span data-ttu-id="1ed55-108">可以通过 `IJSRuntime` 从 JavaScript 互操作调用中获取 `JSObjectReference`。</span><span class="sxs-lookup"><span data-stu-id="1ed55-108">A `JSObjectReference` can be obtained from a JavaScript interop call via `IJSRuntime`.</span></span> <span data-ttu-id="1ed55-109">例如：</span><span class="sxs-lookup"><span data-stu-id="1ed55-109">For example:</span></span>

```csharp
var jsObjectReference = await JSRuntime.InvokeAsync<JSObjectReference>(...);
```

## <a name="new-behavior"></a><span data-ttu-id="1ed55-110">新行为</span><span class="sxs-lookup"><span data-stu-id="1ed55-110">New behavior</span></span>

<span data-ttu-id="1ed55-111">`JSObjectReference` 使用 [internal](../../../../csharp/language-reference/keywords/internal.md) 访问修饰符。</span><span class="sxs-lookup"><span data-stu-id="1ed55-111">`JSObjectReference` uses the [internal](../../../../csharp/language-reference/keywords/internal.md) access modifier.</span></span> <span data-ttu-id="1ed55-112">必须改为使用 `public` `IJSObjectReference` 接口。</span><span class="sxs-lookup"><span data-stu-id="1ed55-112">The `public` `IJSObjectReference` interface must be used instead.</span></span> <span data-ttu-id="1ed55-113">例如：</span><span class="sxs-lookup"><span data-stu-id="1ed55-113">For example:</span></span>

```csharp
var jsObjectReference = await JSRuntime.InvokeAsync<IJSObjectReference>(...);
```

<span data-ttu-id="1ed55-114">`JSInProcessObjectReference` 也被标记为 `internal` 并由 `IJSInProcessObjectReference` 替换。</span><span class="sxs-lookup"><span data-stu-id="1ed55-114">`JSInProcessObjectReference` was also marked as `internal` and was replaced by `IJSInProcessObjectReference`.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="1ed55-115">更改原因</span><span class="sxs-lookup"><span data-stu-id="1ed55-115">Reason for change</span></span>

<span data-ttu-id="1ed55-116">此更改使 JavaScript 互操作功能与 Blazor 中的其他模式更加一致。</span><span class="sxs-lookup"><span data-stu-id="1ed55-116">The change makes the JavaScript interop feature more consistent with other patterns within Blazor.</span></span> <span data-ttu-id="1ed55-117">`IJSObjectReference` 类似于 `IJSRuntime`，因为它有类似的目的，并且有类似的方法和扩展。</span><span class="sxs-lookup"><span data-stu-id="1ed55-117">`IJSObjectReference` is analogous to `IJSRuntime` in that it serves a similar purpose and has similar methods and extensions.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="1ed55-118">建议操作</span><span class="sxs-lookup"><span data-stu-id="1ed55-118">Recommended action</span></span>

<span data-ttu-id="1ed55-119">分别用 `IJSObjectReference` 和 `IJSInProcessObjectReference` 替换出现的 `JSObjectReference` 和 `JSInProcessObjectReference`。</span><span class="sxs-lookup"><span data-stu-id="1ed55-119">Replace occurrences of `JSObjectReference` and `JSInProcessObjectReference` with `IJSObjectReference` and `IJSInProcessObjectReference`, respectively.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="1ed55-120">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="1ed55-120">Affected APIs</span></span>

- `Microsoft.JSInterop.JSObjectReference`
- `Microsoft.JSInterop.JSInProcessObjectReference`

<!--

### Category

ASP.NET Core

### Affected APIs

- `T:Microsoft.JSInterop.JSObjectReference`
- `T:Microsoft.JSInterop.JSInProcessObjectReference`

-->
