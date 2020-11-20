---
title: .NET SDK 遥测
description: 了解可收集使用情况信息以供分析的 .NET SDK 遥测功能、收集的数据，以及如何禁用遥测。
author: KathleenDollard
ms.date: 08/27/2019
ms.openlocfilehash: 4f137822c61e1a04eccd28ebd0cd56c04f4a85e2
ms.sourcegitcommit: b201d177e01480a139622f3bf8facd367657a472
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2020
ms.locfileid: "94633864"
---
# <a name="net-sdk-telemetry"></a><span data-ttu-id="5bc0a-103">.NET SDK 遥测</span><span class="sxs-lookup"><span data-stu-id="5bc0a-103">.NET SDK telemetry</span></span>

<span data-ttu-id="5bc0a-104">[.NET SDK](index.md) 包含遥测功能，可在 .NET CLI 崩溃时收集使用情况数据和异常信息。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-104">The [.NET SDK](index.md) includes a telemetry feature that collects usage data and exception information when the .NET CLI crashes.</span></span> <span data-ttu-id="5bc0a-105">.NET CLI 附带 .NET SDK，是一组用于生成、测试和发布 .NET 应用的谓词。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-105">The .NET CLI comes with the .NET SDK and is the set of verbs that enable you to build, test, and publish your .NET apps.</span></span> <span data-ttu-id="5bc0a-106">请务必让 .NET 团队了解到工具使用情况，以便我们对其做出改进。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-106">It's important that the .NET team understands how the tools are used so they can be improved.</span></span> <span data-ttu-id="5bc0a-107">有关故障的信息可帮助团队解决问题并修复 bug。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-107">Information on failures helps the team resolve problems and fix bugs.</span></span>

