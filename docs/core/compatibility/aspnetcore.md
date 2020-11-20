---
title: ASP.NET Core 中断性变更
titleSuffix: ''
description: 列出 ASP.NET Core 中的中断性变更。
ms.date: 11/03/2020
author: scottaddie
ms.author: scaddie
ms.openlocfilehash: 6e8e35d01ea7ff91c45bf1febd822e8497b608f0
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94440471"
---
# <a name="aspnet-core-breaking-changes"></a><span data-ttu-id="29095-103">ASP.NET Core 中断性变更</span><span class="sxs-lookup"><span data-stu-id="29095-103">ASP.NET Core breaking changes</span></span>

<span data-ttu-id="29095-104">ASP.NET Core 提供 .NET Core 使用的 Web 应用开发功能。</span><span class="sxs-lookup"><span data-stu-id="29095-104">ASP.NET Core provides the web app development features used by .NET Core.</span></span>

<span data-ttu-id="29095-105">选择以下链接之一，了解特定版本中的中断性变更：</span><span class="sxs-lookup"><span data-stu-id="29095-105">Select one of the following links for breaking changes in a specific version:</span></span>

* [<span data-ttu-id="29095-106">ASP.NET Core 5.0</span><span class="sxs-lookup"><span data-stu-id="29095-106">ASP.NET Core 5.0</span></span>](#aspnet-core-50)
* [<span data-ttu-id="29095-107">ASP.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="29095-107">ASP.NET Core 3.1</span></span>](#aspnet-core-31)
* [<span data-ttu-id="29095-108">ASP.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="29095-108">ASP.NET Core 3.0</span></span>](#aspnet-core-30)

<span data-ttu-id="29095-109">本页记录了 ASP.NET Core 3.0、3.1 和 5.0 中的以下中断性变更：</span><span class="sxs-lookup"><span data-stu-id="29095-109">The following breaking changes in ASP.NET Core 3.0, 3.1, and 5.0 are documented on this page:</span></span>

- [<span data-ttu-id="29095-110">已删除过时防伪、CORS、诊断、MVC 和路由 API</span><span class="sxs-lookup"><span data-stu-id="29095-110">Obsolete Antiforgery, CORS, Diagnostics, MVC, and Routing APIs removed</span></span>](#obsolete-antiforgery-cors-diagnostics-mvc-and-routing-apis-removed)
- [<span data-ttu-id="29095-111">身份验证：标记为已过时的 AzureAD.UI 和 AzureADB2C.UI API 和包</span><span class="sxs-lookup"><span data-stu-id="29095-111">Authentication: AzureAD.UI and AzureADB2C.UI APIs and packages marked obsolete</span></span>](#authentication-azureadui-and-azureadb2cui-apis-and-packages-marked-obsolete)
- [<span data-ttu-id="29095-112">身份验证：Google+ 弃用</span><span class="sxs-lookup"><span data-stu-id="29095-112">Authentication: Google+ deprecation</span></span>](#authentication-google-deprecated-and-replaced)
- [<span data-ttu-id="29095-113">身份验证：已删除 HttpContext.Authentication 属性</span><span class="sxs-lookup"><span data-stu-id="29095-113">Authentication: HttpContext.Authentication property removed</span></span>](#authentication-httpcontextauthentication-property-removed)
- [<span data-ttu-id="29095-114">身份验证：已替换 Newtonsoft.json 类型</span><span class="sxs-lookup"><span data-stu-id="29095-114">Authentication: Newtonsoft.Json types replaced</span></span>](#authentication-newtonsoftjson-types-replaced)
- [<span data-ttu-id="29095-115">身份验证：已更改 OAuthHandler ExchangeCodeAsync 签名</span><span class="sxs-lookup"><span data-stu-id="29095-115">Authentication: OAuthHandler ExchangeCodeAsync signature changed</span></span>](#authentication-oauthhandler-exchangecodeasync-signature-changed)
- [<span data-ttu-id="29095-116">授权：AddAuthorization 重载已移到不同的程序集</span><span class="sxs-lookup"><span data-stu-id="29095-116">Authorization: AddAuthorization overload moved to different assembly</span></span>](#authorization-addauthorization-overload-moved-to-different-assembly)
- [<span data-ttu-id="29095-117">授权：已从 AuthorizationFilterContext.Filters 中删除 IAllowAnonymous</span><span class="sxs-lookup"><span data-stu-id="29095-117">Authorization: IAllowAnonymous removed from AuthorizationFilterContext.Filters</span></span>](#authorization-iallowanonymous-removed-from-authorizationfiltercontextfilters)
- [<span data-ttu-id="29095-118">授权：IAuthorizationPolicyProvider 实现需要新方法</span><span class="sxs-lookup"><span data-stu-id="29095-118">Authorization: IAuthorizationPolicyProvider implementations require new method</span></span>](#authorization-iauthorizationpolicyprovider-implementations-require-new-method)
- [<span data-ttu-id="29095-119">授权：终结点路由中的资源为 HttpContext</span><span class="sxs-lookup"><span data-stu-id="29095-119">Authorization: Resource in endpoint routing is HttpContext</span></span>](#authorization-resource-in-endpoint-routing-is-httpcontext)
- [<span data-ttu-id="29095-120">Azure:Microsoft 预先指定的 Azure 集成包已删除</span><span class="sxs-lookup"><span data-stu-id="29095-120">Azure: Microsoft-prefixed Azure integration packages removed</span></span>](#azure-microsoft-prefixed-azure-integration-packages-removed)
- [<span data-ttu-id="29095-121">BinaryFormatter 序列化方法已过时，并且已在 ASP.NET 应用中禁用</span><span class="sxs-lookup"><span data-stu-id="29095-121">BinaryFormatter serialization methods are obsolete and prohibited in ASP.NET apps</span></span>](#binaryformatter-serialization-methods-are-obsolete-and-prohibited-in-aspnet-apps)
- [<span data-ttu-id="29095-122">Blazor：在编译时从组件中剪裁掉无意义的空白</span><span class="sxs-lookup"><span data-stu-id="29095-122">Blazor: Insignificant whitespace trimmed from components at compile time</span></span>](#blazor-insignificant-whitespace-trimmed-from-components-at-compile-time)
- [<span data-ttu-id="29095-123">Blazor：JSObjectReference 和 JSInProcessObjectReference 类型已更改为 internal</span><span class="sxs-lookup"><span data-stu-id="29095-123">Blazor: JSObjectReference and JSInProcessObjectReference types changed to internal</span></span>](#blazor-jsobjectreference-and-jsinprocessobjectreference-types-changed-to-internal)
- [<span data-ttu-id="29095-124">Blazor：ProtectedBrowserStorage 功能已移动到共享框架</span><span class="sxs-lookup"><span data-stu-id="29095-124">Blazor: ProtectedBrowserStorage feature moved to shared framework</span></span>](#blazor-protectedbrowserstorage-feature-moved-to-shared-framework)
- [<span data-ttu-id="29095-125">Blazor：RenderTreeFrame readonly 公共字段已成为属性</span><span class="sxs-lookup"><span data-stu-id="29095-125">Blazor: RenderTreeFrame readonly public fields have become properties</span></span>](#blazor-rendertreeframe-readonly-public-fields-have-become-properties)
- [<span data-ttu-id="29095-126">Blazor：NuGet 包的目标框架已更改</span><span class="sxs-lookup"><span data-stu-id="29095-126">Blazor: Target framework of NuGet packages changed</span></span>](#blazor-target-framework-of-nuget-packages-changed)
- [<span data-ttu-id="29095-127">Blazor：更新的浏览器支持</span><span class="sxs-lookup"><span data-stu-id="29095-127">Blazor: Updated browser support</span></span>](#blazor-updated-browser-support)
- [<span data-ttu-id="29095-128">Blazor：更新的静态 Web 资产的验证逻辑</span><span class="sxs-lookup"><span data-stu-id="29095-128">Blazor: Updated validation logic for static web assets</span></span>](#blazor-updated-validation-logic-for-static-web-assets)
- [<span data-ttu-id="29095-129">缓存：已删除 CompactOnMemoryPressure 属性</span><span class="sxs-lookup"><span data-stu-id="29095-129">Caching: CompactOnMemoryPressure property removed</span></span>](#caching-compactonmemorypressure-property-removed)
- [<span data-ttu-id="29095-130">缓存：Microsoft.Extensions.Caching.SqlServer 使用新的 SqlClient 包</span><span class="sxs-lookup"><span data-stu-id="29095-130">Caching: Microsoft.Extensions.Caching.SqlServer uses new SqlClient package</span></span>](#caching-microsoftextensionscachingsqlserver-uses-new-sqlclient-package)
- [<span data-ttu-id="29095-131">缓存：ResponseCaching“Pubternal”类型已更改为内部类型</span><span class="sxs-lookup"><span data-stu-id="29095-131">Caching: ResponseCaching "pubternal" types changed to internal</span></span>](#caching-responsecaching-pubternal-types-changed-to-internal)
- [<span data-ttu-id="29095-132">数据保护：DataProtection.Blobs 使用新的 Azure 存储 API</span><span class="sxs-lookup"><span data-stu-id="29095-132">Data Protection: DataProtection.Blobs uses new Azure Storage APIs</span></span>](#data-protection-dataprotectionblobs-uses-new-azure-storage-apis)
- [<span data-ttu-id="29095-133">扩展：影响某些 NuGet 包的包引用更改</span><span class="sxs-lookup"><span data-stu-id="29095-133">Extensions: Package reference changes affecting some NuGet packages</span></span>](#extensions-package-reference-changes-affecting-some-nuget-packages)
- [<span data-ttu-id="29095-134">托管：已从 Windows 托管捆绑包中删除 AspNetCoreModule V1</span><span class="sxs-lookup"><span data-stu-id="29095-134">Hosting: AspNetCoreModule V1 removed from Windows Hosting Bundle</span></span>](#hosting-aspnetcoremodule-v1-removed-from-windows-hosting-bundle)
- [<span data-ttu-id="29095-135">托管：通用主机限制 Startup 构造函数注入</span><span class="sxs-lookup"><span data-stu-id="29095-135">Hosting: Generic host restricts Startup constructor injection</span></span>](#hosting-generic-host-restricts-startup-constructor-injection)
- [<span data-ttu-id="29095-136">托管：已为 IIS 进程外应用启用 HTTPS 重定向</span><span class="sxs-lookup"><span data-stu-id="29095-136">Hosting: HTTPS redirection enabled for IIS out-of-process apps</span></span>](#hosting-https-redirection-enabled-for-iis-out-of-process-apps)
- [<span data-ttu-id="29095-137">托管：已替换 IHostingEnvironment 和 IApplicationLifetime 类型</span><span class="sxs-lookup"><span data-stu-id="29095-137">Hosting: IHostingEnvironment and IApplicationLifetime types replaced</span></span>](#hosting-ihostingenvironment-and-iapplicationlifetime-types-marked-obsolete-and-replaced)
- [<span data-ttu-id="29095-138">托管：已从 WebHostBuilder 依赖项中删除 ObjectPoolProvider</span><span class="sxs-lookup"><span data-stu-id="29095-138">Hosting: ObjectPoolProvider removed from WebHostBuilder dependencies</span></span>](#hosting-objectpoolprovider-removed-from-webhostbuilder-dependencies)
- [<span data-ttu-id="29095-139">HTTP：标记为已过时并被替换的 Kestrel 和 IIS BadHttpRequestException 类型</span><span class="sxs-lookup"><span data-stu-id="29095-139">HTTP: Kestrel and IIS BadHttpRequestException types marked obsolete and replaced</span></span>](#http-kestrel-and-iis-badhttprequestexception-types-marked-obsolete-and-replaced)
- [<span data-ttu-id="29095-140">HTTP：浏览器的 SameSite 更改会影响身份验证</span><span class="sxs-lookup"><span data-stu-id="29095-140">HTTP: Browser SameSite changes impact authentication</span></span>](#http-browser-samesite-changes-impact-authentication)
- [<span data-ttu-id="29095-141">HTTP：已删除 DefaultHttpContext 扩展性</span><span class="sxs-lookup"><span data-stu-id="29095-141">HTTP: DefaultHttpContext extensibility removed</span></span>](#http-defaulthttpcontext-extensibility-removed)
- [<span data-ttu-id="29095-142">HTTP：HeaderNames 字段已更改为静态只读</span><span class="sxs-lookup"><span data-stu-id="29095-142">HTTP: HeaderNames fields changed to static readonly</span></span>](#http-headernames-constants-changed-to-static-readonly)
- [<span data-ttu-id="29095-143">HTTP：IHttpClientFactory 创建的 HttpClient 实例记录整数状态代码</span><span class="sxs-lookup"><span data-stu-id="29095-143">HTTP: HttpClient instances created by IHttpClientFactory log integer status codes</span></span>](#http-httpclient-instances-created-by-ihttpclientfactory-log-integer-status-codes)
- [<span data-ttu-id="29095-144">HTTP：响应正文基础结构更改</span><span class="sxs-lookup"><span data-stu-id="29095-144">HTTP: Response body infrastructure changes</span></span>](#http-response-body-infrastructure-changes)
- [<span data-ttu-id="29095-145">HTTP：已更改某些 Cookie SameSite 默认值</span><span class="sxs-lookup"><span data-stu-id="29095-145">HTTP: Some cookie SameSite default values changed</span></span>](#http-some-cookie-samesite-defaults-changed-to-none)
- [<span data-ttu-id="29095-146">HTTP：已默认禁用同步 IO</span><span class="sxs-lookup"><span data-stu-id="29095-146">HTTP: Synchronous IO disabled by default</span></span>](#http-synchronous-io-disabled-in-all-servers)
- [<span data-ttu-id="29095-147">HttpSys：默认情况下禁用客户端证书重新协商</span><span class="sxs-lookup"><span data-stu-id="29095-147">HttpSys: Client certificate renegotiation disabled by default</span></span>](#httpsys-client-certificate-renegotiation-disabled-by-default)
- [<span data-ttu-id="29095-148">标识：已删除 AddDefaultUI 方法重载</span><span class="sxs-lookup"><span data-stu-id="29095-148">Identity: AddDefaultUI method overload removed</span></span>](#identity-adddefaultui-method-overload-removed)
- [<span data-ttu-id="29095-149">标识：UI 启动版本更改</span><span class="sxs-lookup"><span data-stu-id="29095-149">Identity: UI Bootstrap version change</span></span>](#identity-default-bootstrap-version-of-ui-changed)
- [<span data-ttu-id="29095-150">标识：对于未经身份验证的标识，SignInAsync 会引发异常</span><span class="sxs-lookup"><span data-stu-id="29095-150">Identity: SignInAsync throws exception for unauthenticated identity</span></span>](#identity-signinasync-throws-exception-for-unauthenticated-identity)
- [<span data-ttu-id="29095-151">标识：SignInManager 构造函数接受新参数</span><span class="sxs-lookup"><span data-stu-id="29095-151">Identity: SignInManager constructor accepts new parameter</span></span>](#identity-signinmanager-constructor-accepts-new-parameter)
- [<span data-ttu-id="29095-152">标识：UI 使用静态 Web 资产功能</span><span class="sxs-lookup"><span data-stu-id="29095-152">Identity: UI uses static web assets feature</span></span>](#identity-ui-uses-static-web-assets-feature)
- [<span data-ttu-id="29095-153">IIS：保留 UrlRewrite 中间件查询字符串</span><span class="sxs-lookup"><span data-stu-id="29095-153">IIS: UrlRewrite middleware query strings are preserved</span></span>](#iis-urlrewrite-middleware-query-strings-are-preserved)
- [<span data-ttu-id="29095-154">Kestrel：默认检测运行时的配置更改</span><span class="sxs-lookup"><span data-stu-id="29095-154">Kestrel: Configuration changes at run time detected by default</span></span>](#kestrel-configuration-changes-at-run-time-detected-by-default)
- [<span data-ttu-id="29095-155">Kestrel：已删除连接适配器</span><span class="sxs-lookup"><span data-stu-id="29095-155">Kestrel: Connection adapters removed</span></span>](#kestrel-connection-adapters-removed)
- [<span data-ttu-id="29095-156">Kestrel：默认支持的 TLS 协议版本已更改</span><span class="sxs-lookup"><span data-stu-id="29095-156">Kestrel: Default supported TLS protocol versions changed</span></span>](#kestrel-default-supported-tls-protocol-versions-changed)
- [<span data-ttu-id="29095-157">Kestrel：已删除空 HTTPS 程序集</span><span class="sxs-lookup"><span data-stu-id="29095-157">Kestrel: Empty HTTPS assembly removed</span></span>](#kestrel-empty-https-assembly-removed)
- [<span data-ttu-id="29095-158">Kestrel：在不兼容的 Windows 版本上通过 TLS 禁用 HTTP/2</span><span class="sxs-lookup"><span data-stu-id="29095-158">Kestrel: HTTP/2 disabled over TLS on incompatible Windows versions</span></span>](#kestrel-http2-disabled-over-tls-on-incompatible-windows-versions)
- [<span data-ttu-id="29095-159">Kestrel：Libuv 传输标记为已过时</span><span class="sxs-lookup"><span data-stu-id="29095-159">Kestrel: Libuv transport marked as obsolete</span></span>](#kestrel-libuv-transport-marked-as-obsolete)
- [<span data-ttu-id="29095-160">Kestrel：请求尾部标头已移到新集合</span><span class="sxs-lookup"><span data-stu-id="29095-160">Kestrel: Request trailer headers moved to new collection</span></span>](#kestrel-request-trailer-headers-moved-to-new-collection)
- [<span data-ttu-id="29095-161">Kestrel：传输抽象层更改</span><span class="sxs-lookup"><span data-stu-id="29095-161">Kestrel: Transport abstraction layer changes</span></span>](#kestrel-transport-abstractions-removed-and-made-public)
- [<span data-ttu-id="29095-162">本地化：API 已标记为已过时</span><span class="sxs-lookup"><span data-stu-id="29095-162">Localization: APIs marked obsolete</span></span>](#localization-resourcemanagerwithculturestringlocalizer-and-withculture-marked-obsolete)
- [<span data-ttu-id="29095-163">本地化：已删除“Pubternal”API</span><span class="sxs-lookup"><span data-stu-id="29095-163">Localization: "Pubternal" APIs removed</span></span>](#localization-pubternal-apis-removed)
- [<span data-ttu-id="29095-164">本地化：请求本地化中间件中删除了已过时的构造函数</span><span class="sxs-lookup"><span data-stu-id="29095-164">Localization: Obsolete constructor removed in request localization middleware</span></span>](#localization-obsolete-constructor-removed-in-request-localization-middleware)
- [<span data-ttu-id="29095-165">本地化：ResourceManagerWithCultureStringLocalizer 类和 WithCulture 接口成员已删除</span><span class="sxs-lookup"><span data-stu-id="29095-165">Localization: ResourceManagerWithCultureStringLocalizer class and WithCulture interface member removed</span></span>](#localization-resourcemanagerwithculturestringlocalizer-class-and-withculture-interface-member-removed)
- [<span data-ttu-id="29095-166">日志记录：已将 DebugLogger 类设为内部类</span><span class="sxs-lookup"><span data-stu-id="29095-166">Logging: DebugLogger class made internal</span></span>](#logging-debuglogger-class-made-internal)
- [<span data-ttu-id="29095-167">中间件：数据库错误页标记为已过时</span><span class="sxs-lookup"><span data-stu-id="29095-167">Middleware: Database error page marked as obsolete</span></span>](#middleware-database-error-page-marked-as-obsolete)
- [<span data-ttu-id="29095-168">中间件：如果找不到处理程序，则异常处理程序中间件会引发原始异常</span><span class="sxs-lookup"><span data-stu-id="29095-168">Middleware: Exception Handler Middleware throws original exception if handler not found</span></span>](#middleware-exception-handler-middleware-throws-original-exception-if-handler-not-found)
- [<span data-ttu-id="29095-169">MVC：已删除控制器操作 Async 后缀</span><span class="sxs-lookup"><span data-stu-id="29095-169">MVC: Controller action Async suffix removed</span></span>](#mvc-async-suffix-trimmed-from-controller-action-names)
- [<span data-ttu-id="29095-170">MVC：JsonResult 已移至 Microsoft.AspNetCore.Mvc.Core</span><span class="sxs-lookup"><span data-stu-id="29095-170">MVC: JsonResult moved to Microsoft.AspNetCore.Mvc.Core</span></span>](#mvc-jsonresult-moved-to-microsoftaspnetcoremvccore)
- [<span data-ttu-id="29095-171">MVC：ObjectModelValidator 调用 ValidationVisitor.Validate 的新重载</span><span class="sxs-lookup"><span data-stu-id="29095-171">MVC: ObjectModelValidator calls a new overload of ValidationVisitor.Validate</span></span>](#mvc-objectmodelvalidator-calls-a-new-overload-of-validationvisitorvalidate)
- [<span data-ttu-id="29095-172">MVC：已弃用预编译工具</span><span class="sxs-lookup"><span data-stu-id="29095-172">MVC: Precompilation tool deprecated</span></span>](#mvc-precompilation-tool-deprecated)
- [<span data-ttu-id="29095-173">MVC：类型已更改为内部</span><span class="sxs-lookup"><span data-stu-id="29095-173">MVC: Types changed to internal</span></span>](#mvc-pubternal-types-changed-to-internal)
- [<span data-ttu-id="29095-174">MVC：已删除 Web API 兼容性填充码</span><span class="sxs-lookup"><span data-stu-id="29095-174">MVC: Web API compatibility shim removed</span></span>](#mvc-web-api-compatibility-shim-removed)
- [<span data-ttu-id="29095-175">Razor：已删除 RazorTemplateEngine API</span><span class="sxs-lookup"><span data-stu-id="29095-175">Razor: RazorTemplateEngine API removed</span></span>](#razor-razortemplateengine-api-removed)
- [<span data-ttu-id="29095-176">Razor：运行时编译已移到包</span><span class="sxs-lookup"><span data-stu-id="29095-176">Razor: Runtime compilation moved to a package</span></span>](#razor-runtime-compilation-moved-to-a-package)
- [<span data-ttu-id="29095-177">安全性：Cookie 名称编码已删除</span><span class="sxs-lookup"><span data-stu-id="29095-177">Security: Cookie name encoding removed</span></span>](#security-cookie-name-encoding-removed)
- [<span data-ttu-id="29095-178">安全性：IdentityModel NuGet 包版本已更新</span><span class="sxs-lookup"><span data-stu-id="29095-178">Security: IdentityModel NuGet package versions updated</span></span>](#security-identitymodel-nuget-package-versions-updated)
- [<span data-ttu-id="29095-179">会话状态：已删除过时的 API</span><span class="sxs-lookup"><span data-stu-id="29095-179">Session state: Obsolete APIs removed</span></span>](#session-state-obsolete-apis-removed)
- [<span data-ttu-id="29095-180">共享框架：已从 Microsoft.AspNetCore.App 中删除程序集</span><span class="sxs-lookup"><span data-stu-id="29095-180">Shared framework: Assembly removal from Microsoft.AspNetCore.App</span></span>](#shared-framework-assemblies-removed-from-microsoftaspnetcoreapp)
- [<span data-ttu-id="29095-181">共享框架：已删除 Microsoft.AspNetCore.All</span><span class="sxs-lookup"><span data-stu-id="29095-181">Shared framework: Microsoft.AspNetCore.All removed</span></span>](#shared-framework-removed-microsoftaspnetcoreall)
- [<span data-ttu-id="29095-182">SignalR：已替换 HandshakeProtocol.SuccessHandshakeData</span><span class="sxs-lookup"><span data-stu-id="29095-182">SignalR: HandshakeProtocol.SuccessHandshakeData replaced</span></span>](#signalr-handshakeprotocolsuccesshandshakedata-replaced)
- [<span data-ttu-id="29095-183">SignalR：已删除 HubConnection 方法</span><span class="sxs-lookup"><span data-stu-id="29095-183">SignalR: HubConnection methods removed</span></span>](#signalr-hubconnection-resetsendping-and-resettimeout-methods-removed)
- [<span data-ttu-id="29095-184">SignalR：已更改 HubConnectionContext 构造函数</span><span class="sxs-lookup"><span data-stu-id="29095-184">SignalR: HubConnectionContext constructors changed</span></span>](#signalr-hubconnectioncontext-constructors-changed)
- [<span data-ttu-id="29095-185">SignalR：JavaScript 客户端包名称更改</span><span class="sxs-lookup"><span data-stu-id="29095-185">SignalR: JavaScript client package name change</span></span>](#signalr-javascript-client-package-name-changed)
- [<span data-ttu-id="29095-186">SignalR：MessagePack 中心协议已移至 MessagePack 2.x 包</span><span class="sxs-lookup"><span data-stu-id="29095-186">SignalR: MessagePack Hub Protocol moved to MessagePack 2.x package</span></span>](#signalr-messagepack-hub-protocol-moved-to-messagepack-2x-package)
- [<span data-ttu-id="29095-187">SignalR：MessagePack 中心协议选项类型已更改</span><span class="sxs-lookup"><span data-stu-id="29095-187">SignalR: MessagePack Hub Protocol options type changed</span></span>](#signalr-messagepack-hub-protocol-options-type-changed)
- [<span data-ttu-id="29095-188">SignalR：过时的 API</span><span class="sxs-lookup"><span data-stu-id="29095-188">SignalR: Obsolete APIs</span></span>](#signalr-usesignalr-and-useconnections-methods-marked-obsolete)
- [<span data-ttu-id="29095-189">SignalR：UseSignalR 和 UseConnections 方法已删除</span><span class="sxs-lookup"><span data-stu-id="29095-189">SignalR: UseSignalR and UseConnections methods removed</span></span>](#signalr-usesignalr-and-useconnections-methods-removed)
- [<span data-ttu-id="29095-190">SPA：SpaServices 和 NodeServices 控制台记录器回退默认更改</span><span class="sxs-lookup"><span data-stu-id="29095-190">SPAs: SpaServices and NodeServices console logger fallback default change</span></span>](#spas-spaservices-and-nodeservices-no-longer-fall-back-to-console-logger)
- [<span data-ttu-id="29095-191">SPA：SpaServices 和 NodeServices 已标记为过时</span><span class="sxs-lookup"><span data-stu-id="29095-191">SPAs: SpaServices and NodeServices marked obsolete</span></span>](#spas-spaservices-and-nodeservices-marked-obsolete)
- [<span data-ttu-id="29095-192">静态文件：CSV 内容类型已更改为符合标准</span><span class="sxs-lookup"><span data-stu-id="29095-192">Static files: CSV content type changed to standards-compliant</span></span>](#static-files-csv-content-type-changed-to-standards-compliant)
- [<span data-ttu-id="29095-193">Blazor WebAssembly 不支持的 System.Security.Cryptography API</span><span class="sxs-lookup"><span data-stu-id="29095-193">System.Security.Cryptography APIs not supported on Blazor WebAssembly</span></span>](#systemsecuritycryptography-apis-not-supported-on-blazor-webassembly)
- [<span data-ttu-id="29095-194">目标框架：不支持 .NET Framework</span><span class="sxs-lookup"><span data-stu-id="29095-194">Target framework: .NET Framework not supported</span></span>](#target-framework-net-framework-support-dropped)

## <a name="aspnet-core-50"></a><span data-ttu-id="29095-195">ASP.NET Core 5.0</span><span class="sxs-lookup"><span data-stu-id="29095-195">ASP.NET Core 5.0</span></span>

[!INCLUDE[Authentication: AzureAD.UI and AzureADB2C.UI APIs and packages marked obsolete](~/includes/core-changes/aspnetcore/5.0/authentication-aad-packages-obsolete.md)]

***

[!INCLUDE[Authorization: Resource in endpoint routing is HttpContext](~/includes/core-changes/aspnetcore/5.0/authorization-resource-in-endpoint-routing.md)]

<span data-ttu-id="29095-196">\*\*_</span><span class="sxs-lookup"><span data-stu-id="29095-196">\*\*_</span></span>

[!INCLUDE[Azure: Microsoft-prefixed Azure integration packages removed](~/includes/core-changes/aspnetcore/5.0/azure-integration-packages-removed.md)]

_*_

[!INCLUDE[Serialization: BinaryFormatter serialization obsolete](~/includes/core-changes/corefx/5.0/binaryformatter-serialization-obsolete.md)]

_*_

[!INCLUDE[Blazor: Insignificant whitespace trimmed from components at compile time](~/includes/core-changes/aspnetcore/5.0/blazor-components-trim-insignificant-whitespace.md)]

_*_

[!INCLUDE[Blazor: JSObjectReference and JSInProcessObjectReference types changed to internal](~/includes/core-changes/aspnetcore/5.0/blazor-jsobjectreference-to-internal.md)]

_*_

[!INCLUDE[Blazor: ProtectedBrowserStorage feature moved to shared framework](~/includes/core-changes/aspnetcore/5.0/blazor-protectedbrowserstorage-moved.md)]

_*_

[!INCLUDE[Blazor: RenderTreeFrame readonly public fields have become properties](~/includes/core-changes/aspnetcore/5.0/blazor-rendertreeframe-fields-become-properties.md)]

_*_

[!INCLUDE[Blazor: Target framework of NuGet packages changed](~/includes/core-changes/aspnetcore/5.0/blazor-packages-target-framework-changed.md)]

_*_

[!INCLUDE[Blazor: Updated browser support](~/includes/core-changes/aspnetcore/5.0/blazor-browser-support-updated.md)]

_*_

[!INCLUDE[Blazor: Static web assets validation logic updated](~/includes/core-changes/aspnetcore/5.0/blazor-static-web-assets-validation-logic-updated.md)]

_*_

[!INCLUDE[Extensions: Package reference changes](~/includes/core-changes/aspnetcore/5.0/extensions-package-reference-changes.md)]

_*_

[!INCLUDE[HTTP: HttpClient instances created by IHttpClientFactory log integer status codes](~/includes/core-changes/aspnetcore/5.0/http-httpclient-instances-log-integer-status-codes.md)]

_*_

[!INCLUDE[HTTP: Kestrel and IIS BadHttpRequestException types marked obsolete and replaced](~/includes/core-changes/aspnetcore/5.0/http-badhttprequestexception-obsolete.md)]

_*_

[!INCLUDE[HttpSys: Client certificate renegotiation disabled by default](~/includes/core-changes/aspnetcore/5.0/httpsys-client-certificate-renegotiation-disabled-by-default.md)]

_*_

[!INCLUDE[IIS: UrlRewrite middleware query strings are preserved](~/includes/core-changes/aspnetcore/5.0/iis-urlrewrite-middleware-query-strings-are-preserved.md)]

_*_

[!INCLUDE[Kestrel: Configuration changes at run time detected by default](~/includes/core-changes/aspnetcore/5.0/kestrel-configuration-changes-at-run-time-detected-by-default.md)]

_*_
[!INCLUDE[Kestrel: Default supported TLS protocol versions changed](~/includes/core-changes/aspnetcore/5.0/kestrel-default-supported-tls-protocol-versions-changed.md)]

_*_

[!INCLUDE[Kestrel: HTTP/2 disabled over TLS on incompatible Windows versions](~/includes/core-changes/aspnetcore/5.0/kestrel-disables-http2-over-tls.md)]

_*_

[!INCLUDE[Kestrel: Libuv transport marked as obsolete](~/includes/core-changes/aspnetcore/5.0/kestrel-libuv-transport-obsolete.md)]

_*_

[!INCLUDE[Localization: "Pubternal" APIs removed](~/includes/core-changes/aspnetcore/5.0/localization-pubternal-apis-removed.md)]

_*_

[!INCLUDE[Localization: Obsolete constructor removed in request localization middleware](~/includes/core-changes/aspnetcore/5.0/localization-requestlocalizationmiddleware-constructor-removed.md)]

_*_

[!INCLUDE[Localization: ResourceManagerWithCultureStringLocalizer class and WithCulture interface member removed](~/includes/core-changes/aspnetcore/5.0/localization-members-removed.md)]

_*_

[!INCLUDE[Middleware: Database error page marked as obsolete](~/includes/core-changes/aspnetcore/5.0/middleware-database-error-page-obsolete.md)]

_*_

[!INCLUDE[Middleware: Exception Handler Middleware throws original exception if handler not found](~/includes/core-changes/aspnetcore/5.0/middleware-exception-handler-throws-original-exception.md)]

_*_

[!INCLUDE[MVC: ObjectModelValidator calls a new overload of ValidationVisitor.Validate](~/includes/core-changes/aspnetcore/5.0/mvc-objectmodelvalidator-calls-new-overload.md)]

_*_

[!INCLUDE[Security: Cookie name encoding removed](~/includes/core-changes/aspnetcore/5.0/security-cookie-name-encoding-removed.md)]

_*_

[!INCLUDE[Security: IdentityModel NuGet package versions updated](~/includes/core-changes/aspnetcore/5.0/security-identitymodel-nuget-package-versions-updated.md)]

_*_

[!INCLUDE[SignalR: MessagePack Hub Protocol moved to MessagePack 2.x package](~/includes/core-changes/aspnetcore/5.0/signalr-messagepack-package.md)]

_*_

[!INCLUDE[SignalR: MessagePack Hub Protocol options type changed](~/includes/core-changes/aspnetcore/5.0/signalr-messagepack-hub-protocol-options-changed.md)]

_*_

[!INCLUDE[SignalR: UseSignalR and UseConnections methods removed](~/includes/core-changes/aspnetcore/5.0/signalr-usesignalr-useconnections-removed.md)]

_*_

[!INCLUDE[Cryptography APIs not supported on Blazor WebAssembly](~/includes/core-changes/cryptography/5.0/cryptography-apis-not-supported-on-blazor-webassembly.md)]

_*_

[!INCLUDE[Static files: CSV content type changed to standards-compliant](~/includes/core-changes/aspnetcore/5.0/static-files-csv-content-type-changed.md)]

_*_

## <a name="aspnet-core-31"></a><span data-ttu-id="29095-197">ASP.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="29095-197">ASP.NET Core 3.1</span></span>

[!INCLUDE[HTTP: Browser SameSite changes impact authentication](~/includes/core-changes/aspnetcore/3.1/http-cookie-samesite-authn-impacts.md)]

_*_

## <a name="aspnet-core-30"></a><span data-ttu-id="29095-198">ASP.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="29095-198">ASP.NET Core 3.0</span></span>

[!INCLUDE[Obsolete Antiforgery, CORS, Diagnostics, MVC, and Routing APIs removed](~/includes/core-changes/aspnetcore/3.0/obsolete-apis-removed.md)]

_*_

[!INCLUDE[Authentication: Google+ deprecation](~/includes/core-changes/aspnetcore/3.0/authn-google-plus-authn-changes.md)]

_*_

[!INCLUDE[Authentication: HttpContext.Authentication property removed](~/includes/core-changes/aspnetcore/3.0/authn-httpcontext-property-removed.md)]

_*_

[!INCLUDE[Authentication: Newtonsoft.Json types replaced](~/includes/core-changes/aspnetcore/3.0/authn-apis-json-types.md)]

_*_

[!INCLUDE[Authentication: OAuthHandler ExchangeCodeAsync signature changed](~/includes/core-changes/aspnetcore/3.0/authn-exchangecodeasync-signature-change.md)]

_*_

[!INCLUDE[Authorization: AddAuthorization overload assembly change](~/includes/core-changes/aspnetcore/3.0/authz-assembly-change.md)]

_*_

[!INCLUDE[Authorization: IAllowAnonymous removed from AuthorizationFilterContext.Filters](~/includes/core-changes/aspnetcore/3.0/authz-iallowanonymous-removed-from-collection.md)]

_*_

[!INCLUDE[Authorization: IAuthorizationPolicyProvider implementations require new method](~/includes/core-changes/aspnetcore/3.0/authz-iauthzpolicyprovider-new-method.md)]

_*_

[!INCLUDE[Caching: CompactOnMemoryPressure property removed](~/includes/core-changes/aspnetcore/3.0/caching-memory-property-removed.md)]

_*_

[!INCLUDE[Caching: Microsoft.Extensions.Caching.SqlServer uses new SqlClient package](~/includes/core-changes/aspnetcore/3.0/caching-new-sqlclient-package.md)]

_*_

[!INCLUDE[Caching: ResponseCaching types changed to internal](~/includes/core-changes/aspnetcore/3.0/caching-response-pubternal-to-internal.md)]

_*_

[!INCLUDE[Data Protection: DataProtection.AzureStorage uses new Azure Storage APIs](~/includes/core-changes/aspnetcore/3.0/dataprotection-azstorage-using-azstorage-apis.md)]

_*_

[!INCLUDE[Hosting: ANCM version 1 removed from hosting bundle](~/includes/core-changes/aspnetcore/3.0/hosting-ancmv1-hosting-bundle-removal.md)]

_*_

[!INCLUDE[Hosting: Generic host restriction on Startup constructor injection](~/includes/core-changes/aspnetcore/3.0/hosting-generic-host-startup-ctor-restriction.md)]

_*_

[!INCLUDE[Hosting: HTTPS redirection enabled for IIS OutOfProcess](~/includes/core-changes/aspnetcore/3.0/hosting-https-redirection-iis-outofprocess.md)]

_*_

[!INCLUDE[Hosting: IHostingEnvironment and IApplicationLifetime types replaced](~/includes/core-changes/aspnetcore/3.0/hosting-ihostingenv-iapplifetime-types-replaced.md)]

_*_

[!INCLUDE[Hosting: ObjectPoolProvider removed from WebHostBuilder dependencies](~/includes/core-changes/aspnetcore/3.0/hosting-objectpoolprovider-webhostbuilder-dependencies.md)]

_*_

[!INCLUDE[HTTP: DefaultHttpContext extensibility removed](~/includes/core-changes/aspnetcore/3.0/http-defaulthttpcontext-extensibility-removed.md)]

_*_

[!INCLUDE[HTTP: HeaderNames fields changed to static readonly](~/includes/core-changes/aspnetcore/3.0/http-headernames-constants-staticreadonly.md)]

_*_

[!INCLUDE[HTTP: Response body infrastructure changes](~/includes/core-changes/aspnetcore/3.0/http-response-body-changes.md)]

_*_

[!INCLUDE[HTTP: Some cookie SameSite default values changed](~/includes/core-changes/aspnetcore/3.0/http-cookie-samesite-defaults-change.md)]

_*_

[!INCLUDE[HTTP: Synchronous IO disabled by default](~/includes/core-changes/aspnetcore/3.0/http-synchronous-io-disabled.md)]

_*_

[!INCLUDE[Identity: AddDefaultUI method overload removed](~/includes/core-changes/aspnetcore/3.0/identity-ui-adddefaultui-overload-removed.md)]

_*_

[!INCLUDE[Identity: UI Bootstrap version change](~/includes/core-changes/aspnetcore/3.0/identity-ui-bootstrap-version.md)]

_*_

[!INCLUDE[Identity: SignInAsync throws exception for unauthenticated identity](~/includes/core-changes/aspnetcore/3.0/identity-signinasync-throws-exception.md)]

_*_

[!INCLUDE[Identity: SignInManager constructor accepts new parameter](~/includes/core-changes/aspnetcore/3.0/identity-signinmanager-ctor-parameter.md)]

_*_

[!INCLUDE[Identity: UI uses static web assets feature](~/includes/core-changes/aspnetcore/3.0/identity-ui-static-web-assets.md)]

_*_

[!INCLUDE[Kestrel: Connection adapters removed](~/includes/core-changes/aspnetcore/3.0/kestrel-connection-adapters-removed.md)]

_*_

[!INCLUDE[Kestrel: Empty HTTPS assembly removed](~/includes/core-changes/aspnetcore/3.0/kestrel-empty-assembly-removed.md)]

_*_

[!INCLUDE[Kestrel: Request trailer headers moved to new collection](~/includes/core-changes/aspnetcore/3.0/kestrel-request-trailer-headers.md)]

_*_

[!INCLUDE[Kestrel: Transport abstraction layer changes](~/includes/core-changes/aspnetcore/3.0/kestrel-transport-abstractions.md)]

_*_

[!INCLUDE[Localization: APIs marked obsolete](~/includes/core-changes/aspnetcore/3.0/localization-apis-marked-obsolete.md)]

_*_

[!INCLUDE[Logging: DebugLogger class made internal](~/includes/core-changes/aspnetcore/3.0/logging-debuglogger-to-internal.md)]

_*_

[!INCLUDE[MVC: Controller action Async suffix removed](~/includes/core-changes/aspnetcore/3.0/mvc-action-async-suffix-trimmed.md)]

_*_

[!INCLUDE[MVC: JsonResult moved to Microsoft.AspNetCore.Mvc.Core](~/includes/core-changes/aspnetcore/3.0/mvc-jsonresult-moved.md)]

_*_

[!INCLUDE[MVC: Precompilation tool deprecated](~/includes/core-changes/aspnetcore/3.0/mvc-precompilation-tool-deprecated.md)]

_*_

[!INCLUDE[MVC: Types changed to internal](~/includes/core-changes/aspnetcore/3.0/mvc-pubternal-to-internal.md)]

_*_

[!INCLUDE[MVC: Web API compatibility shim removed](~/includes/core-changes/aspnetcore/3.0/mvc-webapi-compat-shim-removed.md)]

_*_

[!INCLUDE[Razor: RazorTemplatEengine API removed](~/includes/core-changes/aspnetcore/3.0/razor-razortemplateengine-api-removed.md)]

_*_

[!INCLUDE[Razor: Runtime compilation moved to a package](~/includes/core-changes/aspnetcore/3.0/razor-runtime-compilation-package.md)]

_*_

[!INCLUDE[Session state: Obsolete APIs removed](~/includes/core-changes/aspnetcore/3.0/session-obsolete-apis-removed.md)]

_*_

[!INCLUDE[Shared framework: Assembly removal from Microsoft.AspNetCore.App](~/includes/core-changes/aspnetcore/3.0/sharedfx-app-shared-framework-assemblies.md)]

_*_

[!INCLUDE[Shared framework: Microsoft.AspNetCore.All removed](~/includes/core-changes/aspnetcore/3.0/sharedfx-all-framework-removed.md)]

_*_

[!INCLUDE[SignalR: HandshakeProtocol.SuccessHandshakeData replaced](~/includes/core-changes/aspnetcore/3.0/signalr-successhandshakedata-replaced.md)]

_*_

[!INCLUDE[SignalR: HubConnection methods removed](~/includes/core-changes/aspnetcore/3.0/signalr-hubconnection-methods-removed.md)]

_*_

[!INCLUDE[SignalR: HubConnectionContext constructors changed](~/includes/core-changes/aspnetcore/3.0/signalr-hubconnectioncontext-ctors.md)]

_*_

[!INCLUDE[SignalR: JavaScript client package name change](~/includes/core-changes/aspnetcore/3.0/signalr-js-client-package-name.md)]

_*_

[!INCLUDE[SignalR: Obsolete APIs](~/includes/core-changes/aspnetcore/3.0/signalr-obsolete-apis.md)]

_*_

[!INCLUDE[SPAs: SpaServices and NodeServices marked obsolete](~/includes/core-changes/aspnetcore/3.0/spas-spaservices-nodeservices-obsolete.md)]

_*_

[!INCLUDE[SPAs: SpaServices and NodeServices console logger fallback default change](~/includes/core-changes/aspnetcore/3.0/spas-spaservices-nodeservices-fallback.md)]

_*_

[!INCLUDE[Target framework: .NET Framework not supported](~/includes/core-changes/aspnetcore/3.0/targetfx-netfx-tfm-support.md)]

<span data-ttu-id="29095-199">_\*\*</span><span class="sxs-lookup"><span data-stu-id="29095-199">_\*\*</span></span>
