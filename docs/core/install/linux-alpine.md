---
title: 在 Alpine 上安装 .NET - .NET
description: 演示在 Alpine 上安装 .NET SDK 和 .NET 运行时的各种方式。
author: adegeo
ms.author: adegeo
ms.date: 11/10/2020
ms.openlocfilehash: 29901cc24ddd4bbe8200a36765ddd29f501394c0
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506793"
---
# <a name="install-the-net-sdk-or-the-net-runtime-on-alpine"></a><span data-ttu-id="6ce0f-103">在 Alpine 上安装 .NET SDK 或 .NET 运行时</span><span class="sxs-lookup"><span data-stu-id="6ce0f-103">Install the .NET SDK or the .NET Runtime on Alpine</span></span>

<span data-ttu-id="6ce0f-104">本文介绍如何在 Alpine 上安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-104">This article describes how to install .NET on Alpine.</span></span> <span data-ttu-id="6ce0f-105">如果 Alpine 版本不再受到支持，则该版本不再支持 .NET。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-105">When an Alpine version falls out of support, .NET is no longer supported with that version.</span></span> <span data-ttu-id="6ce0f-106">不过，可以按照这些说明在这些版本上运行 .NET，即使它不受支持。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-106">However, these instructions may help you to get .NET running on those versions, even though it isn't supported.</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

