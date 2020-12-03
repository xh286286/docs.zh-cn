---
title: 中断性变更：中间件：如果找不到处理程序，则异常处理程序中间件会引发原始异常
description: 了解 ASP.NET Core 5.0 中的以下中断性变更：中间件：如果找不到处理程序，则异常处理程序中间件会引发原始异常
author: scottaddie
ms.author: scaddie
ms.date: 10/01/2020
ms.openlocfilehash: 8801d3e6950d66fd9f24e051fd8729c50eb0b282
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95759278"
---
# <a name="middleware-exception-handler-middleware-throws-original-exception-if-handler-not-found"></a><span data-ttu-id="841ed-103">中间件：如果找不到处理程序，则异常处理程序中间件会引发原始异常</span><span class="sxs-lookup"><span data-stu-id="841ed-103">Middleware: Exception Handler Middleware throws original exception if handler not found</span></span>

<span data-ttu-id="841ed-104">在 ASP.NET Core 5.0 及更低版本中，[异常处理程序中间件](xref:Microsoft.AspNetCore.Builder.ExceptionHandlerExtensions.UseExceptionHandler%2A)在发生异常时执行配置的异常处理程序。</span><span class="sxs-lookup"><span data-stu-id="841ed-104">Before ASP.NET Core 5.0, the [Exception Handler Middleware](xref:Microsoft.AspNetCore.Builder.ExceptionHandlerExtensions.UseExceptionHandler%2A) executes the configured exception handler when an exception has occurred.</span></span> <span data-ttu-id="841ed-105">如果找不到通过 <xref:Microsoft.AspNetCore.Builder.ExceptionHandlerOptions.ExceptionHandlingPath> 配置的异常处理程序，则会生成 HTTP 404 响应。</span><span class="sxs-lookup"><span data-stu-id="841ed-105">If the exception handler, configured via <xref:Microsoft.AspNetCore.Builder.ExceptionHandlerOptions.ExceptionHandlingPath>, can't be found, an HTTP 404 response is produced.</span></span> <span data-ttu-id="841ed-106">该响应具有误导性，因为它：</span><span class="sxs-lookup"><span data-stu-id="841ed-106">The response is misleading in that it:</span></span>

* <span data-ttu-id="841ed-107">似乎是一个用户错误。</span><span class="sxs-lookup"><span data-stu-id="841ed-107">Seems to be a user error.</span></span>
* <span data-ttu-id="841ed-108">掩盖了服务器上发生异常的事实。</span><span class="sxs-lookup"><span data-stu-id="841ed-108">Obscures the fact that an exception occurred on the server.</span></span>

<span data-ttu-id="841ed-109">为了解决 ASP.NET Core 5.0 中的误导性错误，`ExceptionHandlerMiddleware` 会在找不到异常处理程序的情况下引发原始异常。</span><span class="sxs-lookup"><span data-stu-id="841ed-109">To address the misleading error in ASP.NET Core 5.0, the `ExceptionHandlerMiddleware` throws the original exception if the exception handler can't be found.</span></span> <span data-ttu-id="841ed-110">因此，服务器会生成 HTTP 500 响应。</span><span class="sxs-lookup"><span data-stu-id="841ed-110">As a result, an HTTP 500 response is produced by the server.</span></span> <span data-ttu-id="841ed-111">调试发生的错误时，可以更容易地在服务器日志中检查响应。</span><span class="sxs-lookup"><span data-stu-id="841ed-111">The response will be easier to examine in the server logs when debugging the error that occurred.</span></span>

