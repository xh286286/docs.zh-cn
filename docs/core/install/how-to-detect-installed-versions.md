---
title: 检查 Windows、Linux 和 macOS 上安装的 .NET 版本 - .NET
description: 了解如何列出计算机上安装的 .NET 版本。 这包括 .NET 运行时和 SDK。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.custom: updateeachrelease
zone_pivot_groups: operating-systems-set-one
ms.openlocfilehash: 39020a32cdea9b82dc9d30e62e663ebc4ee39ebb
ms.sourcegitcommit: 34968a61e9bac0f6be23ed6ffb837f52d2390c85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "94687436"
---
# <a name="how-to-check-that-net-is-already-installed"></a><span data-ttu-id="d00b2-104">如何检查是否已安装 .NET</span><span class="sxs-lookup"><span data-stu-id="d00b2-104">How to check that .NET is already installed</span></span>

<span data-ttu-id="d00b2-105">本文介绍如何检查计算机上安装的 .NET 运行时和 SDK 的版本。</span><span class="sxs-lookup"><span data-stu-id="d00b2-105">This article teaches you how to check which versions of the .NET runtime and SDK are installed on your computer.</span></span> <span data-ttu-id="d00b2-106">如果你拥有一个集成开发环境（如 Visual Studio 或 Visual Studio for Mac），则可能已安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="d00b2-106">.NET may have already been installed if you have an integrated development environment, such as Visual Studio or Visual Studio for Mac.</span></span>

<span data-ttu-id="d00b2-107">安装 SDK 便会安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="d00b2-107">Installing an SDK installs the corresponding runtime.</span></span>

<span data-ttu-id="d00b2-108">如果本文中的任何命令失败，则未安装运行时或 SDK。</span><span class="sxs-lookup"><span data-stu-id="d00b2-108">If any command in this article fails, you don't have the runtime or SDK installed.</span></span> <span data-ttu-id="d00b2-109">有关详细信息，请参阅 [Windows](windows.md)、[macOS](macos.md) 或 [Linux](linux.md) 的安装文章。</span><span class="sxs-lookup"><span data-stu-id="d00b2-109">For more information, see the install articles for [Windows](windows.md), [macOS](macos.md), or [Linux](linux.md).</span></span>

## <a name="check-sdk-versions"></a><span data-ttu-id="d00b2-110">检查 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="d00b2-110">Check SDK versions</span></span>

<span data-ttu-id="d00b2-111">可使用终端查看当前安装的 .NET SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="d00b2-111">You can see which versions of the .NET SDK are currently installed with a terminal.</span></span> <span data-ttu-id="d00b2-112">打开终端并运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="d00b2-112">Open a terminal and run the following command.</span></span>

```dotnetcli
dotnet --list-sdks
```

<span data-ttu-id="d00b2-113">将获得类似于下面的输出。</span><span class="sxs-lookup"><span data-stu-id="d00b2-113">You get output similar to the following.</span></span>

::: zone pivot="os-windows"

```console
2.1.500 [C:\program files\dotnet\sdk]
2.1.502 [C:\program files\dotnet\sdk]
2.1.504 [C:\program files\dotnet\sdk]
2.1.600 [C:\program files\dotnet\sdk]
2.1.602 [C:\program files\dotnet\sdk]
3.1.100 [C:\program files\dotnet\sdk]
5.0.100 [C:\program files\dotnet\sdk]
```

::: zone-end

::: zone pivot="os-linux"

```bash
2.1.500 [/home/user/dotnet/sdk]
2.1.502 [/home/user/dotnet/sdk]
2.1.504 [/home/user/dotnet/sdk]
2.1.600 [/home/user/dotnet/sdk]
2.1.602 [/home/user/dotnet/sdk]
3.1.100 [/home/user/dotnet/sdk]
5.0.100 [/home/user/dotnet/sdk]
```

::: zone-end

::: zone pivot="os-macos"

