---
title: 在 Windows 上安装 .NET
description: 了解可在其上安装 .NET 的 Windows 版本。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: 786814549724948fa69b18a05cee966e0940aaf4
ms.sourcegitcommit: c6de55556add9f92af17e0f8d1da8f356a19a03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2020
ms.locfileid: "96549340"
---
# <a name="install-net-on-windows"></a><span data-ttu-id="97752-103">在 Windows 上安装 .NET</span><span class="sxs-lookup"><span data-stu-id="97752-103">Install .NET on Windows</span></span>

> [!div class="op_single_selector"]
>
> - [在 Windows 上安装](windows.md)
> - [在 macOS 上安装](macos.md)
> - [在 Linux 上安装](linux.md)

<span data-ttu-id="97752-107">本文介绍如何在 Windows 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="97752-107">In this article, you'll learn how to install .NET on Windows.</span></span> <span data-ttu-id="97752-108">.NET 由运行时和 SDK 组成。</span><span class="sxs-lookup"><span data-stu-id="97752-108">.NET is made up of the runtime and the SDK.</span></span> <span data-ttu-id="97752-109">运行时用于运行 .NET 应用，应用可能包含也可能不包含它。</span><span class="sxs-lookup"><span data-stu-id="97752-109">The runtime is used to run a .NET app and may or may not be included with the app.</span></span> <span data-ttu-id="97752-110">SDK 用于创建 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="97752-110">The SDK is used to create .NET apps and libraries.</span></span> <span data-ttu-id="97752-111">.NET 运行时始终随 SDK 一起安装。</span><span class="sxs-lookup"><span data-stu-id="97752-111">The .NET runtime is always installed with the SDK.</span></span>

<span data-ttu-id="97752-112">最新版本的 .NET 是 5.0。</span><span class="sxs-lookup"><span data-stu-id="97752-112">The latest version of .NET is 5.0.</span></span>

> [!div class="button"]
> [<span data-ttu-id="97752-113">下载 .NET</span><span class="sxs-lookup"><span data-stu-id="97752-113">Download .NET</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="supported-releases"></a><span data-ttu-id="97752-114">支持的版本</span><span class="sxs-lookup"><span data-stu-id="97752-114">Supported releases</span></span>

<span data-ttu-id="97752-115">下表列出了当前支持的 .NET 版本以及支持它们的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="97752-115">The following table is a list of currently supported .NET releases and the versions of Windows they're supported on.</span></span> <span data-ttu-id="97752-116">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Windows 版本达到生命周期](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="97752-116">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Windows reaches end-of-life](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

<span data-ttu-id="97752-117">Windows 10 版本终止服务日期按版本分段。</span><span class="sxs-lookup"><span data-stu-id="97752-117">Windows 10 versions end-of-service dates are segmented by edition.</span></span> <span data-ttu-id="97752-118">下表中仅考虑家庭版、专业版、专业教育版和专业工作站版。   </span><span class="sxs-lookup"><span data-stu-id="97752-118">Only **Home**, **Pro**, **Pro Education**, and **Pro for Workstations** editions are considered in the following table.</span></span> <span data-ttu-id="97752-119">查看 [Windows 生命周期事实表单](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)，了解具体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="97752-119">Check the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet) for specific details.</span></span>

