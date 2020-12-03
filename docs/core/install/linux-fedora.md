---
title: 在 Fedora 上安装 .NET - .NET
description: 演示在 Fedora 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: f7422941af7e39d69d286a0f79920b025c1bf9c0
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031899"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-fedora"></a><span data-ttu-id="acd11-103">在 Fedora 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="acd11-103">Install the .NET SDK or the .NET Runtime on Fedora</span></span>

<span data-ttu-id="acd11-104">Fedora 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="acd11-104">.NET is supported on Fedora.</span></span> <span data-ttu-id="acd11-105">本文介绍如何在 Fedora 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="acd11-105">This article describes how to install .NET on Fedora.</span></span> <span data-ttu-id="acd11-106">如果 Fedora 版本不受支持，则该版本不再支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="acd11-106">When a Fedora version falls out of support, .NET is no longer supported with that version.</span></span> <span data-ttu-id="acd11-107">不过，可以按照这些说明在这些版本上运行 .NET，即使它不受支持。</span><span class="sxs-lookup"><span data-stu-id="acd11-107">However, these instructions may help you to get .NET running on those versions, even though it isn't supported.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="acd11-108">支持的发行版</span><span class="sxs-lookup"><span data-stu-id="acd11-108">Supported distributions</span></span>

<span data-ttu-id="acd11-109">下表列出了当前支持的 .NET 版本以及支持它们的 Fedora 版本。</span><span class="sxs-lookup"><span data-stu-id="acd11-109">The following table is a list of currently supported .NET releases and the versions of Fedora they're supported on.</span></span> <span data-ttu-id="acd11-110">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Fedora 版本达到生命周期](https://fedoraproject.org/wiki/End_of_life)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="acd11-110">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Fedora reaches end-of-life](https://fedoraproject.org/wiki/End_of_life).</span></span>

