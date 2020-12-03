---
title: 中断性变更：Cookie 路径处理现在符合 RFC 6265
description: 了解 .NET 5.0 中的以下中断性变更：RFC 6265 中定义的路径处理算法之前针对 Cookie 和 CookieContainer 类而实现，
ms.date: 08/18/2020
ms.openlocfilehash: 4aea06f434c4bbbef7d94b4b39ff647dd954745e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759126"
---
# <a name="cookie-path-handling-now-conforms-to-rfc-6265"></a><span data-ttu-id="ddab0-103">Cookie 路径处理现在符合 RFC 6265</span><span class="sxs-lookup"><span data-stu-id="ddab0-103">Cookie path handling now conforms to RFC 6265</span></span>

<span data-ttu-id="ddab0-104">[RFC 6265](https://tools.ietf.org/html/rfc6265) 中定义的路径处理算法是针对 <xref:System.Net.Cookie> 和 <xref:System.Net.CookieContainer> 类实现的。</span><span class="sxs-lookup"><span data-stu-id="ddab0-104">Path-handling algorithms defined in [RFC 6265](https://tools.ietf.org/html/rfc6265) were implemented for the <xref:System.Net.Cookie> and <xref:System.Net.CookieContainer> classes.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="ddab0-105">引入的版本</span><span class="sxs-lookup"><span data-stu-id="ddab0-105">Version introduced</span></span>

<span data-ttu-id="ddab0-106">5.0</span><span class="sxs-lookup"><span data-stu-id="ddab0-106">5.0</span></span>

## <a name="change-description"></a><span data-ttu-id="ddab0-107">更改描述</span><span class="sxs-lookup"><span data-stu-id="ddab0-107">Change description</span></span>

- <span data-ttu-id="ddab0-108">无需再将 <xref:System.Net.Cookie.Path> 属性作为请求路径的前缀。</span><span class="sxs-lookup"><span data-stu-id="ddab0-108">The <xref:System.Net.Cookie.Path> property is no longer required to be a prefix of the request path.</span></span>
- <span data-ttu-id="ddab0-109"><xref:System.Net.Cookie.Path> 的默认值的计算和路径匹配算法是按照 RFC 6265 的[第 5.1.4 节](https://tools.ietf.org/html/rfc6265#section-5.1.4)中的定义实现的。</span><span class="sxs-lookup"><span data-stu-id="ddab0-109">The calculation of the default value of <xref:System.Net.Cookie.Path> and path-matching algorithms were implemented as defined in [section 5.1.4](https://tools.ietf.org/html/rfc6265#section-5.1.4) of RFC 6265.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="ddab0-110">建议操作</span><span class="sxs-lookup"><span data-stu-id="ddab0-110">Recommended action</span></span>

<span data-ttu-id="ddab0-111">在大多数情况下，无需执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="ddab0-111">In most cases, you won't need to take any action.</span></span> <span data-ttu-id="ddab0-112">但是，如果代码依赖于 <xref:System.Net.Cookie.Path> 验证，则需要在代码中实现所需的验证。</span><span class="sxs-lookup"><span data-stu-id="ddab0-112">However, if your code was dependent on <xref:System.Net.Cookie.Path> validation, you'll need to implement required validation in your code.</span></span> <span data-ttu-id="ddab0-113">如果代码依赖于 <xref:System.Net.Cookie.Path> 的默认值计算，请考虑手动提供 <xref:System.Net.Cookie.Path> 值，而不使用默认值。</span><span class="sxs-lookup"><span data-stu-id="ddab0-113">If your code was dependent on default value calculation for <xref:System.Net.Cookie.Path>, consider supplying the <xref:System.Net.Cookie.Path> value manually instead of using the default value.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="ddab0-114">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="ddab0-114">Affected APIs</span></span>

- <xref:System.Net.Cookie?displayProperty=fullName>
- <xref:System.Net.CookieContainer?displayProperty=fullName>

<!--

### Affected APIs

- `T:System.Net.Cookie`
- `T:System.Net.CookieContainer`

### Category

Networking

-->