```bash
2.1.500 [/usr/local/share/dotnet/sdk]
2.1.502 [/usr/local/share/dotnet/sdk]
2.1.504 [/usr/local/share/dotnet/sdk]
2.1.600 [/usr/local/share/dotnet/sdk]
2.1.602 [/usr/local/share/dotnet/sdk]
3.1.100 [/usr/local/share/dotnet/sdk]
5.0.100 [/usr/local/share/dotnet/sdk]
```

::: zone-end

## <a name="check-runtime-versions"></a><span data-ttu-id="d00b2-114">检查运行时版本</span><span class="sxs-lookup"><span data-stu-id="d00b2-114">Check runtime versions</span></span>

<span data-ttu-id="d00b2-115">可使用以下命令查看当前安装的 .NET 运行时版本。</span><span class="sxs-lookup"><span data-stu-id="d00b2-115">You can see which versions of the .NET runtime are currently installed with the following command.</span></span>

```dotnetcli
dotnet --list-runtimes
```

<span data-ttu-id="d00b2-116">将获得类似于下面的输出。</span><span class="sxs-lookup"><span data-stu-id="d00b2-116">You get output similar to the following.</span></span>

::: zone pivot="os-windows"

```console
Microsoft.AspNetCore.All 2.1.7 [c:\program files\dotnet\shared\Microsoft.AspNetCore.All]
Microsoft.AspNetCore.All 2.1.13 [c:\program files\dotnet\shared\Microsoft.AspNetCore.All]
Microsoft.AspNetCore.App 2.1.7 [c:\program files\dotnet\shared\Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 2.1.13 [c:\program files\dotnet\shared\Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 3.1.0 [c:\program files\dotnet\shared\Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 5.0.0 [c:\program files\dotnet\shared\Microsoft.AspNetCore.App]
Microsoft.NETCore.App 2.1.7 [c:\program files\dotnet\shared\Microsoft.NETCore.App]
Microsoft.NETCore.App 2.1.13 [c:\program files\dotnet\shared\Microsoft.NETCore.App]
Microsoft.NETCore.App 3.1.0 [c:\program files\dotnet\shared\Microsoft.NETCore.App]
Microsoft.NETCore.App 5.0.0 [c:\program files\dotnet\shared\Microsoft.NETCore.App]
Microsoft.WindowsDesktop.App 3.0.0 [c:\program files\dotnet\shared\Microsoft.WindowsDesktop.App]
Microsoft.WindowsDesktop.App 3.1.0 [c:\program files\dotnet\shared\Microsoft.WindowsDesktop.App]
Microsoft.WindowsDesktop.App 5.0.0 [c:\program files\dotnet\shared\Microsoft.WindowsDesktop.App]
```

::: zone-end

::: zone pivot="os-linux"

```bash
Microsoft.AspNetCore.All 2.1.7 [/home/user/dotnet/shared/Microsoft.AspNetCore.All]
Microsoft.AspNetCore.All 2.1.13 [/home/user/dotnet/shared/Microsoft.AspNetCore.All]
Microsoft.AspNetCore.App 2.1.7 [/home/user/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 2.1.13 [/home/user/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 3.1.0 [/home/user/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 5.0.0 [/home/user/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.NETCore.App 2.1.7 [/home/user/dotnet/shared/Microsoft.NETCore.App]
Microsoft.NETCore.App 2.1.13 [/home/user/dotnet/shared/Microsoft.NETCore.App]
Microsoft.NETCore.App 3.1.0 [/home/user/dotnet/shared/Microsoft.NETCore.App]
Microsoft.NETCore.App 5.0.0 [/home/user/dotnet/shared/Microsoft.NETCore.App]
```

::: zone-end

::: zone pivot="os-macos"

