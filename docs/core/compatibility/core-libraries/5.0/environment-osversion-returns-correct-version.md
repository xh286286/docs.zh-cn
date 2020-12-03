---
title: 中断性变更：Environment.OSVersion 返回正确的操作系统版本
description: 了解核心 .NET 库中的以下 .NET 5.0 中断性变更：Environment.OSVersion 返回操作系统的实际版本而不是为应用程序兼容性选择的 OS。
ms.date: 11/01/2020
ms.openlocfilehash: b78ca1c7be50f76b99b5558a976d8f00e2f560c3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759310"
---
# <a name="environmentosversion-returns-the-correct-operating-system-version"></a><span data-ttu-id="5c128-103">Environment.OSVersion 返回正确的操作系统版本</span><span class="sxs-lookup"><span data-stu-id="5c128-103">Environment.OSVersion returns the correct operating system version</span></span>

<span data-ttu-id="5c128-104"><xref:System.Environment.OSVersion?displayProperty=nameWithType> 返回操作系统 (OS) 的实际版本，而不是为应用程序兼容性而选择的 OS。</span><span class="sxs-lookup"><span data-stu-id="5c128-104"><xref:System.Environment.OSVersion?displayProperty=nameWithType> returns the actual version of the operating system (OS) instead of, for example, the OS that's selected for application compatibility.</span></span>

## <a name="change-description"></a><span data-ttu-id="5c128-105">更改描述</span><span class="sxs-lookup"><span data-stu-id="5c128-105">Change description</span></span>

<span data-ttu-id="5c128-106">在以前的 .NET 版本中，当应用程序在 Windows 兼容模式下运行时，<xref:System.Environment.OSVersion?displayProperty=nameWithType> 返回的 OS 版本可能不正确。</span><span class="sxs-lookup"><span data-stu-id="5c128-106">In previous .NET versions, <xref:System.Environment.OSVersion?displayProperty=nameWithType> returns an OS version that may be incorrect when an application runs under Windows compatibility mode.</span></span> <span data-ttu-id="5c128-107">有关详细信息，请参阅 [GetVersionExA 函数备注](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa#remarks)。</span><span class="sxs-lookup"><span data-stu-id="5c128-107">For more information, see [GetVersionExA function remarks](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa#remarks).</span></span>

<span data-ttu-id="5c128-108">从 .NET 5.0 开始，<xref:System.Environment.OSVersion?displayProperty=nameWithType> 返回操作系统的实际版本。</span><span class="sxs-lookup"><span data-stu-id="5c128-108">Starting in .NET 5.0, <xref:System.Environment.OSVersion?displayProperty=nameWithType> returns the actual version of the operating system.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="5c128-109">更改原因</span><span class="sxs-lookup"><span data-stu-id="5c128-109">Reason for change</span></span>

<span data-ttu-id="5c128-110">此属性的用户希望它返回操作系统的实际版本。</span><span class="sxs-lookup"><span data-stu-id="5c128-110">Users of this property expect it to return the actual version of the operating system.</span></span> <span data-ttu-id="5c128-111">大多数 .NET 应用并未在其应用程序清单中指定其支持的版本，因此会从 dotnet 主机获取默认的支持版本。</span><span class="sxs-lookup"><span data-stu-id="5c128-111">Most .NET apps don't specify their supported version in their application manifest, and thus get the default supported version from the dotnet host.</span></span> <span data-ttu-id="5c128-112">因此，兼容性填充码对于正在运行的应用没有什么意义。</span><span class="sxs-lookup"><span data-stu-id="5c128-112">As a result, the compatibility shim is rarely meaningful for the app that's running.</span></span> <span data-ttu-id="5c128-113">当 Windows 发布新版本时，如果较旧的 dotnet 主机仍在使用，这些应用可能会收到错误的 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="5c128-113">When Windows releases a new version and an older dotnet host is still in use, these apps may get an incorrect OS version.</span></span> <span data-ttu-id="5c128-114">返回实际版本更符合开发人员对此 API 的期望。</span><span class="sxs-lookup"><span data-stu-id="5c128-114">Returning the actual version is more inline with developers' expectations of this API.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="5c128-115">引入的版本</span><span class="sxs-lookup"><span data-stu-id="5c128-115">Version introduced</span></span>

<span data-ttu-id="5c128-116">5.0</span><span class="sxs-lookup"><span data-stu-id="5c128-116">5.0</span></span>

## <a name="recommended-action"></a><span data-ttu-id="5c128-117">建议操作</span><span class="sxs-lookup"><span data-stu-id="5c128-117">Recommended action</span></span>

<span data-ttu-id="5c128-118">查看和测试使用 <xref:System.Environment.OSVersion?displayProperty=nameWithType> 的任何代码，以确保其行为符合预期。</span><span class="sxs-lookup"><span data-stu-id="5c128-118">Review and test any code that uses <xref:System.Environment.OSVersion?displayProperty=nameWithType> to ensure it behaves as desired.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="5c128-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="5c128-119">Affected APIs</span></span>

- <xref:System.Environment.OSVersion?displayProperty=fullName>

<!--

### Category

Core .NET libraries

### Affected APIs

- `P:System.Environment.OSVersion`

-->
