---
title: 在 Ubuntu 上安装 .NET - .NET
description: 演示在 Ubuntu 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: 22ce3379e028f065528e1f507a2d8c1ae598f0e8
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031836"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-ubuntu"></a><span data-ttu-id="f651e-103">在 Ubuntu 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="f651e-103">Install the .NET SDK or the .NET Runtime on Ubuntu</span></span>

<span data-ttu-id="f651e-104">Ubuntu 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="f651e-104">.NET is supported on Ubuntu.</span></span> <span data-ttu-id="f651e-105">本文介绍如何在 Ubuntu 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="f651e-105">This article describes how to install .NET on Ubuntu.</span></span> <span data-ttu-id="f651e-106">如果 Ubuntu 版本不受支持，则该版本不再支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="f651e-106">When an Ubuntu version falls out of support, .NET is no longer supported with that version.</span></span> <span data-ttu-id="f651e-107">不过，可以按照这些说明在这些版本上运行 .NET，即使它不受支持。</span><span class="sxs-lookup"><span data-stu-id="f651e-107">However, these instructions may help you to get .NET running on those versions, even though it isn't supported.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="f651e-108">支持的分发</span><span class="sxs-lookup"><span data-stu-id="f651e-108">Supported distributions</span></span>

<span data-ttu-id="f651e-109">下表列出了当前支持的 .NET 版本以及支持它们的 Ubuntu 版本。</span><span class="sxs-lookup"><span data-stu-id="f651e-109">The following table is a list of currently supported .NET releases and the versions of Ubuntu they're supported on.</span></span> <span data-ttu-id="f651e-110">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Ubuntu 的版本达到生命周期](https://wiki.ubuntu.com/Releases)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="f651e-110">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Ubuntu reaches end-of-life](https://wiki.ubuntu.com/Releases).</span></span>

