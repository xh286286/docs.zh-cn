---
title: 中断性变更：Activity.Tags 中的标记顺序是相反的
description: 了解核心 .NET 库中的以下 .NET 5.0 中断性变更：Activity.Tags 现在根据项目的添加顺序将它们存储在列表中。
ms.date: 11/01/2020
ms.openlocfilehash: 1ff14dc1a4f7a0bf8cf9e79f3750b819f4d4a5ca
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759150"
---
# <a name="order-of-tags-in-activitytags-is-reversed"></a><span data-ttu-id="af568-103">Activity.Tags 中的标记顺序是相反的</span><span class="sxs-lookup"><span data-stu-id="af568-103">Order of tags in Activity.Tags is reversed</span></span>

<span data-ttu-id="af568-104"><xref:System.Diagnostics.Activity.Tags?displayProperty=nameWithType> 现根据项目的添加顺序将其存储在列表中，也就是说，添加的第一个项目排在列表第一位。</span><span class="sxs-lookup"><span data-stu-id="af568-104"><xref:System.Diagnostics.Activity.Tags?displayProperty=nameWithType> now stores items in the list according to the order they are added, that is, the first item that's added is first in the list.</span></span> <span data-ttu-id="af568-105">此更改是为了与 [OpenTelemetry 属性规范](https://github.com/open-telemetry/opentelemetry-specification/blob/master/specification/common/common.md#attributes)一致。</span><span class="sxs-lookup"><span data-stu-id="af568-105">This change was made to match the [OpenTelemetry Attributes specification](https://github.com/open-telemetry/opentelemetry-specification/blob/master/specification/common/common.md#attributes).</span></span>

## <a name="change-description"></a><span data-ttu-id="af568-106">更改描述</span><span class="sxs-lookup"><span data-stu-id="af568-106">Change description</span></span>

<span data-ttu-id="af568-107">在以前的 .NET 版本中，<xref:System.Diagnostics.Activity.Tags?displayProperty=nameWithType> 存储项目的顺序与项目的添加顺序相反。</span><span class="sxs-lookup"><span data-stu-id="af568-107">In previous .NET versions, <xref:System.Diagnostics.Activity.Tags?displayProperty=nameWithType> stores items in the reverse order from which they're added.</span></span> <span data-ttu-id="af568-108">也就是说，添加的第一个项目排在列表中的最后一位。</span><span class="sxs-lookup"><span data-stu-id="af568-108">That is, the first item added is last in the list.</span></span> <span data-ttu-id="af568-109">从 .NET 5.0 开始，项目的顺序是相反的，添加的第一项始终排在列表第一位。</span><span class="sxs-lookup"><span data-stu-id="af568-109">Starting in .NET 5.0, the order of the items is reversed, and the first item added is always first in the list.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="af568-110">引入的版本</span><span class="sxs-lookup"><span data-stu-id="af568-110">Version introduced</span></span>

<span data-ttu-id="af568-111">5.0</span><span class="sxs-lookup"><span data-stu-id="af568-111">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="af568-112">建议操作</span><span class="sxs-lookup"><span data-stu-id="af568-112">Recommended action</span></span>

<span data-ttu-id="af568-113">如果应用依赖于 <xref:System.Diagnostics.Activity.Tags?displayProperty=nameWithType> 列表顺序，并且要升级到 .NET 5.0 或更高版本，则需要你更改代码的此部分。</span><span class="sxs-lookup"><span data-stu-id="af568-113">If your app has a dependency on the <xref:System.Diagnostics.Activity.Tags?displayProperty=nameWithType> list order and you're upgrading to .NET 5.0 or later, you'll need to change this part of your code.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="af568-114">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="af568-114">Affected APIs</span></span>

- <xref:System.Diagnostics.Activity.Tags?displayProperty=fullName>

<!--

#### Category

Core .NET libraries

### Affected APIs

- `P:System.Diagnostics.Activity.Tags`

-->
