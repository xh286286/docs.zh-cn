---
title: dotnet-counters - .NET Core
description: 了解如何安装和使用 dotnet-counter 命令行工具。
ms.date: 02/26/2020
ms.openlocfilehash: 7ff29ad91ad271afd35e3d38a4d748bc79ad6c03
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94507249"
---
# <a name="dotnet-counters"></a><span data-ttu-id="e8655-103">dotnet-counters</span><span class="sxs-lookup"><span data-stu-id="e8655-103">dotnet-counters</span></span>

<span data-ttu-id="e8655-104"> 本文适用于： ✔️ .NET Core 3.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="e8655-104">**This article applies to:** ✔️ .NET Core 3.0 SDK and later versions</span></span>

## <a name="install-dotnet-counters"></a><span data-ttu-id="e8655-105">安装 dotnet-counters</span><span class="sxs-lookup"><span data-stu-id="e8655-105">Install dotnet-counters</span></span>

<span data-ttu-id="e8655-106">若要安装最新版 `dotnet-counters` [NuGet 包](https://www.nuget.org/packages/dotnet-counters)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：</span><span class="sxs-lookup"><span data-stu-id="e8655-106">To install the latest release version of the `dotnet-counters` [NuGet package](https://www.nuget.org/packages/dotnet-counters), use the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

```dotnetcli
dotnet tool install --global dotnet-counters
```

## <a name="synopsis"></a><span data-ttu-id="e8655-107">摘要</span><span class="sxs-lookup"><span data-stu-id="e8655-107">Synopsis</span></span>

```console
dotnet-counters [-h|--help] [--version] <command>
```

## <a name="description"></a><span data-ttu-id="e8655-108">描述</span><span class="sxs-lookup"><span data-stu-id="e8655-108">Description</span></span>

<span data-ttu-id="e8655-109">`dotnet-counters` 是一个性能监视工具，用于临时运行状况监视和初级性能调查。</span><span class="sxs-lookup"><span data-stu-id="e8655-109">`dotnet-counters` is a performance monitoring tool for ad-hoc health monitoring and first-level performance investigation.</span></span> <span data-ttu-id="e8655-110">它可以观察通过 <xref:System.Diagnostics.Tracing.EventCounter> API 发布的性能计数器值。</span><span class="sxs-lookup"><span data-stu-id="e8655-110">It can observe performance counter values that are published via the <xref:System.Diagnostics.Tracing.EventCounter> API.</span></span> <span data-ttu-id="e8655-111">例如，可以快速监视 CPU 使用情况或 .NET Core 应用程序中引发的异常率，以了解在使用 `PerfView` 或 `dotnet-trace` 深入调查更严重的性能问题之前是否有任何可疑操作。</span><span class="sxs-lookup"><span data-stu-id="e8655-111">For example, you can quickly monitor things like the CPU usage or the rate of exceptions being thrown in your .NET Core application to see if there's anything suspicious before diving into more serious performance investigation using `PerfView` or `dotnet-trace`.</span></span>

## <a name="options"></a><span data-ttu-id="e8655-112">选项</span><span class="sxs-lookup"><span data-stu-id="e8655-112">Options</span></span>

- **`--version`**

  <span data-ttu-id="e8655-113">显示 dotnet-counters 实用工具的版本。</span><span class="sxs-lookup"><span data-stu-id="e8655-113">Displays the version of the dotnet-counters utility.</span></span>

- **`-h|--help`**

  <span data-ttu-id="e8655-114">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="e8655-114">Shows command-line help.</span></span>

## <a name="commands"></a><span data-ttu-id="e8655-115">命令</span><span class="sxs-lookup"><span data-stu-id="e8655-115">Commands</span></span>

| <span data-ttu-id="e8655-116">命令</span><span class="sxs-lookup"><span data-stu-id="e8655-116">Command</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="e8655-117">dotnet-counters collect</span><span class="sxs-lookup"><span data-stu-id="e8655-117">dotnet-counters collect</span></span>](#dotnet-counters-collect) |
| [<span data-ttu-id="e8655-118">dotnet-counters list</span><span class="sxs-lookup"><span data-stu-id="e8655-118">dotnet-counters list</span></span>](#dotnet-counters-list)       |
| [<span data-ttu-id="e8655-119">dotnet-counters monitor</span><span class="sxs-lookup"><span data-stu-id="e8655-119">dotnet-counters monitor</span></span>](#dotnet-counters-monitor) |
| [<span data-ttu-id="e8655-120">dotnet-counters ps</span><span class="sxs-lookup"><span data-stu-id="e8655-120">dotnet-counters ps</span></span>](#dotnet-counters-ps)           |

## <a name="dotnet-counters-collect"></a><span data-ttu-id="e8655-121">dotnet-counters collect</span><span class="sxs-lookup"><span data-stu-id="e8655-121">dotnet-counters collect</span></span>

<span data-ttu-id="e8655-122">定期收集所选计数器的值，并将它们导出为指定的文件格式以进行后续处理。</span><span class="sxs-lookup"><span data-stu-id="e8655-122">Periodically collect selected counter values and export them into a specified file format for post-processing.</span></span>

### <a name="synopsis"></a><span data-ttu-id="e8655-123">摘要</span><span class="sxs-lookup"><span data-stu-id="e8655-123">Synopsis</span></span>

```console
dotnet-counters collect [-h|--help] [-p|--process-id] [--refreshInterval] [--counters <COUNTERS>] [--format] [-o|--output] [-- <command>]
```

### <a name="options"></a><span data-ttu-id="e8655-124">选项</span><span class="sxs-lookup"><span data-stu-id="e8655-124">Options</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="e8655-125">要监视的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="e8655-125">The ID of the process to be monitored.</span></span>

- **`--refresh-interval <SECONDS>`**

  <span data-ttu-id="e8655-126">更新显示的计数器之间延迟的秒数</span><span class="sxs-lookup"><span data-stu-id="e8655-126">The number of seconds to delay between updating the displayed counters</span></span>

- **`--counters <COUNTERS>`**

  <span data-ttu-id="e8655-127">计数器的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="e8655-127">A comma-separated list of counters.</span></span> <span data-ttu-id="e8655-128">计数器可以指定为 `provider_name[:counter_name]`。</span><span class="sxs-lookup"><span data-stu-id="e8655-128">Counters can be specified `provider_name[:counter_name]`.</span></span> <span data-ttu-id="e8655-129">如果使用 `provider_name` 时没有限定的计数器列表，则显示来自提供程序的所有计数器。</span><span class="sxs-lookup"><span data-stu-id="e8655-129">If the `provider_name` is used without a qualifying list of counters, then all counters from the provider are shown.</span></span> <span data-ttu-id="e8655-130">若要发现提供程序和计数器名称，请使用 [dotnet-counters list](#dotnet-counters-list) 命令。</span><span class="sxs-lookup"><span data-stu-id="e8655-130">To discover provider and counter names, use the [dotnet-counters list](#dotnet-counters-list) command.</span></span>

- **`--format <csv|json>`**

  <span data-ttu-id="e8655-131">要导出的格式。</span><span class="sxs-lookup"><span data-stu-id="e8655-131">The format to be exported.</span></span> <span data-ttu-id="e8655-132">当前可用的格式：csv 和 json。</span><span class="sxs-lookup"><span data-stu-id="e8655-132">Currently available: csv, json.</span></span>

- **`-o|--output <output>`**

  <span data-ttu-id="e8655-133">输出文件的名称。</span><span class="sxs-lookup"><span data-stu-id="e8655-133">The name of the output file.</span></span>

- <span data-ttu-id="e8655-134">`-- <command>`（仅适用于运行 .NET 5.0 或更高版本的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="e8655-134">**`-- <command>` (for target applications running .NET 5.0 or later only)**</span></span>

  <span data-ttu-id="e8655-135">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="e8655-135">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="e8655-136">`dotnet-counters` 将启动一个进程，并收集请求的指标。</span><span class="sxs-lookup"><span data-stu-id="e8655-136">`dotnet-counters` will launch a process with the provided command and collect the requested metrics.</span></span> <span data-ttu-id="e8655-137">这通常用于收集应用程序的启动路径的指标，并可用于诊断或监视在主入口点前后发生的问题。</span><span class="sxs-lookup"><span data-stu-id="e8655-137">This is often useful to collect metrics for the application's startup path and can be used to diagnose or monitor issues that happen early before or shortly after the main entrypoint.</span></span>

> [!NOTE]
> <span data-ttu-id="e8655-138">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="e8655-138">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="e8655-139">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="e8655-139">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

### <a name="examples"></a><span data-ttu-id="e8655-140">示例</span><span class="sxs-lookup"><span data-stu-id="e8655-140">Examples</span></span>

- <span data-ttu-id="e8655-141">以 3 秒的刷新间隔时间收集所有计数器的值，并生成 csv 输出文件：</span><span class="sxs-lookup"><span data-stu-id="e8655-141">Collect all counters at a refresh interval of 3 seconds and generate a csv as output:</span></span>

  ```console
  > dotnet-counters collect --process-id 1902 --refresh-interval 3 --format csv

  counter_list is unspecified. Monitoring all counters by default.
  Starting a counter session. Press Q to quit.
  ```

- <span data-ttu-id="e8655-142">将 `dotnet mvc.dll` 作为子进程启动，开始从启动中收集运行时计算器和 ASP.NET Core Hosting 计算器，并将其另存为 JSON 输出：</span><span class="sxs-lookup"><span data-stu-id="e8655-142">Start `dotnet mvc.dll` as a child process and start collecting runtime counters and ASP.NET Core Hosting counters from startup and save it as a JSON output:</span></span>

  ```console
  > dotnet-counters collect --format json --counters System.Runtime,Microsoft.AspNetCore.Hosting -- dotnet mvc.dll
  Starting a counter session. Press Q to quit.
  File saved to counter.json
  ```

## <a name="dotnet-counters-list"></a><span data-ttu-id="e8655-143">dotnet-counters list</span><span class="sxs-lookup"><span data-stu-id="e8655-143">dotnet-counters list</span></span>

<span data-ttu-id="e8655-144">显示按提供程序分组的计数器名称和说明的列表。</span><span class="sxs-lookup"><span data-stu-id="e8655-144">Displays a list of counter names and descriptions, grouped by provider.</span></span>

### <a name="synopsis"></a><span data-ttu-id="e8655-145">摘要</span><span class="sxs-lookup"><span data-stu-id="e8655-145">Synopsis</span></span>

```console
dotnet-counters list [-h|--help]
```

### <a name="example"></a><span data-ttu-id="e8655-146">示例</span><span class="sxs-lookup"><span data-stu-id="e8655-146">Example</span></span>

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
> <span data-ttu-id="e8655-147">当有已标记的进程支持 `Microsoft.AspNetCore.Hosting` 计数器时（例如当 ASP.NET Core 应用程序在主机上运行时），将显示这些计数器。</span><span class="sxs-lookup"><span data-stu-id="e8655-147">The `Microsoft.AspNetCore.Hosting` counters are displayed when there are processes identified that support these counters, for example; when an ASP.NET Core application is running on the host machine.</span></span>

## <a name="dotnet-counters-monitor"></a><span data-ttu-id="e8655-148">dotnet-counters monitor</span><span class="sxs-lookup"><span data-stu-id="e8655-148">dotnet-counters monitor</span></span>

<span data-ttu-id="e8655-149">显示所选计数器的定期刷新值。</span><span class="sxs-lookup"><span data-stu-id="e8655-149">Displays periodically refreshing values of selected counters.</span></span>

### <a name="synopsis"></a><span data-ttu-id="e8655-150">摘要</span><span class="sxs-lookup"><span data-stu-id="e8655-150">Synopsis</span></span>

```console
dotnet-counters monitor [-h|--help] [-p|--process-id] [--refreshInterval] [--counters] [-- <command>]
```

### <a name="options"></a><span data-ttu-id="e8655-151">选项</span><span class="sxs-lookup"><span data-stu-id="e8655-151">Options</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="e8655-152">要监视的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="e8655-152">The ID of the process to be monitored.</span></span>

- **`--refresh-interval <SECONDS>`**

  <span data-ttu-id="e8655-153">更新显示的计数器之间延迟的秒数</span><span class="sxs-lookup"><span data-stu-id="e8655-153">The number of seconds to delay between updating the displayed counters</span></span>

- **`--counters <COUNTERS>`**

  <span data-ttu-id="e8655-154">计数器的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="e8655-154">A comma-separated list of counters.</span></span> <span data-ttu-id="e8655-155">计数器可以指定为 `provider_name[:counter_name]`。</span><span class="sxs-lookup"><span data-stu-id="e8655-155">Counters can be specified `provider_name[:counter_name]`.</span></span> <span data-ttu-id="e8655-156">如果使用 `provider_name` 时没有限定的计数器列表，则显示来自提供程序的所有计数器。</span><span class="sxs-lookup"><span data-stu-id="e8655-156">If the `provider_name` is used without a qualifying list of counters, then all counters from the provider are shown.</span></span> <span data-ttu-id="e8655-157">若要发现提供程序和计数器名称，请使用 [dotnet-counters list](#dotnet-counters-list) 命令。</span><span class="sxs-lookup"><span data-stu-id="e8655-157">To discover provider and counter names, use the [dotnet-counters list](#dotnet-counters-list) command.</span></span>

 <span data-ttu-id="e8655-158">`-- <command>`（仅适用于运行 .NET 5.0 或更高版本的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="e8655-158">**`-- <command>` (for target applications running .NET 5.0 or later only)**</span></span>

  <span data-ttu-id="e8655-159">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="e8655-159">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="e8655-160">`dotnet-counters` 将启动一个进程，并监视请求的指标。</span><span class="sxs-lookup"><span data-stu-id="e8655-160">`dotnet-counters` will launch a process with the provided command and monitor the requested metrics.</span></span> <span data-ttu-id="e8655-161">这通常用于收集应用程序的启动路径的指标，并可用于诊断或监视在主入口点前后发生的问题。</span><span class="sxs-lookup"><span data-stu-id="e8655-161">This is often useful to collect metrics for the application's startup path and can be used to diagnose or monitor issues that happen early before or shortly after the main entrypoint.</span></span>

  > [!NOTE]
  > <span data-ttu-id="e8655-162">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="e8655-162">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="e8655-163">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="e8655-163">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

### <a name="examples"></a><span data-ttu-id="e8655-164">示例</span><span class="sxs-lookup"><span data-stu-id="e8655-164">Examples</span></span>

- <span data-ttu-id="e8655-165">以 3 秒的刷新间隔监视 `System.Runtime` 中的所有计数器：</span><span class="sxs-lookup"><span data-stu-id="e8655-165">Monitor all counters from `System.Runtime` at a refresh interval of 3 seconds:</span></span>

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

- <span data-ttu-id="e8655-166">仅监视 `System.Runtime` 中的 CPU 使用情况和 GC 堆大小：</span><span class="sxs-lookup"><span data-stu-id="e8655-166">Monitor just CPU usage and GC heap size from `System.Runtime`:</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902 --counters System.Runtime[cpu-usage,gc-heap-size]

  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      CPU Usage (%)                                 24
      GC Heap Size (MB)                            811
  ```

- <span data-ttu-id="e8655-167">监视用户定义的 `EventSource` 中的 `EventCounter` 值。</span><span class="sxs-lookup"><span data-stu-id="e8655-167">Monitor `EventCounter` values from user-defined `EventSource`.</span></span> <span data-ttu-id="e8655-168">有关详细信息，请参阅[教程：使用 .NET Core 中的 EventCounters 衡量性能](event-counter-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="e8655-168">For more information, see [Tutorial: Measure performance using EventCounters in .NET Core](event-counter-perf.md).</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902 --counters Samples-EventCounterDemos-Minimal

  Press p to pause, r to resume, q to quit.
      request                                      100
  ```

- <span data-ttu-id="e8655-169">启动 `my-aspnet-server.exe` 并从其启动监视加载的程序集的数量（仅限 .NET 5.0 或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="e8655-169">Launch `my-aspnet-server.exe` and monitor the # of assemblies loaded from its startup (.NET 5.0 or later only):</span></span>

  <span data-ttu-id="e8655-170">注意：这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="e8655-170">NOTE: This works for apps running .NET 5.0 or later only.</span></span>

  ```console
  > dotnet-counters monitor --counters System.Runtime[assembly-count] -- my-aspnet-server.exe

  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      Number of Assemblies Loaded                   24
  ```
  
- <span data-ttu-id="e8655-171">启动 `my-aspnet-server.exe`，以 `arg1` 及 `arg2` 作为命令行参数，并从其启动监视其工作集和 GC 堆大小（仅限 .NET 5.0 或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="e8655-171">Launch `my-aspnet-server.exe` with `arg1` and `arg2` as command-line arguments and monitor its working set and GC heap size from its startup (.NET 5.0 or later only):</span></span>

  <span data-ttu-id="e8655-172">注意：这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="e8655-172">NOTE: This works for apps running .NET 5.0 or later only.</span></span>

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

## <a name="dotnet-counters-ps"></a><span data-ttu-id="e8655-173">dotnet-counters ps</span><span class="sxs-lookup"><span data-stu-id="e8655-173">dotnet-counters ps</span></span>

<span data-ttu-id="e8655-174">显示可监视的 dotnet 进程的列表。</span><span class="sxs-lookup"><span data-stu-id="e8655-174">Display a list of dotnet processes that can be monitored.</span></span>

### <a name="synopsis"></a><span data-ttu-id="e8655-175">摘要</span><span class="sxs-lookup"><span data-stu-id="e8655-175">Synopsis</span></span>

```console
dotnet-counters ps [-h|--help]
```

### <a name="example"></a><span data-ttu-id="e8655-176">示例</span><span class="sxs-lookup"><span data-stu-id="e8655-176">Example</span></span>

```console
> dotnet-counters ps
  
  15683 WebApi     /home/suwhang/repos/WebApi/WebApi
  16324 dotnet     /usr/local/share/dotnet/dotnet
```