> [!TIP]
> <span data-ttu-id="97752-120">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-120">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="97752-121">操作系统</span><span class="sxs-lookup"><span data-stu-id="97752-121">Operating System</span></span>            | <span data-ttu-id="97752-122">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="97752-122">.NET Core 2.1</span></span> | <span data-ttu-id="97752-123">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="97752-123">.NET Core 3.1</span></span> | <span data-ttu-id="97752-124">.NET 5</span><span class="sxs-lookup"><span data-stu-id="97752-124">.NET 5</span></span> |
|-----------------------------|---------------|---------------|--------|
| <span data-ttu-id="97752-125">Windows 10 版本 2004</span><span class="sxs-lookup"><span data-stu-id="97752-125">Windows 10, Version 2004</span></span>    | <span data-ttu-id="97752-126">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-126">✔️</span></span>           | <span data-ttu-id="97752-127">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-127">✔️</span></span>            | <span data-ttu-id="97752-128">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-128">✔️</span></span>    |
| <span data-ttu-id="97752-129">Windows 10 版本 1909</span><span class="sxs-lookup"><span data-stu-id="97752-129">Windows 10, Version 1909</span></span>    | <span data-ttu-id="97752-130">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-130">✔️</span></span>           | <span data-ttu-id="97752-131">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-131">✔️</span></span>            | <span data-ttu-id="97752-132">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-132">✔️</span></span>    |
| <span data-ttu-id="97752-133">Windows 10 版本 1903</span><span class="sxs-lookup"><span data-stu-id="97752-133">Windows 10, Version 1903</span></span>    | <span data-ttu-id="97752-134">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-134">✔️</span></span>           | <span data-ttu-id="97752-135">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-135">✔️</span></span>            | <span data-ttu-id="97752-136">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-136">✔️</span></span>    |
| <span data-ttu-id="97752-137">Windows 10 版本 1809</span><span class="sxs-lookup"><span data-stu-id="97752-137">Windows 10, Version 1809</span></span>    | <span data-ttu-id="97752-138">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-138">✔️</span></span>           | <span data-ttu-id="97752-139">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-139">✔️</span></span>            | <span data-ttu-id="97752-140">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-140">✔️</span></span>    |
| <span data-ttu-id="97752-141"> Windows 10 版本 1803</span><span class="sxs-lookup"><span data-stu-id="97752-141">Windows 10, Version 1803</span></span>    | <span data-ttu-id="97752-142">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-142">✔️</span></span>           | <span data-ttu-id="97752-143">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-143">✔️</span></span>            | <span data-ttu-id="97752-144">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-144">✔️</span></span>    |
| <span data-ttu-id="97752-145"> Windows 10 版本 1709</span><span class="sxs-lookup"><span data-stu-id="97752-145">Windows 10, Version 1709</span></span>    | <span data-ttu-id="97752-146">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-146">✔️</span></span>           | <span data-ttu-id="97752-147">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-147">✔️</span></span>            | <span data-ttu-id="97752-148">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-148">✔️</span></span>    |
| <span data-ttu-id="97752-149">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="97752-149">Windows 10, Version 1607</span></span>    | <span data-ttu-id="97752-150">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-150">✔️</span></span>           | <span data-ttu-id="97752-151">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-151">✔️</span></span>            | <span data-ttu-id="97752-152">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-152">✔️</span></span>    |
| <span data-ttu-id="97752-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="97752-153">Windows 8.1</span></span>                 | <span data-ttu-id="97752-154">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-154">✔️</span></span>           | <span data-ttu-id="97752-155">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-155">✔️</span></span>            | <span data-ttu-id="97752-156">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-156">✔️</span></span>    |
| <span data-ttu-id="97752-157">Windows 7 SP1 [ESU][esu]</span><span class="sxs-lookup"><span data-stu-id="97752-157">Windows 7 SP1 [ESU][esu]</span></span>    | <span data-ttu-id="97752-158">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-158">✔️</span></span>           | <span data-ttu-id="97752-159">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-159">✔️</span></span>            | <span data-ttu-id="97752-160">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-160">✔️</span></span>    |
| <span data-ttu-id="97752-161">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="97752-161">Windows 10, Version 1607</span></span>    | <span data-ttu-id="97752-162">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-162">✔️</span></span>           | <span data-ttu-id="97752-163">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-163">✔️</span></span>            | <span data-ttu-id="97752-164">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-164">✔️</span></span>    |
| <span data-ttu-id="97752-165">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="97752-165">Windows 10, Version 1607</span></span>    | <span data-ttu-id="97752-166">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-166">✔️</span></span>           | <span data-ttu-id="97752-167">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-167">✔️</span></span>            | <span data-ttu-id="97752-168">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-168">✔️</span></span>    |
| <span data-ttu-id="97752-169">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97752-169">Windows Server 2012 R2</span></span>      | <span data-ttu-id="97752-170">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-170">✔️</span></span>           | <span data-ttu-id="97752-171">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-171">✔️</span></span>            | <span data-ttu-id="97752-172">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-172">✔️</span></span>    |
| <span data-ttu-id="97752-173">Windows Server Core 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97752-173">Windows Server Core 2012 R2</span></span> | <span data-ttu-id="97752-174">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-174">✔️</span></span>           | <span data-ttu-id="97752-175">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-175">✔️</span></span>            | <span data-ttu-id="97752-176">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-176">✔️</span></span>    |
| <span data-ttu-id="97752-177">Nano Server 版本 1809+</span><span class="sxs-lookup"><span data-stu-id="97752-177">Nano Server, Version 1809+</span></span>  | <span data-ttu-id="97752-178">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-178">✔️</span></span>           | <span data-ttu-id="97752-179">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-179">✔️</span></span>            | <span data-ttu-id="97752-180">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-180">✔️</span></span>    |
| <span data-ttu-id="97752-181">Nano Server 版本 1803</span><span class="sxs-lookup"><span data-stu-id="97752-181">Nano Server, Version 1803</span></span>   | <span data-ttu-id="97752-182">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-182">✔️</span></span>           | <span data-ttu-id="97752-183">✔️</span><span class="sxs-lookup"><span data-stu-id="97752-183">✔️</span></span>            | ❌    |

## <a name="unsupported-releases"></a><span data-ttu-id="97752-184">不支持的版本</span><span class="sxs-lookup"><span data-stu-id="97752-184">Unsupported releases</span></span>

<span data-ttu-id="97752-185">以下 .NET 版本 ❌ 不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="97752-185">The following versions of .NET are ❌ no longer supported.</span></span> <span data-ttu-id="97752-186">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="97752-186">The downloads for these still remain published:</span></span>

- <span data-ttu-id="97752-187">3.0</span><span class="sxs-lookup"><span data-stu-id="97752-187">3.0</span></span>
- <span data-ttu-id="97752-188">2.2</span><span class="sxs-lookup"><span data-stu-id="97752-188">2.2</span></span>
- <span data-ttu-id="97752-189">2.0</span><span class="sxs-lookup"><span data-stu-id="97752-189">2.0</span></span>

## <a name="runtime-information"></a><span data-ttu-id="97752-190">运行时信息</span><span class="sxs-lookup"><span data-stu-id="97752-190">Runtime information</span></span>

<span data-ttu-id="97752-191">运行时用于运行使用 .NET 创建的应用。</span><span class="sxs-lookup"><span data-stu-id="97752-191">The runtime is used to run apps created with .NET.</span></span> <span data-ttu-id="97752-192">应用作者发布应用时，可以在其应用中包含运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-192">When an app author publishes an app, they can include the runtime with their app.</span></span> <span data-ttu-id="97752-193">如果作者未包含运行时，则由用户安装运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-193">If they don't include the runtime, it's up to the user to install the runtime.</span></span>

<span data-ttu-id="97752-194">可以在 Windows 上安装三个不同的运行时：</span><span class="sxs-lookup"><span data-stu-id="97752-194">There are three different runtimes you can install on Windows:</span></span>

<span data-ttu-id="97752-195">*ASP.NET Core 运行时*</span><span class="sxs-lookup"><span data-stu-id="97752-195">*ASP.NET Core runtime*</span></span>\
<span data-ttu-id="97752-196">运行 ASP.NET Core 应用。</span><span class="sxs-lookup"><span data-stu-id="97752-196">Runs ASP.NET Core apps.</span></span> <span data-ttu-id="97752-197">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-197">Includes the .NET runtime.</span></span>