- <span data-ttu-id="f651e-111">✔️ 指示 Ubuntu 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="f651e-111">A ✔️ indicates that the version of Ubuntu or .NET is still supported.</span></span>
- <span data-ttu-id="f651e-112">❌ 指示 Ubuntu 或 .NET 版本在该 Ubuntu 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="f651e-112">A ❌ indicates that the version of Ubuntu or .NET isn't supported on that Ubuntu release.</span></span>
- <span data-ttu-id="f651e-113">当 Ubuntu 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="f651e-113">When both a version of Ubuntu and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="f651e-114">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="f651e-114">Ubuntu</span></span>                   | <span data-ttu-id="f651e-115">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-115">.NET Core 2.1</span></span> | <span data-ttu-id="f651e-116">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-116">.NET Core 3.1</span></span> | <span data-ttu-id="f651e-117">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-117">.NET 5.0</span></span> |
|--------------------------|---------------|---------------|----------------|
| <span data-ttu-id="f651e-118">✔️ [20.10](#2010-)</span><span class="sxs-lookup"><span data-stu-id="f651e-118">✔️ [20.10](#2010-)</span></span>       | <span data-ttu-id="f651e-119">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-119">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-120">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-120">✔️ 3.1</span></span>        | <span data-ttu-id="f651e-121">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-121">✔️ 5.0</span></span> |
| <span data-ttu-id="f651e-122">✔️ [20.04 (LTS)](#2004-)</span><span class="sxs-lookup"><span data-stu-id="f651e-122">✔️ [20.04 (LTS)](#2004-)</span></span> | <span data-ttu-id="f651e-123">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-123">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-124">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-124">✔️ 3.1</span></span>        | <span data-ttu-id="f651e-125">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-125">✔️ 5.0</span></span> |
| <span data-ttu-id="f651e-126">❌ [19.10](#1910-)</span><span class="sxs-lookup"><span data-stu-id="f651e-126">❌ [19.10](#1910-)</span></span>       | <span data-ttu-id="f651e-127">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-127">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-128">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-128">✔️ 3.1</span></span>        | <span data-ttu-id="f651e-129">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-129">✔️ 5.0</span></span> |
| <span data-ttu-id="f651e-130">❌ [19.04](#1904-)</span><span class="sxs-lookup"><span data-stu-id="f651e-130">❌ [19.04](#1904-)</span></span>       | <span data-ttu-id="f651e-131">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-131">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-132">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-132">✔️ 3.1</span></span>        | <span data-ttu-id="f651e-133">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-133">❌ 5.0</span></span> |
| <span data-ttu-id="f651e-134">❌ [18.10](#1810-)</span><span class="sxs-lookup"><span data-stu-id="f651e-134">❌ [18.10](#1810-)</span></span>       | <span data-ttu-id="f651e-135">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-135">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-136">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-136">❌ 3.1</span></span>        | <span data-ttu-id="f651e-137">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-137">❌ 5.0</span></span> |
| <span data-ttu-id="f651e-138">✔️ [18.04 (LTS)](#1804-)</span><span class="sxs-lookup"><span data-stu-id="f651e-138">✔️ [18.04 (LTS)](#1804-)</span></span> | <span data-ttu-id="f651e-139">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-139">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-140">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-140">✔️ 3.1</span></span>        | <span data-ttu-id="f651e-141">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-141">✔️ 5.0</span></span> |
| <span data-ttu-id="f651e-142">❌ [17.10](#1710-)</span><span class="sxs-lookup"><span data-stu-id="f651e-142">❌ [17.10](#1710-)</span></span>       | <span data-ttu-id="f651e-143">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-143">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-144">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-144">❌ 3.1</span></span>        | <span data-ttu-id="f651e-145">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-145">❌ 5.0</span></span> |
| <span data-ttu-id="f651e-146">❌ [17.04](#1704-)</span><span class="sxs-lookup"><span data-stu-id="f651e-146">❌ [17.04](#1704-)</span></span>       | <span data-ttu-id="f651e-147">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-147">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-148">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-148">❌ 3.1</span></span>        | <span data-ttu-id="f651e-149">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-149">❌ 5.0</span></span> |
| <span data-ttu-id="f651e-150">❌ [16.10](#1610-)</span><span class="sxs-lookup"><span data-stu-id="f651e-150">❌ [16.10](#1610-)</span></span>       | <span data-ttu-id="f651e-151">❌ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-151">❌ 2.1</span></span>        | <span data-ttu-id="f651e-152">❌ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-152">❌ 3.1</span></span>        | <span data-ttu-id="f651e-153">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-153">❌ 5.0</span></span> |
| <span data-ttu-id="f651e-154">✔️ [16.04 (LTS)](#1604-)</span><span class="sxs-lookup"><span data-stu-id="f651e-154">✔️ [16.04 (LTS)](#1604-)</span></span> | <span data-ttu-id="f651e-155">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="f651e-155">✔️ 2.1</span></span>        | <span data-ttu-id="f651e-156">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="f651e-156">✔️ 3.1</span></span>        | <span data-ttu-id="f651e-157">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="f651e-157">✔️ 5.0</span></span> |

<span data-ttu-id="f651e-158">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="f651e-158">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="f651e-159">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="f651e-159">The downloads for these still remain published:</span></span>

- <span data-ttu-id="f651e-160">3.0</span><span class="sxs-lookup"><span data-stu-id="f651e-160">3.0</span></span>
- <span data-ttu-id="f651e-161">2.2</span><span class="sxs-lookup"><span data-stu-id="f651e-161">2.2</span></span>
- <span data-ttu-id="f651e-162">2.0</span><span class="sxs-lookup"><span data-stu-id="f651e-162">2.0</span></span>

## <a name="remove-preview-versions"></a><span data-ttu-id="f651e-163">删除预览版本</span><span class="sxs-lookup"><span data-stu-id="f651e-163">Remove preview versions</span></span>

[!INCLUDE [package-manager uninstall notice](./includes/linux-uninstall-preview-info.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="f651e-164">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="f651e-164">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="2010-"></a><span data-ttu-id="f651e-165">20.10 ✔️</span><span class="sxs-lookup"><span data-stu-id="f651e-165">20.10 ✔️</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f651e-166">.NET Core 2.1 在包源中尚不可用。</span><span class="sxs-lookup"><span data-stu-id="f651e-166">.NET Core 2.1 isn't yet available in the package feed.</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/20.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="2004-"></a><span data-ttu-id="f651e-167">20.04 ✔️</span><span class="sxs-lookup"><span data-stu-id="f651e-167">20.04 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="1910-"></a><span data-ttu-id="f651e-168">19.10 ❌</span><span class="sxs-lookup"><span data-stu-id="f651e-168">19.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/19.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-31](includes/linux-install-31-apt.md)]

## <a name="1904-"></a><span data-ttu-id="f651e-169">19.04 ❌</span><span class="sxs-lookup"><span data-stu-id="f651e-169">19.04 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/19.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-31](includes/linux-install-31-apt.md)]

## <a name="1810-"></a><span data-ttu-id="f651e-170">18.10 ❌</span><span class="sxs-lookup"><span data-stu-id="f651e-170">18.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/18.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1804-"></a><span data-ttu-id="f651e-171">18.04 ✔️</span><span class="sxs-lookup"><span data-stu-id="f651e-171">18.04 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="1710-"></a><span data-ttu-id="f651e-172">17.10 ❌</span><span class="sxs-lookup"><span data-stu-id="f651e-172">17.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/17.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1704-"></a><span data-ttu-id="f651e-173">17.04 ❌</span><span class="sxs-lookup"><span data-stu-id="f651e-173">17.04 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/17.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1610-"></a><span data-ttu-id="f651e-174">16.10 ❌</span><span class="sxs-lookup"><span data-stu-id="f651e-174">16.10 ❌</span></span>

[!INCLUDE [linux-not-supported](includes/linux-not-supported-ubuntu.md)]

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/16.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-21](includes/linux-install-21-apt.md)]

## <a name="1604-"></a><span data-ttu-id="f651e-175">16.04 ✔️</span><span class="sxs-lookup"><span data-stu-id="f651e-175">16.04 ✔️</span></span>

[!INCLUDE [linux-prep-intro-apt](includes/linux-prep-intro-apt.md)]

```bash
wget https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

[!INCLUDE [linux-apt-install-50](includes/linux-install-50-apt.md)]

## <a name="apt-update-sdk-or-runtime"></a><span data-ttu-id="f651e-176">APT 更新 SDK 或运行时</span><span class="sxs-lookup"><span data-stu-id="f651e-176">APT update SDK or runtime</span></span>

<span data-ttu-id="f651e-177">当新的修补程序版本适用于 .NET 时，只需使用以下命令通过 APT 进行升级：</span><span class="sxs-lookup"><span data-stu-id="f651e-177">When a new patch release is available for .NET, you can simply upgrade it through APT with the following commands:</span></span>

```bash
sudo apt-get update
sudo apt-get upgrade
```

## <a name="apt-troubleshooting"></a><span data-ttu-id="f651e-178">APT 疑难解答</span><span class="sxs-lookup"><span data-stu-id="f651e-178">APT troubleshooting</span></span>

<span data-ttu-id="f651e-179">本部分提供有关使用 APT 安装 .NET 时可能会遇到的常见错误的信息。</span><span class="sxs-lookup"><span data-stu-id="f651e-179">This section provides information on common errors you may get while using APT to install .NET.</span></span>

### <a name="unable-to-find-package"></a><span data-ttu-id="f651e-180">找不到包</span><span class="sxs-lookup"><span data-stu-id="f651e-180">Unable to find package</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

### <a name="unable-to-locate--some-packages-could-not-be-installed"></a><span data-ttu-id="f651e-181">找不到 \\ 无法安装某些包</span><span class="sxs-lookup"><span data-stu-id="f651e-181">Unable to locate \\ Some packages could not be installed</span></span>

[!INCLUDE [package-manager-failed-to-find-deb](includes/package-manager-failed-to-find-deb.md)]

```bash
sudo apt-get install -y gpg
wget -O - https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor -o microsoft.asc.gpg
sudo mv microsoft.asc.gpg /etc/apt/trusted.gpg.d/
wget https://packages.microsoft.com/config/ubuntu/{os-version}/prod.list
sudo mv prod.list /etc/apt/sources.list.d/microsoft-prod.list
sudo chown root:root /etc/apt/trusted.gpg.d/microsoft.asc.gpg
sudo chown root:root /etc/apt/sources.list.d/microsoft-prod.list
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y {dotnet-package}
```

### <a name="failed-to-fetch"></a><span data-ttu-id="f651e-182">未能提取</span><span class="sxs-lookup"><span data-stu-id="f651e-182">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-deb](includes/package-manager-failed-to-fetch-deb.md)]

## <a name="snap"></a><span data-ttu-id="f651e-183">对齐</span><span class="sxs-lookup"><span data-stu-id="f651e-183">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="f651e-184">依赖项</span><span class="sxs-lookup"><span data-stu-id="f651e-184">Dependencies</span></span>

<span data-ttu-id="f651e-185">使用包管理器进行安装时，将为你安装这些库。</span><span class="sxs-lookup"><span data-stu-id="f651e-185">When you install with a package manager, these libraries are installed for you.</span></span> <span data-ttu-id="f651e-186">但是，如果手动安装 .NET 或发布自包含的应用，则需要确保已安装以下库：</span><span class="sxs-lookup"><span data-stu-id="f651e-186">But, if you manually install .NET or you publish a self-contained app, you'll need to make sure these libraries are installed:</span></span>

- <span data-ttu-id="f651e-187">libc6</span><span class="sxs-lookup"><span data-stu-id="f651e-187">libc6</span></span>
- <span data-ttu-id="f651e-188">libgcc1</span><span class="sxs-lookup"><span data-stu-id="f651e-188">libgcc1</span></span>
- <span data-ttu-id="f651e-189">libgssapi-krb5-2</span><span class="sxs-lookup"><span data-stu-id="f651e-189">libgssapi-krb5-2</span></span>
- <span data-ttu-id="f651e-190">libicu52（针对 14.x）</span><span class="sxs-lookup"><span data-stu-id="f651e-190">libicu52 (for 14.x)</span></span>
- <span data-ttu-id="f651e-191">libicu55（针对 16.x）</span><span class="sxs-lookup"><span data-stu-id="f651e-191">libicu55 (for 16.x)</span></span>
- <span data-ttu-id="f651e-192">libicu60（针对 18.x）</span><span class="sxs-lookup"><span data-stu-id="f651e-192">libicu60 (for 18.x)</span></span>
- <span data-ttu-id="f651e-193">libicu66（适用于 20. x）</span><span class="sxs-lookup"><span data-stu-id="f651e-193">libicu66 (for 20.x)</span></span>
- <span data-ttu-id="f651e-194">libssl1.0.0（适用于 14.x、16.x）</span><span class="sxs-lookup"><span data-stu-id="f651e-194">libssl1.0.0 (for 14.x, 16.x)</span></span>
- <span data-ttu-id="f651e-195">libssl1.1（适用于18.x、20.x）</span><span class="sxs-lookup"><span data-stu-id="f651e-195">libssl1.1 (for 18.x, 20.x)</span></span>
- <span data-ttu-id="f651e-196">libstdc++6</span><span class="sxs-lookup"><span data-stu-id="f651e-196">libstdc++6</span></span>
- <span data-ttu-id="f651e-197">zlib1g</span><span class="sxs-lookup"><span data-stu-id="f651e-197">zlib1g</span></span>

<span data-ttu-id="f651e-198">对于使用 System.Drawing.Common 程序集的 .NET 应用，还需要以下依赖项：</span><span class="sxs-lookup"><span data-stu-id="f651e-198">For .NET apps that use the *System.Drawing.Common* assembly, you also need the following dependency:</span></span>

- <span data-ttu-id="f651e-199">libgdiplus（版本 6.0.1 或更高版本）</span><span class="sxs-lookup"><span data-stu-id="f651e-199">libgdiplus (version 6.0.1 or later)</span></span>

  > [!WARNING]
  > <span data-ttu-id="f651e-200">可以通过将 Mono 存储库添加到系统来安装最新版 libgdiplus。</span><span class="sxs-lookup"><span data-stu-id="f651e-200">You can install a recent version of *libgdiplus* by adding the Mono repository to your system.</span></span> <span data-ttu-id="f651e-201">有关详细信息，请参阅 <https://www.mono-project.com/download/stable/>。</span><span class="sxs-lookup"><span data-stu-id="f651e-201">For more information, see <https://www.mono-project.com/download/stable/>.</span></span>

## <a name="scripted-install"></a><span data-ttu-id="f651e-202">脚本安装</span><span class="sxs-lookup"><span data-stu-id="f651e-202">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="f651e-203">手动安装</span><span class="sxs-lookup"><span data-stu-id="f651e-203">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="f651e-204">后续步骤</span><span class="sxs-lookup"><span data-stu-id="f651e-204">Next steps</span></span>

- [<span data-ttu-id="f651e-205">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="f651e-205">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
