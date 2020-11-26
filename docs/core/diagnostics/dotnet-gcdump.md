---
title: dotnet-gcdump 诊断工具 - .NET CLI
description: 了解如何安装和使用 dotnet-gcdump CLI 工具，以使用 .NET EventPipe 收集实时 .NET 进程的 GC（垃圾回收器）转储。
ms.date: 11/17/2020
ms.openlocfilehash: 59de1845ada9e5bdd0b24bf4312517283324ce94
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94826035"
---
# <a name="heap-analysis-tool-dotnet-gcdump"></a><span data-ttu-id="25d4f-103">堆分析工具 (dotnet-gcdump)</span><span class="sxs-lookup"><span data-stu-id="25d4f-103">Heap analysis tool (dotnet-gcdump)</span></span>

<span data-ttu-id="25d4f-104">**本文适用于：** ✔️ .NET Core 3.1 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="25d4f-104">**This article applies to:** ✔️ .NET Core 3.1 SDK and later versions</span></span>

## <a name="install"></a><span data-ttu-id="25d4f-105">安装</span><span class="sxs-lookup"><span data-stu-id="25d4f-105">Install</span></span>

<span data-ttu-id="25d4f-106">可采用两种方法来下载和安装 `dotnet-gcdump`：</span><span class="sxs-lookup"><span data-stu-id="25d4f-106">There are two ways to download and install `dotnet-gcdump`:</span></span>

