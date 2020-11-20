---
title: 在 RHEL 上安装 .NET - .NET
description: 演示在 RHEL 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: cb03f84cf84557d467f0a067b8d5629a843ec7e3
ms.sourcegitcommit: c38bf879a2611ff46aacdd529b9f2725f93e18a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "94594564"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-rhel"></a><span data-ttu-id="dce37-103">在 RHEL 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="dce37-103">Install the .NET SDK or the .NET Runtime on RHEL</span></span>

<span data-ttu-id="dce37-104">RHEL 支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="dce37-104">.NET is supported on RHEL.</span></span> <span data-ttu-id="dce37-105">本文介绍如何在 RHEL 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="dce37-105">This article describes how to install .NET on RHEL.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

## <a name="register-your-red-hat-subscription"></a><span data-ttu-id="dce37-106">注册 Red Hat 订阅</span><span class="sxs-lookup"><span data-stu-id="dce37-106">Register your Red Hat subscription</span></span>

<span data-ttu-id="dce37-107">若要在 RHEL 上从 Red Hat 安装 .NET，首先需要使用 Red Hat 订阅管理器进行注册。</span><span class="sxs-lookup"><span data-stu-id="dce37-107">To install .NET from Red Hat on RHEL, you first need to register using the Red Hat Subscription Manager.</span></span> <span data-ttu-id="dce37-108">如果未在系统上完成此操作，或者不确定是否完成了此操作，请参阅[适用于 .NET 的 Red Hat 产品文档](https://access.redhat.com/documentation/net/5.0/)。</span><span class="sxs-lookup"><span data-stu-id="dce37-108">If this hasn't been done on your system, or if you're unsure, see the [Red Hat Product Documentation for .NET](https://access.redhat.com/documentation/net/5.0/).</span></span>

## <a name="supported-distributions"></a><span data-ttu-id="dce37-109">支持的发行版</span><span class="sxs-lookup"><span data-stu-id="dce37-109">Supported distributions</span></span>

<span data-ttu-id="dce37-110">下表列出了 RHEL 7 和 RHEL 8 上当前受支持的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="dce37-110">The following table is a list of currently supported .NET releases on both RHEL 7 and RHEL 8.</span></span> <span data-ttu-id="dce37-111">这些版本在 [.NET 达到支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 RHEL 版本不再受到支持之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="dce37-111">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of RHEL is no longer supported.</span></span>

- <span data-ttu-id="dce37-112">✔️ 指示 RHEL 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="dce37-112">A ✔️ indicates that the version of RHEL or .NET is still supported.</span></span>
- <span data-ttu-id="dce37-113">❌ 指示 RHEL 或 .NET 版本在该 RHEL 版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="dce37-113">A ❌ indicates that the version of RHEL or .NET isn't supported on that RHEL release.</span></span>
- <span data-ttu-id="dce37-114">当 RHEL 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="dce37-114">When both a version of RHEL and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="dce37-115">RHEL</span><span class="sxs-lookup"><span data-stu-id="dce37-115">RHEL</span></span>                     | <span data-ttu-id="dce37-116">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="dce37-116">.NET Core 2.1</span></span> | <span data-ttu-id="dce37-117">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="dce37-117">.NET Core 3.1</span></span> | <span data-ttu-id="dce37-118">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="dce37-118">.NET 5.0</span></span> |
|--------------------------|---------------|---------------|----------------|
| <span data-ttu-id="dce37-119">✔️ [8](#rhel-8-)</span><span class="sxs-lookup"><span data-stu-id="dce37-119">✔️ [8](#rhel-8-)</span></span>        | <span data-ttu-id="dce37-120">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="dce37-120">✔️ 2.1</span></span>        | <span data-ttu-id="dce37-121">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="dce37-121">✔️ 3.1</span></span>        | <span data-ttu-id="dce37-122">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="dce37-122">✔️ 5.0</span></span> |
| <span data-ttu-id="dce37-123">✔️ [7](#rhel-7--net-50)</span><span class="sxs-lookup"><span data-stu-id="dce37-123">✔️ [7](#rhel-7--net-50)</span></span> | <span data-ttu-id="dce37-124">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="dce37-124">✔️ 2.1</span></span>        | <span data-ttu-id="dce37-125">✔️ [3.1](#rhel-7--net-core-31)</span><span class="sxs-lookup"><span data-stu-id="dce37-125">✔️ [3.1](#rhel-7--net-core-31)</span></span>        | <span data-ttu-id="dce37-126">✔️ [5.0](#rhel-7--net-50)</span><span class="sxs-lookup"><span data-stu-id="dce37-126">✔️ [5.0](#rhel-7--net-50)</span></span> |

<span data-ttu-id="dce37-127">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="dce37-127">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="dce37-128">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="dce37-128">The downloads for these still remain published:</span></span>

- <span data-ttu-id="dce37-129">3.0</span><span class="sxs-lookup"><span data-stu-id="dce37-129">3.0</span></span>
- <span data-ttu-id="dce37-130">2.2</span><span class="sxs-lookup"><span data-stu-id="dce37-130">2.2</span></span>
- <span data-ttu-id="dce37-131">2.0</span><span class="sxs-lookup"><span data-stu-id="dce37-131">2.0</span></span>

## <a name="how-to-install-other-versions"></a><span data-ttu-id="dce37-132">如何安装其他版本</span><span class="sxs-lookup"><span data-stu-id="dce37-132">How to install other versions</span></span>

<span data-ttu-id="dce37-133">有关安装其他版本的 .NET 所需的步骤，请参阅[适用于 .NET 的 Red Hat 文档](https://access.redhat.com/documentation/net/5.0/)。</span><span class="sxs-lookup"><span data-stu-id="dce37-133">Consult the [Red Hat documentation for .NET](https://access.redhat.com/documentation/net/5.0/) on the steps required to install other releases of .NET.</span></span>

## <a name="rhel-8-"></a><span data-ttu-id="dce37-134">RHEL 8 ✔️</span><span class="sxs-lookup"><span data-stu-id="dce37-134">RHEL 8 ✔️</span></span>

> [!TIP]
> <span data-ttu-id="dce37-135">.NET 5.0 在 AppStream 存储库中尚不可用，但 .NET Core 3.1 可用。</span><span class="sxs-lookup"><span data-stu-id="dce37-135">.NET 5.0 isn't yet available in the AppStream repositories, but .NET Core 3.1 is.</span></span> <span data-ttu-id="dce37-136">若要安装 .NET Core 3.1，请对相应的包（如 `aspnetcore-runtime-3.1` 或 `dotnet-sdk-3.1`）使用 `dnf install` 命令。</span><span class="sxs-lookup"><span data-stu-id="dce37-136">To install .NET Core 3.1, use the `dnf install` command with the appropriate package, such as `aspnetcore-runtime-3.1` or `dotnet-sdk-3.1`.</span></span> <span data-ttu-id="dce37-137">下列说明适用于 .NET 5.0。</span><span class="sxs-lookup"><span data-stu-id="dce37-137">The following instructions are for .NET 5.0.</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/rhel/8/prod.repo
```

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-dnf.md)]

## <a name="rhel-7--net-50"></a><span data-ttu-id="dce37-138">RHEL 7 ✔️ .NET 5.0</span><span class="sxs-lookup"><span data-stu-id="dce37-138">RHEL 7 ✔️ .NET 5.0</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo wget -O /etc/yum.repos.d/microsoft-prod.repo https://packages.microsoft.com/config/rhel/7/prod.repo
```

[!INCLUDE [linux-dnf-install-50](includes/linux-install-50-yum.md)]

## <a name="rhel-7--net-core-31"></a><span data-ttu-id="dce37-139">RHEL 7 ✔️ .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="dce37-139">RHEL 7 ✔️ .NET Core 3.1</span></span>

[!INCLUDE [linux-prep-intro-generic](includes/linux-prep-intro-generic.md)]

<span data-ttu-id="dce37-140">以下命令安装 `scl-utils` 包：</span><span class="sxs-lookup"><span data-stu-id="dce37-140">The following command installs the `scl-utils` package:</span></span>

```bash
sudo yum install scl-utils
```

### <a name="install-the-sdk"></a><span data-ttu-id="dce37-141">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="dce37-141">Install the SDK</span></span>

<span data-ttu-id="dce37-142">.NET Core SDK 使你可以通过 .NET Core 开发应用。</span><span class="sxs-lookup"><span data-stu-id="dce37-142">.NET Core SDK allows you to develop apps with .NET Core.</span></span> <span data-ttu-id="dce37-143">如果安装 .NET Core SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="dce37-143">If you install .NET Core SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="dce37-144">若要安装 .NET Core SDK，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="dce37-144">To install .NET Core SDK, run the following commands:</span></span>

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31 -y
scl enable rh-dotnet31 bash
```

<span data-ttu-id="dce37-145">Red Hat 建议不要永久启用 `rh-dotnet31`，因为这可能会影响其他程序。</span><span class="sxs-lookup"><span data-stu-id="dce37-145">Red Hat does not recommend permanently enabling `rh-dotnet31` because it may affect other programs.</span></span> <span data-ttu-id="dce37-146">例如，`rh-dotnet31` 包括与基本 RHEL 版本不同的 `libcurl` 版本。</span><span class="sxs-lookup"><span data-stu-id="dce37-146">For example, `rh-dotnet31` includes a version of `libcurl` that differs from the base RHEL version.</span></span> <span data-ttu-id="dce37-147">这可能会导致不需要不同版本的 `libcurl` 的程序出现问题。</span><span class="sxs-lookup"><span data-stu-id="dce37-147">This may lead to issues in programs that do not expect a different version of `libcurl`.</span></span> <span data-ttu-id="dce37-148">如果要永久启用 `rh-dotnet`，请将以下行添加到 ~/.bashrc 文件中。</span><span class="sxs-lookup"><span data-stu-id="dce37-148">If you want to enable `rh-dotnet` permanently, add the following line to your _~/.bashrc_ file.</span></span>

```bash
source scl_source enable rh-dotnet31
```

### <a name="install-the-runtime"></a><span data-ttu-id="dce37-149">安装运行时</span><span class="sxs-lookup"><span data-stu-id="dce37-149">Install the runtime</span></span>

<span data-ttu-id="dce37-150">.NET Core 运行时允许运行使用不随附运行时的 .NET Core 所开发的应用。</span><span class="sxs-lookup"><span data-stu-id="dce37-150">The .NET Core Runtime allows you to run apps that were made with .NET Core that didn't include the runtime.</span></span> <span data-ttu-id="dce37-151">以下命令安装 ASP.NET Core 运行时，这是与 .NET Core 最兼容的运行时。</span><span class="sxs-lookup"><span data-stu-id="dce37-151">The commands below install the ASP.NET Core Runtime, which is the most compatible runtime for .NET Core.</span></span> <span data-ttu-id="dce37-152">在终端中，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="dce37-152">In your terminal, run the following commands.</span></span>

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31-aspnetcore-runtime-3.1 -y
scl enable rh-dotnet31-aspnetcore-runtime-3.1 bash
```

<span data-ttu-id="dce37-153">Red Hat 建议不要永久启用 `rh-dotnet31-aspnetcore-runtime-3.1`，因为这可能会影响其他程序。</span><span class="sxs-lookup"><span data-stu-id="dce37-153">Red Hat does not recommend permanently enabling `rh-dotnet31-aspnetcore-runtime-3.1` because it may affect other programs.</span></span> <span data-ttu-id="dce37-154">例如，`rh-dotnet31-aspnetcore-runtime-3.1` 包括与基本 RHEL 版本不同的 `libcurl` 版本。</span><span class="sxs-lookup"><span data-stu-id="dce37-154">For example, `rh-dotnet31-aspnetcore-runtime-3.1` includes a version of `libcurl` that differs from the base RHEL version.</span></span> <span data-ttu-id="dce37-155">这可能会导致不需要不同版本的 `libcurl` 的程序出现问题。</span><span class="sxs-lookup"><span data-stu-id="dce37-155">This may lead to issues in programs that do not expect a different version of `libcurl`.</span></span> <span data-ttu-id="dce37-156">如果要永久启用 `rh-dotnet31-aspnetcore-runtime-3.1`，请将以下行添加到 ~/.bashrc 文件中。</span><span class="sxs-lookup"><span data-stu-id="dce37-156">If you want to enable `rh-dotnet31-aspnetcore-runtime-3.1` permanently, add the following line to your _~/.bashrc_ file.</span></span>

```bash
source scl_source enable rh-dotnet31-aspnetcore-runtime-3.1
```

<span data-ttu-id="dce37-157">作为 ASP.NET Core 运行时的一种替代方法，你可以安装不包含 ASP.NET Core 支持的 .NET Core 运行时：将上述命令中的 `rh-dotnet31-aspnetcore-runtime-3.1` 替换为 `rh-dotnet31-dotnet-runtime-3.1`。</span><span class="sxs-lookup"><span data-stu-id="dce37-157">As an alternative to the ASP.NET Core Runtime, you can install the .NET Core Runtime that doesn't include ASP.NET Core support: replace `rh-dotnet31-aspnetcore-runtime-3.1` in the commands above with `rh-dotnet31-dotnet-runtime-3.1`.</span></span>

## <a name="snap"></a><span data-ttu-id="dce37-158">Snap</span><span class="sxs-lookup"><span data-stu-id="dce37-158">Snap</span></span>

[!INCLUDE [linux-install-snap](includes/linux-install-snap.md)]

## <a name="dependencies"></a><span data-ttu-id="dce37-159">依赖项</span><span class="sxs-lookup"><span data-stu-id="dce37-159">Dependencies</span></span>

[!INCLUDE [linux-rpm-install-dependencies](includes/linux-rpm-install-dependencies.md)]

## <a name="scripted-install"></a><span data-ttu-id="dce37-160">脚本安装</span><span class="sxs-lookup"><span data-stu-id="dce37-160">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="dce37-161">手动安装</span><span class="sxs-lookup"><span data-stu-id="dce37-161">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="dce37-162">后续步骤</span><span class="sxs-lookup"><span data-stu-id="dce37-162">Next steps</span></span>

- [<span data-ttu-id="dce37-163">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="dce37-163">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