<span data-ttu-id="5bc0a-108">收集的数据根据 [Creative Commons Attribution 许可证](https://creativecommons.org/licenses/by/4.0/)以汇总形式发布。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-108">The collected data is published in aggregate under the [Creative Commons Attribution License](https://creativecommons.org/licenses/by/4.0/).</span></span>

## <a name="scope"></a><span data-ttu-id="5bc0a-109">范围</span><span class="sxs-lookup"><span data-stu-id="5bc0a-109">Scope</span></span>

<span data-ttu-id="5bc0a-110">`dotnet` 具有两个功能：运行应用程序和执行 CLI 命令。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-110">`dotnet` has two functions: to run apps, and to execute CLI commands.</span></span> <span data-ttu-id="5bc0a-111">按以下格式使用 `dotnet` 来启动应用程序时，不会收集遥测数据：</span><span class="sxs-lookup"><span data-stu-id="5bc0a-111">Telemetry *isn't collected* when using `dotnet` to start an application in the following format:</span></span>

- `dotnet [path-to-app].dll`

<span data-ttu-id="5bc0a-112">使用任何 [.NET CLI 命令](index.md)时，都会收集遥测数据，如：</span><span class="sxs-lookup"><span data-stu-id="5bc0a-112">Telemetry *is collected* when using any of the [.NET CLI commands](index.md), such as:</span></span>

- `dotnet build`
- `dotnet pack`
- `dotnet run`

## <a name="how-to-opt-out"></a><span data-ttu-id="5bc0a-113">如何选择退出</span><span class="sxs-lookup"><span data-stu-id="5bc0a-113">How to opt out</span></span>

<span data-ttu-id="5bc0a-114">.NET SDK 遥测功能默认处于启用状态。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-114">The .NET SDK telemetry feature is enabled by default.</span></span> <span data-ttu-id="5bc0a-115">要选择退出遥测功能，请将 `DOTNET_CLI_TELEMETRY_OPTOUT` 环境变量设置为 `1` 或 `true`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-115">To opt out of the telemetry feature, set the `DOTNET_CLI_TELEMETRY_OPTOUT` environment variable to `1` or `true`.</span></span>

<span data-ttu-id="5bc0a-116">如果安装成功，.NET SDK 安装程序也会发送一个遥测条目。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-116">A single telemetry entry is also sent by the .NET SDK installer when a successful installation happens.</span></span> <span data-ttu-id="5bc0a-117">若要选择退出，请在安装 .NET SDK 之前设置 `DOTNET_CLI_TELEMETRY_OPTOUT` 环境变量。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-117">To opt out, set the `DOTNET_CLI_TELEMETRY_OPTOUT` environment variable before you install the .NET SDK.</span></span>

## <a name="disclosure"></a><span data-ttu-id="5bc0a-118">公开</span><span class="sxs-lookup"><span data-stu-id="5bc0a-118">Disclosure</span></span>

<span data-ttu-id="5bc0a-119">首次运行其中一个 [.NET CLI 命令](index.md)（如 `dotnet build`）时，.NET SDK 显示以下类似文本。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-119">The .NET SDK displays text similar to the following when you first run one of the [.NET CLI commands](index.md) (for example, `dotnet build`).</span></span> <span data-ttu-id="5bc0a-120">文本可能会因运行的 SDK 版本而略有不同。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-120">Text may vary slightly depending on the version of the SDK you're running.</span></span> <span data-ttu-id="5bc0a-121">此“首次运行”体验是 Microsoft 通知用户有关数据收集信息的方式。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-121">This "first run" experience is how Microsoft notifies you about data collection.</span></span>

```console
Telemetry
---------
The .NET tools collect usage data in order to help us improve your experience. The data is collected by Microsoft and shared with the community. You can opt-out of telemetry by setting the DOTNET_CLI_TELEMETRY_OPTOUT environment variable to '1' or 'true' using your favorite shell.

Read more about .NET CLI Tools telemetry: https://aka.ms/dotnet-cli-telemetry
```

<span data-ttu-id="5bc0a-122">若要禁用此消息和 .NET 欢迎消息，请将 `DOTNET_NOLOGO` 环境变量设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-122">To disable this message and the .NET welcome message, set the `DOTNET_NOLOGO` environment variable to `true`.</span></span> <span data-ttu-id="5bc0a-123">请注意，此变量在遥测选择退出时不起作用。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-123">Note that this variable has no effect on telemetry opt out.</span></span>

## <a name="data-points"></a><span data-ttu-id="5bc0a-124">数据点</span><span class="sxs-lookup"><span data-stu-id="5bc0a-124">Data points</span></span>

<span data-ttu-id="5bc0a-125">遥测功能不收集用户名或电子邮件地址等个人数据。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-125">The telemetry feature doesn't collect personal data, such as usernames or email addresses.</span></span> <span data-ttu-id="5bc0a-126">也不会扫描代码，更不会提取项目级敏感数据，如名称、存储库或作者。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-126">It doesn't scan your code and doesn't extract project-level data, such as name, repository, or author.</span></span> <span data-ttu-id="5bc0a-127">数据通过 [Azure Monitor](https://azure.microsoft.com/services/monitor/) 技术安全地发送到 Microsoft 服务器，提供对保留数据的受限访问权限，并在严格的安全控制下从安全的 [Azure 存储](https://azure.microsoft.com/services/storage/)系统发布。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-127">The data is sent securely to Microsoft servers using [Azure Monitor](https://azure.microsoft.com/services/monitor/) technology, held under restricted access, and published under strict security controls from secure [Azure Storage](https://azure.microsoft.com/services/storage/) systems.</span></span>

<span data-ttu-id="5bc0a-128">保护你的隐私对我们很重要。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-128">Protecting your privacy is important to us.</span></span> <span data-ttu-id="5bc0a-129">如果你怀疑遥测在收集敏感数据，或认为处理数据的方式不安全或不恰当，请在 [dotnet/sdk](https://github.com/dotnet/sdk/issues) 存储库中记录问题或发送电子邮件至 [dotnet@microsoft.com](mailto:dotnet@microsoft.com) 以供我们展开调查。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-129">If you suspect the telemetry is collecting sensitive data or the data is being insecurely or inappropriately handled, file an issue in the [dotnet/sdk](https://github.com/dotnet/sdk/issues) repository or send an email to [dotnet@microsoft.com](mailto:dotnet@microsoft.com) for investigation.</span></span>

<span data-ttu-id="5bc0a-130">遥测功能收集以下数据：</span><span class="sxs-lookup"><span data-stu-id="5bc0a-130">The telemetry feature collects the following data:</span></span>

| <span data-ttu-id="5bc0a-131">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="5bc0a-131">SDK versions</span></span> | <span data-ttu-id="5bc0a-132">数据</span><span class="sxs-lookup"><span data-stu-id="5bc0a-132">Data</span></span> |
|--------------|------|
| <span data-ttu-id="5bc0a-133">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-133">All</span></span>          | <span data-ttu-id="5bc0a-134">调用时间戳。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-134">Timestamp of invocation.</span></span> |
| <span data-ttu-id="5bc0a-135">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-135">All</span></span>          | <span data-ttu-id="5bc0a-136">调用的命令（例如，“build”），从 2.1 开始进行哈希处理。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-136">Command invoked (for example, "build"), hashed starting in 2.1.</span></span> |
| <span data-ttu-id="5bc0a-137">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-137">All</span></span>          | <span data-ttu-id="5bc0a-138">用于确定地理位置的三个八进制数 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-138">Three octet IP address used to determine the geographical location.</span></span> |
| <span data-ttu-id="5bc0a-139">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-139">All</span></span>          | <span data-ttu-id="5bc0a-140">操作系统和版本。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-140">Operating system and version.</span></span> |
| <span data-ttu-id="5bc0a-141">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-141">All</span></span>          | <span data-ttu-id="5bc0a-142">运行 SDK 的运行时 ID (RID)。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-142">Runtime ID (RID) the SDK is running on.</span></span> |
| <span data-ttu-id="5bc0a-143">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-143">All</span></span>          | <span data-ttu-id="5bc0a-144">.NET SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-144">.NET SDK version.</span></span> |
| <span data-ttu-id="5bc0a-145">全部</span><span class="sxs-lookup"><span data-stu-id="5bc0a-145">All</span></span>          | <span data-ttu-id="5bc0a-146">遥测配置文件：一个可选值，仅在用户显式选择加入时可用，并在 Microsoft 内部使用。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-146">Telemetry profile: an optional value only used with explicit user opt-in and used internally at Microsoft.</span></span> |
| <span data-ttu-id="5bc0a-147">>=2.0</span><span class="sxs-lookup"><span data-stu-id="5bc0a-147">>=2.0</span></span>        | <span data-ttu-id="5bc0a-148">命令参数和选项：收集若干参数和选项（非任意字符串）。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-148">Command arguments and options: several arguments and options are collected (not arbitrary strings).</span></span> <span data-ttu-id="5bc0a-149">请参阅[收集的选项](#collected-options)。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-149">See [collected options](#collected-options).</span></span> <span data-ttu-id="5bc0a-150">从 2.1.300 后进行哈希处理。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-150">Hashed after 2.1.300.</span></span> |
| <span data-ttu-id="5bc0a-151">>=2.0</span><span class="sxs-lookup"><span data-stu-id="5bc0a-151">>=2.0</span></span>         | <span data-ttu-id="5bc0a-152">SDK 是否在容器中运行。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-152">Whether the SDK is running in a container.</span></span> |
| <span data-ttu-id="5bc0a-153">>=2.0</span><span class="sxs-lookup"><span data-stu-id="5bc0a-153">>=2.0</span></span>         | <span data-ttu-id="5bc0a-154">目标框架（来自 `TargetFramework` 事件），从 2.1 开始进行哈希处理。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-154">Target frameworks (from the `TargetFramework` event), hashed starting in 2.1.</span></span> |
| <span data-ttu-id="5bc0a-155">>=2.0</span><span class="sxs-lookup"><span data-stu-id="5bc0a-155">>=2.0</span></span>         | <span data-ttu-id="5bc0a-156">经过哈希处理的媒体访问控制 (MAC) 地址 (SHA256)。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-156">Hashed Media Access Control (MAC) address (SHA256).</span></span> |
| <span data-ttu-id="5bc0a-157">>=2.0</span><span class="sxs-lookup"><span data-stu-id="5bc0a-157">>=2.0</span></span>         | <span data-ttu-id="5bc0a-158">经过哈希处理的当前工作目录。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-158">Hashed current working directory.</span></span> |
| <span data-ttu-id="5bc0a-159">>=2.0</span><span class="sxs-lookup"><span data-stu-id="5bc0a-159">>=2.0</span></span>         | <span data-ttu-id="5bc0a-160">安装成功报告，包含进行了哈希处理的安装程序 exe 文件名。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-160">Install success report, with hashed installer exe filename.</span></span> |
| <span data-ttu-id="5bc0a-161">>=2.1.300</span><span class="sxs-lookup"><span data-stu-id="5bc0a-161">>=2.1.300</span></span>     | <span data-ttu-id="5bc0a-162">内核版本。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-162">Kernel version.</span></span> |
| <span data-ttu-id="5bc0a-163">>=2.1.300</span><span class="sxs-lookup"><span data-stu-id="5bc0a-163">>=2.1.300</span></span>     | <span data-ttu-id="5bc0a-164">Libc 发行/版本。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-164">Libc release/version.</span></span> |
| <span data-ttu-id="5bc0a-165">>=3.0.100</span><span class="sxs-lookup"><span data-stu-id="5bc0a-165">>=3.0.100</span></span>     | <span data-ttu-id="5bc0a-166">是否已重定向输出（true 或 false）。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-166">Whether the output was redirected (true or false).</span></span> |
| <span data-ttu-id="5bc0a-167">>=3.0.100</span><span class="sxs-lookup"><span data-stu-id="5bc0a-167">>=3.0.100</span></span>     | <span data-ttu-id="5bc0a-168">CLI/SDK 故障时的异常类型及其堆栈跟踪（发送的堆栈跟踪中仅包含 CLI/SDK 代码）。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-168">On a CLI/SDK crash, the exception type and its stack trace (only CLI/SDK code is included in the stack trace sent).</span></span> <span data-ttu-id="5bc0a-169">有关详细信息，请参阅[收集的 .NET CLI/SDK 故障异常遥测](#net-clisdk-crash-exception-telemetry-collected)。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-169">For more information, see [.NET CLI/SDK crash exception telemetry collected](#net-clisdk-crash-exception-telemetry-collected).</span></span> |

### <a name="collected-options"></a><span data-ttu-id="5bc0a-170">收集的选项</span><span class="sxs-lookup"><span data-stu-id="5bc0a-170">Collected options</span></span>

<span data-ttu-id="5bc0a-171">某些命令发送其他数据。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-171">Certain commands send additional data.</span></span> <span data-ttu-id="5bc0a-172">小部分命令发送第一个参数：</span><span class="sxs-lookup"><span data-stu-id="5bc0a-172">A subset of commands sends the first argument:</span></span>

| <span data-ttu-id="5bc0a-173">命令</span><span class="sxs-lookup"><span data-stu-id="5bc0a-173">Command</span></span>               | <span data-ttu-id="5bc0a-174">发送的第一个参数数据</span><span class="sxs-lookup"><span data-stu-id="5bc0a-174">First argument data sent</span></span>                |
|-----------------------|-----------------------------------------|
| `dotnet help <arg>`   | <span data-ttu-id="5bc0a-175">正在查询命令帮助。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-175">The command help is being queried for.</span></span>  |
| `dotnet new <arg>`    | <span data-ttu-id="5bc0a-176">模板名称（进行哈希处理）。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-176">The template name (hashed).</span></span>             |
| `dotnet add <arg>`    | <span data-ttu-id="5bc0a-177">单词 `package` 或 `reference`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-177">The word `package` or `reference`.</span></span>      |
| `dotnet remove <arg>` | <span data-ttu-id="5bc0a-178">单词 `package` 或 `reference`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-178">The word `package` or `reference`.</span></span>      |
| `dotnet list <arg>`   | <span data-ttu-id="5bc0a-179">单词 `package` 或 `reference`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-179">The word `package` or `reference`.</span></span>      |
| `dotnet sln <arg>`    | <span data-ttu-id="5bc0a-180">单词 `add`、`list` 或 `remove`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-180">The word `add`, `list`, or `remove`.</span></span>    |
| `dotnet nuget <arg>`  | <span data-ttu-id="5bc0a-181">单词 `delete`、`locals` 或 `push`。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-181">The word `delete`, `locals`, or `push`.</span></span> |

<span data-ttu-id="5bc0a-182">一小部分命令发送所选项目（如果使用）及其值：</span><span class="sxs-lookup"><span data-stu-id="5bc0a-182">A subset of commands sends selected options if they're used, along with their values:</span></span>

| <span data-ttu-id="5bc0a-183">选项</span><span class="sxs-lookup"><span data-stu-id="5bc0a-183">Option</span></span>                  | <span data-ttu-id="5bc0a-184">命令</span><span class="sxs-lookup"><span data-stu-id="5bc0a-184">Commands</span></span>                                                                                       |
|-------------------------|------------------------------------------------------------------------------------------------|
| `--verbosity`           | <span data-ttu-id="5bc0a-185">所有命令</span><span class="sxs-lookup"><span data-stu-id="5bc0a-185">All commands</span></span>                                                                                   |
| `--language`            | `dotnet new`                                                                                   |
| `--configuration`       | <span data-ttu-id="5bc0a-186">`dotnet build`, `dotnet clean`, `dotnet publish`, `dotnet run`, `dotnet test`</span><span class="sxs-lookup"><span data-stu-id="5bc0a-186">`dotnet build`, `dotnet clean`, `dotnet publish`, `dotnet run`, `dotnet test`</span></span>                  |
| `--framework`           | <span data-ttu-id="5bc0a-187">`dotnet build`, `dotnet clean`, `dotnet publish`, `dotnet run`, `dotnet test`, `dotnet vstest`</span><span class="sxs-lookup"><span data-stu-id="5bc0a-187">`dotnet build`, `dotnet clean`, `dotnet publish`, `dotnet run`, `dotnet test`, `dotnet vstest`</span></span> |
| `--runtime`             | <span data-ttu-id="5bc0a-188">`dotnet build`、`dotnet publish`</span><span class="sxs-lookup"><span data-stu-id="5bc0a-188">`dotnet build`,  `dotnet publish`</span></span>                                                              |
| `--platform`            | `dotnet vstest`                                                                                |
| `--logger`              | `dotnet vstest`                                                                                |
| `--sdk-package-version` | `dotnet migrate`                                                                               |

<span data-ttu-id="5bc0a-189">除 `--verbosity` 和 `--sdk-package-version` 外，从 .NET Core 2.1.100 SDK 开始，所有其他值都会进行哈希处理。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-189">Except for `--verbosity` and `--sdk-package-version`, all the other values are hashed starting with .NET Core 2.1.100 SDK.</span></span>

## <a name="net-clisdk-crash-exception-telemetry-collected"></a><span data-ttu-id="5bc0a-190">收集的 .NET CLI/SDK 故障异常遥测</span><span class="sxs-lookup"><span data-stu-id="5bc0a-190">.NET CLI/SDK crash exception telemetry collected</span></span>

<span data-ttu-id="5bc0a-191">如果 .NET CLI/SDK 崩溃，则会收集 CLI/SDK 代码的异常和堆栈跟踪名称。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-191">If the .NET CLI/SDK crashes, it collects the name of the exception and stack trace of the CLI/SDK code.</span></span> <span data-ttu-id="5bc0a-192">收集此信息是为了评估问题并改善 .NET SDK 和 CLI 的质量。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-192">This information is collected to assess problems and improve the quality of the .NET SDK and CLI.</span></span> <span data-ttu-id="5bc0a-193">本文提供了所收集数据的信息。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-193">This article provides information about the data we collect.</span></span> <span data-ttu-id="5bc0a-194">本文还提供了有关生成自己的 .NET SDK 版本的用户如何避免无意泄露个人或敏感信息的提示。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-194">It also provides tips on how users building their own version of the .NET SDK can avoid inadvertent disclosure of personal or sensitive information.</span></span>

### <a name="types-of-collected-data"></a><span data-ttu-id="5bc0a-195">收集的数据类型</span><span class="sxs-lookup"><span data-stu-id="5bc0a-195">Types of collected data</span></span>

<span data-ttu-id="5bc0a-196">.NET CLI 只收集有关 CLI/SDK 异常的信息，不收集应用程序中的异常信息。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-196">.NET CLI collects information for CLI/SDK exceptions only, not exceptions in your application.</span></span> <span data-ttu-id="5bc0a-197">收集的数据包含异常和堆栈跟踪的名称。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-197">The collected data contains the name of the exception and the stack trace.</span></span> <span data-ttu-id="5bc0a-198">此堆栈跟踪为 CLI/SDK 代码。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-198">This stack trace is of CLI/SDK code.</span></span>

<span data-ttu-id="5bc0a-199">下面的示例显示所收集的数据类型：</span><span class="sxs-lookup"><span data-stu-id="5bc0a-199">The following example shows the kind of data that is collected:</span></span>

```console
System.IO.IOException
at System.ConsolePal.WindowsConsoleStream.Write(Byte[] buffer, Int32 offset, Int32 count)
at System.IO.StreamWriter.Flush(Boolean flushStream, Boolean flushEncoder)
at System.IO.StreamWriter.Write(Char[] buffer)
at System.IO.TextWriter.WriteLine()
at System.IO.TextWriter.SyncTextWriter.WriteLine()
at Microsoft.DotNet.Cli.Utils.Reporter.WriteLine()
at Microsoft.DotNet.Tools.Run.RunCommand.EnsureProjectIsBuilt()
at Microsoft.DotNet.Tools.Run.RunCommand.Execute()
at Microsoft.DotNet.Tools.Run.RunCommand.Run(String[] args)
at Microsoft.DotNet.Cli.Program.ProcessArgs(String[] args, ITelemetry telemetryClient)
at Microsoft.DotNet.Cli.Program.Main(String[] args)
```

### <a name="avoid-inadvertent-disclosure-of-information"></a><span data-ttu-id="5bc0a-200">避免意外泄露信息</span><span class="sxs-lookup"><span data-stu-id="5bc0a-200">Avoid inadvertent disclosure of information</span></span>

<span data-ttu-id="5bc0a-201">.NET 参与者以及运行自己生成的 .NET SDK 版本的任何其他人都应考虑其 SDK 源代码的路径。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-201">.NET contributors and anyone else running a version of the .NET SDK that they built themselves should consider the path to their SDK source code.</span></span> <span data-ttu-id="5bc0a-202">如果在使用属于自定义调试生成或者使用自定义生成符号文件配置的 .NET SDK 时出现故障，则生成计算机的 SDK 源文件路径将作为堆栈跟踪的一部分收集，并且不会进行哈希处理。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-202">If a crash occurs while using a .NET SDK that is a custom debug build or configured with custom build symbol files, the SDK source file path from the build machine is collected as part of the stack trace and isn't hashed.</span></span>

<span data-ttu-id="5bc0a-203">因此，.NET SDK 的自定义生成不应位于路径名公开个人或敏感信息的目录中。</span><span class="sxs-lookup"><span data-stu-id="5bc0a-203">Because of this, custom builds of the .NET SDK shouldn't be located in directories whose path names expose personal or sensitive information.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc0a-204">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bc0a-204">See also</span></span>

- [<span data-ttu-id="5bc0a-205">.NET CLI 遥测数据</span><span class="sxs-lookup"><span data-stu-id="5bc0a-205">.NET CLI Telemetry Data</span></span>](https://dotnet.microsoft.com/platform/telemetry)
- [<span data-ttu-id="5bc0a-206">遥测参考源（dotnet/sdk 存储库）</span><span class="sxs-lookup"><span data-stu-id="5bc0a-206">Telemetry reference source (dotnet/sdk repository)</span></span>](https://github.com/dotnet/sdk/tree/master/src/Cli/dotnet/Telemetry)