```bash
Microsoft.AspNetCore.All 2.1.7 [/usr/local/share/dotnet/shared/Microsoft.AspNetCore.All]
Microsoft.AspNetCore.All 2.1.13 [/usr/local/share/dotnet/shared/Microsoft.AspNetCore.All]
Microsoft.AspNetCore.App 2.1.7 [/usr/local/share/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 2.1.13 [/usr/local/share/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 3.1.0 [/usr/local/share/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.AspNetCore.App 5.0.0 [/usr/local/share/dotnet/shared/Microsoft.AspNetCore.App]
Microsoft.NETCore.App 2.1.7 [/usr/local/share/dotnet/shared/Microsoft.NETCore.App]
Microsoft.NETCore.App 2.1.13 [/usr/local/share/dotnet/shared/Microsoft.NETCore.App]
Microsoft.NETCore.App 3.1.0 [/usr/local/share/dotnet/shared/Microsoft.NETCore.App]
Microsoft.NETCore.App 5.0.0 [/usr/local/share/dotnet/shared/Microsoft.NETCore.App]
```

::: zone-end

## <a name="check-for-install-folders"></a><span data-ttu-id="d00b2-117">检查安装文件夹</span><span class="sxs-lookup"><span data-stu-id="d00b2-117">Check for install folders</span></span>

<span data-ttu-id="d00b2-118">可以安装 .NET，但不能将其添加到操作系统或用户配置文件的 `PATH` 变量。</span><span class="sxs-lookup"><span data-stu-id="d00b2-118">It's possible that .NET is installed but not added to the `PATH` variable for your operating system or user profile.</span></span> <span data-ttu-id="d00b2-119">运行前面几节中的命令可能不起作用。</span><span class="sxs-lookup"><span data-stu-id="d00b2-119">Running the commands from the previous sections may not work.</span></span> <span data-ttu-id="d00b2-120">作为替代方法，可以检查 .NET 安装文件夹是否存在。</span><span class="sxs-lookup"><span data-stu-id="d00b2-120">As an alternative, you can check that the .NET install folders exist.</span></span>

<span data-ttu-id="d00b2-121">从安装程序或脚本安装 .NET 时，会将其安装到标准文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d00b2-121">When you install .NET from an installer or script, it's installed to a standard folder.</span></span> <span data-ttu-id="d00b2-122">大多数时候，安装 .NET 时使用的安装程序或脚本会让你选择安装到另一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="d00b2-122">Much of the time the installer or script you're using to install .NET gives you an option to install to a different folder.</span></span> <span data-ttu-id="d00b2-123">如果选择安装到其他文件夹，请调整文件夹路径的开头。</span><span class="sxs-lookup"><span data-stu-id="d00b2-123">If you choose to install to a different folder, adjust the start of the folder path.</span></span>

::: zone pivot="os-windows"

- <span data-ttu-id="d00b2-124">dotnet executable</span><span class="sxs-lookup"><span data-stu-id="d00b2-124">**dotnet executable**</span></span>\
<span data-ttu-id="d00b2-125">C:\\program files\\dotnet\\dotnet.exe</span><span class="sxs-lookup"><span data-stu-id="d00b2-125">_C:\\program files\\dotnet\\dotnet.exe_</span></span>

- <span data-ttu-id="d00b2-126">**.NET SDK**</span><span class="sxs-lookup"><span data-stu-id="d00b2-126">**.NET SDK**</span></span>\
<span data-ttu-id="d00b2-127">C:\\program files\\dotnet\\sdk\\{version}\\</span><span class="sxs-lookup"><span data-stu-id="d00b2-127">_C:\\program files\\dotnet\\sdk\\{version}\\_</span></span>

- <span data-ttu-id="d00b2-128">.NET Runtime</span><span class="sxs-lookup"><span data-stu-id="d00b2-128">**.NET Runtime**</span></span>\
<span data-ttu-id="d00b2-129">C:\\program files\\dotnet\\shared\\{runtime-type}\\{version}\\</span><span class="sxs-lookup"><span data-stu-id="d00b2-129">_C:\\program files\\dotnet\\shared\\{runtime-type}\\{version}\\_</span></span>

::: zone-end

::: zone pivot="os-linux"

- <span data-ttu-id="d00b2-130">dotnet executable</span><span class="sxs-lookup"><span data-stu-id="d00b2-130">**dotnet executable**</span></span>\
<span data-ttu-id="d00b2-131">/home/user/share/dotnet/dotnet</span><span class="sxs-lookup"><span data-stu-id="d00b2-131">_/home/user/share/dotnet/dotnet_</span></span>

