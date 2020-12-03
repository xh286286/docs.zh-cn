---
title: 中断性变更：WinForms 属性现在引发 ArgumentOutOfRangeException
description: 了解 .NET 5.0 中的以下中断性变更：某些 Windows 窗体属性现在将针对无效参数引发 ArgumentOutOfRangeException。
ms.date: 06/18/2020
ms.openlocfilehash: 94593047d16304ce401b23993ad4ca173c10812b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759243"
---
# <a name="winforms-properties-now-throw-argumentoutofrangeexception"></a><span data-ttu-id="2ef91-103">WinForms 属性现在引发 ArgumentOutOfRangeException</span><span class="sxs-lookup"><span data-stu-id="2ef91-103">WinForms properties now throw ArgumentOutOfRangeException</span></span>

<span data-ttu-id="2ef91-104">某些 Windows 窗体属性现在将针对无效参数引发 <xref:System.ArgumentOutOfRangeException>，之前不会这样。</span><span class="sxs-lookup"><span data-stu-id="2ef91-104">Some Windows Forms properties now throw an <xref:System.ArgumentOutOfRangeException> for invalid arguments, where previously they did not.</span></span>

## <a name="change-description"></a><span data-ttu-id="2ef91-105">更改描述</span><span class="sxs-lookup"><span data-stu-id="2ef91-105">Change description</span></span>

<span data-ttu-id="2ef91-106">以前，当传递超出范围的参数时，这些属性将引发各种异常，如 <xref:System.NullReferenceException>、<xref:System.IndexOutOfRangeException> 或 <xref:System.ArgumentException>。</span><span class="sxs-lookup"><span data-stu-id="2ef91-106">Previously, these properties threw various exceptions, such as <xref:System.NullReferenceException>, <xref:System.IndexOutOfRangeException>, or <xref:System.ArgumentException>, when passed out-of-range arguments.</span></span> <span data-ttu-id="2ef91-107">从 .NET 5.0 开始，如果传递的参数超出范围，则这些属性现在将引发 <xref:System.ArgumentOutOfRangeException>。</span><span class="sxs-lookup"><span data-stu-id="2ef91-107">Starting in .NET 5.0, these properties now throw an <xref:System.ArgumentOutOfRangeException> when passed arguments that are out of range.</span></span>

<span data-ttu-id="2ef91-108">引发 <xref:System.ArgumentOutOfRangeException> 符合 .NET 运行时的行为。</span><span class="sxs-lookup"><span data-stu-id="2ef91-108">Throwing an <xref:System.ArgumentOutOfRangeException> conforms to the behavior of the .NET runtime.</span></span> <span data-ttu-id="2ef91-109">它还通过清楚地指示具体的无效参数来改进调试体验。</span><span class="sxs-lookup"><span data-stu-id="2ef91-109">It also improves the debugging experience by clearly communicating which argument is invalid.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="2ef91-110">引入的版本</span><span class="sxs-lookup"><span data-stu-id="2ef91-110">Version introduced</span></span>

<span data-ttu-id="2ef91-111">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="2ef91-111">.NET 5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="2ef91-112">建议操作</span><span class="sxs-lookup"><span data-stu-id="2ef91-112">Recommended action</span></span>

- <span data-ttu-id="2ef91-113">更新代码以防止传递无效参数。</span><span class="sxs-lookup"><span data-stu-id="2ef91-113">Update the code to prevent passing invalid arguments.</span></span>
- <span data-ttu-id="2ef91-114">如有必要，请在设置属性时处理 <xref:System.ArgumentOutOfRangeException>。</span><span class="sxs-lookup"><span data-stu-id="2ef91-114">If necessary, handle an <xref:System.ArgumentOutOfRangeException> when setting the property.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="2ef91-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="2ef91-115">Affected APIs</span></span>

<span data-ttu-id="2ef91-116">下表列出了受影响的方法和参数：</span><span class="sxs-lookup"><span data-stu-id="2ef91-116">The following table lists the affected properties and parameters:</span></span>

> [!div class="mx-tdBreakAll"]
> | <span data-ttu-id="2ef91-117">Property</span><span class="sxs-lookup"><span data-stu-id="2ef91-117">Property</span></span> | <span data-ttu-id="2ef91-118">参数名称</span><span class="sxs-lookup"><span data-stu-id="2ef91-118">Parameter name</span></span> | <span data-ttu-id="2ef91-119">新增的版本</span><span class="sxs-lookup"><span data-stu-id="2ef91-119">Version added</span></span> |
> |-|-|-|
> | <xref:System.Windows.Forms.ListBox.IntegerCollection.Item(System.Int32)?displayProperty=nameWithType> | `index` | <span data-ttu-id="2ef91-120">5.0 预览版 5</span><span class="sxs-lookup"><span data-stu-id="2ef91-120">5.0 Preview 5</span></span> |
> | <xref:System.Windows.Forms.TreeNode.ImageIndex?displayProperty=nameWithType> | `value` | <span data-ttu-id="2ef91-121">5.0 预览版 6</span><span class="sxs-lookup"><span data-stu-id="2ef91-121">5.0 Preview 6</span></span> |
> | <xref:System.Windows.Forms.TreeNode.SelectedImageIndex?displayProperty=nameWithType> | `value` | <span data-ttu-id="2ef91-122">5.0 预览版 6</span><span class="sxs-lookup"><span data-stu-id="2ef91-122">5.0 Preview 6</span></span> |

<!--

### Affected APIs

- `P:System.Windows.Forms.ListBox.IntegerCollection.Item(System.Int32)`
- `P:System.Windows.Forms.TreeNode.ImageIndex`
- `P:System.Windows.Forms.TreeNode.SelectedImageIndex`

### Category

Windows Forms

-->
