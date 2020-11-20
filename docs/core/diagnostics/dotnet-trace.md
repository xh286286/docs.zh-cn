---
title: dotnet-trace 工具 - .NET Core
description: 安装和使用 dotnet-trace 命令行工具。
ms.date: 11/21/2019
ms.openlocfilehash: d4175ccad785b21f860044a4fd5d691624ec495e
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94507221"
---
# <a name="dotnet-trace-performance-analysis-utility"></a><span data-ttu-id="612c5-103">dotnet-trace 性能分析实用工具</span><span class="sxs-lookup"><span data-stu-id="612c5-103">dotnet-trace performance analysis utility</span></span>

<span data-ttu-id="612c5-104">本文适用于： ✔️ .NET Core 3.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="612c5-104">**This article applies to:** ✔️ .NET Core 3.0 SDK and later versions</span></span>

## <a name="install-dotnet-trace"></a><span data-ttu-id="612c5-105">安装 dotnet-trace</span><span class="sxs-lookup"><span data-stu-id="612c5-105">Install dotnet-trace</span></span>

<span data-ttu-id="612c5-106">使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令安装 `dotnet-trace` [NuGet 包](https://www.nuget.org/packages/dotnet-trace)：</span><span class="sxs-lookup"><span data-stu-id="612c5-106">Install `dotnet-trace` [NuGet package](https://www.nuget.org/packages/dotnet-trace) with the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

```dotnetcli
dotnet tool install --global dotnet-trace
```

## <a name="synopsis"></a><span data-ttu-id="612c5-107">摘要</span><span class="sxs-lookup"><span data-stu-id="612c5-107">Synopsis</span></span>

```console
dotnet-trace [-h, --help] [--version] <command>
```

## <a name="description"></a><span data-ttu-id="612c5-108">描述</span><span class="sxs-lookup"><span data-stu-id="612c5-108">Description</span></span>

<span data-ttu-id="612c5-109">`dotnet-trace` 工具：</span><span class="sxs-lookup"><span data-stu-id="612c5-109">The `dotnet-trace` tool:</span></span>

* <span data-ttu-id="612c5-110">是一个跨平台的 .NET Core 工具。</span><span class="sxs-lookup"><span data-stu-id="612c5-110">Is a cross-platform .NET Core tool.</span></span>
* <span data-ttu-id="612c5-111">在不使用本机探查器的情况下启用正在运行的进程的 .NET Core 跟踪集合。</span><span class="sxs-lookup"><span data-stu-id="612c5-111">Enables the collection of .NET Core traces of a running process without a native profiler.</span></span>
* <span data-ttu-id="612c5-112">它是围绕 .NET Core 运行时的跨平台 `EventPipe` 技术而构建的。</span><span class="sxs-lookup"><span data-stu-id="612c5-112">Is built around the cross-platform `EventPipe` technology of the .NET Core runtime.</span></span>
* <span data-ttu-id="612c5-113">在 Windows、Linux 或 macOS 上提供相同体验。</span><span class="sxs-lookup"><span data-stu-id="612c5-113">Delivers the same experience on Windows, Linux, or macOS.</span></span>

## <a name="options"></a><span data-ttu-id="612c5-114">选项</span><span class="sxs-lookup"><span data-stu-id="612c5-114">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="612c5-115">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="612c5-115">Shows command-line help.</span></span>

- **`--version`**

  <span data-ttu-id="612c5-116">显示 dotnet-dump 实用工具的版本。</span><span class="sxs-lookup"><span data-stu-id="612c5-116">Displays the version of the dotnet-trace utility.</span></span>

## <a name="commands"></a><span data-ttu-id="612c5-117">命令</span><span class="sxs-lookup"><span data-stu-id="612c5-117">Commands</span></span>

| <span data-ttu-id="612c5-118">命令</span><span class="sxs-lookup"><span data-stu-id="612c5-118">Command</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="612c5-119">dotnet-trace collect</span><span class="sxs-lookup"><span data-stu-id="612c5-119">dotnet-trace collect</span></span>](#dotnet-trace-collect)             |
| [<span data-ttu-id="612c5-120">dotnet-trace convert</span><span class="sxs-lookup"><span data-stu-id="612c5-120">dotnet-trace convert</span></span>](#dotnet-trace-convert)             |
| [<span data-ttu-id="612c5-121">dotnet-trace ps</span><span class="sxs-lookup"><span data-stu-id="612c5-121">dotnet-trace ps</span></span>](#dotnet-trace-ps)                       |
| [<span data-ttu-id="612c5-122">dotnet-trace list-profiles</span><span class="sxs-lookup"><span data-stu-id="612c5-122">dotnet-trace list-profiles</span></span>](#dotnet-trace-list-profiles) |

## <a name="dotnet-trace-collect"></a><span data-ttu-id="612c5-123">dotnet-trace collect</span><span class="sxs-lookup"><span data-stu-id="612c5-123">dotnet-trace collect</span></span>

<span data-ttu-id="612c5-124">从正在运行的进程中收集诊断跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-124">Collects a diagnostic trace from a running process.</span></span>

### <a name="synopsis"></a><span data-ttu-id="612c5-125">摘要</span><span class="sxs-lookup"><span data-stu-id="612c5-125">Synopsis</span></span>

```console
dotnet-trace collect [--buffersize <size>] [--clreventlevel <clreventlevel>] [--clrevents <clrevents>]
    [--format <Chromium|NetTrace|Speedscope>] [-h|--help]
    [-n, --name <name>]  [-o|--output <trace-file-path>] [-p|--process-id <pid>]
    [--profile <profile-name>] [--providers <list-of-comma-separated-providers>]
    [-- <command>] (for target applications running .NET 5.0 or later)
```

### <a name="options"></a><span data-ttu-id="612c5-126">选项</span><span class="sxs-lookup"><span data-stu-id="612c5-126">Options</span></span>

- **`--buffersize <size>`**

  <span data-ttu-id="612c5-127">设置内存中循环缓冲区的大小（以 MB 表示）。</span><span class="sxs-lookup"><span data-stu-id="612c5-127">Sets the size of the in-memory circular buffer, in megabytes.</span></span> <span data-ttu-id="612c5-128">默认值为 256 MB。</span><span class="sxs-lookup"><span data-stu-id="612c5-128">Default 256 MB.</span></span>

- **`--clreventlevel <clreventlevel>`**

  <span data-ttu-id="612c5-129">要发出的 CLR 事件的详细级别。</span><span class="sxs-lookup"><span data-stu-id="612c5-129">Verbosity of CLR events to be emitted.</span></span>

- **`--clrevents <clrevents>`**

  <span data-ttu-id="612c5-130">要发出的 CLR 运行时事件的列表。</span><span class="sxs-lookup"><span data-stu-id="612c5-130">List of CLR runtime events to emit.</span></span>

- **`--format {Chromium|NetTrace|Speedscope}`**

  <span data-ttu-id="612c5-131">设置跟踪文件转换的输出格式。</span><span class="sxs-lookup"><span data-stu-id="612c5-131">Sets the output format for the trace file conversion.</span></span> <span data-ttu-id="612c5-132">默认值为 `NetTrace`。</span><span class="sxs-lookup"><span data-stu-id="612c5-132">The default is `NetTrace`.</span></span>

- **`-n, --name <name>`**

  <span data-ttu-id="612c5-133">从中收集跟踪的进程的名称。</span><span class="sxs-lookup"><span data-stu-id="612c5-133">The name of the process to collect the trace from.</span></span>

- **`-o|--output <trace-file-path>`**

  <span data-ttu-id="612c5-134">收集的跟踪数据的输出路径。</span><span class="sxs-lookup"><span data-stu-id="612c5-134">The output path for the collected trace data.</span></span> <span data-ttu-id="612c5-135">如果未指定，则默认为 `trace.nettrace`。</span><span class="sxs-lookup"><span data-stu-id="612c5-135">If not specified, it defaults to `trace.nettrace`.</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="612c5-136">从中收集跟踪的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="612c5-136">The process id to collect the trace from.</span></span>

- **`--profile <profile-name>`**

  <span data-ttu-id="612c5-137">一组命名的预定义提供程序配置，允许简明地指定常见跟踪方案。</span><span class="sxs-lookup"><span data-stu-id="612c5-137">A named pre-defined set of provider configurations that allows common tracing scenarios to be specified succinctly.</span></span>

- **`--providers <list-of-comma-separated-providers>`**

  <span data-ttu-id="612c5-138">要启用的 `EventPipe` 提供程序的以逗号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="612c5-138">A comma-separated list of `EventPipe` providers to be enabled.</span></span> <span data-ttu-id="612c5-139">这些提供程序会补充 `--profile <profile-name>` 隐含的任何提供程序。</span><span class="sxs-lookup"><span data-stu-id="612c5-139">These providers supplement any providers implied by `--profile <profile-name>`.</span></span> <span data-ttu-id="612c5-140">如果特定提供程序存在任何不一致的情况，此配置将优先于配置文件中的隐式配置。</span><span class="sxs-lookup"><span data-stu-id="612c5-140">If there's any inconsistency for a particular provider, this configuration takes precedence over the implicit configuration from the profile.</span></span>

  <span data-ttu-id="612c5-141">此提供程序列表的格式为：</span><span class="sxs-lookup"><span data-stu-id="612c5-141">This list of providers is in the form:</span></span>

  - `Provider[,Provider]`
  - <span data-ttu-id="612c5-142">`Provider` 的格式为：`KnownProviderName[:Flags[:Level][:KeyValueArgs]]`。</span><span class="sxs-lookup"><span data-stu-id="612c5-142">`Provider` is in the form: `KnownProviderName[:Flags[:Level][:KeyValueArgs]]`.</span></span>
  - <span data-ttu-id="612c5-143">`KeyValueArgs` 的格式为：`[key1=value1][;key2=value2]`。</span><span class="sxs-lookup"><span data-stu-id="612c5-143">`KeyValueArgs` is in the form: `[key1=value1][;key2=value2]`.</span></span>

- <span data-ttu-id="612c5-144">`-- <command>`（仅适用于运行 .NET 5.0 的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="612c5-144">**`-- <command>` (for target applications running .NET 5.0 only)**</span></span>

  <span data-ttu-id="612c5-145">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="612c5-145">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="612c5-146">这在过程早期发生诊断问题（如启动性能问题或程序集加载程序和绑定器错误）时可能会有所帮助。</span><span class="sxs-lookup"><span data-stu-id="612c5-146">This may be helpful when diagnosing issues that happen early in the process, such as startup performance issue or assembly loader and binder errors.</span></span>

  > [!NOTE]
  > <span data-ttu-id="612c5-147">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="612c5-147">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="612c5-148">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="612c5-148">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

## <a name="dotnet-trace-convert"></a><span data-ttu-id="612c5-149">dotnet-trace convert</span><span class="sxs-lookup"><span data-stu-id="612c5-149">dotnet-trace convert</span></span>

<span data-ttu-id="612c5-150">将 `nettrace` 跟踪转换为备用格式，以便用于备用跟踪分析工具。</span><span class="sxs-lookup"><span data-stu-id="612c5-150">Converts `nettrace` traces to alternate formats for use with alternate trace analysis tools.</span></span>

### <a name="synopsis"></a><span data-ttu-id="612c5-151">摘要</span><span class="sxs-lookup"><span data-stu-id="612c5-151">Synopsis</span></span>

```console
dotnet-trace convert [<input-filename>] [--format <Chromium|NetTrace|Speedscope>] [-h|--help] [-o|--output <output-filename>]
```

### <a name="arguments"></a><span data-ttu-id="612c5-152">自变量</span><span class="sxs-lookup"><span data-stu-id="612c5-152">Arguments</span></span>

- **`<input-filename>`**

  <span data-ttu-id="612c5-153">要转换的输入跟踪文件。</span><span class="sxs-lookup"><span data-stu-id="612c5-153">Input trace file to be converted.</span></span> <span data-ttu-id="612c5-154">默认为 trace.nettrace  。</span><span class="sxs-lookup"><span data-stu-id="612c5-154">Defaults to *trace.nettrace*.</span></span>

### <a name="options"></a><span data-ttu-id="612c5-155">选项</span><span class="sxs-lookup"><span data-stu-id="612c5-155">Options</span></span>

- **`--format <Chromium|NetTrace|Speedscope>`**

  <span data-ttu-id="612c5-156">设置跟踪文件转换的输出格式。</span><span class="sxs-lookup"><span data-stu-id="612c5-156">Sets the output format for the trace file conversion.</span></span>

- **`-o|--output <output-filename>`**

  <span data-ttu-id="612c5-157">输出文件名。</span><span class="sxs-lookup"><span data-stu-id="612c5-157">Output filename.</span></span> <span data-ttu-id="612c5-158">将添加目标格式的扩展。</span><span class="sxs-lookup"><span data-stu-id="612c5-158">Extension of target format will be added.</span></span>

## <a name="dotnet-trace-ps"></a><span data-ttu-id="612c5-159">dotnet-trace ps</span><span class="sxs-lookup"><span data-stu-id="612c5-159">dotnet-trace ps</span></span>

 <span data-ttu-id="612c5-160">列出可从中收集跟踪的 dotnet 进程。</span><span class="sxs-lookup"><span data-stu-id="612c5-160">Lists the dotnet processes that traces can be collected from.</span></span>

### <a name="synopsis"></a><span data-ttu-id="612c5-161">摘要</span><span class="sxs-lookup"><span data-stu-id="612c5-161">Synopsis</span></span>

```console
dotnet-trace ps [-h|--help]
```

## <a name="dotnet-trace-list-profiles"></a><span data-ttu-id="612c5-162">dotnet-trace list-profiles</span><span class="sxs-lookup"><span data-stu-id="612c5-162">dotnet-trace list-profiles</span></span>

<span data-ttu-id="612c5-163">列出预生成的跟踪配置文件，并描述每个配置文件中包含的提供程序和筛选器。</span><span class="sxs-lookup"><span data-stu-id="612c5-163">Lists pre-built tracing profiles with a description of what providers and filters are in each profile.</span></span>

### <a name="synopsis"></a><span data-ttu-id="612c5-164">摘要</span><span class="sxs-lookup"><span data-stu-id="612c5-164">Synopsis</span></span>

```console
dotnet-trace list-profiles [-h|--help]
```

## <a name="collect-a-trace-with-dotnet-trace"></a><span data-ttu-id="612c5-165">使用 dotnet-trace 收集跟踪</span><span class="sxs-lookup"><span data-stu-id="612c5-165">Collect a trace with dotnet-trace</span></span>

<span data-ttu-id="612c5-166">若要使用 `dotnet-trace` 收集跟踪，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="612c5-166">To collect traces using `dotnet-trace`:</span></span>

- <span data-ttu-id="612c5-167">需要首先查找要从中收集跟踪的 .NET Core 应用程序的进程标识符 (PID)。</span><span class="sxs-lookup"><span data-stu-id="612c5-167">Get the process identifier (PID) of the .NET Core application to collect traces from.</span></span>

  - <span data-ttu-id="612c5-168">例如，在 Windows 上，可以使用任务管理器或 `tasklist` 命令。</span><span class="sxs-lookup"><span data-stu-id="612c5-168">On Windows, you can use Task Manager or the `tasklist` command, for example.</span></span>
  - <span data-ttu-id="612c5-169">在 Linux 上，使用 `ps` 命令。</span><span class="sxs-lookup"><span data-stu-id="612c5-169">On Linux, for example, the `ps` command.</span></span>
  - [<span data-ttu-id="612c5-170">dotnet-trace ps</span><span class="sxs-lookup"><span data-stu-id="612c5-170">dotnet-trace ps</span></span>](#dotnet-trace-ps)

- <span data-ttu-id="612c5-171">运行下面的命令：</span><span class="sxs-lookup"><span data-stu-id="612c5-171">Run the following command:</span></span>

  ```console
  dotnet-trace collect --process-id <PID>
  ```

  <span data-ttu-id="612c5-172">前面的命令生成类似于以下内容的输出：</span><span class="sxs-lookup"><span data-stu-id="612c5-172">The preceding command generates output similar to the following:</span></span>

  ```console
  Press <Enter> to exit...
  Connecting to process: <Full-Path-To-Process-Being-Profiled>/dotnet.exe
  Collecting to file: <Full-Path-To-Trace>/trace.nettrace
  Session Id: <SessionId>
  Recording trace 721.025 (KB)
  ```

- <span data-ttu-id="612c5-173">按 `<Enter>` 键停止收集。</span><span class="sxs-lookup"><span data-stu-id="612c5-173">Stop collection by pressing the `<Enter>` key.</span></span> <span data-ttu-id="612c5-174">`dotnet-trace` 会将完成将事件记录到 trace.nettrace 文件中  。</span><span class="sxs-lookup"><span data-stu-id="612c5-174">`dotnet-trace` will finish logging events to the *trace.nettrace* file.</span></span>

## <a name="launch-a-child-application-and-collect-a-trace-from-its-startup-using-dotnet-trace"></a><span data-ttu-id="612c5-175">启动子应用程序，并使用 dotnet-trace 从启动中收集跟踪</span><span class="sxs-lookup"><span data-stu-id="612c5-175">Launch a child application and collect a trace from its startup using dotnet-trace</span></span>

<span data-ttu-id="612c5-176">注意：这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="612c5-176">NOTE: This works for apps running .NET 5.0 or later only.</span></span>

<span data-ttu-id="612c5-177">有时，从进程启动中收集进程的跟踪可能很有用。</span><span class="sxs-lookup"><span data-stu-id="612c5-177">Sometimes it may be useful to collect a trace of a process from its startup.</span></span> <span data-ttu-id="612c5-178">对于运行 .NET 5.0 或更高版本的应用，可以使用 dotnet-trace 来做到这一点。</span><span class="sxs-lookup"><span data-stu-id="612c5-178">For apps running .NET 5.0 or later, it is possible to do this by using dotnet-trace.</span></span>

<span data-ttu-id="612c5-179">这将启动 `hello.exe`并以 `arg1` 及 `arg2` 作为其命令行参数，从其运行时启动中收集跟踪：</span><span class="sxs-lookup"><span data-stu-id="612c5-179">This will launch `hello.exe` with `arg1` and `arg2` as its command line arguments and collect a trace from its runtime startup:</span></span>

```console
dotnet-trace collect -- hello.exe arg1 arg2
```

<span data-ttu-id="612c5-180">前面的命令生成类似于以下内容的输出：</span><span class="sxs-lookup"><span data-stu-id="612c5-180">The preceding command generates output similar to the following:</span></span>

```console
No profile or providers specified, defaulting to trace profile 'cpu-sampling'

Provider Name                           Keywords            Level               Enabled By
Microsoft-DotNETCore-SampleProfiler     0x0000F00000000000  Informational(4)    --profile
Microsoft-Windows-DotNETRuntime         0x00000014C14FCCBD  Informational(4)    --profile

Process        : E:\temp\gcperfsim\bin\Debug\net5.0\gcperfsim.exe
Output File    : E:\temp\gcperfsim\trace.nettrace


[00:00:00:05]   Recording trace 122.244  (KB)
Press <Enter> or <Ctrl+C> to exit...
```

<span data-ttu-id="612c5-181">可以通过按 `<Enter>` 或 `<Ctrl + C>` 键来停止收集跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-181">You can stop collecting the trace by pressing `<Enter>` or `<Ctrl + C>` key.</span></span> <span data-ttu-id="612c5-182">此操作还将退出 `hello.exe`。</span><span class="sxs-lookup"><span data-stu-id="612c5-182">Doing this will also exit `hello.exe`.</span></span>

> [!NOTE]
> <span data-ttu-id="612c5-183">通过 dotnet-trace 启动 `hello.exe` 将重定向其输入/输出，你将无法与其 stdin/stdout 进行交互。</span><span class="sxs-lookup"><span data-stu-id="612c5-183">Launching `hello.exe` via dotnet-trace will make its input/output to be redirected and you won't be able to interact with its stdin/stdout.</span></span>
> <span data-ttu-id="612c5-184">通过 CTRL+C 或 SIGTERM 退出工具将安全地结束该工具和子进程。</span><span class="sxs-lookup"><span data-stu-id="612c5-184">Exiting the tool via CTRL+C or SIGTERM will safely end both the tool and the child process.</span></span>
> <span data-ttu-id="612c5-185">如果子进程在工具之前退出，工具也将退出，应可安全查看跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-185">If the child process exits before the tool, the tool will exit as well and the trace should be safely viewable.</span></span>

## <a name="view-the-trace-captured-from-dotnet-trace"></a><span data-ttu-id="612c5-186">查看由 dotnet-trace 捕获的跟踪</span><span class="sxs-lookup"><span data-stu-id="612c5-186">View the trace captured from dotnet-trace</span></span>

<span data-ttu-id="612c5-187">在 Windows 上，可以使用 [PerfView](https://github.com/microsoft/perfview) 查看 .nettrace 文件以进行分析  ：对于其他平台上收集的跟踪，可以将跟踪文件移动到 Windows 计算机上，以在 PerfView 上进行查看。</span><span class="sxs-lookup"><span data-stu-id="612c5-187">On Windows, *.nettrace* files can be viewed on [PerfView](https://github.com/microsoft/perfview) for analysis: For traces collected on other platforms, the trace file can be moved to a Windows machine to be viewed on PerfView.</span></span>

<span data-ttu-id="612c5-188">在 Linux 上，可以通过将 `dotnet-trace` 的输出格式更改为 `speedscope` 来查看跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-188">On Linux, the trace can be viewed by changing the output format of `dotnet-trace` to `speedscope`.</span></span> <span data-ttu-id="612c5-189">可以使用 `-f|--format` 选项更改输出文件格式 - `-f speedscope` 会使 `dotnet-trace` 生成 `speedscope` 文件。</span><span class="sxs-lookup"><span data-stu-id="612c5-189">The output file format can be changed using the `-f|--format` option - `-f speedscope` will make `dotnet-trace` produce a `speedscope` file.</span></span> <span data-ttu-id="612c5-190">可以在 `nettrace`（默认选项）和 `speedscope` 之间进行选择。</span><span class="sxs-lookup"><span data-stu-id="612c5-190">You can choose between `nettrace` (the default option) and `speedscope`.</span></span> <span data-ttu-id="612c5-191">可以在 <https://www.speedscope.app> 打开 `Speedscope` 文件。</span><span class="sxs-lookup"><span data-stu-id="612c5-191">`Speedscope` files can be opened at <https://www.speedscope.app>.</span></span>

> [!NOTE]
> <span data-ttu-id="612c5-192">.NET Core 运行时以 `nettrace` 格式生成跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-192">The .NET Core runtime generates traces in the `nettrace` format.</span></span> <span data-ttu-id="612c5-193">跟踪完成后，跟踪将转换为 speedscope（如果指定）。</span><span class="sxs-lookup"><span data-stu-id="612c5-193">The traces are converted to speedscope (if specified) after the trace is completed.</span></span> <span data-ttu-id="612c5-194">由于某些转换可能会导致数据丢失，因此，原始 `nettrace` 文件将保留在转换后的文件旁边。</span><span class="sxs-lookup"><span data-stu-id="612c5-194">Since some conversions may result in loss of data, the original `nettrace` file is preserved next to the converted file.</span></span>

## <a name="use-dotnet-trace-to-collect-counter-values-over-time"></a><span data-ttu-id="612c5-195">使用 dotnet-trace 收集随时间变化的计数器值</span><span class="sxs-lookup"><span data-stu-id="612c5-195">Use dotnet-trace to collect counter values over time</span></span>

<span data-ttu-id="612c5-196">`dotnet-trace` 可以：</span><span class="sxs-lookup"><span data-stu-id="612c5-196">`dotnet-trace` can:</span></span>

* <span data-ttu-id="612c5-197">在性能敏感的环境中使用 `EventCounter` 进行基本运行状况监视。</span><span class="sxs-lookup"><span data-stu-id="612c5-197">Use `EventCounter` for basic health monitoring in performance-sensitive environments.</span></span> <span data-ttu-id="612c5-198">例如，在生产环境中。</span><span class="sxs-lookup"><span data-stu-id="612c5-198">For example, in production.</span></span>
* <span data-ttu-id="612c5-199">收集跟踪，这样就不需要实时查看。</span><span class="sxs-lookup"><span data-stu-id="612c5-199">Collect traces so they don't need to be viewed in real time.</span></span>

<span data-ttu-id="612c5-200">例如，若要收集运行时性能计数器值，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="612c5-200">For example, to collect runtime performance counter values, use the following command:</span></span>

```console
dotnet-trace collect --process-id <PID> --providers System.Runtime:0:1:EventCounterIntervalSec=1
```

<span data-ttu-id="612c5-201">上述命令通知运行时计数器每秒报告一次，以便进行轻量型运行状况监视。</span><span class="sxs-lookup"><span data-stu-id="612c5-201">The preceding command tells the runtime counters to report once every second for lightweight health monitoring.</span></span> <span data-ttu-id="612c5-202">通过使用较大的值（例如 60）替换 `EventCounterIntervalSec=1`，可以收集计数器数据中粒度较小的跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-202">Replacing `EventCounterIntervalSec=1` with a higher value (for example, 60) allows collection of a smaller trace with less granularity in the counter data.</span></span>

<span data-ttu-id="612c5-203">以下命令比以上命令产生更小的开销和跟踪大小：</span><span class="sxs-lookup"><span data-stu-id="612c5-203">The following command reduces overhead and trace size more than the preceding one:</span></span>

```console
dotnet-trace collect --process-id <PID> --providers System.Runtime:0:1:EventCounterIntervalSec=1,Microsoft-Windows-DotNETRuntime:0:1,Microsoft-DotNETCore-SampleProfiler:0:1
```

<span data-ttu-id="612c5-204">以上命令会禁用运行时事件和托管堆栈探查器。</span><span class="sxs-lookup"><span data-stu-id="612c5-204">The preceding command disables runtime events and the managed stack profiler.</span></span>

## <a name="net-providers"></a><span data-ttu-id="612c5-205">.NET 提供程序</span><span class="sxs-lookup"><span data-stu-id="612c5-205">.NET Providers</span></span>

<span data-ttu-id="612c5-206">.NET Core 运行时支持以下 .NET 提供程序：</span><span class="sxs-lookup"><span data-stu-id="612c5-206">The .NET Core runtime supports the following .NET providers.</span></span> <span data-ttu-id="612c5-207">.NET Core 使用相同的关键字来启用 `Event Tracing for Windows (ETW)` 和 `EventPipe` 跟踪。</span><span class="sxs-lookup"><span data-stu-id="612c5-207">.NET Core uses the same keywords to enable both `Event Tracing for Windows (ETW)` and `EventPipe` traces.</span></span>

| <span data-ttu-id="612c5-208">提供程序名称</span><span class="sxs-lookup"><span data-stu-id="612c5-208">Provider name</span></span>                            | <span data-ttu-id="612c5-209">信息</span><span class="sxs-lookup"><span data-stu-id="612c5-209">Information</span></span> |
|------------------------------------------|-------------|
| `Microsoft-Windows-DotNETRuntime`        | [<span data-ttu-id="612c5-210">运行时提供程序</span><span class="sxs-lookup"><span data-stu-id="612c5-210">The Runtime Provider</span></span>](../../framework/performance/clr-etw-providers.md#the-runtime-provider)<br>[<span data-ttu-id="612c5-211">CLR 运行时关键字</span><span class="sxs-lookup"><span data-stu-id="612c5-211">CLR Runtime Keywords</span></span>](../../framework/performance/clr-etw-keywords-and-levels.md#runtime) |
| `Microsoft-Windows-DotNETRuntimeRundown` | [<span data-ttu-id="612c5-212">断开提供程序</span><span class="sxs-lookup"><span data-stu-id="612c5-212">The Rundown Provider</span></span>](../../framework/performance/clr-etw-providers.md#the-rundown-provider)<br>[<span data-ttu-id="612c5-213">CLR 断开关键字</span><span class="sxs-lookup"><span data-stu-id="612c5-213">CLR Rundown Keywords</span></span>](../../framework/performance/clr-etw-keywords-and-levels.md#rundown) |
| `Microsoft-DotNETCore-SampleProfiler`    | <span data-ttu-id="612c5-214">启用示例探查器。</span><span class="sxs-lookup"><span data-stu-id="612c5-214">Enables the sample profiler.</span></span> |
