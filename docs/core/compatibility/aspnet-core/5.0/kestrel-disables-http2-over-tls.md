---
title: 中断性变更：Kestrel：在不兼容的 Windows 版本上通过 TLS 禁用 HTTP/2
description: 了解 ASP.NET Core 5.0 中的以下中断性变更：Kestrel：在不兼容的 Windows 版本上通过 TLS 禁用 HTTP/2
author: scottaddie
ms.author: scaddie
ms.date: 10/01/2020
ms.openlocfilehash: befd393795f3e1859d391bca513dd9856101d295
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759246"
---
# <a name="kestrel-http2-disabled-over-tls-on-incompatible-windows-versions"></a><span data-ttu-id="7b99f-103">Kestrel：在不兼容的 Windows 版本上通过 TLS 禁用 HTTP/2</span><span class="sxs-lookup"><span data-stu-id="7b99f-103">Kestrel: HTTP/2 disabled over TLS on incompatible Windows versions</span></span>

<span data-ttu-id="7b99f-104">要在 Windows 上启用基于传输层安全性 (TLS) 的 HTTP/2，需要满足以下两个要求：</span><span class="sxs-lookup"><span data-stu-id="7b99f-104">To enable HTTP/2 over Transport Layer Security (TLS) on Windows, two requirements need to be met:</span></span>

- <span data-ttu-id="7b99f-105">应用层协议协商 (ALPN) 支持，从 Windows 8.1 和 Windows Server 2012 R2 开始提供。</span><span class="sxs-lookup"><span data-stu-id="7b99f-105">Application-Layer Protocol Negotiation (ALPN) support, which is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>
- <span data-ttu-id="7b99f-106">与 HTTP/2 兼容的一组密码，从 Windows 10 和 Windows Server 2016 开始提供。</span><span class="sxs-lookup"><span data-stu-id="7b99f-106">A set of ciphers compatible with HTTP/2, which is available starting with Windows 10 and Windows Server 2016.</span></span>

<span data-ttu-id="7b99f-107">因此，配置基于 TLS 的 HTTP/2 时，Kestrel 的行为已更改为：</span><span class="sxs-lookup"><span data-stu-id="7b99f-107">As such, Kestrel's behavior when HTTP/2 over TLS is configured has changed to:</span></span>

- <span data-ttu-id="7b99f-108">当 [ListenOptions.HttpProtocols](/dotnet/api/microsoft.aspnetcore.server.kestrel.core.httpprotocols) 设置为 `Http1AndHttp2` 时，降级到 `Http1` 并记录 `Information` 级别的消息。</span><span class="sxs-lookup"><span data-stu-id="7b99f-108">Downgrade to `Http1` and log a message at the `Information` level when [ListenOptions.HttpProtocols](/dotnet/api/microsoft.aspnetcore.server.kestrel.core.httpprotocols) is set to `Http1AndHttp2`.</span></span> <span data-ttu-id="7b99f-109">`Http1AndHttp2` 是 `ListenOptions.HttpProtocols` 的默认值。</span><span class="sxs-lookup"><span data-stu-id="7b99f-109">`Http1AndHttp2` is the default value for `ListenOptions.HttpProtocols`.</span></span>
- <span data-ttu-id="7b99f-110">当 `ListenOptions.HttpProtocols` 设置为 `Http2` 时，引发 `NotSupportedException`。</span><span class="sxs-lookup"><span data-stu-id="7b99f-110">Throw a `NotSupportedException` when `ListenOptions.HttpProtocols` is set to `Http2`.</span></span>

