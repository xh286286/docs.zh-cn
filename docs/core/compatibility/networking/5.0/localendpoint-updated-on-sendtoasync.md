---
title: 中断性变更：调用 SendToAsync 后更新 Socket.LocalEndPoint
description: 了解 .NET 5.0 中的以下中断性变更：SendToAsync 现在将本地终结点属性的值更新为套接字的本地地址。
ms.date: 10/18/2020
ms.openlocfilehash: 53d7da350eac6e65832012331044427fd90fe796
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759123"
---
# <a name="socketlocalendpoint-is-updated-after-calling-sendtoasync"></a><span data-ttu-id="15880-103">调用 SendToAsync 后更新 Socket.LocalEndPoint</span><span class="sxs-lookup"><span data-stu-id="15880-103">Socket.LocalEndPoint is updated after calling SendToAsync</span></span>

<span data-ttu-id="15880-104"><xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)?displayProperty=nameWithType> 现将 <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> 属性的值更新为套接字的本地地址。</span><span class="sxs-lookup"><span data-stu-id="15880-104"><xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)?displayProperty=nameWithType> now updates the value of the <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> property to the socket's local address.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="15880-105">引入的版本</span><span class="sxs-lookup"><span data-stu-id="15880-105">Version introduced</span></span>

<span data-ttu-id="15880-106">5.0</span><span class="sxs-lookup"><span data-stu-id="15880-106">5.0</span></span>

## <a name="change-description"></a><span data-ttu-id="15880-107">更改描述</span><span class="sxs-lookup"><span data-stu-id="15880-107">Change description</span></span>

<span data-ttu-id="15880-108">在以前的 .NET 版本中，<xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)?displayProperty=nameWithType> 不会更改套接字实例上 <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> 属性的值。</span><span class="sxs-lookup"><span data-stu-id="15880-108">In previous .NET versions, <xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)?displayProperty=nameWithType> does not alter the value of the <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> property on the socket instance.</span></span> <span data-ttu-id="15880-109">从 .NET 5.0 开始，<xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)> 成功完成后，<xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> 的值为隐式绑定的套接字的本地地址。</span><span class="sxs-lookup"><span data-stu-id="15880-109">Starting in .NET 5.0, when <xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)> successfully completes, the value of <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> is the implicitly bound socket's local address.</span></span> <span data-ttu-id="15880-110">这一新行为与 <xref:System.Net.Sockets.Socket.SendTo(System.Byte[],System.Net.EndPoint)> 和 <xref:System.Net.Sockets.Socket.BeginSendTo(System.Byte[],System.Int32,System.Int32,System.Net.Sockets.SocketFlags,System.Net.EndPoint,System.AsyncCallback,System.Object)>/<xref:System.Net.Sockets.Socket.EndSendTo(System.IAsyncResult)> 的行为一致。</span><span class="sxs-lookup"><span data-stu-id="15880-110">This new behavior is consistent with the behavior of <xref:System.Net.Sockets.Socket.SendTo(System.Byte[],System.Net.EndPoint)> and <xref:System.Net.Sockets.Socket.BeginSendTo(System.Byte[],System.Int32,System.Int32,System.Net.Sockets.SocketFlags,System.Net.EndPoint,System.AsyncCallback,System.Object)>/<xref:System.Net.Sockets.Socket.EndSendTo(System.IAsyncResult)>.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="15880-111">更改原因</span><span class="sxs-lookup"><span data-stu-id="15880-111">Reason for change</span></span>

<span data-ttu-id="15880-112">此更改会[修复一个 bug](https://github.com/dotnet/runtime/issues/915)，并使该行为在 `SendTo` 变体中保持一致。</span><span class="sxs-lookup"><span data-stu-id="15880-112">This change [fixes a bug](https://github.com/dotnet/runtime/issues/915) and makes the behavior consistent across `SendTo` variants.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="15880-113">建议的操作</span><span class="sxs-lookup"><span data-stu-id="15880-113">Recommended action</span></span>

<span data-ttu-id="15880-114">更改所有假定 <xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)> 不会更改 <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType> 的值的代码。</span><span class="sxs-lookup"><span data-stu-id="15880-114">Alter any code that assumes that <xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)> won't alter the value of <xref:System.Net.Sockets.Socket.LocalEndPoint?displayProperty=nameWithType>.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="15880-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="15880-115">Affected APIs</span></span>

- <xref:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)?displayProperty=fullName>

<!--

### Affected APIs

- `M:System.Net.Sockets.Socket.SendToAsync(System.Net.Sockets.SocketAsyncEventArgs)`

### Category

Networking

-->