<span data-ttu-id="97752-198">*桌面运行时*</span><span class="sxs-lookup"><span data-stu-id="97752-198">*Desktop runtime*</span></span>\
<span data-ttu-id="97752-199">运行适用于 Windows 的 .NET WPF 和 Windows 窗体桌面应用。</span><span class="sxs-lookup"><span data-stu-id="97752-199">Runs .NET WPF and Windows Forms desktop apps for Windows.</span></span> <span data-ttu-id="97752-200">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-200">Includes the .NET runtime.</span></span>

<span data-ttu-id="97752-201">.NET 运行时</span><span class="sxs-lookup"><span data-stu-id="97752-201">*.NET runtime*</span></span>\
<span data-ttu-id="97752-202">此运行时是最简单的运行时，不包括任何其他运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-202">This runtime is the simplest runtime and doesn't include any other runtime.</span></span> <span data-ttu-id="97752-203">强烈建议同时安装 ASP.NET Core 运行时和桌面运行时，以最大限度地提升与 .NET 应用的兼容性 。</span><span class="sxs-lookup"><span data-stu-id="97752-203">It's highly recommended that you install both *ASP.NET Core runtime* and *Desktop runtime* for the best compatibility with .NET apps.</span></span>

> [!div class="button"]
> [<span data-ttu-id="97752-204">下载 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="97752-204">Download .NET Runtime</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="sdk-information"></a><span data-ttu-id="97752-205">SDK 信息</span><span class="sxs-lookup"><span data-stu-id="97752-205">SDK information</span></span>

<span data-ttu-id="97752-206">SDK 用于生成和发布 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="97752-206">The SDK is used to build and publish .NET apps and libraries.</span></span> <span data-ttu-id="97752-207">安装 SDK 会包含三个[运行时](#runtime-information)：ASP.NET Core、桌面和 .NET。</span><span class="sxs-lookup"><span data-stu-id="97752-207">Installing the SDK includes all three [runtimes](#runtime-information): ASP.NET Core, Desktop, and .NET.</span></span>

## <a name="dependencies"></a><span data-ttu-id="97752-208">依赖项</span><span class="sxs-lookup"><span data-stu-id="97752-208">Dependencies</span></span>

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD024 -->

# <a name="net-50"></a>[<span data-ttu-id="97752-209">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="97752-209">.NET 5.0</span></span>](#tab/net50)

<span data-ttu-id="97752-210">.NET 5.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="97752-210">The following Windows versions are supported with .NET 5.0:</span></span>

> [!NOTE]
> <span data-ttu-id="97752-211">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-211">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="97752-212">(OS)</span><span class="sxs-lookup"><span data-stu-id="97752-212">OS</span></span>                  | <span data-ttu-id="97752-213">Version</span><span class="sxs-lookup"><span data-stu-id="97752-213">Version</span></span>       | <span data-ttu-id="97752-214">体系结构</span><span class="sxs-lookup"><span data-stu-id="97752-214">Architectures</span></span>   |
|---------------------|---------------|-----------------|
| <span data-ttu-id="97752-215">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-215">Windows 10 Client</span></span>   | <span data-ttu-id="97752-216">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="97752-216">Version 1607+</span></span> | <span data-ttu-id="97752-217">x64、x86、ARM64</span><span class="sxs-lookup"><span data-stu-id="97752-217">x64, x86, ARM64</span></span> |
| <span data-ttu-id="97752-218">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-218">Windows Client</span></span>      | <span data-ttu-id="97752-219">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="97752-219">7 SP1+, 8.1</span></span>   | <span data-ttu-id="97752-220">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-220">x64, x86</span></span>        |
| <span data-ttu-id="97752-221">Windows Server</span><span class="sxs-lookup"><span data-stu-id="97752-221">Windows Server</span></span>      | <span data-ttu-id="97752-222">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="97752-222">2012 R2+</span></span>      | <span data-ttu-id="97752-223">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-223">x64, x86</span></span>        |
| <span data-ttu-id="97752-224">Windows Server 核心</span><span class="sxs-lookup"><span data-stu-id="97752-224">Windows Server Core</span></span> | <span data-ttu-id="97752-225">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="97752-225">2012 R2+</span></span>      | <span data-ttu-id="97752-226">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-226">x64, x86</span></span>        |
| <span data-ttu-id="97752-227">Nano Server</span><span class="sxs-lookup"><span data-stu-id="97752-227">Nano Server</span></span>         | <span data-ttu-id="97752-228">版本 1809+</span><span class="sxs-lookup"><span data-stu-id="97752-228">Version 1809+</span></span> | <span data-ttu-id="97752-229">X64</span><span class="sxs-lookup"><span data-stu-id="97752-229">x64</span></span>             |

<span data-ttu-id="97752-230">有关 .NET 5.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET 5.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-230">For more information about .NET 5.0 supported operating systems, distributions, and lifecycle policy, see [.NET 5.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md).</span></span>

# <a name="net-core-31"></a>[<span data-ttu-id="97752-231">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="97752-231">.NET Core 3.1</span></span>](#tab/netcore31)

<span data-ttu-id="97752-232">.NET Core 3.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="97752-232">The following Windows versions are supported with .NET Core 3.1:</span></span>

> [!NOTE]
> <span data-ttu-id="97752-233">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-233">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="97752-234">(OS)</span><span class="sxs-lookup"><span data-stu-id="97752-234">OS</span></span>                            | <span data-ttu-id="97752-235">Version</span><span class="sxs-lookup"><span data-stu-id="97752-235">Version</span></span>                        | <span data-ttu-id="97752-236">体系结构</span><span class="sxs-lookup"><span data-stu-id="97752-236">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="97752-237">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-237">Windows Client</span></span>                | <span data-ttu-id="97752-238">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="97752-238">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="97752-239">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-239">x64, x86</span></span>        |
| <span data-ttu-id="97752-240">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-240">Windows 10 Client</span></span>             | <span data-ttu-id="97752-241">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="97752-241">Version 1607+</span></span>                  | <span data-ttu-id="97752-242">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-242">x64, x86</span></span>        |
| <span data-ttu-id="97752-243">Windows Server</span><span class="sxs-lookup"><span data-stu-id="97752-243">Windows Server</span></span>                | <span data-ttu-id="97752-244">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="97752-244">2012 R2+</span></span>                       | <span data-ttu-id="97752-245">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-245">x64, x86</span></span>        |
| <span data-ttu-id="97752-246">Nano Server</span><span class="sxs-lookup"><span data-stu-id="97752-246">Nano Server</span></span>                   | <span data-ttu-id="97752-247">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="97752-247">Version 1803+</span></span>                  | <span data-ttu-id="97752-248">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="97752-248">x64, ARM32</span></span>      |

<span data-ttu-id="97752-249">有关 .NET Core 3.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-249">For more information about .NET Core 3.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md).</span></span>

# <a name="net-core-30"></a>[<span data-ttu-id="97752-250">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="97752-250">.NET Core 3.0</span></span>](#tab/netcore30)

<span data-ttu-id="97752-251">目前不 ❌ 支持 .NET Core 3.0 *。* 有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="97752-251">*.NET Core 3.0 is currently ❌ out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="97752-252">.NET Core 3.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="97752-252">The following Windows versions are supported with .NET Core 3.0:</span></span>

> [!NOTE]
> <span data-ttu-id="97752-253">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-253">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="97752-254">(OS)</span><span class="sxs-lookup"><span data-stu-id="97752-254">OS</span></span>                            | <span data-ttu-id="97752-255">Version</span><span class="sxs-lookup"><span data-stu-id="97752-255">Version</span></span>                        | <span data-ttu-id="97752-256">体系结构</span><span class="sxs-lookup"><span data-stu-id="97752-256">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="97752-257">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-257">Windows Client</span></span>                | <span data-ttu-id="97752-258">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="97752-258">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="97752-259">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-259">x64, x86</span></span>        |
| <span data-ttu-id="97752-260">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-260">Windows 10 Client</span></span>             | <span data-ttu-id="97752-261">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="97752-261">Version 1607+</span></span>                  | <span data-ttu-id="97752-262">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-262">x64, x86</span></span>        |
| <span data-ttu-id="97752-263">Windows Server</span><span class="sxs-lookup"><span data-stu-id="97752-263">Windows Server</span></span>                | <span data-ttu-id="97752-264">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="97752-264">2012 R2+</span></span>                       | <span data-ttu-id="97752-265">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-265">x64, x86</span></span>        |
| <span data-ttu-id="97752-266">Nano Server</span><span class="sxs-lookup"><span data-stu-id="97752-266">Nano Server</span></span>                   | <span data-ttu-id="97752-267">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="97752-267">Version 1803+</span></span>                  | <span data-ttu-id="97752-268">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="97752-268">x64, ARM32</span></span>      |

<span data-ttu-id="97752-269">有关 .NET Core 3.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-269">For more information about .NET Core 3.0 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md).</span></span>

# <a name="net-core-22"></a>[<span data-ttu-id="97752-270">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="97752-270">.NET Core 2.2</span></span>](#tab/netcore22)

<span data-ttu-id="97752-271">目前不 ❌ 支持 .NET Core 2.2。有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="97752-271">*.NET Core 2.2 is currently ❌ out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="97752-272">.NET Core 2.2 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="97752-272">The following Windows versions are supported with .NET Core 2.2:</span></span>

> [!NOTE]
> <span data-ttu-id="97752-273">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-273">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="97752-274">(OS)</span><span class="sxs-lookup"><span data-stu-id="97752-274">OS</span></span>                            | <span data-ttu-id="97752-275">Version</span><span class="sxs-lookup"><span data-stu-id="97752-275">Version</span></span>                        | <span data-ttu-id="97752-276">体系结构</span><span class="sxs-lookup"><span data-stu-id="97752-276">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="97752-277">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-277">Windows Client</span></span>                | <span data-ttu-id="97752-278">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="97752-278">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="97752-279">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-279">x64, x86</span></span>        |
| <span data-ttu-id="97752-280">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-280">Windows 10 Client</span></span>             | <span data-ttu-id="97752-281">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="97752-281">Version 1607+</span></span>                  | <span data-ttu-id="97752-282">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-282">x64, x86</span></span>        |
| <span data-ttu-id="97752-283">Windows Server</span><span class="sxs-lookup"><span data-stu-id="97752-283">Windows Server</span></span>                | <span data-ttu-id="97752-284">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="97752-284">2008 R2 SP1+</span></span>                   | <span data-ttu-id="97752-285">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-285">x64, x86</span></span>        |
| <span data-ttu-id="97752-286">Nano Server</span><span class="sxs-lookup"><span data-stu-id="97752-286">Nano Server</span></span>                   | <span data-ttu-id="97752-287">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="97752-287">Version 1803+</span></span>                   | <span data-ttu-id="97752-288">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="97752-288">x64, ARM32</span></span>      |

<span data-ttu-id="97752-289">有关 .NET Core 2.2 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.2 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-289">For more information about .NET Core 2.2 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.2 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md).</span></span>

# <a name="net-core-21"></a>[<span data-ttu-id="97752-290">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="97752-290">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="97752-291">.NET Core 2.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="97752-291">The following Windows versions are supported with .NET Core 2.1:</span></span>

> [!NOTE]
> <span data-ttu-id="97752-292">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-292">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="97752-293">(OS)</span><span class="sxs-lookup"><span data-stu-id="97752-293">OS</span></span>                            | <span data-ttu-id="97752-294">Version</span><span class="sxs-lookup"><span data-stu-id="97752-294">Version</span></span>                        | <span data-ttu-id="97752-295">体系结构</span><span class="sxs-lookup"><span data-stu-id="97752-295">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="97752-296">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-296">Windows Client</span></span>                | <span data-ttu-id="97752-297">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="97752-297">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="97752-298">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-298">x64, x86</span></span>        |
| <span data-ttu-id="97752-299">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="97752-299">Windows 10 Client</span></span>             | <span data-ttu-id="97752-300">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="97752-300">Version 1607+</span></span>                  | <span data-ttu-id="97752-301">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-301">x64, x86</span></span>        |
| <span data-ttu-id="97752-302">Windows Server</span><span class="sxs-lookup"><span data-stu-id="97752-302">Windows Server</span></span>                | <span data-ttu-id="97752-303">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="97752-303">2008 R2 SP1+</span></span>                   | <span data-ttu-id="97752-304">x64、x86</span><span class="sxs-lookup"><span data-stu-id="97752-304">x64, x86</span></span>        |
| <span data-ttu-id="97752-305">Nano Server</span><span class="sxs-lookup"><span data-stu-id="97752-305">Nano Server</span></span>                   | <span data-ttu-id="97752-306">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="97752-306">Version 1803+</span></span>                  | <span data-ttu-id="97752-307">x64</span><span class="sxs-lookup"><span data-stu-id="97752-307">x64,</span></span>            |

<span data-ttu-id="97752-308">有关 .NET Core 2.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-308">For more information about .NET Core 2.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md).</span></span>

---

<!-- markdownlint-disable MD001 -->

### <a name="windows-7--vista--81--server-2008-r2--server-2012-r2"></a><a name="additional-deps"></a> <span data-ttu-id="97752-309">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97752-309">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span></span>

<span data-ttu-id="97752-310">如果要在以下 Windows 版本上安装 .NET SDK 或运行时，则需要其他依赖项：</span><span class="sxs-lookup"><span data-stu-id="97752-310">Additional dependencies are required if you're installing the .NET SDK or runtime on the following Windows versions:</span></span>

- <span data-ttu-id="97752-311">Windows 7 SP1 [ESU][esu]</span><span class="sxs-lookup"><span data-stu-id="97752-311">Windows 7 SP1 [ESU][esu]</span></span>
- <span data-ttu-id="97752-312">Windows Vista SP 2</span><span class="sxs-lookup"><span data-stu-id="97752-312">Windows Vista SP 2</span></span>
- <span data-ttu-id="97752-313">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="97752-313">Windows 8.1</span></span>
- <span data-ttu-id="97752-314">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97752-314">Windows Server 2008 R2</span></span>
- <span data-ttu-id="97752-315">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97752-315">Windows Server 2012 R2</span></span>

<span data-ttu-id="97752-316">安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="97752-316">Install the following:</span></span>

- <span data-ttu-id="97752-317">[Microsoft Visual C++ 2015 Redistributable 更新 3](https://www.microsoft.com/download/details.aspx?id=52685)。</span><span class="sxs-lookup"><span data-stu-id="97752-317">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685).</span></span>
- [<span data-ttu-id="97752-318">KB2533623</span><span class="sxs-lookup"><span data-stu-id="97752-318">KB2533623</span></span>](https://support.microsoft.com/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot)

<span data-ttu-id="97752-319">如果遇到以下错误之一，也需要满足上述要求：</span><span class="sxs-lookup"><span data-stu-id="97752-319">The previous requirements are also required if you come across one of the following errors:</span></span>

> <span data-ttu-id="97752-320">此程序无法启动，因为计算机上缺少 api-ms-win-crt-runtime-l1-1-0.dll。</span><span class="sxs-lookup"><span data-stu-id="97752-320">The program can't start because *api-ms-win-crt-runtime-l1-1-0.dll* is missing from your computer.</span></span> <span data-ttu-id="97752-321">尝试重新安装该程序以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="97752-321">Try reinstalling the program to fix this problem.</span></span>
>
> <span data-ttu-id="97752-322">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="97752-322">\- or -</span></span>
>
> <span data-ttu-id="97752-323">此程序无法启动，因为计算机上缺少 api-ms-win-cor-timezone-l1-1-0.dll。</span><span class="sxs-lookup"><span data-stu-id="97752-323">The program can't start because *api-ms-win-cor-timezone-l1-1-0.dll* is missing from your computer.</span></span> <span data-ttu-id="97752-324">尝试重新安装该程序以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="97752-324">Try reinstalling the program to fix this problem.</span></span>
>
> <span data-ttu-id="97752-325">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="97752-325">\- or -</span></span>
>
> <span data-ttu-id="97752-326">已找到库 hostfxr.dll，但未能将其从 C:\\\<path_to_app>\\hostfxr.dll 中加载。</span><span class="sxs-lookup"><span data-stu-id="97752-326">The library *hostfxr.dll* was found, but loading it from *C:\\\<path_to_app>\\hostfxr.dll* failed.</span></span>

## <a name="install-with-powershell-automation"></a><span data-ttu-id="97752-327">使用 PowerShell 自动化安装</span><span class="sxs-lookup"><span data-stu-id="97752-327">Install with PowerShell automation</span></span>

<span data-ttu-id="97752-328">[dotnet-install 脚本](../tools/dotnet-install-script.md)用于运行时的 CI 自动化和非管理员安装。</span><span class="sxs-lookup"><span data-stu-id="97752-328">The [dotnet-install scripts](../tools/dotnet-install-script.md) are used for CI automation and non-admin installs of the runtime.</span></span> <span data-ttu-id="97752-329">可从 [dotnet-install 脚本引用页](../tools/dotnet-install-script.md)下载该脚本。</span><span class="sxs-lookup"><span data-stu-id="97752-329">You can download the script from the [dotnet-install script reference page](../tools/dotnet-install-script.md).</span></span>

<span data-ttu-id="97752-330">此脚本默认安装最新的[长期支持 (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) 版本，即 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="97752-330">The script defaults to installing the latest [long term support (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) version, which is .NET Core 3.1.</span></span> <span data-ttu-id="97752-331">可通过指定 `Channel` 开关以选择特定版本。</span><span class="sxs-lookup"><span data-stu-id="97752-331">You can choose a specific release by specifying the `Channel` switch.</span></span> <span data-ttu-id="97752-332">包括 `Runtime` 开关以安装运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-332">Include the `Runtime` switch to install a runtime.</span></span> <span data-ttu-id="97752-333">否则，该脚本安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="97752-333">Otherwise, the script installs the SDK.</span></span>

```powershell
dotnet-install.ps1 -Channel 5.0 -Runtime aspnetcore
```

<span data-ttu-id="97752-334">通过省略 `-Runtime` 开关来安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="97752-334">Install the SDK by omitting the `-Runtime` switch.</span></span> <span data-ttu-id="97752-335">在此示例中将 `-Channel` 开关设置为 `Current`，这将安装受支持的最新版本。</span><span class="sxs-lookup"><span data-stu-id="97752-335">The `-Channel` switch is set in this example to `Current`, which installs the latest supported version.</span></span>

```powershell
dotnet-install.ps1 -Channel Current
```

## <a name="install-with-visual-studio"></a><span data-ttu-id="97752-336">使用 Visual Studio 安装</span><span class="sxs-lookup"><span data-stu-id="97752-336">Install with Visual Studio</span></span>

<span data-ttu-id="97752-337">如果你要使用 Visual Studio 开发 .NET 应用，请参阅下表，了解不同目标 .NET SDK 版本所需的 Visual Studio 最低版本。</span><span class="sxs-lookup"><span data-stu-id="97752-337">If you're using Visual Studio to develop .NET apps, the following table describes the minimum required version of Visual Studio based on the target .NET SDK version.</span></span>

| <span data-ttu-id="97752-338">.NET SDK 版本</span><span class="sxs-lookup"><span data-stu-id="97752-338">.NET SDK version</span></span>      | <span data-ttu-id="97752-339">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="97752-339">Visual Studio version</span></span>                      |
| --------------------- | ------------------------------------------ |
| <span data-ttu-id="97752-340">5.0</span><span class="sxs-lookup"><span data-stu-id="97752-340">5.0</span></span>                   | <span data-ttu-id="97752-341">Visual Studio 2019 版本 16.8 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="97752-341">Visual Studio 2019 version 16.8 or higher.</span></span> |
| <span data-ttu-id="97752-342">3.1</span><span class="sxs-lookup"><span data-stu-id="97752-342">3.1</span></span>                   | <span data-ttu-id="97752-343">Visual Studio 2019 版本 16.4 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="97752-343">Visual Studio 2019 version 16.4 or higher.</span></span> |
| <span data-ttu-id="97752-344">3.0</span><span class="sxs-lookup"><span data-stu-id="97752-344">3.0</span></span>                   | <span data-ttu-id="97752-345">Visual Studio 2019 版本 16.3 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="97752-345">Visual Studio 2019 version 16.3 or higher.</span></span> |
| <span data-ttu-id="97752-346">2.2</span><span class="sxs-lookup"><span data-stu-id="97752-346">2.2</span></span>                   | <span data-ttu-id="97752-347">Visual Studio 2017 版本 15.9 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="97752-347">Visual Studio 2017 version 15.9 or higher.</span></span> |
| <span data-ttu-id="97752-348">2.1</span><span class="sxs-lookup"><span data-stu-id="97752-348">2.1</span></span>                   | <span data-ttu-id="97752-349">Visual Studio 2017 版本 15.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="97752-349">Visual Studio 2017 version 15.7 or higher.</span></span> |

<span data-ttu-id="97752-350">如果你已安装 Visual Studio，则可以使用以下步骤检查你的版本。</span><span class="sxs-lookup"><span data-stu-id="97752-350">If you already have Visual Studio installed, you can check your version with the following steps.</span></span>

01. <span data-ttu-id="97752-351">打开 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="97752-351">Open Visual Studio.</span></span>
01. <span data-ttu-id="97752-352">选择“帮助” > “Microsoft Visual Studio”。</span><span class="sxs-lookup"><span data-stu-id="97752-352">Select **Help** > **About Microsoft Visual Studio**.</span></span>
01. <span data-ttu-id="97752-353">从“关于”对话框中读取版本号。</span><span class="sxs-lookup"><span data-stu-id="97752-353">Read the version number from the **About** dialog.</span></span>

<span data-ttu-id="97752-354">Visual Studio 可安装最新的 .NET SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-354">Visual Studio can install the latest .NET SDK and runtime.</span></span>

> [!div class="button"]
> <span data-ttu-id="97752-355">[下载 Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019)。</span><span class="sxs-lookup"><span data-stu-id="97752-355">[Download Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019).</span></span>

### <a name="select-a-workload"></a><span data-ttu-id="97752-356">选择工作负载</span><span class="sxs-lookup"><span data-stu-id="97752-356">Select a workload</span></span>

<span data-ttu-id="97752-357">安装或修改 Visual Studio 时，根据要生成的应用程序的类型，选择以下一个或多个工作负载：</span><span class="sxs-lookup"><span data-stu-id="97752-357">When installing or modifying Visual Studio, select one or more of the following workloads, depending on the kind of application you're building:</span></span>

- <span data-ttu-id="97752-358">“其他工具集”部分中的“.NET Core 跨平台开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="97752-358">The **.NET Core cross-platform development** workload in the **Other Toolsets** section.</span></span>
- <span data-ttu-id="97752-359">“Web 和云”部分中的“ASP.NET 和 Web 开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="97752-359">The **ASP.NET and web development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="97752-360">“Web 和云”部分中的“Azure 开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="97752-360">The **Azure development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="97752-361">“桌面和移动”部分中的“NET 桌面开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="97752-361">The **.NET desktop development** workload in the **Desktop & Mobile** section.</span></span>

<span data-ttu-id="97752-362">[![具有 .NET Core 工作负载的 Windows Visual Studio 2019](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="97752-362">[![Windows Visual Studio 2019 with .NET Core workload](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span></span>

## <a name="install-alongside-visual-studio-code"></a><span data-ttu-id="97752-363">随 Visual Studio Code 一起安装</span><span class="sxs-lookup"><span data-stu-id="97752-363">Install alongside Visual Studio Code</span></span>

<span data-ttu-id="97752-364">Visual Studio Code 是一个功能强大的轻量级源代码编辑器，可在桌面上运行。</span><span class="sxs-lookup"><span data-stu-id="97752-364">Visual Studio Code is a powerful and lightweight source code editor that runs on your desktop.</span></span> <span data-ttu-id="97752-365">Visual Studio Code 适用于 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="97752-365">Visual Studio Code is available for Windows, macOS, and Linux.</span></span>

<span data-ttu-id="97752-366">虽然 Visual Studio Code 不像 Visual Studio 一样附带自动的 .NET Core 安装程序，但添加 .NET Core 支持非常简单。</span><span class="sxs-lookup"><span data-stu-id="97752-366">While Visual Studio Code doesn't come with an automated .NET Core installer like Visual Studio does, adding .NET Core support is simple.</span></span>

01. <span data-ttu-id="97752-367">[下载并安装 Visual Studio Code](https://code.visualstudio.com/Download)。</span><span class="sxs-lookup"><span data-stu-id="97752-367">[Download and install Visual Studio Code](https://code.visualstudio.com/Download).</span></span>
01. <span data-ttu-id="97752-368">[下载并安装 .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="97752-368">[Download and install the .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core).</span></span>
01. <span data-ttu-id="97752-369">[从 Visual Studio Code 市场安装 C# 扩展](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)。</span><span class="sxs-lookup"><span data-stu-id="97752-369">[Install the C# extension from the Visual Studio Code marketplace](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="97752-370">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="97752-370">Windows Installer</span></span>

<span data-ttu-id="97752-371">适用于 .NET 的[下载页面](https://dotnet.microsoft.com/download/dotnet-core)提供了 Windows Installer 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="97752-371">The [download page](https://dotnet.microsoft.com/download/dotnet-core) for .NET provides Windows Installer executables.</span></span>

<span data-ttu-id="97752-372">使用 MSI 文件安装 .NET< 时，可以通过设置 `DOTNETHOME_X64` 和 `DOTNETHOME_X86` 参数来自定义安装路径：</span><span class="sxs-lookup"><span data-stu-id="97752-372">When you use the MSI files to install .NET< you can customize the installation path by setting the `DOTNETHOME_X64` and `DOTNETHOME_X86` parameters:</span></span>

```console
dotnet-sdk-3.1.301-win-x64.exe DOTNETHOME_X64="F:\dotnet\x64" DOTNETHOME_X86="F:\dotnet\x86"
```

## <a name="download-and-manually-install"></a><span data-ttu-id="97752-373">下载并手动安装</span><span class="sxs-lookup"><span data-stu-id="97752-373">Download and manually install</span></span>

<span data-ttu-id="97752-374">除了使用适用于 .NET 的 Windows 安装程序，还可以下载并手动安装 SDK 或运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-374">As an alternative to the Windows installers for .NET, you can download and manually install the SDK or runtime.</span></span> <span data-ttu-id="97752-375">手动安装通常作为持续集成测试的一部分执行。</span><span class="sxs-lookup"><span data-stu-id="97752-375">Manual install is usually performed as part of continuous integration testing.</span></span> <span data-ttu-id="97752-376">对于开发人员或用户，一般使用[安装程序](https://dotnet.microsoft.com/download/dotnet-core)会更好。</span><span class="sxs-lookup"><span data-stu-id="97752-376">For a developer or user, it's generally better to use an [installer](https://dotnet.microsoft.com/download/dotnet-core).</span></span>

<span data-ttu-id="97752-377">在下载 .NET SDK 和 .NET 运行时后，可以手动安装它们。</span><span class="sxs-lookup"><span data-stu-id="97752-377">Both .NET SDK and .NET Runtime can be manually installed after they've been downloaded.</span></span> <span data-ttu-id="97752-378">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="97752-378">If you install .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="97752-379">首先，从以下站点之一下载 SDK 或运行时的二进制版本：</span><span class="sxs-lookup"><span data-stu-id="97752-379">First, download a binary release for either the SDK or the runtime from one of the following sites:</span></span>

- [<span data-ttu-id="97752-380">.NET 5.0 下载</span><span class="sxs-lookup"><span data-stu-id="97752-380">.NET 5.0 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet/5.0)
- [<span data-ttu-id="97752-381">.NET Core 3.1 下载</span><span class="sxs-lookup"><span data-stu-id="97752-381">.NET Core 3.1 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [<span data-ttu-id="97752-382">.NET Core 2.1 下载</span><span class="sxs-lookup"><span data-stu-id="97752-382">.NET Core 2.1 downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core/2.1)
- [<span data-ttu-id="97752-383">所有 .NET Core 下载项</span><span class="sxs-lookup"><span data-stu-id="97752-383">All .NET Core downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

<span data-ttu-id="97752-384">创建要将 .NET 提取到的目录，例如 `%USERPROFILE%\dotnet`。</span><span class="sxs-lookup"><span data-stu-id="97752-384">Create a directory to extract .NET to, for example `%USERPROFILE%\dotnet`.</span></span> <span data-ttu-id="97752-385">然后，将下载的 zip 文件提取到该目录中。</span><span class="sxs-lookup"><span data-stu-id="97752-385">Then, extract the downloaded zip file into that directory.</span></span>

<span data-ttu-id="97752-386">默认情况下，.NET CLI 命令和应用不会使用通过这种方式安装的 .NET，并且你必须显式选择才能使用它。</span><span class="sxs-lookup"><span data-stu-id="97752-386">By default, .NET CLI commands and apps won't use .NET installed in this way and you must explicitly choose to use it.</span></span> <span data-ttu-id="97752-387">为此，请更改用于启动应用程序的环境变量：</span><span class="sxs-lookup"><span data-stu-id="97752-387">To do so, change the environment variables with which an application is started:</span></span>

```console
set DOTNET_ROOT=%USERPROFILE%\dotnet
set PATH=%USERPROFILE%\dotnet;%PATH%
set DOTNET_MULTILEVEL_LOOKUP=0
```

<span data-ttu-id="97752-388">使用此方法可以将多个版本安装到不同的位置，然后通过使用指向安装位置的环境变量运行应用程序来明确选择应用程序应使用哪个安装位置。</span><span class="sxs-lookup"><span data-stu-id="97752-388">This approach lets you install multiple versions into separate locations, then explicitly choose which install location an application should use by running the application with environment variables pointing at that location.</span></span>

<span data-ttu-id="97752-389">将 `DOTNET_MULTILEVEL_LOOKUP` 设置为 `0` 时，.NET 将忽略任何全局安装的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="97752-389">When `DOTNET_MULTILEVEL_LOOKUP` is set to `0`, .NET ignores any globally installed .NET version.</span></span> <span data-ttu-id="97752-390">删除环境设置，让 .NET 在选择用于运行应用程序的最佳框架时考虑默认的全局安装位置。</span><span class="sxs-lookup"><span data-stu-id="97752-390">Remove that environment setting to let .NET consider the default global install location when selecting the best framework for running the application.</span></span> <span data-ttu-id="97752-391">默认值通常为 `C:\Program Files\dotnet`，这是安装 .NET 的安装程序所在的位置。</span><span class="sxs-lookup"><span data-stu-id="97752-391">The default is typically `C:\Program Files\dotnet`, which is where the installers install .NET.</span></span>

## <a name="docker"></a><span data-ttu-id="97752-392">Docker</span><span class="sxs-lookup"><span data-stu-id="97752-392">Docker</span></span>

<span data-ttu-id="97752-393">容器提供了一种将应用程序与主机系统的其余部分隔离的轻量级方法。</span><span class="sxs-lookup"><span data-stu-id="97752-393">Containers provide a lightweight way to isolate your application from the rest of the host system.</span></span> <span data-ttu-id="97752-394">同一计算机上的容器只共享内核，并使用为应用程序提供的资源。</span><span class="sxs-lookup"><span data-stu-id="97752-394">Containers on the same machine share just the kernel and use resources given to your application.</span></span>

<span data-ttu-id="97752-395">.NET 可在 Docker 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="97752-395">.NET can run in a Docker container.</span></span> <span data-ttu-id="97752-396">官方 .NET Docker 映像发布到 Microsoft 容器注册表 (MCR)，用户可在 [Microsoft.NET Docker Hub 存储库](https://hub.docker.com/_/microsoft-dotnet)中找到这些映像。</span><span class="sxs-lookup"><span data-stu-id="97752-396">Official .NET Docker images are published to the Microsoft Container Registry (MCR) and are discoverable at the [Microsoft .NET Docker Hub repository](https://hub.docker.com/_/microsoft-dotnet).</span></span> <span data-ttu-id="97752-397">每个存储库包含 .NET（SDK 或运行时）和可以使用的操作系统的不同组合的映像。</span><span class="sxs-lookup"><span data-stu-id="97752-397">Each repository contains images for different combinations of the .NET (SDK or Runtime) and OS that you can use.</span></span>

<span data-ttu-id="97752-398">Microsoft 提供适合特定场景的映像。</span><span class="sxs-lookup"><span data-stu-id="97752-398">Microsoft provides images that are tailored for specific scenarios.</span></span> <span data-ttu-id="97752-399">例如，[ASP.NET Core 存储库](https://hub.docker.com/_/microsoft-dotnet-aspnet)提供针对在生产环境中运行 ASP.NET Core 应用生成的映像。</span><span class="sxs-lookup"><span data-stu-id="97752-399">For example, the [ASP.NET Core repository](https://hub.docker.com/_/microsoft-dotnet-aspnet) provides images that are built for running ASP.NET Core apps in production.</span></span>

<span data-ttu-id="97752-400">有关在 Docker 容器中使用 .NET 的详细信息，请参阅 [.NET 和 Docker 简介](../docker/introduction.md)和[示例](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-400">For more information about using .NET in a Docker container, see [Introduction to .NET and Docker](../docker/introduction.md) and [Samples](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="97752-401">后续步骤</span><span class="sxs-lookup"><span data-stu-id="97752-401">Next steps</span></span>

- <span data-ttu-id="97752-402">[如何检查是否已安装 .NET](how-to-detect-installed-versions.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="97752-402">[How to check if .NET is already installed](how-to-detect-installed-versions.md?pivots=os-windows).</span></span>
- <span data-ttu-id="97752-403">[教程：Hello World 教程](../tutorials/with-visual-studio.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-403">[Tutorial: Hello World tutorial](../tutorials/with-visual-studio.md).</span></span>
- <span data-ttu-id="97752-404">[教程：使用 Visual Studio Code 创建一个新应用](../tutorials/with-visual-studio-code.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-404">[Tutorial: Create a new app with Visual Studio Code](../tutorials/with-visual-studio-code.md).</span></span>
- <span data-ttu-id="97752-405">[教程：使 .NET Core 应用容器化](../docker/build-container.md)。</span><span class="sxs-lookup"><span data-stu-id="97752-405">[Tutorial: Containerize a .NET Core app](../docker/build-container.md).</span></span>

[esu]: /troubleshoot/windows-client/windows-7-eos-faq/windows-7-extended-security-updates-faq