<span data-ttu-id="7b99f-111">有关讨论，请参阅问题 [dotnet/aspnetcore#23068](https://github.com/dotnet/aspnetcore/issues/23068)。</span><span class="sxs-lookup"><span data-stu-id="7b99f-111">For discussion, see issue [dotnet/aspnetcore#23068](https://github.com/dotnet/aspnetcore/issues/23068).</span></span>

## <a name="version-introduced"></a><span data-ttu-id="7b99f-112">引入的版本</span><span class="sxs-lookup"><span data-stu-id="7b99f-112">Version introduced</span></span>

<span data-ttu-id="7b99f-113">ASP.NET Core 5.0 预览版 7</span><span class="sxs-lookup"><span data-stu-id="7b99f-113">ASP.NET Core 5.0 Preview 7</span></span>

## <a name="old-behavior"></a><span data-ttu-id="7b99f-114">旧行为</span><span class="sxs-lookup"><span data-stu-id="7b99f-114">Old behavior</span></span>

<span data-ttu-id="7b99f-115">下表概述了配置基于 TLS 的 HTTP/2 时的行为。</span><span class="sxs-lookup"><span data-stu-id="7b99f-115">The following table outlines the behavior when HTTP/2 over TLS is configured.</span></span>

| <span data-ttu-id="7b99f-116">协议</span><span class="sxs-lookup"><span data-stu-id="7b99f-116">Protocols</span></span> | <span data-ttu-id="7b99f-117">Windows 7、</span><span class="sxs-lookup"><span data-stu-id="7b99f-117">Windows 7,</span></span><br /><span data-ttu-id="7b99f-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b99f-118">Windows Server 2008 R2,</span></span><br /><span data-ttu-id="7b99f-119">或更早版本</span><span class="sxs-lookup"><span data-stu-id="7b99f-119">or earlier</span></span> | <span data-ttu-id="7b99f-120">Windows 8、</span><span class="sxs-lookup"><span data-stu-id="7b99f-120">Windows 8,</span></span><br /><span data-ttu-id="7b99f-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b99f-121">Windows Server 2012</span></span> | <span data-ttu-id="7b99f-122">Windows 8.1、</span><span class="sxs-lookup"><span data-stu-id="7b99f-122">Windows 8.1,</span></span><br /><span data-ttu-id="7b99f-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7b99f-123">Windows Server 2012 R2</span></span> | <span data-ttu-id="7b99f-124">Windows 10、</span><span class="sxs-lookup"><span data-stu-id="7b99f-124">Windows 10,</span></span><br /><span data-ttu-id="7b99f-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b99f-125">Windows Server 2016,</span></span><br /><span data-ttu-id="7b99f-126">或更高版本</span><span class="sxs-lookup"><span data-stu-id="7b99f-126">or newer</span></span> |
|---------------|-----------------------------------------------|--------------------------------|-------------------------------------|------------------------------------------|
| `Http2`         | <span data-ttu-id="7b99f-127">引发 `NotSupportedException`</span><span class="sxs-lookup"><span data-stu-id="7b99f-127">Throw `NotSupportedException`</span></span>                   | <span data-ttu-id="7b99f-128">TLS 握手期间出错</span><span class="sxs-lookup"><span data-stu-id="7b99f-128">Error during TLS handshake</span></span>     | <span data-ttu-id="7b99f-129">TLS 握手期间出错 &ast;</span><span class="sxs-lookup"><span data-stu-id="7b99f-129">Error during TLS handshake &ast;</span></span>     | <span data-ttu-id="7b99f-130">无错误</span><span class="sxs-lookup"><span data-stu-id="7b99f-130">No error</span></span> |
| `Http1AndHttp2` | <span data-ttu-id="7b99f-131">降级到 `Http1`</span><span class="sxs-lookup"><span data-stu-id="7b99f-131">Downgrade to `Http1`</span></span>                    | <span data-ttu-id="7b99f-132">降级到 `Http1`</span><span class="sxs-lookup"><span data-stu-id="7b99f-132">Downgrade to `Http1`</span></span>     | <span data-ttu-id="7b99f-133">TLS 握手期间出错 &ast;</span><span class="sxs-lookup"><span data-stu-id="7b99f-133">Error during TLS handshake &ast;</span></span>     | <span data-ttu-id="7b99f-134">无错误</span><span class="sxs-lookup"><span data-stu-id="7b99f-134">No error</span></span> |

<span data-ttu-id="7b99f-135">&ast; 配置兼容密码套件以支持这些方案。</span><span class="sxs-lookup"><span data-stu-id="7b99f-135">&ast; Configure compatible cipher suites to enable these scenarios.</span></span>

## <a name="new-behavior"></a><span data-ttu-id="7b99f-136">新行为</span><span class="sxs-lookup"><span data-stu-id="7b99f-136">New behavior</span></span>

<span data-ttu-id="7b99f-137">下表概述了配置基于 TLS 的 HTTP/2 时的行为。</span><span class="sxs-lookup"><span data-stu-id="7b99f-137">The following table outlines the behavior when HTTP/2 over TLS is configured.</span></span>

| <span data-ttu-id="7b99f-138">协议</span><span class="sxs-lookup"><span data-stu-id="7b99f-138">Protocols</span></span> | <span data-ttu-id="7b99f-139">Windows 7、</span><span class="sxs-lookup"><span data-stu-id="7b99f-139">Windows 7,</span></span><br /><span data-ttu-id="7b99f-140">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b99f-140">Windows Server 2008 R2,</span></span><br /><span data-ttu-id="7b99f-141">或更早版本</span><span class="sxs-lookup"><span data-stu-id="7b99f-141">or earlier</span></span> | <span data-ttu-id="7b99f-142">Windows 8、</span><span class="sxs-lookup"><span data-stu-id="7b99f-142">Windows 8,</span></span><br /><span data-ttu-id="7b99f-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b99f-143">Windows Server 2012</span></span> | <span data-ttu-id="7b99f-144">Windows 8.1、</span><span class="sxs-lookup"><span data-stu-id="7b99f-144">Windows 8.1,</span></span><br /><span data-ttu-id="7b99f-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7b99f-145">Windows Server 2012 R2</span></span> | <span data-ttu-id="7b99f-146">Windows 10、</span><span class="sxs-lookup"><span data-stu-id="7b99f-146">Windows 10,</span></span><br /><span data-ttu-id="7b99f-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b99f-147">Windows Server 2016,</span></span><br /><span data-ttu-id="7b99f-148">或更高版本</span><span class="sxs-lookup"><span data-stu-id="7b99f-148">or newer</span></span> |
|---------------|-----------------------------------------------|--------------------------------|-------------------------------------|------------------------------------------|
| `Http2`         | <span data-ttu-id="7b99f-149">引发 `NotSupportedException`</span><span class="sxs-lookup"><span data-stu-id="7b99f-149">Throw `NotSupportedException`</span></span>                   | <span data-ttu-id="7b99f-150">引发 `NotSupportedException`</span><span class="sxs-lookup"><span data-stu-id="7b99f-150">Throw `NotSupportedException`</span></span>     | <span data-ttu-id="7b99f-151">引发 `NotSupportedException` &ast;&ast;</span><span class="sxs-lookup"><span data-stu-id="7b99f-151">Throw `NotSupportedException` &ast;&ast;</span></span>     | <span data-ttu-id="7b99f-152">无错误</span><span class="sxs-lookup"><span data-stu-id="7b99f-152">No error</span></span> |
| `Http1AndHttp2` | <span data-ttu-id="7b99f-153">降级到 `Http1`</span><span class="sxs-lookup"><span data-stu-id="7b99f-153">Downgrade to `Http1`</span></span>                    | <span data-ttu-id="7b99f-154">降级到 `Http1`</span><span class="sxs-lookup"><span data-stu-id="7b99f-154">Downgrade to `Http1`</span></span>     | <span data-ttu-id="7b99f-155">降级到 `Http1` &ast;&ast;</span><span class="sxs-lookup"><span data-stu-id="7b99f-155">Downgrade to `Http1` &ast;&ast;</span></span>     | <span data-ttu-id="7b99f-156">无错误</span><span class="sxs-lookup"><span data-stu-id="7b99f-156">No error</span></span> |

<span data-ttu-id="7b99f-157">&ast;&ast; 配置兼容的密码套件并将应用上下文切换 `Microsoft.AspNetCore.Server.Kestrel.EnableWindows81Http2` 设置为 `true` 以启用这些方案。</span><span class="sxs-lookup"><span data-stu-id="7b99f-157">&ast;&ast; Configure compatible cipher suites and set the app context switch `Microsoft.AspNetCore.Server.Kestrel.EnableWindows81Http2` to `true` to enable these scenarios.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="7b99f-158">更改原因</span><span class="sxs-lookup"><span data-stu-id="7b99f-158">Reason for change</span></span>

<span data-ttu-id="7b99f-159">此更改可确保在较早的 Windows 版本上尽早、尽可能清晰地呈现基于 TLS 的 HTTP/2 的兼容性错误。</span><span class="sxs-lookup"><span data-stu-id="7b99f-159">This change ensures compatibility errors for HTTP/2 over TLS on older Windows versions are surfaced as early and as clearly as possible.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="7b99f-160">建议操作</span><span class="sxs-lookup"><span data-stu-id="7b99f-160">Recommended action</span></span>

<span data-ttu-id="7b99f-161">确保在不兼容的 Windows 版本上禁用基于 TLS 的 HTTP/2。</span><span class="sxs-lookup"><span data-stu-id="7b99f-161">Ensure HTTP/2 over TLS is disabled on incompatible Windows versions.</span></span> <span data-ttu-id="7b99f-162">Windows 8.1 和 Windows Server 2012 R2 是不兼容的，因为默认情况下它们缺少必要的密码。</span><span class="sxs-lookup"><span data-stu-id="7b99f-162">Windows 8.1 and Windows Server 2012 R2 are incompatible since they lack the necessary ciphers by default.</span></span> <span data-ttu-id="7b99f-163">但是，可以将“计算机配置”设置更新为使用 HTTP/2 兼容密码。</span><span class="sxs-lookup"><span data-stu-id="7b99f-163">However, it's possible to update the Computer Configuration settings to use HTTP/2 compatible ciphers.</span></span> <span data-ttu-id="7b99f-164">有关详细信息，请参阅 [Windows 8.1 中的 TLS 密码套件](/windows/win32/secauthn/tls-cipher-suites-in-windows-8-1)。</span><span class="sxs-lookup"><span data-stu-id="7b99f-164">For more information, see [TLS cipher suites in Windows 8.1](/windows/win32/secauthn/tls-cipher-suites-in-windows-8-1).</span></span> <span data-ttu-id="7b99f-165">配置完成后，必须通过设置应用上下文切换 `Microsoft.AspNetCore.Server.Kestrel.EnableWindows81Http2`，在 Kestrel 上启用基于 TLS 的 HTTP/2。</span><span class="sxs-lookup"><span data-stu-id="7b99f-165">Once configured, HTTP/2 over TLS on Kestrel must be enabled by setting the app context switch `Microsoft.AspNetCore.Server.Kestrel.EnableWindows81Http2`.</span></span> <span data-ttu-id="7b99f-166">例如：</span><span class="sxs-lookup"><span data-stu-id="7b99f-166">For example:</span></span>

```csharp
AppContext.SetSwitch("Microsoft.AspNetCore.Server.Kestrel.EnableWindows81Http2", true);
```

<span data-ttu-id="7b99f-167">未更改基础支持。</span><span class="sxs-lookup"><span data-stu-id="7b99f-167">No underlying support has changed.</span></span> <span data-ttu-id="7b99f-168">例如，基于 TLS 的 HTTP/2 在 Windows 8 或 Windows Server 2012 上始终无效。</span><span class="sxs-lookup"><span data-stu-id="7b99f-168">For example, HTTP/2 over TLS has never worked on Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="7b99f-169">此更改将修改这些不受支持的方案中错误的呈现方式。</span><span class="sxs-lookup"><span data-stu-id="7b99f-169">This change modifies how errors in these unsupported scenarios are presented.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="7b99f-170">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="7b99f-170">Affected APIs</span></span>

<span data-ttu-id="7b99f-171">None</span><span class="sxs-lookup"><span data-stu-id="7b99f-171">None</span></span>

<!--

### Category

ASP.NET Core

### Affected APIs

Not detectable via API analysis

-->
