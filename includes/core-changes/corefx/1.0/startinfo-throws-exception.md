---
ms.openlocfilehash: 92c03328414410d56a2ff5f445639757367b42c7
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031969"
---
### <a name="processstartinfo-throws-invalidoperationexception-for-processes-you-didnt-start"></a><span data-ttu-id="c88a6-101">Process.StartInfo 对未启动的进程引发 InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="c88a6-101">Process.StartInfo throws InvalidOperationException for processes you didn't start</span></span>

<span data-ttu-id="c88a6-102">对于你的代码未启动的进程，读取其 <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> 属性会引发 <xref:System.InvalidOperationException>。</span><span class="sxs-lookup"><span data-stu-id="c88a6-102">Reading the <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> property for processes that your code didn't start throws an <xref:System.InvalidOperationException>.</span></span>

#### <a name="change-description"></a><span data-ttu-id="c88a6-103">更改描述</span><span class="sxs-lookup"><span data-stu-id="c88a6-103">Change description</span></span>

<span data-ttu-id="c88a6-104">在 .NET Framework 中，访问你的代码未启动的进程的 <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> 属性将返回虚拟 <xref:System.Diagnostics.ProcessStartInfo> 对象。</span><span class="sxs-lookup"><span data-stu-id="c88a6-104">In .NET Framework, accessing the <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> property for processes that your code didn't start returns a dummy <xref:System.Diagnostics.ProcessStartInfo> object.</span></span> <span data-ttu-id="c88a6-105">虚拟对象包含其所有属性（<xref:System.Diagnostics.ProcessStartInfo.EnvironmentVariables> 除外）的默认值。</span><span class="sxs-lookup"><span data-stu-id="c88a6-105">The dummy object contains default values for all of its properties except <xref:System.Diagnostics.ProcessStartInfo.EnvironmentVariables>.</span></span>

<span data-ttu-id="c88a6-106">从 .NET Core 1.0 开始，如果读取你未启动的进程的 <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> 属性（即通过调用 <xref:System.Diagnostics.Process.Start%2A?displayProperty=nameWithType>），则会引发 <xref:System.InvalidOperationException>。</span><span class="sxs-lookup"><span data-stu-id="c88a6-106">Starting in .NET Core 1.0, if you read the <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> property for a process that you didn't start (that is, by calling <xref:System.Diagnostics.Process.Start%2A?displayProperty=nameWithType>), an <xref:System.InvalidOperationException> is thrown.</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="c88a6-107">引入的版本</span><span class="sxs-lookup"><span data-stu-id="c88a6-107">Version introduced</span></span>

<span data-ttu-id="c88a6-108">1.0</span><span class="sxs-lookup"><span data-stu-id="c88a6-108">1.0</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="c88a6-109">建议操作</span><span class="sxs-lookup"><span data-stu-id="c88a6-109">Recommended action</span></span>

<span data-ttu-id="c88a6-110">不要访问你的代码未启动的进程的 <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> 属性。</span><span class="sxs-lookup"><span data-stu-id="c88a6-110">Do not access the <xref:System.Diagnostics.Process.StartInfo?displayProperty=nameWithType> property for processes that your code didn't start.</span></span> <span data-ttu-id="c88a6-111">例如，不要读取 <xref:System.Diagnostics.Process.GetProcesses%2A?displayProperty=nameWithType> 返回的进程的此属性。</span><span class="sxs-lookup"><span data-stu-id="c88a6-111">For example, don't read this property for processes returned by <xref:System.Diagnostics.Process.GetProcesses%2A?displayProperty=nameWithType>.</span></span>

#### <a name="category"></a><span data-ttu-id="c88a6-112">类别</span><span class="sxs-lookup"><span data-stu-id="c88a6-112">Category</span></span>

<span data-ttu-id="c88a6-113">Core .NET 库</span><span class="sxs-lookup"><span data-stu-id="c88a6-113">Core .NET libraries</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="c88a6-114">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="c88a6-114">Affected APIs</span></span>

- <xref:System.Diagnostics.Process.StartInfo?displayProperty=fullName>

<!--

#### Affected APIs

- `P:System.Diagnostics.Process.StartInfo`

-->