<span data-ttu-id="6ce0f-107">Alpine 没有安装程序。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-107">There are no installers for Alpine.</span></span> <span data-ttu-id="6ce0f-108">必须使用[安装脚本](#scripted-install)或按照[手动安装](#manual-install)说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-108">You must either use the [install script](#scripted-install) or follow the [manual install](#manual-install) instructions.</span></span>

## <a name="supported-distributions"></a><span data-ttu-id="6ce0f-109">支持的发行版</span><span class="sxs-lookup"><span data-stu-id="6ce0f-109">Supported distributions</span></span>

<span data-ttu-id="6ce0f-110">下表列出了当前支持的 .NET 版本以及支持它们的 Alpine 版本。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-110">The following table is a list of currently supported .NET releases and the versions of Alpine they're supported on.</span></span> <span data-ttu-id="6ce0f-111">这些版本在 [.NET 到达支持终止日期](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)或 [Alpine 的版本到达有效期](https://wiki.alpinelinux.org/wiki/Alpine_Linux:Releases)之前仍受支持。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-111">These versions remain supported until either the version of [.NET reaches end-of-support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) or the version of [Alpine reaches end-of-life](https://wiki.alpinelinux.org/wiki/Alpine_Linux:Releases).</span></span>

- <span data-ttu-id="6ce0f-112">✔️ 指示 Alpine 或 .NET 版本仍受支持。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-112">A ✔️ indicates that the version of Alpine or .NET is still supported.</span></span>
- <span data-ttu-id="6ce0f-113">❌ 指示 Alpine 或 .NET 版本在该 Alpine 发行版本上不受支持。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-113">A ❌ indicates that the version of Alpine or .NET isn't supported on that Alpine release.</span></span>
- <span data-ttu-id="6ce0f-114">当 Alpine 版本和 .NET 版本都有 ✔️ 时，将支持该 OS 和 .NET 组合。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-114">When both a version of Alpine and a version of .NET have ✔️, that OS and .NET combination is supported.</span></span>

| <span data-ttu-id="6ce0f-115">Alpine</span><span class="sxs-lookup"><span data-stu-id="6ce0f-115">Alpine</span></span>  | <span data-ttu-id="6ce0f-116">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-116">.NET Core 2.1</span></span> | <span data-ttu-id="6ce0f-117">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-117">.NET Core 3.1</span></span> | <span data-ttu-id="6ce0f-118">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-118">.NET 5.0</span></span> |
|-------- |---------------|---------------|----------------|
| <span data-ttu-id="6ce0f-119">✔️ 3.12</span><span class="sxs-lookup"><span data-stu-id="6ce0f-119">✔️ 3.12</span></span> | <span data-ttu-id="6ce0f-120">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-120">✔️ 2.1</span></span>        | <span data-ttu-id="6ce0f-121">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-121">✔️ 3.1</span></span>        | <span data-ttu-id="6ce0f-122">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-122">✔️ 5.0</span></span> |
| <span data-ttu-id="6ce0f-123">✔️ 3.11</span><span class="sxs-lookup"><span data-stu-id="6ce0f-123">✔️ 3.11</span></span> | <span data-ttu-id="6ce0f-124">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-124">✔️ 2.1</span></span>        | <span data-ttu-id="6ce0f-125">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-125">✔️ 3.1</span></span>        | <span data-ttu-id="6ce0f-126">✔️ 5.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-126">✔️ 5.0</span></span> |
| <span data-ttu-id="6ce0f-127">✔️ 3.10</span><span class="sxs-lookup"><span data-stu-id="6ce0f-127">✔️ 3.10</span></span> | <span data-ttu-id="6ce0f-128">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-128">✔️ 2.1</span></span>        | <span data-ttu-id="6ce0f-129">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-129">✔️ 3.1</span></span>        | <span data-ttu-id="6ce0f-130">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-130">❌ 5.0</span></span> |
| <span data-ttu-id="6ce0f-131">❌ 3.9</span><span class="sxs-lookup"><span data-stu-id="6ce0f-131">❌ 3.9</span></span>  | <span data-ttu-id="6ce0f-132">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-132">✔️ 2.1</span></span>        | <span data-ttu-id="6ce0f-133">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-133">✔️ 3.1</span></span>        | <span data-ttu-id="6ce0f-134">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-134">❌ 5.0</span></span> |
| <span data-ttu-id="6ce0f-135">❌ 3.8</span><span class="sxs-lookup"><span data-stu-id="6ce0f-135">❌ 3.8</span></span>  | <span data-ttu-id="6ce0f-136">✔️ 2.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-136">✔️ 2.1</span></span>        | <span data-ttu-id="6ce0f-137">✔️ 3.1</span><span class="sxs-lookup"><span data-stu-id="6ce0f-137">✔️ 3.1</span></span>        | <span data-ttu-id="6ce0f-138">❌ 5.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-138">❌ 5.0</span></span> |

<span data-ttu-id="6ce0f-139">以下 .NET 版本不再受到支持。</span><span class="sxs-lookup"><span data-stu-id="6ce0f-139">The following versions of .NET are no longer supported.</span></span> <span data-ttu-id="6ce0f-140">这些版本的下载仍保持发布状态：</span><span class="sxs-lookup"><span data-stu-id="6ce0f-140">The downloads for these still remain published:</span></span>

- <span data-ttu-id="6ce0f-141">3.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-141">3.0</span></span>
- <span data-ttu-id="6ce0f-142">2.2</span><span class="sxs-lookup"><span data-stu-id="6ce0f-142">2.2</span></span>
- <span data-ttu-id="6ce0f-143">2.0</span><span class="sxs-lookup"><span data-stu-id="6ce0f-143">2.0</span></span>

## <a name="dependencies"></a><span data-ttu-id="6ce0f-144">依赖项</span><span class="sxs-lookup"><span data-stu-id="6ce0f-144">Dependencies</span></span>

<span data-ttu-id="6ce0f-145">Alpine Linux 上的 .NET 要求安装以下依赖项：</span><span class="sxs-lookup"><span data-stu-id="6ce0f-145">.NET on Alpine Linux requires the following dependencies installed:</span></span>

- <span data-ttu-id="6ce0f-146">icu-libs</span><span class="sxs-lookup"><span data-stu-id="6ce0f-146">icu-libs</span></span>
- <span data-ttu-id="6ce0f-147">krb5-libs</span><span class="sxs-lookup"><span data-stu-id="6ce0f-147">krb5-libs</span></span>
- <span data-ttu-id="6ce0f-148">libgcc</span><span class="sxs-lookup"><span data-stu-id="6ce0f-148">libgcc</span></span>
- <span data-ttu-id="6ce0f-149">libintl</span><span class="sxs-lookup"><span data-stu-id="6ce0f-149">libintl</span></span>
- <span data-ttu-id="6ce0f-150">libssl1.1（Alpine v3.9 或更高版本）</span><span class="sxs-lookup"><span data-stu-id="6ce0f-150">libssl1.1 (Alpine v3.9 or greater)</span></span>
- <span data-ttu-id="6ce0f-151">libssl1.0（Alpine v3.8 或更低版本）</span><span class="sxs-lookup"><span data-stu-id="6ce0f-151">libssl1.0 (Alpine v3.8 or lower)</span></span>
- <span data-ttu-id="6ce0f-152">libstdc++</span><span class="sxs-lookup"><span data-stu-id="6ce0f-152">libstdc++</span></span>
- <span data-ttu-id="6ce0f-153">zlib</span><span class="sxs-lookup"><span data-stu-id="6ce0f-153">zlib</span></span>

## <a name="scripted-install"></a><span data-ttu-id="6ce0f-154">脚本安装</span><span class="sxs-lookup"><span data-stu-id="6ce0f-154">Scripted install</span></span>

[!INCLUDE [linux-install-scripted](includes/linux-install-scripted.md)]

## <a name="manual-install"></a><span data-ttu-id="6ce0f-155">手动安装</span><span class="sxs-lookup"><span data-stu-id="6ce0f-155">Manual install</span></span>

[!INCLUDE [linux-install-manual](includes/linux-install-manual.md)]

## <a name="next-steps"></a><span data-ttu-id="6ce0f-156">后续步骤</span><span class="sxs-lookup"><span data-stu-id="6ce0f-156">Next steps</span></span>

- [<span data-ttu-id="6ce0f-157">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="6ce0f-157">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
