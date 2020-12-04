---
title: .NET 中的工具和诊断
author: IEvangelist
description: 了解 .NET 开发人员可用的开发和诊断工具。
ms.author: dapine
ms.date: 10/21/2020
ms.topic: overview
ms.openlocfilehash: 07c1a161a0bb429403db6852fe77749d83c19ec0
ms.sourcegitcommit: 98d20cb038669dca4a195eb39af37d22ea9d008e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2020
ms.locfileid: "96590987"
---
# <a name="tools-and-diagnostics-in-net"></a><span data-ttu-id="72801-103">.NET 中的工具和诊断</span><span class="sxs-lookup"><span data-stu-id="72801-103">Tools and diagnostics in .NET</span></span>

<span data-ttu-id="72801-104">在本文中，你将了解 .NET 开发人员可用的各种工具。</span><span class="sxs-lookup"><span data-stu-id="72801-104">In this article, you'll learn about the various tools available to .NET developers.</span></span> <span data-ttu-id="72801-105">借助 .NET，你有一个强大的软件开发工具包 (SDK) ，其中包含命令行接口 (CLI) 。</span><span class="sxs-lookup"><span data-stu-id="72801-105">With .NET, you have a robust software development kit (SDK) that includes a command-line interface (CLI).</span></span> <span data-ttu-id="72801-106">.NET CLI 可实现中的许多功能。 (Ide) 的已准备好的集成开发环境。</span><span class="sxs-lookup"><span data-stu-id="72801-106">The .NET CLI enables many of the features throughout the .NET-ready integrated development environments (IDEs).</span></span> <span data-ttu-id="72801-107">本文还提供了工作效率功能的资源，例如用于诊断性能问题的 .NET CLI 工具、内存泄漏、高 CPU、死锁和工具对代码分析的支持。</span><span class="sxs-lookup"><span data-stu-id="72801-107">This article also provides resources to productivity capabilities, such as .NET CLI tools for diagnosing performance issues, memory leaks, high CPU, deadlocks, and tooling support for code analysis.</span></span>

## <a name="net-sdk"></a><span data-ttu-id="72801-108">.NET SDK</span><span class="sxs-lookup"><span data-stu-id="72801-108">.NET SDK</span></span>

