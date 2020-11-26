---
title: dotnet-counters 诊断工具 - .NET CLI
description: 了解如何安装和使用 dotnet-counter CLI 工具进行临时运行状况监视和初级性能调查。
ms.date: 11/17/2020
ms.openlocfilehash: 7dd4c06f3abe423552ba1d3eb82f6d0c35a84d0b
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94822212"
---
# <a name="investigate-performance-counters-dotnet-counters"></a><span data-ttu-id="07795-103">调查性能计数器 (dotnet-counters)</span><span class="sxs-lookup"><span data-stu-id="07795-103">Investigate performance counters (dotnet-counters)</span></span>

<span data-ttu-id="07795-104"> 本文适用于： ✔️ .NET Core 3.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="07795-104">**This article applies to:** ✔️ .NET Core 3.0 SDK and later versions</span></span>

## <a name="install"></a><span data-ttu-id="07795-105">安装</span><span class="sxs-lookup"><span data-stu-id="07795-105">Install</span></span>

<span data-ttu-id="07795-106">可采用两种方法来下载和安装 `dotnet-counters`：</span><span class="sxs-lookup"><span data-stu-id="07795-106">There are two ways to download and install `dotnet-counters`:</span></span>

- <span data-ttu-id="07795-107">**dotnet 全局工具：**</span><span class="sxs-lookup"><span data-stu-id="07795-107">**dotnet global tool:**</span></span>

  <span data-ttu-id="07795-108">若要安装最新版 `dotnet-counters` [NuGet 包](https://www.nuget.org/packages/dotnet-counters)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：</span><span class="sxs-lookup"><span data-stu-id="07795-108">To install the latest release version of the `dotnet-counters` [NuGet package](https://www.nuget.org/packages/dotnet-counters), use the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

  ```dotnetcli
  dotnet tool install --global dotnet-counters
  ```

- <span data-ttu-id="07795-109">**直接下载：**</span><span class="sxs-lookup"><span data-stu-id="07795-109">**Direct download:**</span></span>

  <span data-ttu-id="07795-110">下载与平台相匹配的工具可执行文件：</span><span class="sxs-lookup"><span data-stu-id="07795-110">Download the tool executable that matches your platform:</span></span>

  | <span data-ttu-id="07795-111">(OS)</span><span class="sxs-lookup"><span data-stu-id="07795-111">OS</span></span>  | <span data-ttu-id="07795-112">平台</span><span class="sxs-lookup"><span data-stu-id="07795-112">Platform</span></span> |
  | --- | -------- |
  | <span data-ttu-id="07795-113">Windows</span><span class="sxs-lookup"><span data-stu-id="07795-113">Windows</span></span> | <span data-ttu-id="07795-114">[x86](https://aka.ms/dotnet-counters/win-x86) \| [x64](https://aka.ms/dotnet-counters/win-x64) \| [arm](https://aka.ms/dotnet-counters/win-arm) \| [arm-x64](https://aka.ms/dotnet-counters/win-arm64)</span><span class="sxs-lookup"><span data-stu-id="07795-114">[x86](https://aka.ms/dotnet-counters/win-x86) \| [x64](https://aka.ms/dotnet-counters/win-x64) \| [arm](https://aka.ms/dotnet-counters/win-arm) \| [arm-x64](https://aka.ms/dotnet-counters/win-arm64)</span></span> |
  | <span data-ttu-id="07795-115">macOS</span><span class="sxs-lookup"><span data-stu-id="07795-115">macOS</span></span>   | [<span data-ttu-id="07795-116">x64</span><span class="sxs-lookup"><span data-stu-id="07795-116">x64</span></span>](https://aka.ms/dotnet-counters/osx-x64) |
  | <span data-ttu-id="07795-117">Linux</span><span class="sxs-lookup"><span data-stu-id="07795-117">Linux</span></span>   | <span data-ttu-id="07795-118">[x64](https://aka.ms/dotnet-counters/linux-x64) \| [arm](https://aka.ms/dotnet-counters/linux-arm) \| [arm64](https://aka.ms/dotnet-counters/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-counters/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-counters/linux-musl-arm64)</span><span class="sxs-lookup"><span data-stu-id="07795-118">[x64](https://aka.ms/dotnet-counters/linux-x64) \| [arm](https://aka.ms/dotnet-counters/linux-arm) \| [arm64](https://aka.ms/dotnet-counters/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-counters/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-counters/linux-musl-arm64)</span></span> |

## <a name="synopsis"></a><span data-ttu-id="07795-119">摘要</span><span class="sxs-lookup"><span data-stu-id="07795-119">Synopsis</span></span>

```console
dotnet-counters [-h|--help] [--version] <command>
```

## <a name="description"></a><span data-ttu-id="07795-120">描述</span><span class="sxs-lookup"><span data-stu-id="07795-120">Description</span></span>

<span data-ttu-id="07795-121">`dotnet-counters` 是一个性能监视工具，用于临时运行状况监视和初级性能调查。</span><span class="sxs-lookup"><span data-stu-id="07795-121">`dotnet-counters` is a performance monitoring tool for ad-hoc health monitoring and first-level performance investigation.</span></span> <span data-ttu-id="07795-122">它可以观察通过 <xref:System.Diagnostics.Tracing.EventCounter> API 发布的性能计数器值。</span><span class="sxs-lookup"><span data-stu-id="07795-122">It can observe performance counter values that are published via the <xref:System.Diagnostics.Tracing.EventCounter> API.</span></span> <span data-ttu-id="07795-123">例如，可以快速监视 CPU 使用情况或 .NET Core 应用程序中引发的异常率，以了解在使用 `PerfView` 或 `dotnet-trace` 深入调查更严重的性能问题之前是否有任何可疑操作。</span><span class="sxs-lookup"><span data-stu-id="07795-123">For example, you can quickly monitor things like the CPU usage or the rate of exceptions being thrown in your .NET Core application to see if there's anything suspicious before diving into more serious performance investigation using `PerfView` or `dotnet-trace`.</span></span>

## <a name="options"></a><span data-ttu-id="07795-124">选项</span><span class="sxs-lookup"><span data-stu-id="07795-124">Options</span></span>

- **`--version`**

  <span data-ttu-id="07795-125">显示 dotnet-counters 实用工具的版本。</span><span class="sxs-lookup"><span data-stu-id="07795-125">Displays the version of the dotnet-counters utility.</span></span>

- **`-h|--help`**

  <span data-ttu-id="07795-126">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="07795-126">Shows command-line help.</span></span>

## <a name="commands"></a><span data-ttu-id="07795-127">命令</span><span class="sxs-lookup"><span data-stu-id="07795-127">Commands</span></span>

| <span data-ttu-id="07795-128">命令</span><span class="sxs-lookup"><span data-stu-id="07795-128">Command</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="07795-129">dotnet-counters collect</span><span class="sxs-lookup"><span data-stu-id="07795-129">dotnet-counters collect</span></span>](#dotnet-counters-collect) |
| [<span data-ttu-id="07795-130">dotnet-counters list</span><span class="sxs-lookup"><span data-stu-id="07795-130">dotnet-counters list</span></span>](#dotnet-counters-list)       |
| [<span data-ttu-id="07795-131">dotnet-counters monitor</span><span class="sxs-lookup"><span data-stu-id="07795-131">dotnet-counters monitor</span></span>](#dotnet-counters-monitor) |
| [<span data-ttu-id="07795-132">dotnet-counters ps</span><span class="sxs-lookup"><span data-stu-id="07795-132">dotnet-counters ps</span></span>](#dotnet-counters-ps)           |

## <a name="dotnet-counters-collect"></a><span data-ttu-id="07795-133">dotnet-counters collect</span><span class="sxs-lookup"><span data-stu-id="07795-133">dotnet-counters collect</span></span>

<span data-ttu-id="07795-134">定期收集所选计数器的值，并将它们导出为指定的文件格式以进行后续处理。</span><span class="sxs-lookup"><span data-stu-id="07795-134">Periodically collect selected counter values and export them into a specified file format for post-processing.</span></span>

### <a name="synopsis"></a><span data-ttu-id="07795-135">摘要</span><span class="sxs-lookup"><span data-stu-id="07795-135">Synopsis</span></span>

```console
dotnet-counters collect [-h|--help] [-p|--process-id] [-n|--name] [--refresh-interval] [--counters <COUNTERS>] [--format] [-o|--output] [-- <command>]
```

### <a name="options"></a><span data-ttu-id="07795-136">选项</span><span class="sxs-lookup"><span data-stu-id="07795-136">Options</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="07795-137">要从中收集计数器数据的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="07795-137">The ID of the process to be collect counter data from.</span></span>

- **`-n|--name <name>`**

  <span data-ttu-id="07795-138">要从中收集计数器数据的进程的名称。</span><span class="sxs-lookup"><span data-stu-id="07795-138">The name of the process to be collect counter data from.</span></span>

- **`--refresh-interval <SECONDS>`**

  <span data-ttu-id="07795-139">更新显示的计数器之间延迟的秒数</span><span class="sxs-lookup"><span data-stu-id="07795-139">The number of seconds to delay between updating the displayed counters</span></span>

- **`--counters <COUNTERS>`**

  <span data-ttu-id="07795-140">计数器的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="07795-140">A comma-separated list of counters.</span></span> <span data-ttu-id="07795-141">计数器可以指定为 `provider_name[:counter_name]`。</span><span class="sxs-lookup"><span data-stu-id="07795-141">Counters can be specified `provider_name[:counter_name]`.</span></span> <span data-ttu-id="07795-142">如果使用 `provider_name` 时没有限定的计数器列表，则显示来自提供程序的所有计数器。</span><span class="sxs-lookup"><span data-stu-id="07795-142">If the `provider_name` is used without a qualifying list of counters, then all counters from the provider are shown.</span></span> <span data-ttu-id="07795-143">若要发现提供程序和计数器名称，请使用 [dotnet-counters list](#dotnet-counters-list) 命令。</span><span class="sxs-lookup"><span data-stu-id="07795-143">To discover provider and counter names, use the [dotnet-counters list](#dotnet-counters-list) command.</span></span>

- **`--format <csv|json>`**

  <span data-ttu-id="07795-144">要导出的格式。</span><span class="sxs-lookup"><span data-stu-id="07795-144">The format to be exported.</span></span> <span data-ttu-id="07795-145">当前可用的格式：csv 和 json。</span><span class="sxs-lookup"><span data-stu-id="07795-145">Currently available: csv, json.</span></span>

- **`-o|--output <output>`**

  <span data-ttu-id="07795-146">输出文件的名称。</span><span class="sxs-lookup"><span data-stu-id="07795-146">The name of the output file.</span></span>

- <span data-ttu-id="07795-147">`-- <command>`（仅适用于运行 .NET 5.0 或更高版本的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="07795-147">**`-- <command>` (for target applications running .NET 5.0 or later only)**</span></span>

  <span data-ttu-id="07795-148">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="07795-148">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="07795-149">`dotnet-counters` 将启动一个进程，并收集请求的指标。</span><span class="sxs-lookup"><span data-stu-id="07795-149">`dotnet-counters` will launch a process with the provided command and collect the requested metrics.</span></span> <span data-ttu-id="07795-150">这通常用于收集应用程序的启动路径的指标，并可用于诊断或监视在主入口点前后发生的问题。</span><span class="sxs-lookup"><span data-stu-id="07795-150">This is often useful to collect metrics for the application's startup path and can be used to diagnose or monitor issues that happen early before or shortly after the main entrypoint.</span></span>

  > [!NOTE]
  > <span data-ttu-id="07795-151">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="07795-151">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="07795-152">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="07795-152">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

### <a name="examples"></a><span data-ttu-id="07795-153">示例</span><span class="sxs-lookup"><span data-stu-id="07795-153">Examples</span></span>

- <span data-ttu-id="07795-154">以 3 秒的刷新间隔时间收集所有计数器的值，并生成 csv 输出文件：</span><span class="sxs-lookup"><span data-stu-id="07795-154">Collect all counters at a refresh interval of 3 seconds and generate a csv as output:</span></span>

  ```console
  > dotnet-counters collect --process-id 1902 --refresh-interval 3 --format csv

  counter_list is unspecified. Monitoring all counters by default.
  Starting a counter session. Press Q to quit.
  ```

- <span data-ttu-id="07795-155">将 `dotnet mvc.dll` 作为子进程启动，开始从启动中收集运行时计算器和 ASP.NET Core Hosting 计算器，并将其另存为 JSON 输出：</span><span class="sxs-lookup"><span data-stu-id="07795-155">Start `dotnet mvc.dll` as a child process and start collecting runtime counters and ASP.NET Core Hosting counters from startup and save it as a JSON output:</span></span>

  ```console
  > dotnet-counters collect --format json --counters System.Runtime,Microsoft.AspNetCore.Hosting -- dotnet mvc.dll
  Starting a counter session. Press Q to quit.
  File saved to counter.json
  ```

## <a name="dotnet-counters-list"></a><span data-ttu-id="07795-156">dotnet-counters list</span><span class="sxs-lookup"><span data-stu-id="07795-156">dotnet-counters list</span></span>

<span data-ttu-id="07795-157">显示按提供程序分组的计数器名称和说明的列表。</span><span class="sxs-lookup"><span data-stu-id="07795-157">Displays a list of counter names and descriptions, grouped by provider.</span></span>

### <a name="synopsis"></a><span data-ttu-id="07795-158">摘要</span><span class="sxs-lookup"><span data-stu-id="07795-158">Synopsis</span></span>

```console
dotnet-counters list [-h|--help]
```

### <a name="example"></a><span data-ttu-id="07795-159">示例</span><span class="sxs-lookup"><span data-stu-id="07795-159">Example</span></span>

```console
> dotnet-counters list
Showing well-known counters only. Specific processes may support additional counters.

System.Runtime
    cpu-usage                                    Amount of time the process has utilized the CPU (ms)
    working-set                                  Amount of working set used by the process (MB)
    gc-heap-size                                 Total heap size reported by the GC (MB)
    gen-0-gc-count                               Number of Gen 0 GCs / min
    gen-1-gc-count                               Number of Gen 1 GCs / min
    gen-2-gc-count                               Number of Gen 2 GCs / min
    time-in-gc                                   % time in GC since the last GC
    gen-0-size                                   Gen 0 Heap Size
    gen-1-size                                   Gen 1 Heap Size
    gen-2-size                                   Gen 2 Heap Size
    loh-size                                     LOH Heap Size
    alloc-rate                                   Allocation Rate
    assembly-count                               Number of Assemblies Loaded
    exception-count                              Number of Exceptions / sec
    threadpool-thread-count                      Number of ThreadPool Threads
    monitor-lock-contention-count                Monitor Lock Contention Count
    threadpool-queue-length                      ThreadPool Work Items Queue Length
    threadpool-completed-items-count             ThreadPool Completed Work Items Count
    active-timer-count                           Active Timers Count

Microsoft.AspNetCore.Hosting
    requests-per-second                  Request rate
    total-requests                       Total number of requests
    current-requests                     Current number of requests
    failed-requests                      Failed number of requests
```

> [!NOTE]
> <span data-ttu-id="07795-160">当有已标记的进程支持 `Microsoft.AspNetCore.Hosting` 计数器时（例如当 ASP.NET Core 应用程序在主机上运行时），将显示这些计数器。</span><span class="sxs-lookup"><span data-stu-id="07795-160">The `Microsoft.AspNetCore.Hosting` counters are displayed when there are processes identified that support these counters, for example; when an ASP.NET Core application is running on the host machine.</span></span>

## <a name="dotnet-counters-monitor"></a><span data-ttu-id="07795-161">dotnet-counters monitor</span><span class="sxs-lookup"><span data-stu-id="07795-161">dotnet-counters monitor</span></span>

<span data-ttu-id="07795-162">显示所选计数器的定期刷新值。</span><span class="sxs-lookup"><span data-stu-id="07795-162">Displays periodically refreshing values of selected counters.</span></span>

### <a name="synopsis"></a><span data-ttu-id="07795-163">摘要</span><span class="sxs-lookup"><span data-stu-id="07795-163">Synopsis</span></span>

```console
dotnet-counters monitor [-h|--help] [-p|--process-id] [-n|--name] [--refresh-interval] [--counters] [-- <command>]
```

### <a name="options"></a><span data-ttu-id="07795-164">选项</span><span class="sxs-lookup"><span data-stu-id="07795-164">Options</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="07795-165">要监视的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="07795-165">The ID of the process to be monitored.</span></span>

- **`-n|--name <name>`**

  <span data-ttu-id="07795-166">要监视的进程的名称。</span><span class="sxs-lookup"><span data-stu-id="07795-166">The name of the process to be monitored.</span></span>

- **`--refresh-interval <SECONDS>`**

  <span data-ttu-id="07795-167">更新显示的计数器之间延迟的秒数</span><span class="sxs-lookup"><span data-stu-id="07795-167">The number of seconds to delay between updating the displayed counters</span></span>

- **`--counters <COUNTERS>`**

  <span data-ttu-id="07795-168">计数器的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="07795-168">A comma-separated list of counters.</span></span> <span data-ttu-id="07795-169">计数器可以指定为 `provider_name[:counter_name]`。</span><span class="sxs-lookup"><span data-stu-id="07795-169">Counters can be specified `provider_name[:counter_name]`.</span></span> <span data-ttu-id="07795-170">如果使用 `provider_name` 时没有限定的计数器列表，则显示来自提供程序的所有计数器。</span><span class="sxs-lookup"><span data-stu-id="07795-170">If the `provider_name` is used without a qualifying list of counters, then all counters from the provider are shown.</span></span> <span data-ttu-id="07795-171">若要发现提供程序和计数器名称，请使用 [dotnet-counters list](#dotnet-counters-list) 命令。</span><span class="sxs-lookup"><span data-stu-id="07795-171">To discover provider and counter names, use the [dotnet-counters list](#dotnet-counters-list) command.</span></span>

 <span data-ttu-id="07795-172">`-- <command>`（仅适用于运行 .NET 5.0 或更高版本的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="07795-172">**`-- <command>` (for target applications running .NET 5.0 or later only)**</span></span>

  <span data-ttu-id="07795-173">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="07795-173">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="07795-174">`dotnet-counters` 将启动一个进程，并监视请求的指标。</span><span class="sxs-lookup"><span data-stu-id="07795-174">`dotnet-counters` will launch a process with the provided command and monitor the requested metrics.</span></span> <span data-ttu-id="07795-175">这通常用于收集应用程序的启动路径的指标，并可用于诊断或监视在主入口点前后发生的问题。</span><span class="sxs-lookup"><span data-stu-id="07795-175">This is often useful to collect metrics for the application's startup path and can be used to diagnose or monitor issues that happen early before or shortly after the main entrypoint.</span></span>

  > [!NOTE]
  > <span data-ttu-id="07795-176">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="07795-176">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="07795-177">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="07795-177">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

### <a name="examples"></a><span data-ttu-id="07795-178">示例</span><span class="sxs-lookup"><span data-stu-id="07795-178">Examples</span></span>

- <span data-ttu-id="07795-179">以 3 秒的刷新间隔监视 `System.Runtime` 中的所有计数器：</span><span class="sxs-lookup"><span data-stu-id="07795-179">Monitor all counters from `System.Runtime` at a refresh interval of 3 seconds:</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902  --refresh-interval 3 --counters System.Runtime
  Press p to pause, r to resume, q to quit.
      Status: Running

  [System.Runtime]
      % Time in GC since last GC (%)                                 0
      Allocation Rate (B / 1 sec)                                5,376
      CPU Usage (%)                                                  0
      Exception Count (Count / 1 sec)                                0
      GC Fragmentation (%)                                          48.467
      GC Heap Size (MB)                                              0
      Gen 0 GC Count (Count / 1 sec)                                 1
      Gen 0 Size (B)                                                24
      Gen 1 GC Count (Count / 1 sec)                                 1
      Gen 1 Size (B)                                                24
      Gen 2 GC Count (Count / 1 sec)                                 1
      Gen 2 Size (B)                                           272,000
      IL Bytes Jitted (B)                                       19,449
      LOH Size (B)                                              19,640
      Monitor Lock Contention Count (Count / 1 sec)                  0
      Number of Active Timers                                        0
      Number of Assemblies Loaded                                    7
      Number of Methods Jitted                                     166
      POH (Pinned Object Heap) Size (B)                             24
      ThreadPool Completed Work Item Count (Count / 1 sec)           0
      ThreadPool Queue Length                                        0
      ThreadPool Thread Count                                        2
      Working Set (MB)                                              19
  ```

- <span data-ttu-id="07795-180">仅监视 `System.Runtime` 中的 CPU 使用情况和 GC 堆大小：</span><span class="sxs-lookup"><span data-stu-id="07795-180">Monitor just CPU usage and GC heap size from `System.Runtime`:</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902 --counters System.Runtime[cpu-usage,gc-heap-size]

  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      CPU Usage (%)                                 24
      GC Heap Size (MB)                            811
  ```

- <span data-ttu-id="07795-181">监视用户定义的 `EventSource` 中的 `EventCounter` 值。</span><span class="sxs-lookup"><span data-stu-id="07795-181">Monitor `EventCounter` values from user-defined `EventSource`.</span></span> <span data-ttu-id="07795-182">有关详细信息，请参阅[教程：使用 .NET Core 中的 EventCounters 衡量性能](event-counter-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="07795-182">For more information, see [Tutorial: Measure performance using EventCounters in .NET Core](event-counter-perf.md).</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902 --counters Samples-EventCounterDemos-Minimal

  Press p to pause, r to resume, q to quit.
      request                                      100
  ```

- <span data-ttu-id="07795-183">启动 `my-aspnet-server.exe` 并从其启动监视加载的程序集的数量（仅限 .NET 5.0 或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="07795-183">Launch `my-aspnet-server.exe` and monitor the # of assemblies loaded from its startup (.NET 5.0 or later only):</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="07795-184">这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="07795-184">This works for apps running .NET 5.0 or later only.</span></span>

  ```console
  > dotnet-counters monitor --counters System.Runtime[assembly-count] -- my-aspnet-server.exe

  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      Number of Assemblies Loaded                   24
  ```
  
- <span data-ttu-id="07795-185">启动 `my-aspnet-server.exe`，以 `arg1` 及 `arg2` 作为命令行参数，并从其启动监视其工作集和 GC 堆大小（仅限 .NET 5.0 或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="07795-185">Launch `my-aspnet-server.exe` with `arg1` and `arg2` as command-line arguments and monitor its working set and GC heap size from its startup (.NET 5.0 or later only):</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="07795-186">这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="07795-186">This works for apps running .NET 5.0 or later only.</span></span>

  ```console
  > dotnet-counters monitor --counters System.Runtime[working-set,gc-heap-size] -- my-aspnet-server.exe arg1 arg2
  ```

  ```console
  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      GC Heap Size (MB)                                 39
      Working Set (MB)                                  59
  ```

## <a name="dotnet-counters-ps"></a><span data-ttu-id="07795-187">dotnet-counters ps</span><span class="sxs-lookup"><span data-stu-id="07795-187">dotnet-counters ps</span></span>

<span data-ttu-id="07795-188">显示可监视的 dotnet 进程的列表。</span><span class="sxs-lookup"><span data-stu-id="07795-188">Display a list of dotnet processes that can be monitored.</span></span>

### <a name="synopsis"></a><span data-ttu-id="07795-189">摘要</span><span class="sxs-lookup"><span data-stu-id="07795-189">Synopsis</span></span>

```console
dotnet-counters ps [-h|--help]
```

### <a name="example"></a><span data-ttu-id="07795-190">示例</span><span class="sxs-lookup"><span data-stu-id="07795-190">Example</span></span>

```console
> dotnet-counters ps
  
  15683 WebApi     /home/suwhang/repos/WebApi/WebApi
  16324 dotnet     /usr/local/share/dotnet/dotnet
```
