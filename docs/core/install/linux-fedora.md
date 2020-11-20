---
title: 在 Fedora 上安装 .NET - .NET
description: 演示在 Fedora 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: 9e96773e30fb8ee395e37dca7a4794cd42359bb2
ms.sourcegitcommit: c38bf879a2611ff46aacdd529b9f2725f93e18a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "94594603"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-fedora"></a><span data-ttu-id="89d4a-103">在 Fedora 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="89d4a-103">Install the .NET SDK or the .NET Runtime on Fedora</span></span>

<span data-ttu-id="89d4a-104">Fedora 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="89d4a-104">.NET is supported on Fedora.</span></span> <span data-ttu-id="89d4a-105">本文介绍如何在 Fedora 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="89d4a-105">This article describes how to install .NET on Fedora.</span></span> <span data-ttu-id="89d4a-106">如果 Fedora 版本不受支持，则该版本不再支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="89d4a-106">When a Fedora version falls out of support, .NET is no longer supported with that version.</span></span> <span data-ttu-id="89d4a-107">不过，可以按照这些说明在这些版本上运行 .NET，即使它不受支持。</span><span class="sxs-lookup"><span data-stu-id="89d4a-107">However, these instructions may help you to get .NET running on those versions, even though it isn't supported.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="89d4a-108">支持的发行版</span><span class="sxs-lookup"><span data-stu-id="89d4a-108">Supported distributions</span></span>

<span data-ttu-id="89d4a-109">下表列出了当前支持的 .NET 版本以及支持它们的 Fedora 版本。</span><span class="sxs-lookup"><span data-stu-id="89d4a-109">The following table is a list of currently supported .NET releases and the versions of Fedora they're supported on.</span></span> <span data-ttu-id="89d4a-110">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Fedora 版本达到生命周期](https://fedoraproject.org/wiki/End_of_life)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="89d4a-110">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Fedora reaches end-of-life](https://fedoraproject.org/wiki/End_of_life).</span></span>

