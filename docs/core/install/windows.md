---
title: 在 Windows 上安装 .NET
description: 了解可在其上安装 .NET 的 Windows 版本。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: fe18cda64e0c9986884486298adf4a83b604f323
ms.sourcegitcommit: c38bf879a2611ff46aacdd529b9f2725f93e18a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "94594529"
---
# <a name="install-net-on-windows"></a><span data-ttu-id="656a9-103">在 Windows 上安装 .NET</span><span class="sxs-lookup"><span data-stu-id="656a9-103">Install .NET on Windows</span></span>

> [!div class="op_single_selector"]
>
> - [在 Windows 上安装](windows.md)
> - [在 macOS 上安装](macos.md)
> - [在 Linux 上安装](linux.md)

<span data-ttu-id="656a9-107">本文介绍如何在 Windows 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="656a9-107">In this article, you'll learn how to install .NET on Windows.</span></span> <span data-ttu-id="656a9-108">.NET 由运行时和 SDK 组成。</span><span class="sxs-lookup"><span data-stu-id="656a9-108">.NET is made up of the runtime and the SDK.</span></span> <span data-ttu-id="656a9-109">运行时用于运行 .NET 应用，应用可能包含也可能不包含它。</span><span class="sxs-lookup"><span data-stu-id="656a9-109">The runtime is used to run a .NET app and may or may not be included with the app.</span></span> <span data-ttu-id="656a9-110">SDK 用于创建 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="656a9-110">The SDK is used to create .NET apps and libraries.</span></span> <span data-ttu-id="656a9-111">.NET 运行时始终随 SDK 一起安装。</span><span class="sxs-lookup"><span data-stu-id="656a9-111">The .NET runtime is always installed with the SDK.</span></span>

<span data-ttu-id="656a9-112">最新版本的 .NET 是 5.0。</span><span class="sxs-lookup"><span data-stu-id="656a9-112">The latest version of .NET is 5.0.</span></span>

> [!div class="button"]
> [<span data-ttu-id="656a9-113">下载 .NET</span><span class="sxs-lookup"><span data-stu-id="656a9-113">Download .NET</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="supported-releases"></a><span data-ttu-id="656a9-114">支持的版本</span><span class="sxs-lookup"><span data-stu-id="656a9-114">Supported releases</span></span>

<span data-ttu-id="656a9-115">下表列出了当前支持的 .NET 版本以及支持它们的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-115">The following table is a list of currently supported .NET releases and the versions of Windows they're supported on.</span></span> <span data-ttu-id="656a9-116">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Windows 版本达到生命周期](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="656a9-116">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Windows reaches end-of-life](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

<span data-ttu-id="656a9-117">Windows 10 版本终止服务日期按版本分段。</span><span class="sxs-lookup"><span data-stu-id="656a9-117">Windows 10 versions end-of-service dates are segmented by edition.</span></span> <span data-ttu-id="656a9-118">下表中仅考虑家庭版、专业版、专业教育版和专业工作站版。   </span><span class="sxs-lookup"><span data-stu-id="656a9-118">Only **Home**, **Pro**, **Pro Education**, and **Pro for Workstations** editions are considered in the following table.</span></span> <span data-ttu-id="656a9-119">查看 [Windows 生命周期事实表单](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)，了解具体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="656a9-119">Check the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet) for specific details.</span></span>

- <span data-ttu-id="656a9-120">✔️ 指示 Windows 或 .NET Core 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="656a9-120">A ✔️ indicates that the version of Windows or .NET Core is still supported.</span></span>
- <span data-ttu-id="656a9-121">❌ 指示 Windows 或 .NET Core 版本在该 Windows 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="656a9-121">A ❌ indicates that the version of Windows or .NET Core isn't supported on that Windows release.</span></span>
- <span data-ttu-id="656a9-122">当 Windows 版本和 .NET Core 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="656a9-122">When both a version of Windows and a version of .NET Core have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="656a9-123">操作系统</span><span class="sxs-lookup"><span data-stu-id="656a9-123">Operating System</span></span>                      | <span data-ttu-id="656a9-124">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-124">.NET Core 2.1</span></span> | <span data-ttu-id="656a9-125">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-125">.NET Core 3.1</span></span> | <span data-ttu-id="656a9-126">.NET 5</span><span class="sxs-lookup"><span data-stu-id="656a9-126">.NET 5</span></span> |
|-----------------------------|---------------|---------------|----------------|
| <span data-ttu-id="656a9-127">✔️ Windows 10 版本 2004</span><span class="sxs-lookup"><span data-stu-id="656a9-127">✔️ Windows 10, Version 2004</span></span> | <span data-ttu-id="656a9-128">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-128">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-129">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-129">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-130">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-130">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-131">✔️ Windows 10 版本 1909</span><span class="sxs-lookup"><span data-stu-id="656a9-131">✔️ Windows 10, Version 1909</span></span> | <span data-ttu-id="656a9-132">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-132">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-133">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-133">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-134">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-134">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-135">✔️ Windows 10 版本 1903</span><span class="sxs-lookup"><span data-stu-id="656a9-135">✔️ Windows 10, Version 1903</span></span> | <span data-ttu-id="656a9-136">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-136">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-137">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-137">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-138">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-138">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-139">✔️ Windows 10 版本 1809</span><span class="sxs-lookup"><span data-stu-id="656a9-139">✔️ Windows 10, Version 1809</span></span> | <span data-ttu-id="656a9-140">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-140">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-141">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-141">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-142">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-142">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-143">❌ Windows 10 版本 1803</span><span class="sxs-lookup"><span data-stu-id="656a9-143">❌ Windows 10, Version 1803</span></span> | <span data-ttu-id="656a9-144">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-144">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-145">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-145">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-146">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-146">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-147">❌ Windows 10 版本 1709</span><span class="sxs-lookup"><span data-stu-id="656a9-147">❌ Windows 10, Version 1709</span></span> | <span data-ttu-id="656a9-148">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-148">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-149">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-149">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-150">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-150">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-151">❌ Windows 10 版本 1703</span><span class="sxs-lookup"><span data-stu-id="656a9-151">❌ Windows 10, Version 1703</span></span> | <span data-ttu-id="656a9-152">❌ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-152">❌ 2.1</span></span>        | <span data-ttu-id="656a9-153">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-153">❌ 3.1</span></span>        | <span data-ttu-id="656a9-154">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-154">❌ 5.0</span></span> |
| <span data-ttu-id="656a9-155">❌ Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="656a9-155">❌ Windows 10, Version 1607</span></span> | <span data-ttu-id="656a9-156">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-156">✔️ 2.1</span></span>        | <span data-ttu-id="656a9-157">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-157">✔️ 3.1</span></span>        | <span data-ttu-id="656a9-158">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-158">✔️ 5.0</span></span> |
| <span data-ttu-id="656a9-159">❌ Windows 10 版本 1511</span><span class="sxs-lookup"><span data-stu-id="656a9-159">❌ Windows 10, Version 1511</span></span> | <span data-ttu-id="656a9-160">❌ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-160">❌ 2.1</span></span>        | <span data-ttu-id="656a9-161">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-161">❌ 3.1</span></span>        | <span data-ttu-id="656a9-162">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-162">❌ 5.0</span></span> |
| <span data-ttu-id="656a9-163">❌ Windows 10 版本 1507</span><span class="sxs-lookup"><span data-stu-id="656a9-163">❌ Windows 10, Version 1507</span></span> | <span data-ttu-id="656a9-164">❌ 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-164">❌ 2.1</span></span>        | <span data-ttu-id="656a9-165">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-165">❌ 3.1</span></span>        | <span data-ttu-id="656a9-166">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-166">❌ 5.0</span></span> |

