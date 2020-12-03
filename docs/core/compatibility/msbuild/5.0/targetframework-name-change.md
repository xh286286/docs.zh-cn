---
title: 中断性变更：TargetFramework 从 netcoreapp 更改为 net
description: 了解 .NET 5.0 中的以下中断性变更：MSBuild TargetFramework 属性的值已从 netcoreapp 3.1 更改为 net5.0。
ms.date: 10/17/2020
ms.openlocfilehash: c3b39a36548d58d6ed75fd8b1c84b0cccfc738f0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759127"
---
# <a name="targetframework-change-from-netcoreapp-to-net"></a><span data-ttu-id="ad12f-103">TargetFramework 从 netcoreapp 更改为 net</span><span class="sxs-lookup"><span data-stu-id="ad12f-103">TargetFramework change from netcoreapp to net</span></span>

<span data-ttu-id="ad12f-104">MSBuild `TargetFramework` 属性的值已从 `netcoreapp3.1` 更改为 `net5.0`。</span><span class="sxs-lookup"><span data-stu-id="ad12f-104">The value for the MSBuild `TargetFramework` property changed from `netcoreapp3.1` to `net5.0`.</span></span> <span data-ttu-id="ad12f-105">这可能会破坏依赖于分析 `TargetFramework` 的值的代码。</span><span class="sxs-lookup"><span data-stu-id="ad12f-105">This can break code that relies on parsing the value of `TargetFramework`.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="ad12f-106">引入的版本</span><span class="sxs-lookup"><span data-stu-id="ad12f-106">Version introduced</span></span>

<span data-ttu-id="ad12f-107">5.0</span><span class="sxs-lookup"><span data-stu-id="ad12f-107">5.0</span></span>

## <a name="change-description"></a><span data-ttu-id="ad12f-108">更改描述</span><span class="sxs-lookup"><span data-stu-id="ad12f-108">Change description</span></span>

<span data-ttu-id="ad12f-109">在 .NET Core 1.0 - 3.1 中，MSBuild `TargetFramework` 属性的值以 `netcoreapp` 开头（例如，对于面向 .NET Core 3.1 的应用，为 `netcoreapp3.1`）。</span><span class="sxs-lookup"><span data-stu-id="ad12f-109">In .NET Core 1.0 - 3.1, the value for the MSBuild `TargetFramework` property starts with `netcoreapp`, for example, `netcoreapp3.1` for apps that target .NET Core 3.1.</span></span> <span data-ttu-id="ad12f-110">从 .NET 5.0 开始，此值简化为仅以 `net` 开头（例如，对于 .NET 5.0，为 `net5.0`）。</span><span class="sxs-lookup"><span data-stu-id="ad12f-110">Starting in .NET 5.0, this value is simplified to just start with `net`, for example, `net5.0` for .NET 5.0.</span></span>

<span data-ttu-id="ad12f-111">有关详细信息，请参阅 [.NET Standard 的未来](https://devblogs.microsoft.com/dotnet/the-future-of-net-standard/)和 [.NET 5 中的目标框架名称](https://github.com/dotnet/designs/blob/main/accepted/2020/net5/net5.md)。</span><span class="sxs-lookup"><span data-stu-id="ad12f-111">For more information, see [The future of .NET Standard](https://devblogs.microsoft.com/dotnet/the-future-of-net-standard/) and [Target framework names in .NET 5](https://github.com/dotnet/designs/blob/main/accepted/2020/net5/net5.md).</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="ad12f-112">更改原因</span><span class="sxs-lookup"><span data-stu-id="ad12f-112">Reason for change</span></span>

- <span data-ttu-id="ad12f-113">简化 `TargetFramework` 值。</span><span class="sxs-lookup"><span data-stu-id="ad12f-113">Simplifies the `TargetFramework` value.</span></span>
- <span data-ttu-id="ad12f-114">使项目能够在 `TargetFramework` 属性中包含 `TargetPlatform`。</span><span class="sxs-lookup"><span data-stu-id="ad12f-114">Enables projects to include a `TargetPlatform` in the `TargetFramework` property.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="ad12f-115">建议的操作</span><span class="sxs-lookup"><span data-stu-id="ad12f-115">Recommended action</span></span>

<span data-ttu-id="ad12f-116">如果你有用于分析 `TargetFramework` 的值的逻辑，则需要对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="ad12f-116">If you have logic that parses the value of `TargetFramework`, you'll need to update it.</span></span> <span data-ttu-id="ad12f-117">例如，以下 MSBuild 条件依赖于 `TargetFramework` 的值。</span><span class="sxs-lookup"><span data-stu-id="ad12f-117">For example, the following MSBuild condition relies on the value of `TargetFramework`.</span></span>

```xml
<PropertyGroup Condition="$(TargetFramework.StartsWith('netcoreapp'))">
```

<span data-ttu-id="ad12f-118">为满足此要求，可更新代码，改为比较目标框架标识符。</span><span class="sxs-lookup"><span data-stu-id="ad12f-118">For this requirement, you can update the code to compare the target framework identifier instead.</span></span>

```xml
<PropertyGroup Condition="'$([MSBuild]::GetTargetFrameworkIdentifier('$(TargetFramework)'))' == '.NETCoreApp'">
```

## <a name="affected-apis"></a><span data-ttu-id="ad12f-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="ad12f-119">Affected APIs</span></span>

<span data-ttu-id="ad12f-120">不可用</span><span class="sxs-lookup"><span data-stu-id="ad12f-120">N/A</span></span>

<!--

### Affected APIs

Not detectable via API analysis.

### Category

MSBuild

-->