- <span data-ttu-id="acd11-111">✔️ 指示 Fedora 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="acd11-111">A ✔️ indicates that the version of Fedora or .NET is still supported.</span></span>
- <span data-ttu-id="acd11-112">❌ 指示 Fedora 或 .NET 版本在该 Fedora 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="acd11-112">A ❌ indicates that the version of Fedora or .NET isn't supported on that Fedora release.</span></span>
- <span data-ttu-id="acd11-113">当 Fedora 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="acd11-113">When both a version of Fedora and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="acd11-114">Fedora</span><span class="sxs-lookup"><span data-stu-id="acd11-114">Fedora</span></span>               | <span data-ttu-id="acd11-115">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-115">.NET Core 2.1</span></span> | <span data-ttu-id="acd11-116">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-116">.NET Core 3.1</span></span> | <span data-ttu-id="acd11-117">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-117">.NET 5.0</span></span> |
|----------------------|---------------|---------------|----------|
| <span data-ttu-id="acd11-118">✔️ [33](#fedora-33-)</span><span class="sxs-lookup"><span data-stu-id="acd11-118">✔️ [33](#fedora-33-)</span></span> | <span data-ttu-id="acd11-119">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-119">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-120">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-120">✔️ 3.1</span></span>        | <span data-ttu-id="acd11-121">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-121">✔️ 5.0</span></span> |
| <span data-ttu-id="acd11-122">✔️ [32](#fedora-32-)</span><span class="sxs-lookup"><span data-stu-id="acd11-122">✔️ [32](#fedora-32-)</span></span> | <span data-ttu-id="acd11-123">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-123">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-124">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-124">✔️ 3.1</span></span>        | <span data-ttu-id="acd11-125">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-125">✔️ 5.0</span></span> |
| <span data-ttu-id="acd11-126">❌ [31](#fedora-31-)</span><span class="sxs-lookup"><span data-stu-id="acd11-126">❌ [31](#fedora-31-)</span></span> | <span data-ttu-id="acd11-127">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-127">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-128">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-128">✔️ 3.1</span></span>        | <span data-ttu-id="acd11-129">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-129">❌ 5.0</span></span> |
| <span data-ttu-id="acd11-130">❌ [30](#fedora-30-)</span><span class="sxs-lookup"><span data-stu-id="acd11-130">❌ [30](#fedora-30-)</span></span> | <span data-ttu-id="acd11-131">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-131">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-132">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-132">✔️ 3.1</span></span>        | <span data-ttu-id="acd11-133">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-133">❌ 5.0</span></span> |
| <span data-ttu-id="acd11-134">❌ [29](#fedora-29-)</span><span class="sxs-lookup"><span data-stu-id="acd11-134">❌ [29](#fedora-29-)</span></span> | <span data-ttu-id="acd11-135">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-135">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-136">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-136">✔️ 3.1</span></span>        | <span data-ttu-id="acd11-137">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-137">❌ 5.0</span></span> |
| <span data-ttu-id="acd11-138">❌ [28](#fedora-28-)</span><span class="sxs-lookup"><span data-stu-id="acd11-138">❌ [28](#fedora-28-)</span></span> | <span data-ttu-id="acd11-139">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-139">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-140">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-140">❌ 3.1</span></span>        | <span data-ttu-id="acd11-141">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-141">❌ 5.0</span></span> |
| <span data-ttu-id="acd11-142">❌ [27](#fedora-27-)</span><span class="sxs-lookup"><span data-stu-id="acd11-142">❌ [27](#fedora-27-)</span></span> | <span data-ttu-id="acd11-143">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="acd11-143">✔️ 2.1</span></span>        | <span data-ttu-id="acd11-144">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="acd11-144">❌ 3.1</span></span>        | <span data-ttu-id="acd11-145">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="acd11-145">❌ 5.0</span></span> |

<span data-ttu-id="acd11-146">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="acd11-146">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="acd11-147">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="acd11-147">The downloads for these still remain published:</span></span>

- <span data-ttu-id="acd11-148">3.0</span><span class="sxs-lookup"><span data-stu-id="acd11-148">3.0</span></span>
- <span data-ttu-id="acd11-149">2.2</span><span class="sxs-lookup"><span data-stu-id="acd11-149">2.2</span></span>
- <span data-ttu-id="acd11-150">2.0</span><span class="sxs-lookup"><span data-stu-id="acd11-150">2.0</span></span>

## <a name="remove-preview-versions"></a><span data-ttu-id="acd11-151">删除预览版本</span><span class="sxs-lookup"><span data-stu-id="acd11-151">Remove preview versions</span></span>

[!INCLUDE [package-manager uninstall notice](./includes/linux-uninstall-preview-info.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="acd11-152">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="acd11-152">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="fedora-33-"></a><span data-ttu-id="acd11-153">Fedora 33 ✔️</span><span class="sxs-lookup"><span data-stu-id="acd11-153">Fedora 33 ✔️</span></span>

> [!TIP]
> <span data-ttu-id="acd11-154">.NET Core 3.1 在 Fedora 33 的默认包存储库中提供。</span><span class="sxs-lookup"><span data-stu-id="acd11-154">.NET Core 3.1 is available in the default package repositories for Fedora 33.</span></span> <span data-ttu-id="acd11-155">若要安装 .NET Core 3.1，请对相应的包（如 `aspnetcore-runtime-3.1` 或 `dotnet-sdk-3.1`）使用 `dnf install` 命令。</span><span class="sxs-lookup"><span data-stu-id="acd11-155">To install .NET Core 3.1, use the `dnf install` command with the appropriate package, such as `aspnetcore-runtime-3.1` or `dotnet-sdk-3.1`.</span></span> <span data-ttu-id="acd11-156">.NET 5.0 在默认包存储库中尚不可用。</span><span class="sxs-lookup"><span data-stu-id="acd11-156">.NET 5.0 isn't yet available in the default package repositories.</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/33/prod.repo
```

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="fedora-32-"></a><span data-ttu-id="acd11-157">Fedora 32 ✔️</span><span class="sxs-lookup"><span data-stu-id="acd11-157">Fedora 32 ✔️</span></span>

> [!TIP]
> <span data-ttu-id="acd11-158">.NET Core 3.1 在 Fedora 32 的默认包存储库中提供。</span><span class="sxs-lookup"><span data-stu-id="acd11-158">.NET Core 3.1 is available in the default package repositories for Fedora 32.</span></span> <span data-ttu-id="acd11-159">若要安装 .NET Core 3.1，请对相应的包（如 `aspnetcore-runtime-3.1` 或 `dotnet-sdk-3.1`）使用 `dnf install` 命令。</span><span class="sxs-lookup"><span data-stu-id="acd11-159">To install .NET Core 3.1, use the `dnf install` command with the appropriate package, such as `aspnetcore-runtime-3.1` or `dotnet-sdk-3.1`.</span></span> <span data-ttu-id="acd11-160">.NET 5.0 在默认包存储库中尚不可用。</span><span class="sxs-lookup"><span data-stu-id="acd11-160">.NET 5.0 isn't yet available in the default package repositories.</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/32/prod.repo
```

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="fedora-31-"></a><span data-ttu-id="acd11-161">Fedora 31 ❌</span><span class="sxs-lookup"><span data-stu-id="acd11-161">Fedora 31 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/31/prod.repo
```

[!INCLUDE [linux-dnf-install-31](includes/linux-install-31-dnf.md)]

## <a name="fedora-30-"></a><span data-ttu-id="acd11-162">Fedora 30 ❌</span><span class="sxs-lookup"><span data-stu-id="acd11-162">Fedora 30 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/30/prod.repo
```

[!INCLUDE [linux-dnf-install-31](includes/linux-install-31-dnf.md)]

## <a name="fedora-29-"></a><span data-ttu-id="acd11-163">Fedora 29 ❌</span><span class="sxs-lookup"><span data-stu-id="acd11-163">Fedora 29 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/29/prod.repo
```

[!INCLUDE [linux-dnf-install-30](includes/linux-install-30-dnf.md)]

## <a name="fedora-28-"></a><span data-ttu-id="acd11-164">Fedora 28 ❌</span><span class="sxs-lookup"><span data-stu-id="acd11-164">Fedora 28 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/28/prod.repo
```

[!INCLUDE [linux-dnf-install-20](includes/linux-install-20-dnf.md)]

## <a name="fedora-27-"></a><span data-ttu-id="acd11-165">Fedora 27 ❌</span><span class="sxs-lookup"><span data-stu-id="acd11-165">Fedora 27 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/27/prod.repo
```

[!INCLUDE [linux-dnf-install-20](includes/linux-install-20-dnf.md)]

## <a name="troubleshoot-the-package-manager"></a><span data-ttu-id="acd11-166">包管理器疑难解答</span><span class="sxs-lookup"><span data-stu-id="acd11-166">Troubleshoot the package manager</span></span>

<span data-ttu-id="acd11-167">本部分提供有关使用程序包管理器安装 .NET Core 时可能会遇到的常见错误的信息。</span><span class="sxs-lookup"><span data-stu-id="acd11-167">This section provides information on common errors you may get while using the package manager to install .NET Core.</span></span>

### <a name="unable-to-find-package"></a><span data-ttu-id="acd11-168">找不到包</span><span class="sxs-lookup"><span data-stu-id="acd11-168">Unable to find package</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

### <a name="failed-to-fetch"></a><span data-ttu-id="acd11-169">未能提取</span><span class="sxs-lookup"><span data-stu-id="acd11-169">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-rpm](includes/package-manager-failed-to-fetch-rpm.md)]

## <a name="snap"></a><span data-ttu-id="acd11-170">对齐</span><span class="sxs-lookup"><span data-stu-id="acd11-170">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="acd11-171">依赖项</span><span class="sxs-lookup"><span data-stu-id="acd11-171">Dependencies</span></span>

[!INCLUDE [linux-rpm-install-dependencies](includes/linux-rpm-install-dependencies.md)]

## <a name="scripted-install"></a><span data-ttu-id="acd11-172">脚本安装</span><span class="sxs-lookup"><span data-stu-id="acd11-172">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="acd11-173">手动安装</span><span class="sxs-lookup"><span data-stu-id="acd11-173">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="acd11-174">后续步骤</span><span class="sxs-lookup"><span data-stu-id="acd11-174">Next steps</span></span>

- [<span data-ttu-id="acd11-175">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="acd11-175">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