## <a name="unsupported-releases"></a><span data-ttu-id="656a9-167">不支持的版本</span><span class="sxs-lookup"><span data-stu-id="656a9-167">Unsupported releases</span></span>

<span data-ttu-id="656a9-168">以下 .NET 版本 ❌ 不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="656a9-168">The following versions of .NET are ❌ no longer supported.</span></span> <span data-ttu-id="656a9-169">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="656a9-169">The downloads for these still remain published:</span></span>

- <span data-ttu-id="656a9-170">3.0</span><span class="sxs-lookup"><span data-stu-id="656a9-170">3.0</span></span>
- <span data-ttu-id="656a9-171">2.2</span><span class="sxs-lookup"><span data-stu-id="656a9-171">2.2</span></span>
- <span data-ttu-id="656a9-172">2.0</span><span class="sxs-lookup"><span data-stu-id="656a9-172">2.0</span></span>

## <a name="runtime-information"></a><span data-ttu-id="656a9-173">运行时信息</span><span class="sxs-lookup"><span data-stu-id="656a9-173">Runtime information</span></span>

<span data-ttu-id="656a9-174">运行时用于运行使用 .NET 创建的应用。</span><span class="sxs-lookup"><span data-stu-id="656a9-174">The runtime is used to run apps created with .NET.</span></span> <span data-ttu-id="656a9-175">应用作者发布应用时，可以在其应用中包含运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-175">When an app author publishes an app, they can include the runtime with their app.</span></span> <span data-ttu-id="656a9-176">如果作者未包含运行时，则由用户安装运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-176">If they don't include the runtime, it's up to the user to install the runtime.</span></span>

<span data-ttu-id="656a9-177">可以在 Windows 上安装三个不同的运行时：</span><span class="sxs-lookup"><span data-stu-id="656a9-177">There are three different runtimes you can install on Windows:</span></span>

<span data-ttu-id="656a9-178">*ASP.NET Core 运行时*</span><span class="sxs-lookup"><span data-stu-id="656a9-178">*ASP.NET Core runtime*</span></span>\
<span data-ttu-id="656a9-179">运行 ASP.NET Core 应用。</span><span class="sxs-lookup"><span data-stu-id="656a9-179">Runs ASP.NET Core apps.</span></span> <span data-ttu-id="656a9-180">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-180">Includes the .NET runtime.</span></span>

<span data-ttu-id="656a9-181">*桌面运行时*</span><span class="sxs-lookup"><span data-stu-id="656a9-181">*Desktop runtime*</span></span>\
<span data-ttu-id="656a9-182">运行适用于 Windows 的 .NET WPF 和 Windows 窗体桌面应用。</span><span class="sxs-lookup"><span data-stu-id="656a9-182">Runs .NET WPF and Windows Forms desktop apps for Windows.</span></span> <span data-ttu-id="656a9-183">包括 .NET 运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-183">Includes the .NET runtime.</span></span>

<span data-ttu-id="656a9-184">.NET 运行时</span><span class="sxs-lookup"><span data-stu-id="656a9-184">*.NET runtime*</span></span>\
<span data-ttu-id="656a9-185">此运行时是最简单的运行时，不包括任何其他运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-185">This runtime is the simplest runtime and doesn't include any other runtime.</span></span> <span data-ttu-id="656a9-186">强烈建议同时安装 ASP.NET Core 运行时和桌面运行时，以最大限度地提升与 .NET 应用的兼容性 。</span><span class="sxs-lookup"><span data-stu-id="656a9-186">It's highly recommended that you install both *ASP.NET Core runtime* and *Desktop runtime* for the best compatibility with .NET apps.</span></span>

