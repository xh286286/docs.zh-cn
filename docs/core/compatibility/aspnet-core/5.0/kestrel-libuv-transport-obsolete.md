---
title: 中断性变更：Kestrel：Libuv 传输标记为已过时
description: 了解 ASP.NET Core 5.0 中的以下中断性变更：Kestrel：Libuv 传输标记为已过时
author: scottaddie
ms.author: scaddie
ms.date: 10/01/2020
ms.openlocfilehash: f66b9b646671e07957e6d30a95333d392eb29617
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759162"
---
# <a name="kestrel-libuv-transport-marked-as-obsolete"></a><span data-ttu-id="f3109-103">Kestrel：Libuv 传输标记为已过时</span><span class="sxs-lookup"><span data-stu-id="f3109-103">Kestrel: Libuv transport marked as obsolete</span></span>

<span data-ttu-id="f3109-104">早期版本的 ASP.NET Core 使用 Libuv 作为执行异步输入和输出的方法的实现细节。</span><span class="sxs-lookup"><span data-stu-id="f3109-104">Earlier versions of ASP.NET Core used Libuv as an implementation detail of how asynchronous input and output was performed.</span></span> <span data-ttu-id="f3109-105">在 ASP.NET Core 2.0 中，我们开发了一种替代方案：基于 <xref:System.Net.Sockets.Socket> 的传输。</span><span class="sxs-lookup"><span data-stu-id="f3109-105">In ASP.NET Core 2.0, an alternative, <xref:System.Net.Sockets.Socket>-based transport was developed.</span></span> <span data-ttu-id="f3109-106">在 ASP.NET Core 2.1 中，默认情况下，Kestrel 切换为使用基于 `Socket` 的传输。</span><span class="sxs-lookup"><span data-stu-id="f3109-106">In ASP.NET Core 2.1, Kestrel switched to using the `Socket`-based transport by default.</span></span> <span data-ttu-id="f3109-107">出于兼容性原因，保留了 Libuv 支持。</span><span class="sxs-lookup"><span data-stu-id="f3109-107">Libuv support was maintained for compatibility reasons.</span></span>

<span data-ttu-id="f3109-108">目前人们普遍使用基于 `Socket` 的传输，而不使用 Libuv 传输。</span><span class="sxs-lookup"><span data-stu-id="f3109-108">At this point, use of the `Socket`-based transport is far more common than the Libuv transport.</span></span> <span data-ttu-id="f3109-109">因此，Libuv 支持在 .NET 5.0 中标记为已过时，并将完全从 .NET 6.0 中删除。</span><span class="sxs-lookup"><span data-stu-id="f3109-109">Consequently, Libuv support is marked as obsolete in .NET 5.0 and will be removed entirely in .NET 6.0.</span></span>

<span data-ttu-id="f3109-110">作为此更改的一部分，.NET 5.0 时间范围内不会添加对新操作系统平台（例如 Windows ARM64）的 Libuv 支持。</span><span class="sxs-lookup"><span data-stu-id="f3109-110">As part of this change, Libuv support for new operating system platforms (like Windows ARM64) won't be added in the .NET 5.0 timeframe.</span></span>