<span data-ttu-id="841ed-112">有关讨论，请参阅 GitHub 问题 [dotnet/aspnetcore#25288](https://github.com/dotnet/aspnetcore/issues/25288)。</span><span class="sxs-lookup"><span data-stu-id="841ed-112">For discussion, see GitHub issue [dotnet/aspnetcore#25288](https://github.com/dotnet/aspnetcore/issues/25288).</span></span>

## <a name="version-introduced"></a><span data-ttu-id="841ed-113">引入的版本</span><span class="sxs-lookup"><span data-stu-id="841ed-113">Version introduced</span></span>

<span data-ttu-id="841ed-114">5.0 RC 1</span><span class="sxs-lookup"><span data-stu-id="841ed-114">5.0 RC 1</span></span>

## <a name="old-behavior"></a><span data-ttu-id="841ed-115">旧行为</span><span class="sxs-lookup"><span data-stu-id="841ed-115">Old behavior</span></span>

<span data-ttu-id="841ed-116">如果找不到配置的异常处理程序，异常处理程序中间件会生成 HTTP 404 响应。</span><span class="sxs-lookup"><span data-stu-id="841ed-116">The Exception Handler Middleware produces an HTTP 404 response if the configured exception handler can't be found.</span></span>

## <a name="new-behavior"></a><span data-ttu-id="841ed-117">新行为</span><span class="sxs-lookup"><span data-stu-id="841ed-117">New behavior</span></span>

<span data-ttu-id="841ed-118">如果找不到配置的异常处理程序，异常处理程序中间件会引发原始异常。</span><span class="sxs-lookup"><span data-stu-id="841ed-118">The Exception Handler Middleware throws the original exception if the configured exception handler can't be found.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="841ed-119">更改原因</span><span class="sxs-lookup"><span data-stu-id="841ed-119">Reason for change</span></span>

<span data-ttu-id="841ed-120">HTTP 404 错误并不意味着服务器发生了异常。</span><span class="sxs-lookup"><span data-stu-id="841ed-120">The HTTP 404 error doesn't make it obvious that an exception occurred on the server.</span></span> <span data-ttu-id="841ed-121">此更改会生成 HTTP 500 错误，很明显：</span><span class="sxs-lookup"><span data-stu-id="841ed-121">This change produces an HTTP 500 error to make it obvious that:</span></span>

* <span data-ttu-id="841ed-122">此问题不是由用户错误引起的。</span><span class="sxs-lookup"><span data-stu-id="841ed-122">The problem isn't caused by a user error.</span></span>
* <span data-ttu-id="841ed-123">服务器上发生了异常。</span><span class="sxs-lookup"><span data-stu-id="841ed-123">An exception was encountered on the server.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="841ed-124">建议操作</span><span class="sxs-lookup"><span data-stu-id="841ed-124">Recommended action</span></span>

<span data-ttu-id="841ed-125">无 API 更改。</span><span class="sxs-lookup"><span data-stu-id="841ed-125">There are no API changes.</span></span> <span data-ttu-id="841ed-126">所有现有的应用将继续编译并运行。</span><span class="sxs-lookup"><span data-stu-id="841ed-126">All existing apps will continue to compile and run.</span></span> <span data-ttu-id="841ed-127">引发的异常由服务器处理。</span><span class="sxs-lookup"><span data-stu-id="841ed-127">The exception thrown is handled by the server.</span></span> <span data-ttu-id="841ed-128">例如，[Kestrel](/aspnet/core/fundamentals/servers/kestrel) 或 [HTTP.sys](/aspnet/core/fundamentals/servers/httpsys) 会将异常转换为 HTTP 500 错误响应。</span><span class="sxs-lookup"><span data-stu-id="841ed-128">For example, the exception is converted to an HTTP 500 error response by [Kestrel](/aspnet/core/fundamentals/servers/kestrel) or [HTTP.sys](/aspnet/core/fundamentals/servers/httpsys).</span></span>

## <a name="affected-apis"></a><span data-ttu-id="841ed-129">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="841ed-129">Affected APIs</span></span>

<span data-ttu-id="841ed-130">无</span><span class="sxs-lookup"><span data-stu-id="841ed-130">None</span></span>

<!--

### Category

ASP.NET Core

### Affected APIs

Not detectable via API analysis

-->