> [!div class="button"]
> [<span data-ttu-id="656a9-187">下载 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="656a9-187">Download .NET Runtime</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

## <a name="sdk-information"></a><span data-ttu-id="656a9-188">SDK 信息</span><span class="sxs-lookup"><span data-stu-id="656a9-188">SDK information</span></span>

<span data-ttu-id="656a9-189">SDK 用于生成和发布 .NET 应用和库。</span><span class="sxs-lookup"><span data-stu-id="656a9-189">The SDK is used to build and publish .NET apps and libraries.</span></span> <span data-ttu-id="656a9-190">安装 SDK 会包含三个[运行时](#runtime-information)：ASP.NET Core、桌面和 .NET。</span><span class="sxs-lookup"><span data-stu-id="656a9-190">Installing the SDK includes all three [runtimes](#runtime-information): ASP.NET Core, Desktop, and .NET.</span></span>

## <a name="dependencies"></a><span data-ttu-id="656a9-191">依赖项</span><span class="sxs-lookup"><span data-stu-id="656a9-191">Dependencies</span></span>

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD024 -->

# <a name="net-50"></a>[<span data-ttu-id="656a9-192">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-192">.NET 5.0</span></span>](#tab/net50)

<span data-ttu-id="656a9-193">.NET 5.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="656a9-193">The following Windows versions are supported with .NET 5.0:</span></span>

> [!NOTE]
> <span data-ttu-id="656a9-194">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-194">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="656a9-195">(OS)</span><span class="sxs-lookup"><span data-stu-id="656a9-195">OS</span></span>                  | <span data-ttu-id="656a9-196">Version</span><span class="sxs-lookup"><span data-stu-id="656a9-196">Version</span></span>       | <span data-ttu-id="656a9-197">体系结构</span><span class="sxs-lookup"><span data-stu-id="656a9-197">Architectures</span></span>   |
|---------------------|---------------|-----------------|
| <span data-ttu-id="656a9-198">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-198">Windows 10 Client</span></span>   | <span data-ttu-id="656a9-199">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="656a9-199">Version 1607+</span></span> | <span data-ttu-id="656a9-200">x64、x86、ARM64</span><span class="sxs-lookup"><span data-stu-id="656a9-200">x64, x86, ARM64</span></span> |
| <span data-ttu-id="656a9-201">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-201">Windows Client</span></span>      | <span data-ttu-id="656a9-202">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="656a9-202">7 SP1+, 8.1</span></span>   | <span data-ttu-id="656a9-203">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-203">x64, x86</span></span>        |
| <span data-ttu-id="656a9-204">Windows Server</span><span class="sxs-lookup"><span data-stu-id="656a9-204">Windows Server</span></span>      | <span data-ttu-id="656a9-205">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="656a9-205">2012 R2+</span></span>      | <span data-ttu-id="656a9-206">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-206">x64, x86</span></span>        |
| <span data-ttu-id="656a9-207">Windows Server 核心</span><span class="sxs-lookup"><span data-stu-id="656a9-207">Windows Server Core</span></span> | <span data-ttu-id="656a9-208">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="656a9-208">2012 R2+</span></span>      | <span data-ttu-id="656a9-209">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-209">x64, x86</span></span>        |
| <span data-ttu-id="656a9-210">Nano Server</span><span class="sxs-lookup"><span data-stu-id="656a9-210">Nano Server</span></span>         | <span data-ttu-id="656a9-211">版本 1809+</span><span class="sxs-lookup"><span data-stu-id="656a9-211">Version 1809+</span></span> | <span data-ttu-id="656a9-212">X64</span><span class="sxs-lookup"><span data-stu-id="656a9-212">x64</span></span>             |

<span data-ttu-id="656a9-213">有关 .NET 5.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET 5.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-213">For more information about .NET 5.0 supported operating systems, distributions, and lifecycle policy, see [.NET 5.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/5.0/5.0-supported-os.md).</span></span>

# <a name="net-core-31"></a>[<span data-ttu-id="656a9-214">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-214">.NET Core 3.1</span></span>](#tab/netcore31)

<span data-ttu-id="656a9-215">.NET Core 3.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="656a9-215">The following Windows versions are supported with .NET Core 3.1:</span></span>

> [!NOTE]
> <span data-ttu-id="656a9-216">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-216">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="656a9-217">(OS)</span><span class="sxs-lookup"><span data-stu-id="656a9-217">OS</span></span>                            | <span data-ttu-id="656a9-218">Version</span><span class="sxs-lookup"><span data-stu-id="656a9-218">Version</span></span>                        | <span data-ttu-id="656a9-219">体系结构</span><span class="sxs-lookup"><span data-stu-id="656a9-219">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="656a9-220">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-220">Windows Client</span></span>                | <span data-ttu-id="656a9-221">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="656a9-221">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="656a9-222">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-222">x64, x86</span></span>        |
| <span data-ttu-id="656a9-223">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-223">Windows 10 Client</span></span>             | <span data-ttu-id="656a9-224">版本 1609+</span><span class="sxs-lookup"><span data-stu-id="656a9-224">Version 1609+</span></span>                  | <span data-ttu-id="656a9-225">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-225">x64, x86</span></span>        |
| <span data-ttu-id="656a9-226">Windows Server</span><span class="sxs-lookup"><span data-stu-id="656a9-226">Windows Server</span></span>                | <span data-ttu-id="656a9-227">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="656a9-227">2012 R2+</span></span>                       | <span data-ttu-id="656a9-228">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-228">x64, x86</span></span>        |
| <span data-ttu-id="656a9-229">Nano Server</span><span class="sxs-lookup"><span data-stu-id="656a9-229">Nano Server</span></span>                   | <span data-ttu-id="656a9-230">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="656a9-230">Version 1803+</span></span>                  | <span data-ttu-id="656a9-231">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="656a9-231">x64, ARM32</span></span>      |

<span data-ttu-id="656a9-232">有关 .NET Core 3.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-232">For more information about .NET Core 3.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.1/3.1-supported-os.md).</span></span>

# <a name="net-core-30"></a>[<span data-ttu-id="656a9-233">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="656a9-233">.NET Core 3.0</span></span>](#tab/netcore30)

<span data-ttu-id="656a9-234">目前不支持 .NET Core 3.0。有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="656a9-234">*.NET Core 3.0 is currently out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="656a9-235">.NET Core 3.0 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="656a9-235">The following Windows versions are supported with .NET Core 3.0:</span></span>

> [!NOTE]
> <span data-ttu-id="656a9-236">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-236">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="656a9-237">(OS)</span><span class="sxs-lookup"><span data-stu-id="656a9-237">OS</span></span>                            | <span data-ttu-id="656a9-238">Version</span><span class="sxs-lookup"><span data-stu-id="656a9-238">Version</span></span>                        | <span data-ttu-id="656a9-239">体系结构</span><span class="sxs-lookup"><span data-stu-id="656a9-239">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="656a9-240">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-240">Windows Client</span></span>                | <span data-ttu-id="656a9-241">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="656a9-241">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="656a9-242">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-242">x64, x86</span></span>        |
| <span data-ttu-id="656a9-243">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-243">Windows 10 Client</span></span>             | <span data-ttu-id="656a9-244">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="656a9-244">Version 1607+</span></span>                  | <span data-ttu-id="656a9-245">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-245">x64, x86</span></span>        |
| <span data-ttu-id="656a9-246">Windows Server</span><span class="sxs-lookup"><span data-stu-id="656a9-246">Windows Server</span></span>                | <span data-ttu-id="656a9-247">2012 R2+</span><span class="sxs-lookup"><span data-stu-id="656a9-247">2012 R2+</span></span>                       | <span data-ttu-id="656a9-248">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-248">x64, x86</span></span>        |
| <span data-ttu-id="656a9-249">Nano Server</span><span class="sxs-lookup"><span data-stu-id="656a9-249">Nano Server</span></span>                   | <span data-ttu-id="656a9-250">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="656a9-250">Version 1803+</span></span>                  | <span data-ttu-id="656a9-251">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="656a9-251">x64, ARM32</span></span>      |

<span data-ttu-id="656a9-252">有关 .NET Core 3.0 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 3.0 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-252">For more information about .NET Core 3.0 supported operating systems, distributions, and lifecycle policy, see [.NET Core 3.0 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/3.0/3.0-supported-os.md).</span></span>

# <a name="net-core-22"></a>[<span data-ttu-id="656a9-253">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="656a9-253">.NET Core 2.2</span></span>](#tab/netcore22)

<span data-ttu-id="656a9-254">目前不支持 .NET Core 2.2。有关详细信息，请参阅 [.NET Core 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="656a9-254">*.NET Core 2.2 is currently out of support. For more information, see the [.NET Core Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).*</span></span>

<span data-ttu-id="656a9-255">.NET Core 2.2 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="656a9-255">The following Windows versions are supported with .NET Core 2.2:</span></span>

> [!NOTE]
> <span data-ttu-id="656a9-256">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-256">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="656a9-257">(OS)</span><span class="sxs-lookup"><span data-stu-id="656a9-257">OS</span></span>                            | <span data-ttu-id="656a9-258">Version</span><span class="sxs-lookup"><span data-stu-id="656a9-258">Version</span></span>                        | <span data-ttu-id="656a9-259">体系结构</span><span class="sxs-lookup"><span data-stu-id="656a9-259">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="656a9-260">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-260">Windows Client</span></span>                | <span data-ttu-id="656a9-261">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="656a9-261">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="656a9-262">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-262">x64, x86</span></span>        |
| <span data-ttu-id="656a9-263">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-263">Windows 10 Client</span></span>             | <span data-ttu-id="656a9-264">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="656a9-264">Version 1607+</span></span>                  | <span data-ttu-id="656a9-265">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-265">x64, x86</span></span>        |
| <span data-ttu-id="656a9-266">Windows Server</span><span class="sxs-lookup"><span data-stu-id="656a9-266">Windows Server</span></span>                | <span data-ttu-id="656a9-267">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="656a9-267">2008 R2 SP1+</span></span>                   | <span data-ttu-id="656a9-268">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-268">x64, x86</span></span>        |
| <span data-ttu-id="656a9-269">Nano Server</span><span class="sxs-lookup"><span data-stu-id="656a9-269">Nano Server</span></span>                   | <span data-ttu-id="656a9-270">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="656a9-270">Version 1803+</span></span>                   | <span data-ttu-id="656a9-271">x64、ARM32</span><span class="sxs-lookup"><span data-stu-id="656a9-271">x64, ARM32</span></span>      |

<span data-ttu-id="656a9-272">有关 .NET Core 2.2 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.2 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-272">For more information about .NET Core 2.2 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.2 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.2/2.2-supported-os.md).</span></span>

# <a name="net-core-21"></a>[<span data-ttu-id="656a9-273">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-273">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="656a9-274">.NET Core 2.1 支持下列 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="656a9-274">The following Windows versions are supported with .NET Core 2.1:</span></span>

> [!NOTE]
> <span data-ttu-id="656a9-275">`+` 表示最低版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-275">A `+` symbol represents the minimum version.</span></span>

| <span data-ttu-id="656a9-276">(OS)</span><span class="sxs-lookup"><span data-stu-id="656a9-276">OS</span></span>                            | <span data-ttu-id="656a9-277">Version</span><span class="sxs-lookup"><span data-stu-id="656a9-277">Version</span></span>                        | <span data-ttu-id="656a9-278">体系结构</span><span class="sxs-lookup"><span data-stu-id="656a9-278">Architectures</span></span>   |
| ----------------------------- | ------------------------------ | --------------- |
| <span data-ttu-id="656a9-279">Windows 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-279">Windows Client</span></span>                | <span data-ttu-id="656a9-280">7 SP1+、8.1</span><span class="sxs-lookup"><span data-stu-id="656a9-280">7 SP1+, 8.1</span></span>                    | <span data-ttu-id="656a9-281">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-281">x64, x86</span></span>        |
| <span data-ttu-id="656a9-282">Windows 10 客户端</span><span class="sxs-lookup"><span data-stu-id="656a9-282">Windows 10 Client</span></span>             | <span data-ttu-id="656a9-283">版本 1607+</span><span class="sxs-lookup"><span data-stu-id="656a9-283">Version 1607+</span></span>                  | <span data-ttu-id="656a9-284">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-284">x64, x86</span></span>        |
| <span data-ttu-id="656a9-285">Windows Server</span><span class="sxs-lookup"><span data-stu-id="656a9-285">Windows Server</span></span>                | <span data-ttu-id="656a9-286">2008 R2 SP1+</span><span class="sxs-lookup"><span data-stu-id="656a9-286">2008 R2 SP1+</span></span>                   | <span data-ttu-id="656a9-287">x64、x86</span><span class="sxs-lookup"><span data-stu-id="656a9-287">x64, x86</span></span>        |
| <span data-ttu-id="656a9-288">Nano Server</span><span class="sxs-lookup"><span data-stu-id="656a9-288">Nano Server</span></span>                   | <span data-ttu-id="656a9-289">版本 1803+</span><span class="sxs-lookup"><span data-stu-id="656a9-289">Version 1803+</span></span>                  | <span data-ttu-id="656a9-290">x64</span><span class="sxs-lookup"><span data-stu-id="656a9-290">x64,</span></span>            |

<span data-ttu-id="656a9-291">有关 .NET Core 2.1 支持的操作系统、发行版和生命周期策略的详细信息，请参阅 [.NET Core 2.1 支持的 OS 版本](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-291">For more information about .NET Core 2.1 supported operating systems, distributions, and lifecycle policy, see [.NET Core 2.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md).</span></span>

---

<!-- markdownlint-disable MD001 -->

### <a name="windows-7--vista--81--server-2008-r2--server-2012-r2"></a><a name="additional-deps"></a> <span data-ttu-id="656a9-292">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="656a9-292">Windows 7 / Vista / 8.1 / Server 2008 R2 / Server 2012 R2</span></span>

<span data-ttu-id="656a9-293">如果要在以下 Windows 版本上安装 .NET SDK 或运行时，则需要其他依赖项：</span><span class="sxs-lookup"><span data-stu-id="656a9-293">Additional dependencies are required if you're installing the .NET SDK or runtime on the following Windows versions:</span></span>

- <span data-ttu-id="656a9-294">❌ Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="656a9-294">❌ Windows 7 SP1</span></span>
- <span data-ttu-id="656a9-295">❌ Windows Vista SP 2</span><span class="sxs-lookup"><span data-stu-id="656a9-295">❌ Windows Vista SP 2</span></span>
- <span data-ttu-id="656a9-296">✔️ Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="656a9-296">✔️ Windows 8.1</span></span>
- <span data-ttu-id="656a9-297">✔️ Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="656a9-297">✔️ Windows Server 2008 R2</span></span>
- <span data-ttu-id="656a9-298">✔️ Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="656a9-298">✔️ Windows Server 2012 R2</span></span>

<span data-ttu-id="656a9-299">安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="656a9-299">Install the following:</span></span>

- <span data-ttu-id="656a9-300">[Microsoft Visual C++ 2015 Redistributable 更新 3](https://www.microsoft.com/download/details.aspx?id=52685)。</span><span class="sxs-lookup"><span data-stu-id="656a9-300">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685).</span></span>
- [<span data-ttu-id="656a9-301">KB2533623</span><span class="sxs-lookup"><span data-stu-id="656a9-301">KB2533623</span></span>](https://support.microsoft.com/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot)

<span data-ttu-id="656a9-302">如果遇到以下错误之一，也需要满足上述要求：</span><span class="sxs-lookup"><span data-stu-id="656a9-302">The previous requirements are also required if you come across one of the following errors:</span></span>

> <span data-ttu-id="656a9-303">此程序无法启动，因为计算机上缺少 api-ms-win-crt-runtime-l1-1-0.dll。</span><span class="sxs-lookup"><span data-stu-id="656a9-303">The program can't start because *api-ms-win-crt-runtime-l1-1-0.dll* is missing from your computer.</span></span> <span data-ttu-id="656a9-304">尝试重新安装该程序以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="656a9-304">Try reinstalling the program to fix this problem.</span></span>
>
> <span data-ttu-id="656a9-305">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="656a9-305">\- or -</span></span>
>
> <span data-ttu-id="656a9-306">此程序无法启动，因为计算机上缺少 api-ms-win-cor-timezone-l1-1-0.dll。</span><span class="sxs-lookup"><span data-stu-id="656a9-306">The program can't start because *api-ms-win-cor-timezone-l1-1-0.dll* is missing from your computer.</span></span> <span data-ttu-id="656a9-307">尝试重新安装该程序以解决此问题。</span><span class="sxs-lookup"><span data-stu-id="656a9-307">Try reinstalling the program to fix this problem.</span></span>
>
> <span data-ttu-id="656a9-308">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="656a9-308">\- or -</span></span>
>
> <span data-ttu-id="656a9-309">已找到库 hostfxr.dll，但未能将其从 C:\\\<path_to_app>\\hostfxr.dll 中加载。</span><span class="sxs-lookup"><span data-stu-id="656a9-309">The library *hostfxr.dll* was found, but loading it from *C:\\\<path_to_app>\\hostfxr.dll* failed.</span></span>

## <a name="install-with-powershell-automation"></a><span data-ttu-id="656a9-310">使用 PowerShell 自动化安装</span><span class="sxs-lookup"><span data-stu-id="656a9-310">Install with PowerShell automation</span></span>

<span data-ttu-id="656a9-311">[dotnet-install 脚本](../tools/dotnet-install-script.md)用于运行时的 CI 自动化和非管理员安装。</span><span class="sxs-lookup"><span data-stu-id="656a9-311">The [dotnet-install scripts](../tools/dotnet-install-script.md) are used for CI automation and non-admin installs of the runtime.</span></span> <span data-ttu-id="656a9-312">可从 [dotnet-install 脚本引用页](../tools/dotnet-install-script.md)下载该脚本。</span><span class="sxs-lookup"><span data-stu-id="656a9-312">You can download the script from the [dotnet-install script reference page](../tools/dotnet-install-script.md).</span></span>

<span data-ttu-id="656a9-313">此脚本默认安装最新的[长期支持 (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) 版本，即 .NET 3.1。</span><span class="sxs-lookup"><span data-stu-id="656a9-313">The script defaults to installing the latest [long term support (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) version, which is .NET 3.1.</span></span> <span data-ttu-id="656a9-314">可通过指定 `Channel` 开关以选择特定版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-314">You can choose a specific release by specifying the `Channel` switch.</span></span> <span data-ttu-id="656a9-315">包括 `Runtime` 开关以安装运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-315">Include the `Runtime` switch to install a runtime.</span></span> <span data-ttu-id="656a9-316">否则，该脚本安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="656a9-316">Otherwise, the script installs the SDK.</span></span>

```powershell
dotnet-install.ps1 -Channel 5.0 -Runtime aspnetcore
```

<span data-ttu-id="656a9-317">通过省略 `-Runtime` 开关来安装 SDK。</span><span class="sxs-lookup"><span data-stu-id="656a9-317">Install the SDK by omitting the `-Runtime` switch.</span></span> <span data-ttu-id="656a9-318">在此示例中将 `-Channel` 开关设置为 `Current`，这将安装受支持的最新版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-318">The `-Channel` switch is set in this example to `Current`, which installs the latest supported version.</span></span>

```powershell
dotnet-install.ps1 -Channel Current
```

## <a name="install-with-visual-studio"></a><span data-ttu-id="656a9-319">使用 Visual Studio 安装</span><span class="sxs-lookup"><span data-stu-id="656a9-319">Install with Visual Studio</span></span>

<span data-ttu-id="656a9-320">如果你要使用 Visual Studio 开发 .NET 应用，请参阅下表，了解不同目标 .NET SDK 版本所需的 Visual Studio 最低版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-320">If you're using Visual Studio to develop .NET apps, the following table describes the minimum required version of Visual Studio based on the target .NET SDK version.</span></span>

| <span data-ttu-id="656a9-321">.NET SDK 版本</span><span class="sxs-lookup"><span data-stu-id="656a9-321">.NET SDK version</span></span>      | <span data-ttu-id="656a9-322">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="656a9-322">Visual Studio version</span></span>                      |
| --------------------- | ------------------------------------------ |
| <span data-ttu-id="656a9-323">5.0</span><span class="sxs-lookup"><span data-stu-id="656a9-323">5.0</span></span>                   | <span data-ttu-id="656a9-324">Visual Studio 2019 版本 16.8 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-324">Visual Studio 2019 version 16.8 or higher.</span></span> |
| <span data-ttu-id="656a9-325">3.1</span><span class="sxs-lookup"><span data-stu-id="656a9-325">3.1</span></span>                   | <span data-ttu-id="656a9-326">Visual Studio 2019 版本 16.4 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-326">Visual Studio 2019 version 16.4 or higher.</span></span> |
| <span data-ttu-id="656a9-327">3.0</span><span class="sxs-lookup"><span data-stu-id="656a9-327">3.0</span></span>                   | <span data-ttu-id="656a9-328">Visual Studio 2019 版本 16.3 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-328">Visual Studio 2019 version 16.3 or higher.</span></span> |
| <span data-ttu-id="656a9-329">2.2</span><span class="sxs-lookup"><span data-stu-id="656a9-329">2.2</span></span>                   | <span data-ttu-id="656a9-330">Visual Studio 2017 版本 15.9 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-330">Visual Studio 2017 version 15.9 or higher.</span></span> |
| <span data-ttu-id="656a9-331">2.1</span><span class="sxs-lookup"><span data-stu-id="656a9-331">2.1</span></span>                   | <span data-ttu-id="656a9-332">Visual Studio 2017 版本 15.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-332">Visual Studio 2017 version 15.7 or higher.</span></span> |

<span data-ttu-id="656a9-333">如果你已安装 Visual Studio，则可以使用以下步骤检查你的版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-333">If you already have Visual Studio installed, you can check your version with the following steps.</span></span>

01. <span data-ttu-id="656a9-334">打开 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="656a9-334">Open Visual Studio.</span></span>
01. <span data-ttu-id="656a9-335">选择“帮助” > “Microsoft Visual Studio”。</span><span class="sxs-lookup"><span data-stu-id="656a9-335">Select **Help** > **About Microsoft Visual Studio**.</span></span>
01. <span data-ttu-id="656a9-336">从“关于”对话框中读取版本号。</span><span class="sxs-lookup"><span data-stu-id="656a9-336">Read the version number from the **About** dialog.</span></span>

<span data-ttu-id="656a9-337">Visual Studio 可安装最新的 .NET SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-337">Visual Studio can install the latest .NET SDK and runtime.</span></span>

> [!div class="button"]
> <span data-ttu-id="656a9-338">[下载 Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019)。</span><span class="sxs-lookup"><span data-stu-id="656a9-338">[Download Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2019).</span></span>

### <a name="select-a-workload"></a><span data-ttu-id="656a9-339">选择工作负载</span><span class="sxs-lookup"><span data-stu-id="656a9-339">Select a workload</span></span>

<span data-ttu-id="656a9-340">安装或修改 Visual Studio 时，根据要生成的应用程序的类型，选择以下一个或多个工作负载：</span><span class="sxs-lookup"><span data-stu-id="656a9-340">When installing or modifying Visual Studio, select one or more of the following workloads, depending on the kind of application you're building:</span></span>

- <span data-ttu-id="656a9-341">“其他工具集”部分中的“.NET Core 跨平台开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="656a9-341">The **.NET Core cross-platform development** workload in the **Other Toolsets** section.</span></span>
- <span data-ttu-id="656a9-342">“Web 和云”部分中的“ASP.NET 和 Web 开发”工作负荷 。</span><span class="sxs-lookup"><span data-stu-id="656a9-342">The **ASP.NET and web development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="656a9-343">“Web 和云”部分中的“Azure 开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="656a9-343">The **Azure development** workload in the **Web & Cloud** section.</span></span>
- <span data-ttu-id="656a9-344">“桌面和移动”部分中的“NET 桌面开发”工作负载 。</span><span class="sxs-lookup"><span data-stu-id="656a9-344">The **.NET desktop development** workload in the **Desktop & Mobile** section.</span></span>

<span data-ttu-id="656a9-345">[![具有 .NET Core 工作负载的 Windows Visual Studio 2019](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="656a9-345">[![Windows Visual Studio 2019 with .NET Core workload](media/install-sdk/windows-install-visual-studio-2019.png)](media/install-sdk/windows-install-visual-studio-2019.png#lightbox)</span></span>

## <a name="install-alongside-visual-studio-code"></a><span data-ttu-id="656a9-346">随 Visual Studio Code 一起安装</span><span class="sxs-lookup"><span data-stu-id="656a9-346">Install alongside Visual Studio Code</span></span>

<span data-ttu-id="656a9-347">Visual Studio Code 是一个功能强大的轻量级源代码编辑器，可在桌面上运行。</span><span class="sxs-lookup"><span data-stu-id="656a9-347">Visual Studio Code is a powerful and lightweight source code editor that runs on your desktop.</span></span> <span data-ttu-id="656a9-348">Visual Studio Code 适用于 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="656a9-348">Visual Studio Code is available for Windows, macOS, and Linux.</span></span>

<span data-ttu-id="656a9-349">虽然 Visual Studio Code 不像 Visual Studio 一样附带自动的 .NET Core 安装程序，但添加 .NET Core 支持非常简单。</span><span class="sxs-lookup"><span data-stu-id="656a9-349">While Visual Studio Code doesn't come with an automated .NET Core installer like Visual Studio does, adding .NET Core support is simple.</span></span>

01. <span data-ttu-id="656a9-350">[下载并安装 Visual Studio Code](https://code.visualstudio.com/Download)。</span><span class="sxs-lookup"><span data-stu-id="656a9-350">[Download and install Visual Studio Code](https://code.visualstudio.com/Download).</span></span>
01. <span data-ttu-id="656a9-351">[下载并安装 .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="656a9-351">[Download and install the .NET Core SDK](https://dotnet.microsoft.com/download/dotnet-core).</span></span>
01. <span data-ttu-id="656a9-352">[从 Visual Studio Code 市场安装 C# 扩展](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)。</span><span class="sxs-lookup"><span data-stu-id="656a9-352">[Install the C# extension from the Visual Studio Code marketplace](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span>

## <a name="download-and-manually-install"></a><span data-ttu-id="656a9-353">下载并手动安装</span><span class="sxs-lookup"><span data-stu-id="656a9-353">Download and manually install</span></span>

<span data-ttu-id="656a9-354">除了使用适用于 .NET 的 Windows 安装程序，还可以下载并手动安装 SDK 或运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-354">As an alternative to the Windows installers for .NET, you can download and manually install the SDK or runtime.</span></span> <span data-ttu-id="656a9-355">手动安装通常作为持续集成测试的一部分执行。</span><span class="sxs-lookup"><span data-stu-id="656a9-355">Manual install is usually performed as part of continuous integration testing.</span></span> <span data-ttu-id="656a9-356">对于开发人员或用户，一般使用[安装程序](https://dotnet.microsoft.com/download/dotnet-core)会更好。</span><span class="sxs-lookup"><span data-stu-id="656a9-356">For a developer or user, it's generally better to use an [installer](https://dotnet.microsoft.com/download/dotnet-core).</span></span>

<span data-ttu-id="656a9-357">在下载 .NET SDK 和 .NET 运行时后，可以手动安装它们。</span><span class="sxs-lookup"><span data-stu-id="656a9-357">Both .NET SDK and .NET Runtime can be manually installed after they've been downloaded.</span></span> <span data-ttu-id="656a9-358">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="656a9-358">If you install .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="656a9-359">首先，从以下站点之一下载 SDK 或运行时的二进制版本：</span><span class="sxs-lookup"><span data-stu-id="656a9-359">First, download a binary release for either the SDK or the runtime from one of the following sites:</span></span>

- <span data-ttu-id="656a9-360">✔️ [.NET 5.0 下载](https://dotnet.microsoft.com/download/dotnet/5.0)</span><span class="sxs-lookup"><span data-stu-id="656a9-360">✔️ [.NET 5.0 downloads](https://dotnet.microsoft.com/download/dotnet/5.0)</span></span>
- <span data-ttu-id="656a9-361">✔️ [.NET Core 3.1 下载](https://dotnet.microsoft.com/download/dotnet-core/3.1)</span><span class="sxs-lookup"><span data-stu-id="656a9-361">✔️ [.NET Core 3.1 downloads](https://dotnet.microsoft.com/download/dotnet-core/3.1)</span></span>
- <span data-ttu-id="656a9-362">✔️ [.NET Core 2.1 下载](https://dotnet.microsoft.com/download/dotnet-core/2.1)</span><span class="sxs-lookup"><span data-stu-id="656a9-362">✔️ [.NET Core 2.1 downloads](https://dotnet.microsoft.com/download/dotnet-core/2.1)</span></span>
- [<span data-ttu-id="656a9-363">所有 .NET Core 下载项</span><span class="sxs-lookup"><span data-stu-id="656a9-363">All .NET Core downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

<span data-ttu-id="656a9-364">创建要将 .NET 提取到的目录，例如 `%USERPROFILE%\dotnet`。</span><span class="sxs-lookup"><span data-stu-id="656a9-364">Create a directory to extract .NET to, for example `%USERPROFILE%\dotnet`.</span></span> <span data-ttu-id="656a9-365">然后，将下载的 zip 文件提取到该目录中。</span><span class="sxs-lookup"><span data-stu-id="656a9-365">Then, extract the downloaded zip file into that directory.</span></span>

<span data-ttu-id="656a9-366">默认情况下，.NET CLI 命令和应用不会使用通过这种方式安装的 .NET，并且你必须显式选择才能使用它。</span><span class="sxs-lookup"><span data-stu-id="656a9-366">By default, .NET CLI commands and apps won't use .NET installed in this way and you must explicitly choose to use it.</span></span> <span data-ttu-id="656a9-367">为此，请更改用于启动应用程序的环境变量：</span><span class="sxs-lookup"><span data-stu-id="656a9-367">To do so, change the environment variables with which an application is started:</span></span>

```console
set DOTNET_ROOT=%USERPROFILE%\dotnet
set PATH=%USERPROFILE%\dotnet;%PATH%
set DOTNET_MULTILEVEL_LOOKUP=0
```

<span data-ttu-id="656a9-368">使用此方法可以将多个版本安装到不同的位置，然后通过使用指向安装位置的环境变量运行应用程序来明确选择应用程序应使用哪个安装位置。</span><span class="sxs-lookup"><span data-stu-id="656a9-368">This approach lets you install multiple versions into separate locations, then explicitly choose which install location an application should use by running the application with environment variables pointing at that location.</span></span>

<span data-ttu-id="656a9-369">将 `DOTNET_MULTILEVEL_LOOKUP` 设置为 `0` 时，.NET 将忽略任何全局安装的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="656a9-369">When `DOTNET_MULTILEVEL_LOOKUP` is set to `0`, .NET ignores any globally installed .NET version.</span></span> <span data-ttu-id="656a9-370">删除环境设置，让 .NET 在选择用于运行应用程序的最佳框架时考虑默认的全局安装位置。</span><span class="sxs-lookup"><span data-stu-id="656a9-370">Remove that environment setting to let .NET consider the default global install location when selecting the best framework for running the application.</span></span> <span data-ttu-id="656a9-371">默认值通常为 `C:\Program Files\dotnet`，这是安装 .NET 的安装程序所在的位置。</span><span class="sxs-lookup"><span data-stu-id="656a9-371">The default is typically `C:\Program Files\dotnet`, which is where the installers install .NET.</span></span>

## <a name="docker"></a><span data-ttu-id="656a9-372">Docker</span><span class="sxs-lookup"><span data-stu-id="656a9-372">Docker</span></span>

<span data-ttu-id="656a9-373">容器提供了一种将应用程序与主机系统的其余部分隔离的轻量级方法。</span><span class="sxs-lookup"><span data-stu-id="656a9-373">Containers provide a lightweight way to isolate your application from the rest of the host system.</span></span> <span data-ttu-id="656a9-374">同一计算机上的容器只共享内核，并使用为应用程序提供的资源。</span><span class="sxs-lookup"><span data-stu-id="656a9-374">Containers on the same machine share just the kernel and use resources given to your application.</span></span>

<span data-ttu-id="656a9-375">.NET 可在 Docker 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="656a9-375">.NET can run in a Docker container.</span></span> <span data-ttu-id="656a9-376">官方 .NET Docker 映像发布到 Microsoft 容器注册表 (MCR)，用户可在 [Microsoft.NET Docker Hub 存储库](https://hub.docker.com/_/microsoft-dotnet)中找到这些映像。</span><span class="sxs-lookup"><span data-stu-id="656a9-376">Official .NET Docker images are published to the Microsoft Container Registry (MCR) and are discoverable at the [Microsoft .NET Docker Hub repository](https://hub.docker.com/_/microsoft-dotnet).</span></span> <span data-ttu-id="656a9-377">每个存储库包含 .NET（SDK 或运行时）和可以使用的操作系统的不同组合的映像。</span><span class="sxs-lookup"><span data-stu-id="656a9-377">Each repository contains images for different combinations of the .NET (SDK or Runtime) and OS that you can use.</span></span>

<span data-ttu-id="656a9-378">Microsoft 提供适合特定场景的映像。</span><span class="sxs-lookup"><span data-stu-id="656a9-378">Microsoft provides images that are tailored for specific scenarios.</span></span> <span data-ttu-id="656a9-379">例如，[ASP.NET Core 存储库](https://hub.docker.com/_/microsoft-dotnet-aspnet)提供针对在生产环境中运行 ASP.NET Core 应用生成的映像。</span><span class="sxs-lookup"><span data-stu-id="656a9-379">For example, the [ASP.NET Core repository](https://hub.docker.com/_/microsoft-dotnet-aspnet) provides images that are built for running ASP.NET Core apps in production.</span></span>

<span data-ttu-id="656a9-380">有关在 Docker 容器中使用 .NET 的详细信息，请参阅 [.NET 和 Docker 简介](../docker/introduction.md)和[示例](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-380">For more information about using .NET in a Docker container, see [Introduction to .NET and Docker](../docker/introduction.md) and [Samples](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="656a9-381">后续步骤</span><span class="sxs-lookup"><span data-stu-id="656a9-381">Next steps</span></span>

- <span data-ttu-id="656a9-382">[如何检查是否已安装 .NET](how-to-detect-installed-versions.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="656a9-382">[How to check if .NET is already installed](how-to-detect-installed-versions.md?pivots=os-windows).</span></span>
- <span data-ttu-id="656a9-383">[教程：Hello World 教程](../tutorials/with-visual-studio.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-383">[Tutorial: Hello World tutorial](../tutorials/with-visual-studio.md).</span></span>
- <span data-ttu-id="656a9-384">[教程：使用 Visual Studio Code 创建一个新应用](../tutorials/with-visual-studio-code.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-384">[Tutorial: Create a new app with Visual Studio Code](../tutorials/with-visual-studio-code.md).</span></span>
- <span data-ttu-id="656a9-385">[教程：使 .NET Core 应用容器化](../docker/build-container.md)。</span><span class="sxs-lookup"><span data-stu-id="656a9-385">[Tutorial: Containerize a .NET Core app](../docker/build-container.md).</span></span>