<span data-ttu-id="f3109-111">有关阻止需要使用 Libuv 传输的问题的讨论，请参阅 GitHub 问题，网址为：[dotnet/aspnetcore#23409](https://github.com/dotnet/aspnetcore/issues/23409)。</span><span class="sxs-lookup"><span data-stu-id="f3109-111">For discussion on blocking issues that require the use of the Libuv transport, see the GitHub issue at [dotnet/aspnetcore#23409](https://github.com/dotnet/aspnetcore/issues/23409).</span></span>

## <a name="version-introduced"></a><span data-ttu-id="f3109-112">引入的版本</span><span class="sxs-lookup"><span data-stu-id="f3109-112">Version introduced</span></span>

<span data-ttu-id="f3109-113">5.0 预览版 8</span><span class="sxs-lookup"><span data-stu-id="f3109-113">5.0 Preview 8</span></span>

## <a name="old-behavior"></a><span data-ttu-id="f3109-114">旧行为</span><span class="sxs-lookup"><span data-stu-id="f3109-114">Old behavior</span></span>

<span data-ttu-id="f3109-115">Libuv API 未标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="f3109-115">The Libuv APIs aren't marked as obsolete.</span></span>

## <a name="new-behavior"></a><span data-ttu-id="f3109-116">新行为</span><span class="sxs-lookup"><span data-stu-id="f3109-116">New behavior</span></span>

<span data-ttu-id="f3109-117">Libuv API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="f3109-117">The Libuv APIs are marked as obsolete.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="f3109-118">更改原因</span><span class="sxs-lookup"><span data-stu-id="f3109-118">Reason for change</span></span>

<span data-ttu-id="f3109-119">基于 `Socket` 的传输是默认设置。</span><span class="sxs-lookup"><span data-stu-id="f3109-119">The `Socket`-based transport is the default.</span></span> <span data-ttu-id="f3109-120">不必继续使用 Libuv 传输。</span><span class="sxs-lookup"><span data-stu-id="f3109-120">There aren't any compelling reasons to continue using the Libuv transport.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="f3109-121">建议操作</span><span class="sxs-lookup"><span data-stu-id="f3109-121">Recommended action</span></span>

<span data-ttu-id="f3109-122">停止使用 [Libuv 包](https://www.nuget.org/packages/Libuv) 和扩展方法。</span><span class="sxs-lookup"><span data-stu-id="f3109-122">Discontinue use of the [Libuv package](https://www.nuget.org/packages/Libuv) and extension methods.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="f3109-123">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="f3109-123">Affected APIs</span></span>

- [<span data-ttu-id="f3109-124">WebHostBuilderLibuvExtensions</span><span class="sxs-lookup"><span data-stu-id="f3109-124">WebHostBuilderLibuvExtensions</span></span>](/dotnet/api/microsoft.aspnetcore.hosting.webhostbuilderlibuvextensions?view=aspnetcore-3.0)
- [<span data-ttu-id="f3109-125">WebHostBuilderLibuvExtensions.UseLibuv</span><span class="sxs-lookup"><span data-stu-id="f3109-125">WebHostBuilderLibuvExtensions.UseLibuv</span></span>](/dotnet/api/microsoft.aspnetcore.hosting.webhostbuilderlibuvextensions.uselibuv?view=aspnetcore-3.0)
- [<span data-ttu-id="f3109-126">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions</span><span class="sxs-lookup"><span data-stu-id="f3109-126">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions</span></span>](/dotnet/api/microsoft.aspnetcore.server.kestrel.transport.libuv.libuvtransportoptions?view=aspnetcore-3.0)
- [<span data-ttu-id="f3109-127">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.ThreadCount</span><span class="sxs-lookup"><span data-stu-id="f3109-127">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.ThreadCount</span></span>](/dotnet/api/microsoft.aspnetcore.server.kestrel.transport.libuv.libuvtransportoptions.threadcount?view=aspnetcore-3.0)
- [<span data-ttu-id="f3109-128">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.NoDelay</span><span class="sxs-lookup"><span data-stu-id="f3109-128">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.NoDelay</span></span>](/dotnet/api/microsoft.aspnetcore.server.kestrel.transport.libuv.libuvtransportoptions.nodelay?view=aspnetcore-3.0)
- [<span data-ttu-id="f3109-129">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.MaxWriteBufferSize</span><span class="sxs-lookup"><span data-stu-id="f3109-129">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.MaxWriteBufferSize</span></span>](/dotnet/api/microsoft.aspnetcore.server.kestrel.transport.libuv.libuvtransportoptions.maxwritebuffersize?view=aspnetcore-3.0)
- [<span data-ttu-id="f3109-130">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.MaxReadBufferSize</span><span class="sxs-lookup"><span data-stu-id="f3109-130">Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.MaxReadBufferSize</span></span>](/dotnet/api/microsoft.aspnetcore.server.kestrel.transport.libuv.libuvtransportoptions.maxreadbuffersize?view=aspnetcore-3.0)
- `Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.Backlog`

<!--

### Category

ASP.NET Core

### Affected APIs

- `T:Microsoft.AspNetCore.Hosting.WebHostBuilderLibuvExtensions`
- `Overload:Microsoft.AspNetCore.Hosting.WebHostBuilderLibuvExtensions.UseLibuv`
- `T:Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions`
- `P:Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.ThreadCount`
- `P:Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.NoDelay`
- `P:Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.MaxWriteBufferSize`
- `P:Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.MaxReadBufferSize`
- `P:Microsoft.AspNetCore.Server.Kestrel.Transport.Libuv.LibuvTransportOptions.Backlog`

-->