- <span data-ttu-id="d00b2-132">**.NET SDK**</span><span class="sxs-lookup"><span data-stu-id="d00b2-132">**.NET SDK**</span></span>\
<span data-ttu-id="d00b2-133">/home/user/share/dotnet/sdk/{version}/</span><span class="sxs-lookup"><span data-stu-id="d00b2-133">_/home/user/share/dotnet/sdk/{version}/_</span></span>

- <span data-ttu-id="d00b2-134">.NET Runtime</span><span class="sxs-lookup"><span data-stu-id="d00b2-134">**.NET Runtime**</span></span>\
<span data-ttu-id="d00b2-135">/home/user/share/dotnet/shared/{runtime-type}/{version}/</span><span class="sxs-lookup"><span data-stu-id="d00b2-135">_/home/user/share/dotnet/shared/{runtime-type}/{version}/_</span></span>

::: zone-end

::: zone pivot="os-macos"

- <span data-ttu-id="d00b2-136">dotnet executable</span><span class="sxs-lookup"><span data-stu-id="d00b2-136">**dotnet executable**</span></span>\
<span data-ttu-id="d00b2-137">/usr/local/share/dotnet/dotnet</span><span class="sxs-lookup"><span data-stu-id="d00b2-137">_/usr/local/share/dotnet/dotnet_</span></span>

- <span data-ttu-id="d00b2-138">**.NET SDK**</span><span class="sxs-lookup"><span data-stu-id="d00b2-138">**.NET SDK**</span></span>\
<span data-ttu-id="d00b2-139">/usr/local/share/dotnet/sdk/{version}/</span><span class="sxs-lookup"><span data-stu-id="d00b2-139">_/usr/local/share/dotnet/sdk/{version}/_</span></span>

- <span data-ttu-id="d00b2-140">.NET Runtime</span><span class="sxs-lookup"><span data-stu-id="d00b2-140">**.NET Runtime**</span></span>\
<span data-ttu-id="d00b2-141">/usr/local/share/dotnet/shared/{runtime-type}/{version}/</span><span class="sxs-lookup"><span data-stu-id="d00b2-141">_/usr/local/share/dotnet/shared/{runtime-type}/{version}/_</span></span>

::: zone-end

## <a name="more-information"></a><span data-ttu-id="d00b2-142">详细信息</span><span class="sxs-lookup"><span data-stu-id="d00b2-142">More information</span></span>

<span data-ttu-id="d00b2-143">可通过命令 `dotnet --info` 查看 SDK 版本和运行时版本。</span><span class="sxs-lookup"><span data-stu-id="d00b2-143">You can see both the SDK versions and runtime versions with the command `dotnet --info`.</span></span> <span data-ttu-id="d00b2-144">你还将获得其他环境相关信息，如操作系统版本和运行时标识符 (RID)。</span><span class="sxs-lookup"><span data-stu-id="d00b2-144">You'll also get other environmental related information, such as the operating system version and runtime identifier (RID).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d00b2-145">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d00b2-145">Next steps</span></span>

- <span data-ttu-id="d00b2-146">[安装 .NET 运行时和适用于 Windows 的 SDK](windows.md)。</span><span class="sxs-lookup"><span data-stu-id="d00b2-146">[Install the .NET Runtime and SDK for Windows](windows.md).</span></span>
- <span data-ttu-id="d00b2-147">[安装 .NET 运行时和适用于 macOS 的 SDK](macos.md)。</span><span class="sxs-lookup"><span data-stu-id="d00b2-147">[Install the .NET Runtime and SDK for macOS](macos.md).</span></span>
- <span data-ttu-id="d00b2-148">[安装 .NET 运行时和适用于 Linux 的 SDK](linux.md)。</span><span class="sxs-lookup"><span data-stu-id="d00b2-148">[Install the .NET Runtime and SDK for Linux](linux.md).</span></span>
