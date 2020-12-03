---
title: 在 openSUSE 上安装 .NET - .NET
description: 演示在 openSUSE 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: eb31e3109ccd40999c22a27607d48544bf117dc2
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031860"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-opensuse"></a><span data-ttu-id="69110-103">在 openSUSE 上安装 .NET SDK 或 .NET Runtime</span><span class="sxs-lookup"><span data-stu-id="69110-103">Install the .NET SDK or the .NET Runtime on openSUSE</span></span>

<span data-ttu-id="69110-104">openSUSE 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="69110-104">.NET is supported on openSUSE.</span></span> <span data-ttu-id="69110-105">本文介绍如何在 openSUSE 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="69110-105">This article describes how to install .NET on openSUSE.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

## <a name="supported-distributions"></a><span data-ttu-id="69110-106">支持的分发</span><span class="sxs-lookup"><span data-stu-id="69110-106">Supported distributions</span></span>

<span data-ttu-id="69110-107">下表列出了 openSUSE 15 上当前受支持的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="69110-107">The following table is a list of currently supported .NET releases on openSUSE 15.</span></span> <span data-ttu-id="69110-108">这些版本在 [.NET 版本达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 openSUSE 版本不再受支持之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="69110-108">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of openSUSE is no longer supported.</span></span>

- <span data-ttu-id="69110-109">✔️ 指示 openSUSE 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="69110-109">A ✔️ indicates that the version of openSUSE or .NET is still supported.</span></span>
- <span data-ttu-id="69110-110">❌ 指示 openSUSE 或 .NET 版本在该 openSUSE 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="69110-110">A ❌ indicates that the version of openSUSE or .NET isn't supported on that openSUSE release.</span></span>
- <span data-ttu-id="69110-111">当 openSUSE 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="69110-111">When both a version of openSUSE and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="69110-112">openSUSE</span><span class="sxs-lookup"><span data-stu-id="69110-112">openSUSE</span></span>                   | <span data-ttu-id="69110-113">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="69110-113">.NET Core 2.1</span></span> | <span data-ttu-id="69110-114">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="69110-114">.NET Core 3.1</span></span> | <span data-ttu-id="69110-115">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="69110-115">.NET 5.0</span></span> |
|----------------------------|---------------|---------------|----------------|
| <span data-ttu-id="69110-116">✔️ [15](#opensuse-15-)</span><span class="sxs-lookup"><span data-stu-id="69110-116">✔️ [15](#opensuse-15-)</span></span>     | <span data-ttu-id="69110-117">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="69110-117">✔️ 2.1</span></span>        | <span data-ttu-id="69110-118">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="69110-118">✔️ 3.1</span></span>        | <span data-ttu-id="69110-119">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="69110-119">✔️ 5.0</span></span> |

<span data-ttu-id="69110-120">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="69110-120">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="69110-121">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="69110-121">The downloads for these still remain published:</span></span>

- <span data-ttu-id="69110-122">3.0</span><span class="sxs-lookup"><span data-stu-id="69110-122">3.0</span></span>
- <span data-ttu-id="69110-123">2.2</span><span class="sxs-lookup"><span data-stu-id="69110-123">2.2</span></span>
- <span data-ttu-id="69110-124">2.0</span><span class="sxs-lookup"><span data-stu-id="69110-124">2.0</span></span>

## <a name="remove-preview-versions"></a><span data-ttu-id="69110-125">删除预览版本</span><span class="sxs-lookup"><span data-stu-id="69110-125">Remove preview versions</span></span>

[!INCLUDE [package-manager uninstall notice](./includes/linux-uninstall-preview-info.md)]

## <a name="how-to-install-other-versions"></a><span data-ttu-id="69110-126">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="69110-126">How to install other versions</span></span>

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="opensuse-15-"></a><span data-ttu-id="69110-127">openSUSE 15 ✔️</span><span class="sxs-lookup"><span data-stu-id="69110-127">openSUSE 15 ✔️</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo zypper install libicu
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
wget https://packages.microsoft.com/config/opensuse/15/prod.repo
sudo mv prod.repo /etc/zypp/repos.d/microsoft-prod.repo
sudo chown root:root /etc/zypp/repos.d/microsoft-prod.repo
```

[!INCLUDE [linux-zyp-install-50](includes/linux-install-50-zyp.md)]

## <a name="troubleshoot-the-package-manager"></a><span data-ttu-id="69110-128">包管理器疑难解答</span><span class="sxs-lookup"><span data-stu-id="69110-128">Troubleshoot the package manager</span></span>

<span data-ttu-id="69110-129">本部分提供有关使用包管理器安装 .NET 时可能会遇到的常见错误的信息。</span><span class="sxs-lookup"><span data-stu-id="69110-129">This section provides information on common errors you may get while using the package manager to install .NET.</span></span>

### <a name="unable-to-find-package"></a><span data-ttu-id="69110-130">找不到包</span><span class="sxs-lookup"><span data-stu-id="69110-130">Unable to find package</span></span>

[!INCLUDE [linux-install-package-manager-x64-vs-arm](includes/linux-install-package-manager-x64-vs-arm.md)]

### <a name="failed-to-fetch"></a><span data-ttu-id="69110-131">未能提取</span><span class="sxs-lookup"><span data-stu-id="69110-131">Failed to fetch</span></span>

[!INCLUDE [package-manager-failed-to-fetch-rpm](includes/package-manager-failed-to-fetch-rpm.md)]

## <a name="snap"></a><span data-ttu-id="69110-132">对齐</span><span class="sxs-lookup"><span data-stu-id="69110-132">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="69110-133">依赖项</span><span class="sxs-lookup"><span data-stu-id="69110-133">Dependencies</span></span>

<span data-ttu-id="69110-134">使用包管理器进行安装时，将为你安装这些库。</span><span class="sxs-lookup"><span data-stu-id="69110-134">When you install with a package manager, these libraries are installed for you.</span></span> <span data-ttu-id="69110-135">但是，如果手动安装 .NET 或发布自包含的应用，则需要确保已安装以下库：</span><span class="sxs-lookup"><span data-stu-id="69110-135">But, if you manually install .NET or you publish a self-contained app, you'll need to make sure these libraries are installed:</span></span>

- <span data-ttu-id="69110-136">krb5</span><span class="sxs-lookup"><span data-stu-id="69110-136">krb5</span></span>
- <span data-ttu-id="69110-137">libicu</span><span class="sxs-lookup"><span data-stu-id="69110-137">libicu</span></span>
- <span data-ttu-id="69110-138">libopenssl1_0_0</span><span class="sxs-lookup"><span data-stu-id="69110-138">libopenssl1_0_0</span></span>

<span data-ttu-id="69110-139">如果目标运行时环境的 OpenSSL 版本为1.1 或更高版本，则需要安装 compat-openssl10。</span><span class="sxs-lookup"><span data-stu-id="69110-139">If the target runtime environment's OpenSSL version is 1.1 or newer, you'll need to install **compat-openssl10**.</span></span>

<span data-ttu-id="69110-140">有关依赖项的详细信息，请参阅[独立式 Linux 应用](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="69110-140">For more information about the dependencies, see [Self-contained Linux apps](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md).</span></span>

<span data-ttu-id="69110-141">对于使用 System.Drawing.Common 程序集的 .NET 应用，还需要以下依赖项：</span><span class="sxs-lookup"><span data-stu-id="69110-141">For .NET apps that use the *System.Drawing.Common* assembly, you'll also need the following dependency:</span></span>

- [<span data-ttu-id="69110-142">libgdiplus（版本 6.0.1 或更高版本）</span><span class="sxs-lookup"><span data-stu-id="69110-142">libgdiplus (version 6.0.1 or later)</span></span>](https://www.mono-project.com/docs/gui/libgdiplus/)

  > [!WARNING]
  > <span data-ttu-id="69110-143">可以通过将 Mono 存储库添加到系统来安装最新版 libgdiplus。</span><span class="sxs-lookup"><span data-stu-id="69110-143">You can install a recent version of *libgdiplus* by adding the Mono repository to your system.</span></span> <span data-ttu-id="69110-144">有关详细信息，请参阅 <https://www.mono-project.com/download/stable/>。</span><span class="sxs-lookup"><span data-stu-id="69110-144">For more information, see <https://www.mono-project.com/download/stable/>.</span></span>

## <a name="scripted-install"></a><span data-ttu-id="69110-145">脚本安装</span><span class="sxs-lookup"><span data-stu-id="69110-145">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="69110-146">手动安装</span><span class="sxs-lookup"><span data-stu-id="69110-146">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="69110-147">后续步骤</span><span class="sxs-lookup"><span data-stu-id="69110-147">Next steps</span></span>

- [<span data-ttu-id="69110-148">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="69110-148">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
