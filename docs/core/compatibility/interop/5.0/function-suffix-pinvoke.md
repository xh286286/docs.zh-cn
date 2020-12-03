---
title: 中断性变更：不在非 Windows 平台上探测 A/W 后缀
description: 了解 .NET 5.0 中的以下互操作中断性变更：在非 Windows 平台上探测 P/Invoke 期间，不再将后缀添加到函数导出名称。
ms.date: 08/13/2020
ms.openlocfilehash: a4c612a81796faf80fa257df21232a54f7b95431
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759177"
---
# <a name="no-aw-suffix-probing-on-non-windows-platforms"></a><span data-ttu-id="9a067-103">不在非 Windows 平台上探测 A/W 后缀</span><span class="sxs-lookup"><span data-stu-id="9a067-103">No A/W suffix probing on non-Windows platforms</span></span>

<span data-ttu-id="9a067-104">在非 Windows 平台上探测 P/Invoke 期间，.NET 运行时不再向函数导出名称添加 `A` 或 `W` 后缀。</span><span class="sxs-lookup"><span data-stu-id="9a067-104">The .NET runtimes no longer add an `A` or `W` suffix to function export names during probing for P/Invokes on non-Windows platforms.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="9a067-105">引入的版本</span><span class="sxs-lookup"><span data-stu-id="9a067-105">Version introduced</span></span>

<span data-ttu-id="9a067-106">5.0</span><span class="sxs-lookup"><span data-stu-id="9a067-106">5.0</span></span>

## <a name="change-description"></a><span data-ttu-id="9a067-107">更改描述</span><span class="sxs-lookup"><span data-stu-id="9a067-107">Change description</span></span>

<span data-ttu-id="9a067-108">[Windows 有一项约定](/windows/win32/intl/conventions-for-function-prototypes)，即要求向 Windows SDK 函数名称添加 `A` 或 `W` 后缀，这分别与 Windows 代码页面和 Unicode 版本相对应。</span><span class="sxs-lookup"><span data-stu-id="9a067-108">[Windows has a convention](/windows/win32/intl/conventions-for-function-prototypes) of adding an `A` or `W` suffix to Windows SDK function names, which correspond to the Windows code page and Unicode versions, respectively.</span></span>

<span data-ttu-id="9a067-109">对于之前版本的 .NET，在导出对 P/Invoke 的发现结果的过程中，CoreCLR 和 Mono 运行时在所有平台上都会向导出名称添加 `A` 或 `W` 后缀。</span><span class="sxs-lookup"><span data-stu-id="9a067-109">In previous versions of .NET, both the CoreCLR and Mono runtimes add an `A` or `W` suffix to the export name during export discovery for P/Invokes *on all platforms*.</span></span>

<span data-ttu-id="9a067-110">而对于 .NET 5.0 及更高版本，在导出发现结果的过程中，仅在 Windows 上向导出名称添加 `A` 或 `W` 后缀。</span><span class="sxs-lookup"><span data-stu-id="9a067-110">In .NET 5.0 and later versions, an `A` or `W` suffix is added to the export name during export discovery *on Windows only*.</span></span> <span data-ttu-id="9a067-111">在 Unix 平台上，不会添加后缀。</span><span class="sxs-lookup"><span data-stu-id="9a067-111">On Unix platforms, the suffix is not added.</span></span> <span data-ttu-id="9a067-112">在 Windows 平台上，这两种运行时的语义保持不变。</span><span class="sxs-lookup"><span data-stu-id="9a067-112">The semantics of both runtimes on the Windows platform remain unchanged.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="9a067-113">更改原因</span><span class="sxs-lookup"><span data-stu-id="9a067-113">Reason for change</span></span>

<span data-ttu-id="9a067-114">此项更改旨在简化跨平台探测。</span><span class="sxs-lookup"><span data-stu-id="9a067-114">This change was made to simplify cross-platform probing.</span></span> <span data-ttu-id="9a067-115">如果非 Windows 平台不包含此语义，则不得产生此项开销。</span><span class="sxs-lookup"><span data-stu-id="9a067-115">It's overhead that shouldn't be incurred, given that non-Windows platforms don't contain this semantic.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="9a067-116">建议操作</span><span class="sxs-lookup"><span data-stu-id="9a067-116">Recommended action</span></span>

<span data-ttu-id="9a067-117">若要缓解此更改的影响，可在非 Windows 平台上手动添加所需的后缀。</span><span class="sxs-lookup"><span data-stu-id="9a067-117">To mitigate the change, you can manually add the desired suffix on non-Windows platforms.</span></span> <span data-ttu-id="9a067-118">例如：</span><span class="sxs-lookup"><span data-stu-id="9a067-118">For example:</span></span>

```csharp
[DllImport(...)]
extern static void SetWindowTextW();
```

## <a name="affected-apis"></a><span data-ttu-id="9a067-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="9a067-119">Affected APIs</span></span>

- <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>

<!--

### Affected APIs

- `T:System.Runtime.InteropServices.DllImportAttribute`

### Category

Interop

-->