- <span data-ttu-id="89d4a-111">✔️ 指示 Fedora 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="89d4a-111">A ✔️ indicates that the version of Fedora or .NET is still supported.</span></span>
- <span data-ttu-id="89d4a-112">❌ 指示 Fedora 或 .NET 版本在该 Fedora 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="89d4a-112">A ❌ indicates that the version of Fedora or .NET isn't supported on that Fedora release.</span></span>
- <span data-ttu-id="89d4a-113">当 Fedora 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="89d4a-113">When both a version of Fedora and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="89d4a-114">Fedora</span><span class="sxs-lookup"><span data-stu-id="89d4a-114">Fedora</span></span>               | <span data-ttu-id="89d4a-115">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-115">.NET Core 2.1</span></span> | <span data-ttu-id="89d4a-116">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-116">.NET Core 3.1</span></span> | <span data-ttu-id="89d4a-117">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-117">.NET 5.0</span></span> |
|----------------------|---------------|---------------|----------|
| <span data-ttu-id="89d4a-118">✔️ [33](#fedora-33-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-118">✔️ [33](#fedora-33-)</span></span> | <span data-ttu-id="89d4a-119">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-119">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-120">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-120">✔️ 3.1</span></span>        | <span data-ttu-id="89d4a-121">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-121">✔️ 5.0</span></span> |
| <span data-ttu-id="89d4a-122">✔️ [32](#fedora-32-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-122">✔️ [32](#fedora-32-)</span></span> | <span data-ttu-id="89d4a-123">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-123">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-124">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-124">✔️ 3.1</span></span>        | <span data-ttu-id="89d4a-125">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-125">✔️ 5.0</span></span> |
| <span data-ttu-id="89d4a-126">❌ [31](#fedora-31-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-126">❌ [31](#fedora-31-)</span></span> | <span data-ttu-id="89d4a-127">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-127">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-128">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-128">✔️ 3.1</span></span>        | <span data-ttu-id="89d4a-129">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-129">❌ 5.0</span></span> |
| <span data-ttu-id="89d4a-130">❌ [30](#fedora-30-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-130">❌ [30](#fedora-30-)</span></span> | <span data-ttu-id="89d4a-131">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-131">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-132">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-132">✔️ 3.1</span></span>        | <span data-ttu-id="89d4a-133">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-133">❌ 5.0</span></span> |
| <span data-ttu-id="89d4a-134">❌ [29](#fedora-29-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-134">❌ [29](#fedora-29-)</span></span> | <span data-ttu-id="89d4a-135">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-135">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-136">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-136">✔️ 3.1</span></span>        | <span data-ttu-id="89d4a-137">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-137">❌ 5.0</span></span> |
| <span data-ttu-id="89d4a-138">❌ [28](#fedora-28-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-138">❌ [28](#fedora-28-)</span></span> | <span data-ttu-id="89d4a-139">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-139">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-140">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-140">❌ 3.1</span></span>        | <span data-ttu-id="89d4a-141">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-141">❌ 5.0</span></span> |
| <span data-ttu-id="89d4a-142">❌ [27](#fedora-27-)</span><span class="sxs-lookup"><span data-stu-id="89d4a-142">❌ [27](#fedora-27-)</span></span> | <span data-ttu-id="89d4a-143">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-143">✔️ 2.1</span></span>        | <span data-ttu-id="89d4a-144">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="89d4a-144">❌ 3.1</span></span>        | <span data-ttu-id="89d4a-145">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-145">❌ 5.0</span></span> |

<span data-ttu-id="89d4a-146">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="89d4a-146">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="89d4a-147">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="89d4a-147">The downloads for these still remain published:</span></span>

- <span data-ttu-id="89d4a-148">3.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-148">3.0</span></span>
- <span data-ttu-id="89d4a-149">2.2</span><span class="sxs-lookup"><span data-stu-id="89d4a-149">2.2</span></span>
- <span data-ttu-id="89d4a-150">2.0</span><span class="sxs-lookup"><span data-stu-id="89d4a-150">2.0</span></span>

## <a name="how-to-install-other-versions"></a><span data-ttu-id="89d4a-151">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="89d4a-151">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="fedora-33-"></a><span data-ttu-id="89d4a-152">Fedora 33 ✔️</span><span class="sxs-lookup"><span data-stu-id="89d4a-152">Fedora 33 ✔️</span></span>

> [!TIP]
> <span data-ttu-id="89d4a-153">.NET Core 3.1 在 Fedora 33 的默认包存储库中提供。</span><span class="sxs-lookup"><span data-stu-id="89d4a-153">.NET Core 3.1 is available in the default package repositories for Fedora 33.</span></span> <span data-ttu-id="89d4a-154">若要安装 .NET Core 3.1，请对相应的包（如 `aspnetcore-runtime-3.1` 或 `dotnet-sdk-3.1`）使用 `dnf install` 命令。</span><span class="sxs-lookup"><span data-stu-id="89d4a-154">To install .NET Core 3.1, use the `dnf install` command with the appropriate package, such as `aspnetcore-runtime-3.1` or `dotnet-sdk-3.1`.</span></span> <span data-ttu-id="89d4a-155">.NET 5.0 在默认包存储库中尚不可用。</span><span class="sxs-lookup"><span data-stu-id="89d4a-155">.NET 5.0 isn't yet available in the default package repositories.</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/33/prod.repo
```

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="fedora-32-"></a><span data-ttu-id="89d4a-156">Fedora 32 ✔️</span><span class="sxs-lookup"><span data-stu-id="89d4a-156">Fedora 32 ✔️</span></span>

> [!TIP]
> <span data-ttu-id="89d4a-157">.NET Core 3.1 在 Fedora 32 的默认包存储库中提供。</span><span class="sxs-lookup"><span data-stu-id="89d4a-157">.NET Core 3.1 is available in the default package repositories for Fedora 32.</span></span> <span data-ttu-id="89d4a-158">若要安装 .NET Core 3.1，请对相应的包（如 `aspnetcore-runtime-3.1` 或 `dotnet-sdk-3.1`）使用 `dnf install` 命令。</span><span class="sxs-lookup"><span data-stu-id="89d4a-158">To install .NET Core 3.1, use the `dnf install` command with the appropriate package, such as `aspnetcore-runtime-3.1` or `dotnet-sdk-3.1`.</span></span> <span data-ttu-id="89d4a-159">.NET 5.0 在默认包存储库中尚不可用。</span><span class="sxs-lookup"><span data-stu-id="89d4a-159">.NET 5.0 isn't yet available in the default package repositories.</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/32/prod.repo
```

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="fedora-31-"></a><span data-ttu-id="89d4a-160">Fedora 31 ❌</span><span class="sxs-lookup"><span data-stu-id="89d4a-160">Fedora 31 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/31/prod.repo
```

[!INCLUDE [linux-dnf-install-31](includes/linux-install-31-dnf.md)]

## <a name="fedora-30-"></a><span data-ttu-id="89d4a-161">Fedora 30 ❌</span><span class="sxs-lookup"><span data-stu-id="89d4a-161">Fedora 30 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/30/prod.repo
```

[!INCLUDE [linux-dnf-install-31](includes/linux-install-31-dnf.md)]

## <a name="fedora-29-"></a><span data-ttu-id="89d4a-162">Fedora 29 ❌</span><span class="sxs-lookup"><span data-stu-id="89d4a-162">Fedora 29 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/29/prod.repo
```

[!INCLUDE [linux-dnf-install-30](includes/linux-install-30-dnf.md)]

## <a name="fedora-28-"></a><span data-ttu-id="89d4a-163">Fedora 28 ❌</span><span class="sxs-lookup"><span data-stu-id="89d4a-163">Fedora 28 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/28/prod.repo
```

[!INCLUDE [linux-dnf-install-20](includes/linux-install-20-dnf.md)]

## <a name="fedora-27-"></a><span data-ttu-id="89d4a-164">Fedora 27 ❌</span><span class="sxs-lookup"><span data-stu-id="89d4a-164">Fedora 27 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-fedora.md)]

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/fedora/27/prod.repo
```

[!INCLUDE [linux-dnf-install-20](includes/linux-install-20-dnf.md)]

## <a name="troubleshoot-the-package-manager"></a><span data-ttu-id="89d4a-165">包管理器疑难解答</span><span class="sxs-lookup"><span data-stu-id="89d4a-165">Troubleshoot the package manager</span></span>

<span data-ttu-id="89d4a-166">本部分提供有关使用程序包管理器安装 .NET Core 时可能会遇到的常见错误的信息。</span><span class="sxs-lookup"><span data-stu-id="89d4a-166">This section provides information on common errors you may get while using the package manager to install .NET Core.</span></span>

### <a name="unable-to-find-package"></a><span data-ttu-id="89d4a-167">找不到包</span><span class="sxs-lookup"><span data-stu-id="89d4a-167">Unable to find package</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

### <a name="failed-to-fetch"></a><span data-ttu-id="89d4a-168">未能提取</span><span class="sxs-lookup"><span data-stu-id="89d4a-168">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-rpm](includes/package-manager-failed-to-fetch-rpm.md)]

## <a name="snap"></a><span data-ttu-id="89d4a-169">Snap</span><span class="sxs-lookup"><span data-stu-id="89d4a-169">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="89d4a-170">依赖项</span><span class="sxs-lookup"><span data-stu-id="89d4a-170">Dependencies</span></span>

[!INCLUDE [linux-rpm-install-dependencies](includes/linux-rpm-install-dependencies.md)]

## <a name="scripted-install"></a><span data-ttu-id="89d4a-171">脚本安装</span><span class="sxs-lookup"><span data-stu-id="89d4a-171">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="89d4a-172">手动安装</span><span class="sxs-lookup"><span data-stu-id="89d4a-172">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="89d4a-173">后续步骤</span><span class="sxs-lookup"><span data-stu-id="89d4a-173">Next steps</span></span>

- [<span data-ttu-id="89d4a-174">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="89d4a-174">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