<span data-ttu-id="72801-109">.NET SDK 包括 .NET 运行时和 .NET CLI。</span><span class="sxs-lookup"><span data-stu-id="72801-109">The .NET SDK includes both the .NET Runtime and the .NET CLI.</span></span> <span data-ttu-id="72801-110">可以下载适用于 Windows、Linux、macOS 或 Docker 的 [.NET SDK](https://dotnet.microsoft.com/download) 。</span><span class="sxs-lookup"><span data-stu-id="72801-110">You can download the [.NET SDK](https://dotnet.microsoft.com/download) for Windows, Linux, macOS, or Docker.</span></span> <span data-ttu-id="72801-111">有关详细信息，请参阅 [.NET SDK 概述](../core/sdk.md)。</span><span class="sxs-lookup"><span data-stu-id="72801-111">For more information, see [.NET SDK overview](../core/sdk.md).</span></span>

## <a name="net-cli"></a><span data-ttu-id="72801-112">.NET CLI</span><span class="sxs-lookup"><span data-stu-id="72801-112">.NET CLI</span></span>

<span data-ttu-id="72801-113">.NET CLI 是一个跨平台的工具链，用于开发、构建、运行和发布 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="72801-113">The .NET CLI is a cross-platform toolchain for developing, building, running, and publishing .NET applications.</span></span> <span data-ttu-id="72801-114">.NET CLI 附带了 .NET SDK。</span><span class="sxs-lookup"><span data-stu-id="72801-114">The .NET CLI is included with the .NET SDK.</span></span> <span data-ttu-id="72801-115">有关详细信息，请参阅 [.NET CLI 概述](../core/tools/index.md)。</span><span class="sxs-lookup"><span data-stu-id="72801-115">For more information, see [.NET CLI overview](../core/tools/index.md).</span></span>

## <a name="ides"></a><span data-ttu-id="72801-116">IDE</span><span class="sxs-lookup"><span data-stu-id="72801-116">IDEs</span></span>

<span data-ttu-id="72801-117">可以在 [Visual Studio Code](https://code.visualstudio.com/docs)、 [Visual Studio](/visualstudio/windows)或 [Visual Studio for Mac](/visualstudio/mac)中编写 .net 应用程序。</span><span class="sxs-lookup"><span data-stu-id="72801-117">You can write .NET applications in [Visual Studio Code](https://code.visualstudio.com/docs), [Visual Studio](/visualstudio/windows), or [Visual Studio for Mac](/visualstudio/mac).</span></span> <span data-ttu-id="72801-118">有关支持云的开发环境的信息，请参阅 [Visual Studio Codespaces](/visualstudio/codespaces/overview/what-is-vsonline)。</span><span class="sxs-lookup"><span data-stu-id="72801-118">For information on cloud-powered development environments, see [Visual Studio Codespaces](/visualstudio/codespaces/overview/what-is-vsonline).</span></span>

## <a name="additional-tools"></a><span data-ttu-id="72801-119">其他工具</span><span class="sxs-lookup"><span data-stu-id="72801-119">Additional tools</span></span>

<span data-ttu-id="72801-120">除了更常见的工具外，.NET 还提供适用于特定方案的工具。</span><span class="sxs-lookup"><span data-stu-id="72801-120">In addition to the more common tools, .NET also provides tools for specific scenarios.</span></span> <span data-ttu-id="72801-121">一些用例包括卸载 .NET SDK 或 .NET 运行时、检索 Windows Communication Foundation (WCF) 元数据、生成代理源代码和序列化 XML。</span><span class="sxs-lookup"><span data-stu-id="72801-121">Some of the use cases include uninstalling the .NET SDK or the .NET Runtime, retrieving Windows Communication Foundation (WCF) metadata, generating proxy source code, and serializing XML.</span></span> <span data-ttu-id="72801-122">有关详细信息，请参阅 [.net 附加工具概述](../core/additional-tools/index.md)。</span><span class="sxs-lookup"><span data-stu-id="72801-122">For more information, see [.NET additional tools overview](../core/additional-tools/index.md).</span></span>

## <a name="diagnostics-and-instrumentation"></a><span data-ttu-id="72801-123">诊断和检测</span><span class="sxs-lookup"><span data-stu-id="72801-123">Diagnostics and instrumentation</span></span>

<span data-ttu-id="72801-124">作为 .NET 开发人员，你可以使用常见的性能诊断工具来监视应用性能、使用跟踪分析应用、收集性能指标和分析转储文件。</span><span class="sxs-lookup"><span data-stu-id="72801-124">As a .NET developer, you can make use of common performance diagnostic tools to monitor app performance, profile apps with tracing, collect performance metrics, and analyze dump files.</span></span> <span data-ttu-id="72801-125">使用事件计数器收集性能指标，并使用分析工具深入了解应用的执行方式。</span><span class="sxs-lookup"><span data-stu-id="72801-125">You collect performance metrics with event counters, and use profiling tools to gain insights into how apps perform.</span></span> <span data-ttu-id="72801-126">有关详细信息，请参阅 [.net 诊断工具](../core/diagnostics/index.md)。</span><span class="sxs-lookup"><span data-stu-id="72801-126">For more information, see [.NET diagnostics tools](../core/diagnostics/index.md).</span></span>

## <a name="code-analysis"></a><span data-ttu-id="72801-127">代码分析</span><span class="sxs-lookup"><span data-stu-id="72801-127">Code analysis</span></span>

<span data-ttu-id="72801-128">.NET 编译器平台 (Roslyn) 分析器检查 c # 或 Visual Basic 代码以了解代码质量和代码样式问题。</span><span class="sxs-lookup"><span data-stu-id="72801-128">The .NET compiler platform (Roslyn) analyzers inspect your C# or Visual Basic code for code quality and code style issues.</span></span> <span data-ttu-id="72801-129">有关详细信息，请参阅 [.net 源代码分析概述](code-analysis/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="72801-129">For more information, see [.NET source code analysis overview](code-analysis/overview.md).</span></span>
