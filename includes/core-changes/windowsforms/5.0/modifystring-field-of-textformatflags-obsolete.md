---
ms.openlocfilehash: 56127309c5f5993ffc2e2faedd1f481e8131e094
ms.sourcegitcommit: 48466b8fb7332ececff5dc388f19f6b3ff503dd4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/05/2020
ms.locfileid: "93400626"
---
### <a name="textformatflagsmodifystring-is-obsolete"></a><span data-ttu-id="8b34a-101">TextFormatFlags.ModifyString 已过时</span><span class="sxs-lookup"><span data-stu-id="8b34a-101">TextFormatFlags.ModifyString is obsolete</span></span>

<span data-ttu-id="8b34a-102"><xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> 字段已过时（警告），可能会在将来的 .NET 版本中删除。</span><span class="sxs-lookup"><span data-stu-id="8b34a-102">The <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> field is obsolete, as a warning, and may be removed in a future .NET version.</span></span>

#### <a name="change-description"></a><span data-ttu-id="8b34a-103">更改描述</span><span class="sxs-lookup"><span data-stu-id="8b34a-103">Change description</span></span>

<span data-ttu-id="8b34a-104">在以前的 .NET 版本中，<xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> 枚举字段未被标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="8b34a-104">In previous .NET versions, the <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> enumeration field is not marked obsolete.</span></span> <span data-ttu-id="8b34a-105">在 .NET 5.0 及更高版本中，它被标记为已过时（警告）。</span><span class="sxs-lookup"><span data-stu-id="8b34a-105">In .NET 5.0 and later versions, it is marked obsolete as a warning.</span></span> <span data-ttu-id="8b34a-106">此字段可能会在将来的 .NET 版本中删除。</span><span class="sxs-lookup"><span data-stu-id="8b34a-106">This field may be removed in a future .NET version.</span></span>

#### <a name="reason-for-change"></a><span data-ttu-id="8b34a-107">更改原因</span><span class="sxs-lookup"><span data-stu-id="8b34a-107">Reason for change</span></span>

<span data-ttu-id="8b34a-108">在某些情况下，将字符串传递到 <xref:System.Windows.Forms.TextRenderer.MeasureText%2A?displayProperty=nameWithType> 和 <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> 会更改字符串。</span><span class="sxs-lookup"><span data-stu-id="8b34a-108">Passing a string to <xref:System.Windows.Forms.TextRenderer.MeasureText%2A?displayProperty=nameWithType> with <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> alters the string in some situations.</span></span> <span data-ttu-id="8b34a-109">此行为会中断字符串不可变性承诺，并可能导致致命的 .NET 运行时状态损坏。</span><span class="sxs-lookup"><span data-stu-id="8b34a-109">This behavior breaks the string immutability promise and may lead to a fatal .NET runtime state corruption.</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="8b34a-110">引入的版本</span><span class="sxs-lookup"><span data-stu-id="8b34a-110">Version introduced</span></span>

<span data-ttu-id="8b34a-111">.NET 5.0 RC1</span><span class="sxs-lookup"><span data-stu-id="8b34a-111">.NET 5.0 RC1</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="8b34a-112">建议操作</span><span class="sxs-lookup"><span data-stu-id="8b34a-112">Recommended action</span></span>

<span data-ttu-id="8b34a-113">更新依赖于 <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType> 的任何代码。</span><span class="sxs-lookup"><span data-stu-id="8b34a-113">Update any code that relies on <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=nameWithType>.</span></span>

#### <a name="category"></a><span data-ttu-id="8b34a-114">类别</span><span class="sxs-lookup"><span data-stu-id="8b34a-114">Category</span></span>

<span data-ttu-id="8b34a-115">Windows 窗体</span><span class="sxs-lookup"><span data-stu-id="8b34a-115">Windows Forms</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="8b34a-116">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="8b34a-116">Affected APIs</span></span>

- <xref:System.Windows.Forms.TextFormatFlags.ModifyString?displayProperty=fullName>

<!--

#### Affected APIs

- `F:System.Windows.Forms.TextFormatFlags.ModifyString`

-->
