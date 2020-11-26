---
title: dotnet-sos 诊断工具 - .NET CLI
description: 了解如何安装和使用 dotnet-sos CLI 工具来管理 SOS 调试器扩展，该扩展可与 Windows 和 Linux 上的本机调试器一起使用。
ms.date: 11/17/2020
ms.openlocfilehash: 59512c42a778f68bb3cd092dc854dcc727fd2881
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94825437"
---
# <a name="sos-installer-dotnet-sos"></a><span data-ttu-id="1c692-103">SOS 安装程序 (dotnet-sos)</span><span class="sxs-lookup"><span data-stu-id="1c692-103">SOS installer (dotnet-sos)</span></span>

<span data-ttu-id="1c692-104">本文适用于： ✔️ .NET Core 2.1 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="1c692-104">**This article applies to:** ✔️ .NET Core 2.1 SDK and later versions</span></span>

## <a name="install"></a><span data-ttu-id="1c692-105">安装</span><span class="sxs-lookup"><span data-stu-id="1c692-105">Install</span></span>

<span data-ttu-id="1c692-106">可采用两种方法来下载和安装 `dotnet-sos`：</span><span class="sxs-lookup"><span data-stu-id="1c692-106">There are two ways to download and install `dotnet-sos`:</span></span>

- <span data-ttu-id="1c692-107">**dotnet 全局工具：**</span><span class="sxs-lookup"><span data-stu-id="1c692-107">**dotnet global tool:**</span></span>

  <span data-ttu-id="1c692-108">若要安装最新版 `dotnet-sos` [NuGet 包](https://www.nuget.org/packages/dotnet-sos)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：</span><span class="sxs-lookup"><span data-stu-id="1c692-108">To install the latest release version of the `dotnet-sos` [NuGet package](https://www.nuget.org/packages/dotnet-sos), use the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

  ```dotnetcli
  dotnet tool install --global dotnet-sos
  ```

- <span data-ttu-id="1c692-109">**直接下载：**</span><span class="sxs-lookup"><span data-stu-id="1c692-109">**Direct download:**</span></span>

  <span data-ttu-id="1c692-110">下载与平台相匹配的工具可执行文件：</span><span class="sxs-lookup"><span data-stu-id="1c692-110">Download the tool executable that matches your platform:</span></span>

  | <span data-ttu-id="1c692-111">(OS)</span><span class="sxs-lookup"><span data-stu-id="1c692-111">OS</span></span>  | <span data-ttu-id="1c692-112">平台</span><span class="sxs-lookup"><span data-stu-id="1c692-112">Platform</span></span> |
  | --- | -------- |
  | <span data-ttu-id="1c692-113">Windows</span><span class="sxs-lookup"><span data-stu-id="1c692-113">Windows</span></span> | <span data-ttu-id="1c692-114">[x86](https://aka.ms/dotnet-sos/win-x86) \| [x64](https://aka.ms/dotnet-sos/win-x64) \| [arm](https://aka.ms/dotnet-sos/win-arm) \| [arm-x64](https://aka.ms/dotnet-sos/win-arm64)</span><span class="sxs-lookup"><span data-stu-id="1c692-114">[x86](https://aka.ms/dotnet-sos/win-x86) \| [x64](https://aka.ms/dotnet-sos/win-x64) \| [arm](https://aka.ms/dotnet-sos/win-arm) \| [arm-x64](https://aka.ms/dotnet-sos/win-arm64)</span></span> |
  | <span data-ttu-id="1c692-115">macOS</span><span class="sxs-lookup"><span data-stu-id="1c692-115">macOS</span></span>   | [<span data-ttu-id="1c692-116">x64</span><span class="sxs-lookup"><span data-stu-id="1c692-116">x64</span></span>](https://aka.ms/dotnet-sos/osx-x64) |
  | <span data-ttu-id="1c692-117">Linux</span><span class="sxs-lookup"><span data-stu-id="1c692-117">Linux</span></span>   | <span data-ttu-id="1c692-118">[x64](https://aka.ms/dotnet-sos/linux-x64) \| [arm](https://aka.ms/dotnet-sos/linux-arm) \| [arm64](https://aka.ms/dotnet-sos/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-sos/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-sos/linux-musl-arm64)</span><span class="sxs-lookup"><span data-stu-id="1c692-118">[x64](https://aka.ms/dotnet-sos/linux-x64) \| [arm](https://aka.ms/dotnet-sos/linux-arm) \| [arm64](https://aka.ms/dotnet-sos/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-sos/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-sos/linux-musl-arm64)</span></span> |

## <a name="synopsis"></a><span data-ttu-id="1c692-119">摘要</span><span class="sxs-lookup"><span data-stu-id="1c692-119">Synopsis</span></span>

```console
dotnet-sos [-h|--help] [options] [command]]
```

## <a name="description"></a><span data-ttu-id="1c692-120">描述</span><span class="sxs-lookup"><span data-stu-id="1c692-120">Description</span></span>

<span data-ttu-id="1c692-121">`dotnet-sos` 全局工具可安装 [SOS 调试器扩展](../../framework/tools/sos-dll-sos-debugging-extension.md)，从而允许从本机调试器（例如 Windows 上的 WinDbg/cdb 以及 Linux 和 macOS 上的 lldb）[检查托管的 .NET Core 状态](https://github.com/dotnet/diagnostics/blob/master/documentation/sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="1c692-121">The `dotnet-sos` global tool installs the [SOS debugger extension](../../framework/tools/sos-dll-sos-debugging-extension.md) allowing [inspection of managed .NET Core state](https://github.com/dotnet/diagnostics/blob/master/documentation/sos-debugging-extension.md) from native debuggers like WinDbg/cdb on Windows and lldb on Linux and macOS.</span></span> <span data-ttu-id="1c692-122">最新版本（WinDbg 或 cdb 的 10.0.18317.1001 版本及更高版本）的 Windows 调试器将自动从 Microsoft 扩展库加载 SOS，因此，只有在 Linux 和 macOS 或在使用较旧的调试工具的 Windows 上，才需要通过 `dotnet-sos` 工具安装 SOS。</span><span class="sxs-lookup"><span data-stu-id="1c692-122">Recent versions of the Windows Debugger (>= version 10.0.18317.1001 of WinDbg or cdb) will load SOS automatically from the Microsoft extension gallery, so installing SOS via the `dotnet-sos` tool is only needed on Linux and macOS or on Windows if using older debugging tools.</span></span>

## <a name="options"></a><span data-ttu-id="1c692-123">选项</span><span class="sxs-lookup"><span data-stu-id="1c692-123">Options</span></span>

- **`--version`**

  <span data-ttu-id="1c692-124">显示版本信息。</span><span class="sxs-lookup"><span data-stu-id="1c692-124">Displays version information.</span></span>

- **`-h|--help`**

  <span data-ttu-id="1c692-125">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="1c692-125">Shows command-line help.</span></span>

## <a name="dotnet-sos-install"></a><span data-ttu-id="1c692-126">安装 dotnet-sos</span><span class="sxs-lookup"><span data-stu-id="1c692-126">dotnet-sos install</span></span>

<span data-ttu-id="1c692-127">在本地安装用于调试 .NET Core 进程的 [SOS 扩展](../../framework/tools/sos-dll-sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="1c692-127">Installs the [SOS extension](../../framework/tools/sos-dll-sos-debugging-extension.md) locally for debugging .NET Core processes.</span></span> <span data-ttu-id="1c692-128">在 macOS 和 Linux 上，将更新 .lldbinit 文件，以便扩展在 lldb 启动时自动加载。</span><span class="sxs-lookup"><span data-stu-id="1c692-128">On macOS and Linux, the .lldbinit file will be updated so that the extension automatically loads at lldb startup.</span></span> <span data-ttu-id="1c692-129">如果在使用较旧的调试工具（低于版本 10.0.18317.1001）的 Windows 上安装 SOS，则需要通过在调试器中运行 `.load %USERPROFILE%\.dotnet\sos\sos.dll` 以在 WinDbg 或 cdb 中手动加载扩展。</span><span class="sxs-lookup"><span data-stu-id="1c692-129">If installing SOS on Windows with older debugging tools (< version 10.0.18317.1001), you will need to manually load the extension in WinDbg or cdb by running `.load %USERPROFILE%\.dotnet\sos\sos.dll` in the debugger.</span></span>

### <a name="synopsis"></a><span data-ttu-id="1c692-130">摘要</span><span class="sxs-lookup"><span data-stu-id="1c692-130">Synopsis</span></span>

```console
dotnet-sos install
```

## <a name="dotnet-sos-uninstall"></a><span data-ttu-id="1c692-131">卸载 dotnet-sos</span><span class="sxs-lookup"><span data-stu-id="1c692-131">dotnet-sos uninstall</span></span>

<span data-ttu-id="1c692-132">卸载 [SOS 扩展](../../framework/tools/sos-dll-sos-debugging-extension.md)，如果该扩展位于 Linux 或 macOS 上，则将其从 lldb 配置中删除。</span><span class="sxs-lookup"><span data-stu-id="1c692-132">Uninstalls the [SOS extension](../../framework/tools/sos-dll-sos-debugging-extension.md) and, if on Linux or macOS, removes it from lldb configuration.</span></span>

### <a name="synopsis"></a><span data-ttu-id="1c692-133">摘要</span><span class="sxs-lookup"><span data-stu-id="1c692-133">Synopsis</span></span>

```console
dotnet-sos uninstall
```
