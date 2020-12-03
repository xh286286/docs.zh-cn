---
title: 中断性变更：HttpSys：默认情况下禁用客户端证书重新协商
description: 了解 ASP.NET Core 5.0 中的以下中断性变更：HttpSys：默认情况下禁用客户端证书重新协商
author: scottaddie
ms.author: scaddie
ms.date: 10/01/2020
ms.openlocfilehash: 796989e1a21e3cb206d081e4fe8f79630121dc84
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759077"
---
# <a name="httpsys-client-certificate-renegotiation-disabled-by-default"></a><span data-ttu-id="7bc3a-103">HttpSys：默认情况下禁用客户端证书重新协商</span><span class="sxs-lookup"><span data-stu-id="7bc3a-103">HttpSys: Client certificate renegotiation disabled by default</span></span>

<span data-ttu-id="7bc3a-104">默认情况下，重新协商连接和请求客户端证书的选项已禁用。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-104">The option to renegotiate a connection and request a client certificate has been disabled by default.</span></span> <span data-ttu-id="7bc3a-105">有关讨论，请参阅问题 [dotnet/aspnetcore#23181](https://github.com/dotnet/aspnetcore/issues/23181)。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-105">For discussion, see issue [dotnet/aspnetcore#23181](https://github.com/dotnet/aspnetcore/issues/23181).</span></span>

## <a name="version-introduced"></a><span data-ttu-id="7bc3a-106">引入的版本</span><span class="sxs-lookup"><span data-stu-id="7bc3a-106">Version introduced</span></span>

<span data-ttu-id="7bc3a-107">ASP.NET Core 5.0</span><span class="sxs-lookup"><span data-stu-id="7bc3a-107">ASP.NET Core 5.0</span></span>

## <a name="old-behavior"></a><span data-ttu-id="7bc3a-108">旧行为</span><span class="sxs-lookup"><span data-stu-id="7bc3a-108">Old behavior</span></span>

<span data-ttu-id="7bc3a-109">可以重新协商连接以请求客户端证书。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-109">The connection can be renegotiated to request a client certificate.</span></span>

## <a name="new-behavior"></a><span data-ttu-id="7bc3a-110">新行为</span><span class="sxs-lookup"><span data-stu-id="7bc3a-110">New behavior</span></span>

<span data-ttu-id="7bc3a-111">只能在初始连接握手期间请求客户端证书。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-111">Client certificates can only be requested during the initial connection handshake.</span></span> <span data-ttu-id="7bc3a-112">有关详细信息，请参阅拉取请求 [dotnet/aspnetcore#23162](https://github.com/dotnet/aspnetcore/pull/23162)。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-112">For more information, see pull request [dotnet/aspnetcore#23162](https://github.com/dotnet/aspnetcore/pull/23162).</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="7bc3a-113">更改原因</span><span class="sxs-lookup"><span data-stu-id="7bc3a-113">Reason for change</span></span>

<span data-ttu-id="7bc3a-114">重新协商导致了许多性能和死锁问题。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-114">Renegotiation caused a number of performance and deadlock issues.</span></span> <span data-ttu-id="7bc3a-115">它在 HTTP/2 中也不受支持。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-115">It's also not supported in HTTP/2.</span></span> <span data-ttu-id="7bc3a-116">有关 ASP.NET Core 3.1 中引入控制此行为的选项时的其他上下文，请参阅问题 [dotnet/aspnetcore#14806](https://github.com/dotnet/aspnetcore/issues/14806)。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-116">For additional context from when the option to control this behavior was introduced in ASP.NET Core 3.1, see issue [dotnet/aspnetcore#14806](https://github.com/dotnet/aspnetcore/issues/14806).</span></span>

## <a name="recommended-action"></a><span data-ttu-id="7bc3a-117">建议操作</span><span class="sxs-lookup"><span data-stu-id="7bc3a-117">Recommended action</span></span>

<span data-ttu-id="7bc3a-118">需要客户端证书的应用应使用 netsh.exe 将 `clientcertnegotiation` 选项设置为 `enabled`。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-118">Apps that require client certificates should use *netsh.exe* to set the `clientcertnegotiation` option to `enabled`.</span></span> <span data-ttu-id="7bc3a-119">有关详细信息，请参阅 [netsh http 命令](/windows-server/networking/technologies/netsh/netsh-http)。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-119">For more information, see [netsh http commands](/windows-server/networking/technologies/netsh/netsh-http).</span></span>

<span data-ttu-id="7bc3a-120">如果要仅针对应用的某些部分启用客户端证书，请参阅[可选客户端证书](/aspnet/core/security/authentication/certauth?view=aspnetcore-3.1#optional-client-certificates)中的指南。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-120">If you want client certificates enabled for only some parts of your app, see the guidance at [Optional client certificates](/aspnet/core/security/authentication/certauth?view=aspnetcore-3.1#optional-client-certificates).</span></span>

<span data-ttu-id="7bc3a-121">如果需要旧的重新协商行为，请将 `HttpSysOptions.ClientCertificateMethod` 设置为旧值 `ClientCertificateMethod.AllowRenegotiate`。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-121">If you need the old renegotiate behavior, set `HttpSysOptions.ClientCertificateMethod` to the old value `ClientCertificateMethod.AllowRenegotiate`.</span></span> <span data-ttu-id="7bc3a-122">由于上述原因和链接的指南中的原因，不建议这样做。</span><span class="sxs-lookup"><span data-stu-id="7bc3a-122">This isn't recommended for the reasons outlined above and in the linked guidance.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="7bc3a-123">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="7bc3a-123">Affected APIs</span></span>

- <xref:Microsoft.AspNetCore.Http.ConnectionInfo.ClientCertificate%2A?displayProperty=nameWithType>
- <xref:Microsoft.AspNetCore.Http.ConnectionInfo.GetClientCertificateAsync%2A?displayProperty=nameWithType>
- <xref:Microsoft.AspNetCore.Server.HttpSys.HttpSysOptions.ClientCertificateMethod%2A?displayProperty=nameWithType>

<!--

### Category

ASP.NET Core

### Affected APIs

- `Overload:Microsoft.AspNetCore.Http.ConnectionInfo.ClientCertificate`
- `Overload:Microsoft.AspNetCore.Http.ConnectionInfo.GetClientCertificateAsync`
- `Overload:Microsoft.AspNetCore.Server.HttpSys.HttpSysOptions.ClientCertificateMethod`

-->