- <span data-ttu-id="25d4f-107">**dotnet 全局工具：**</span><span class="sxs-lookup"><span data-stu-id="25d4f-107">**dotnet global tool:**</span></span>

  <span data-ttu-id="25d4f-108">若要安装最新版 `dotnet-gcdump` [NuGet 包](https://www.nuget.org/packages/dotnet-gcdump)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：</span><span class="sxs-lookup"><span data-stu-id="25d4f-108">To install the latest release version of the `dotnet-gcdump` [NuGet package](https://www.nuget.org/packages/dotnet-gcdump), use the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

  ```dotnetcli
  dotnet tool install --global dotnet-gcdump
  ```

- <span data-ttu-id="25d4f-109">**直接下载：**</span><span class="sxs-lookup"><span data-stu-id="25d4f-109">**Direct download:**</span></span>

  <span data-ttu-id="25d4f-110">下载与平台相匹配的工具可执行文件：</span><span class="sxs-lookup"><span data-stu-id="25d4f-110">Download the tool executable that matches your platform:</span></span>

  | <span data-ttu-id="25d4f-111">(OS)</span><span class="sxs-lookup"><span data-stu-id="25d4f-111">OS</span></span>  | <span data-ttu-id="25d4f-112">平台</span><span class="sxs-lookup"><span data-stu-id="25d4f-112">Platform</span></span> |
  | --- | -------- |
  | <span data-ttu-id="25d4f-113">Windows</span><span class="sxs-lookup"><span data-stu-id="25d4f-113">Windows</span></span> | <span data-ttu-id="25d4f-114">[x86](https://aka.ms/dotnet-gcdump/win-x86) \| [x64](https://aka.ms/dotnet-gcdump/win-x64) \| [arm](https://aka.ms/dotnet-gcdump/win-arm) \| [arm-x64](https://aka.ms/dotnet-gcdump/win-arm64)</span><span class="sxs-lookup"><span data-stu-id="25d4f-114">[x86](https://aka.ms/dotnet-gcdump/win-x86) \| [x64](https://aka.ms/dotnet-gcdump/win-x64) \| [arm](https://aka.ms/dotnet-gcdump/win-arm) \| [arm-x64](https://aka.ms/dotnet-gcdump/win-arm64)</span></span> |
  | <span data-ttu-id="25d4f-115">macOS</span><span class="sxs-lookup"><span data-stu-id="25d4f-115">macOS</span></span>   | [<span data-ttu-id="25d4f-116">x64</span><span class="sxs-lookup"><span data-stu-id="25d4f-116">x64</span></span>](https://aka.ms/dotnet-gcdump/osx-x64) |
  | <span data-ttu-id="25d4f-117">Linux</span><span class="sxs-lookup"><span data-stu-id="25d4f-117">Linux</span></span>   | <span data-ttu-id="25d4f-118">[x64](https://aka.ms/dotnet-gcdump/linux-x64) \| [arm](https://aka.ms/dotnet-gcdump/linux-arm) \| [arm64](https://aka.ms/dotnet-gcdump/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-gcdump/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-gcdump/linux-musl-arm64)</span><span class="sxs-lookup"><span data-stu-id="25d4f-118">[x64](https://aka.ms/dotnet-gcdump/linux-x64) \| [arm](https://aka.ms/dotnet-gcdump/linux-arm) \| [arm64](https://aka.ms/dotnet-gcdump/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-gcdump/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-gcdump/linux-musl-arm64)</span></span> |

## <a name="synopsis"></a><span data-ttu-id="25d4f-119">摘要</span><span class="sxs-lookup"><span data-stu-id="25d4f-119">Synopsis</span></span>

```console
dotnet-gcdump [-h|--help] [--version] <command>
```

## <a name="description"></a><span data-ttu-id="25d4f-120">说明</span><span class="sxs-lookup"><span data-stu-id="25d4f-120">Description</span></span>

<span data-ttu-id="25d4f-121">`dotnet-gcdump` 全局工具使用 [EventPipe](./eventpipe.md) 收集实时 .NET 进程的 GC（垃圾回收器）转储。</span><span class="sxs-lookup"><span data-stu-id="25d4f-121">The `dotnet-gcdump` global tool collects GC (Garbage Collector) dumps of live .NET processes using [EventPipe](./eventpipe.md).</span></span> <span data-ttu-id="25d4f-122">创建 GC 转储时需要在目标进程中触发 GC、开启特殊事件并从事件流中重新生成对象根图。</span><span class="sxs-lookup"><span data-stu-id="25d4f-122">GC dumps are created by triggering a GC in the target process, turning on special events, and regenerating the graph of object roots from the event stream.</span></span> <span data-ttu-id="25d4f-123">此过程允许在进程运行时以最小的开销收集 GC 转储。</span><span class="sxs-lookup"><span data-stu-id="25d4f-123">This process allows for GC dumps to be collected while the process is running and with minimal overhead.</span></span> <span data-ttu-id="25d4f-124">这些转储对于以下几种情况非常有用：</span><span class="sxs-lookup"><span data-stu-id="25d4f-124">These dumps are useful for several scenarios:</span></span>

- <span data-ttu-id="25d4f-125">比较多个时间点堆上的对象数。</span><span class="sxs-lookup"><span data-stu-id="25d4f-125">Comparing the number of objects on the heap at several points in time.</span></span>
- <span data-ttu-id="25d4f-126">分析对象的根（回答诸如“还有哪些引用此类型的内容？”等问题）。</span><span class="sxs-lookup"><span data-stu-id="25d4f-126">Analyzing roots of objects (answering questions like, "what still has a reference to this type?").</span></span>
- <span data-ttu-id="25d4f-127">收集有关堆上的对象计数的常规统计信息。</span><span class="sxs-lookup"><span data-stu-id="25d4f-127">Collecting general statistics about the counts of objects on the heap.</span></span>

### <a name="view-the-gc-dump-captured-from-dotnet-gcdump"></a><span data-ttu-id="25d4f-128">查看从 dotnet-gcdump 捕获的 GC 转储</span><span class="sxs-lookup"><span data-stu-id="25d4f-128">View the GC dump captured from dotnet-gcdump</span></span>

<span data-ttu-id="25d4f-129">在 Windows 上，可以在 [PerfView](https://github.com/microsoft/perfview) 中查看 `.gcdump` 文件，以便进行分析，也可在 Visual Studio 中查看该文件。</span><span class="sxs-lookup"><span data-stu-id="25d4f-129">On Windows, `.gcdump` files can be viewed in [PerfView](https://github.com/microsoft/perfview) for analysis or in Visual Studio.</span></span> <span data-ttu-id="25d4f-130">目前，无法在非 Windows 平台上打开 `.gcdump`。</span><span class="sxs-lookup"><span data-stu-id="25d4f-130">Currently, There is no way of opening a `.gcdump` on non-Windows platforms.</span></span>

<span data-ttu-id="25d4f-131">可以收集多个 `.gcdump`，并在 Visual Studio 中同时打开它们以获取比较体验。</span><span class="sxs-lookup"><span data-stu-id="25d4f-131">You can collect multiple `.gcdump`s and open them simultaneously in Visual Studio to get a comparison experience.</span></span>

## <a name="options"></a><span data-ttu-id="25d4f-132">选项</span><span class="sxs-lookup"><span data-stu-id="25d4f-132">Options</span></span>

- **`--version`**

  <span data-ttu-id="25d4f-133">显示 `dotnet-gcdump` 实用工具的版本。</span><span class="sxs-lookup"><span data-stu-id="25d4f-133">Displays the version of the `dotnet-gcdump` utility.</span></span>

- **`-h|--help`**

  <span data-ttu-id="25d4f-134">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="25d4f-134">Shows command-line help.</span></span>

## `dotnet-gcdump collect`

<span data-ttu-id="25d4f-135">从当前正在运行的进程中收集 GC 转储。</span><span class="sxs-lookup"><span data-stu-id="25d4f-135">Collects a GC dump from a currently running process.</span></span>

### <a name="synopsis"></a><span data-ttu-id="25d4f-136">摘要</span><span class="sxs-lookup"><span data-stu-id="25d4f-136">Synopsis</span></span>

```console
dotnet-gcdump collect [-h|--help] [-p|--process-id <pid>] [-o|--output <gcdump-file-path>] [-v|--verbose] [-t|--timeout <timeout>] [-n|--name <name>]
```

### <a name="options"></a><span data-ttu-id="25d4f-137">选项</span><span class="sxs-lookup"><span data-stu-id="25d4f-137">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="25d4f-138">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="25d4f-138">Shows command-line help.</span></span>

- **`-p|--process-id <pid>`**

  <span data-ttu-id="25d4f-139">可从中收集 GC 转储的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="25d4f-139">The process ID to collect the GC dump from.</span></span>

- **`-o|--output <gcdump-file-path>`**

  <span data-ttu-id="25d4f-140">应写入收集 GC 转储的路径。</span><span class="sxs-lookup"><span data-stu-id="25d4f-140">The path where collected GC dumps should be written.</span></span> <span data-ttu-id="25d4f-141">默认为 .\\YYYYMMDD\_HHMMSS\_\<pid>.gcdump。</span><span class="sxs-lookup"><span data-stu-id="25d4f-141">Defaults to *.\\YYYYMMDD\_HHMMSS\_\<pid>.gcdump*.</span></span>

- **`-v|--verbose`**

  <span data-ttu-id="25d4f-142">收集 GC 转储时输出日志。</span><span class="sxs-lookup"><span data-stu-id="25d4f-142">Output the log while collecting the GC dump.</span></span>

- **`-t|--timeout <timeout>`**

  <span data-ttu-id="25d4f-143">如果收集 GC 转储的时间超过了此秒数，则放弃收集。</span><span class="sxs-lookup"><span data-stu-id="25d4f-143">Give up on collecting the GC dump if it takes longer than this many seconds.</span></span> <span data-ttu-id="25d4f-144">默认值为 30。</span><span class="sxs-lookup"><span data-stu-id="25d4f-144">The default value is 30.</span></span>

- **`-n|--name <name>`**

  <span data-ttu-id="25d4f-145">可从中收集 GC 转储的进程的名称。</span><span class="sxs-lookup"><span data-stu-id="25d4f-145">The name of the process to collect the GC dump from.</span></span>

## `dotnet-gcdump ps`

<span data-ttu-id="25d4f-146">列出可为其收集 GC 转储的 dotnet 进程。</span><span class="sxs-lookup"><span data-stu-id="25d4f-146">Lists the dotnet processes that GC dumps can be collected for.</span></span>

### <a name="synopsis"></a><span data-ttu-id="25d4f-147">摘要</span><span class="sxs-lookup"><span data-stu-id="25d4f-147">Synopsis</span></span>

```console
dotnet-gcdump ps
```

## `dotnet-gcdump report <gcdump_filename>`

<span data-ttu-id="25d4f-148">从以前生成的 GC 转储或从正在运行的进程生成报表，并将其写入 `stdout`。</span><span class="sxs-lookup"><span data-stu-id="25d4f-148">Generate a report from a previously generated GC dump or from a running process, and write to `stdout`.</span></span>

### <a name="synopsis"></a><span data-ttu-id="25d4f-149">摘要</span><span class="sxs-lookup"><span data-stu-id="25d4f-149">Synopsis</span></span>

```console
dotnet-gcdump report [-h|--help] [-p|--process-id <pid>] [-t|--report-type <HeapStat>]
```

### <a name="options"></a><span data-ttu-id="25d4f-150">选项</span><span class="sxs-lookup"><span data-stu-id="25d4f-150">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="25d4f-151">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="25d4f-151">Shows command-line help.</span></span>

- **`-p|--process-id <pid>`**

  <span data-ttu-id="25d4f-152">可从中收集 GC 转储的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="25d4f-152">The process ID to collect the GC dump from.</span></span>

- **`-t|--report-type <HeapStat>`**

  <span data-ttu-id="25d4f-153">可生成报表的类型。</span><span class="sxs-lookup"><span data-stu-id="25d4f-153">The type of report to generate.</span></span> <span data-ttu-id="25d4f-154">可用选项：heapstat（默认）。</span><span class="sxs-lookup"><span data-stu-id="25d4f-154">Available options: heapstat (default).</span></span>

## <a name="troubleshoot"></a><span data-ttu-id="25d4f-155">疑难解答</span><span class="sxs-lookup"><span data-stu-id="25d4f-155">Troubleshoot</span></span>

- <span data-ttu-id="25d4f-156">gcdump 中没有类型信息。</span><span class="sxs-lookup"><span data-stu-id="25d4f-156">There is no type information in the gcdump.</span></span>

   <span data-ttu-id="25d4f-157">在 .NET Core 3.1 之前，存在一个问题，即使用 EventPipe 调用 gcdump 时，gcdump 之间的类型缓存没有清除。</span><span class="sxs-lookup"><span data-stu-id="25d4f-157">Prior to .NET Core 3.1, there was an issue where a type cache was not cleared between gcdumps when they were invoked with EventPipe.</span></span> <span data-ttu-id="25d4f-158">这导致确定类型信息所需的事件未发送给第二个和后续 gcdump。</span><span class="sxs-lookup"><span data-stu-id="25d4f-158">This resulted in the events needed for determining type information not being sent for the second and subsequent gcdumps.</span></span> <span data-ttu-id="25d4f-159">此问题已在 .NET Core 3.1-preview2 中得以修复。</span><span class="sxs-lookup"><span data-stu-id="25d4f-159">This was fixed in .NET Core 3.1-preview2.</span></span>

- <span data-ttu-id="25d4f-160">COM 和静态类型不在 GC 转储中。</span><span class="sxs-lookup"><span data-stu-id="25d4f-160">COM and static types aren't in the GC dump.</span></span>

   <span data-ttu-id="25d4f-161">在 .NET Core 3.1-preview2 之前，存在一个问题，即通过 EventPipe 调用 GC 转储时，不会发送静态和 COM 类型。</span><span class="sxs-lookup"><span data-stu-id="25d4f-161">Prior to .NET Core 3.1-preview2, there was an issue where static and COM types weren't sent when the GC dump was invoked via EventPipe.</span></span> <span data-ttu-id="25d4f-162">此问题已在 .NET Core 3.1-preview2 中得以修复。</span><span class="sxs-lookup"><span data-stu-id="25d4f-162">This has been fixed in .NET Core 3.1-preview2.</span></span>
