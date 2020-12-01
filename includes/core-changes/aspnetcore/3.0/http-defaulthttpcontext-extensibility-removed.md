---
ms.openlocfilehash: 9d138f79fcede4acac837f8d7793aa343ced737c
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96032274"
---
### <a name="http-defaulthttpcontext-extensibility-removed"></a><span data-ttu-id="cb665-101">HTTP：已删除 DefaultHttpContext 扩展性</span><span class="sxs-lookup"><span data-stu-id="cb665-101">HTTP: DefaultHttpContext extensibility removed</span></span>

<span data-ttu-id="cb665-102">作为 ASP.NET Core 3.0 性能改进的一部分，已删除 `DefaultHttpContext` 的扩展性。</span><span class="sxs-lookup"><span data-stu-id="cb665-102">As part of ASP.NET Core 3.0 performance improvements, the extensibility of `DefaultHttpContext` was removed.</span></span> <span data-ttu-id="cb665-103">此类现在为 `sealed`。</span><span class="sxs-lookup"><span data-stu-id="cb665-103">The class is now `sealed`.</span></span> <span data-ttu-id="cb665-104">有关详细信息，请参阅 [dotnet/aspnetcore#6504](https://github.com/dotnet/aspnetcore/pull/6504)。</span><span class="sxs-lookup"><span data-stu-id="cb665-104">For more information, see [dotnet/aspnetcore#6504](https://github.com/dotnet/aspnetcore/pull/6504).</span></span>

<span data-ttu-id="cb665-105">如果单元测试使用 `Mock<DefaultHttpContext>`，请改用 `Mock<HttpContext>` 或 `new DefaultHttpContext()`。</span><span class="sxs-lookup"><span data-stu-id="cb665-105">If your unit tests use `Mock<DefaultHttpContext>`, use `Mock<HttpContext>` or `new DefaultHttpContext()` instead.</span></span>

<span data-ttu-id="cb665-106">有关讨论，请参阅 [dotnet/aspnetcore#6534](https://github.com/dotnet/aspnetcore/issues/6534)。</span><span class="sxs-lookup"><span data-stu-id="cb665-106">For discussion, see [dotnet/aspnetcore#6534](https://github.com/dotnet/aspnetcore/issues/6534).</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="cb665-107">引入的版本</span><span class="sxs-lookup"><span data-stu-id="cb665-107">Version introduced</span></span>

<span data-ttu-id="cb665-108">3.0</span><span class="sxs-lookup"><span data-stu-id="cb665-108">3.0</span></span>

#### <a name="old-behavior"></a><span data-ttu-id="cb665-109">旧行为</span><span class="sxs-lookup"><span data-stu-id="cb665-109">Old behavior</span></span>

<span data-ttu-id="cb665-110">类可从 `DefaultHttpContext` 派生。</span><span class="sxs-lookup"><span data-stu-id="cb665-110">Classes can derive from `DefaultHttpContext`.</span></span>

#### <a name="new-behavior"></a><span data-ttu-id="cb665-111">新行为</span><span class="sxs-lookup"><span data-stu-id="cb665-111">New behavior</span></span>

<span data-ttu-id="cb665-112">类不可从 `DefaultHttpContext` 派生。</span><span class="sxs-lookup"><span data-stu-id="cb665-112">Classes can't derive from `DefaultHttpContext`.</span></span>

#### <a name="reason-for-change"></a><span data-ttu-id="cb665-113">更改原因</span><span class="sxs-lookup"><span data-stu-id="cb665-113">Reason for change</span></span>

<span data-ttu-id="cb665-114">最初提供扩展性是为了允许 `HttpContext` 合并，但它引入了不必要的复杂性并妨碍了其他优化。</span><span class="sxs-lookup"><span data-stu-id="cb665-114">The extensibility was provided initially to allow pooling of the `HttpContext`, but it introduced unnecessary complexity and impeded other optimizations.</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="cb665-115">建议操作</span><span class="sxs-lookup"><span data-stu-id="cb665-115">Recommended action</span></span>

<span data-ttu-id="cb665-116">如果在单元测试中使用 `Mock<DefaultHttpContext>`，请改为开始使用 `Mock<HttpContext>`。</span><span class="sxs-lookup"><span data-stu-id="cb665-116">If you're using `Mock<DefaultHttpContext>` in your unit tests, begin using `Mock<HttpContext>` instead.</span></span>

#### <a name="category"></a><span data-ttu-id="cb665-117">类别</span><span class="sxs-lookup"><span data-stu-id="cb665-117">Category</span></span>

<span data-ttu-id="cb665-118">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="cb665-118">ASP.NET Core</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="cb665-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="cb665-119">Affected APIs</span></span>

<xref:Microsoft.AspNetCore.Http.DefaultHttpContext?displayProperty=nameWithType>

<!--

#### Affected APIs

`T:Microsoft.AspNetCore.Http.DefaultHttpContext`

-->
