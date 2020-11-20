---
ms.openlocfilehash: 3932cf51b5194dba7956cd62ced3985a2e6311f0
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506791"
---

<!-- Note, this content is copied in ../macos.md. Any fixes should be applied there too, though content may be different -->

<span data-ttu-id="4dee2-101">除了使用包管理器，还可以下载并手动安装 SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="4dee2-101">As an alternative to the package managers, you can download and manually install the SDK and runtime.</span></span> <span data-ttu-id="4dee2-102">手动安装通常作为持续集成测试的一部分执行，或在不支持的 Linux 分发版上执行。</span><span class="sxs-lookup"><span data-stu-id="4dee2-102">Manual install is usually performed as part of continuous integration testing or on an unsupported Linux distribution.</span></span> <span data-ttu-id="4dee2-103">对于开发人员或用户，一般使用包管理器会更好。</span><span class="sxs-lookup"><span data-stu-id="4dee2-103">For a developer or user, it's generally better to use a package manager.</span></span>

<span data-ttu-id="4dee2-104">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="4dee2-104">If you install .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="4dee2-105">首先，从以下站点之一下载 SDK 或运行时的二进制版本：</span><span class="sxs-lookup"><span data-stu-id="4dee2-105">First, download a **binary** release for either the SDK or the runtime from one of the following sites:</span></span>

- <span data-ttu-id="4dee2-106">✔️ [.NET 5.0 下载](https://dotnet.microsoft.com/download/dotnet/5.0)</span><span class="sxs-lookup"><span data-stu-id="4dee2-106">✔️ [.NET 5.0 downloads](https://dotnet.microsoft.com/download/dotnet/5.0)</span></span>
- <span data-ttu-id="4dee2-107">✔️ [.NET Core 3.1 下载](https://dotnet.microsoft.com/download/dotnet-core/3.1)</span><span class="sxs-lookup"><span data-stu-id="4dee2-107">✔️ [.NET Core 3.1 downloads](https://dotnet.microsoft.com/download/dotnet-core/3.1)</span></span>
- <span data-ttu-id="4dee2-108">✔️ [.NET Core 2.1 下载](https://dotnet.microsoft.com/download/dotnet-core/2.1)</span><span class="sxs-lookup"><span data-stu-id="4dee2-108">✔️ [.NET Core 2.1 downloads](https://dotnet.microsoft.com/download/dotnet-core/2.1)</span></span>
- [<span data-ttu-id="4dee2-109">所有 .NET Core 下载项</span><span class="sxs-lookup"><span data-stu-id="4dee2-109">All .NET Core downloads</span></span>](https://dotnet.microsoft.com/download/dotnet-core)

<span data-ttu-id="4dee2-110">接下来，提取已下载的文件并使用 `export` 命令设置 .NET 使用的变量，然后确保 .NET 在 PATH 中。</span><span class="sxs-lookup"><span data-stu-id="4dee2-110">Next, extract the downloaded file and use the `export` command to set variables used by .NET and then ensure .NET is in PATH.</span></span>

<span data-ttu-id="4dee2-111">若要提取运行时并使 .NET CLI 命令可用于终端，请先下载 .NET 二进制版本。</span><span class="sxs-lookup"><span data-stu-id="4dee2-111">To extract the runtime and make the .NET CLI commands available at the terminal, first download a .NET binary release.</span></span> <span data-ttu-id="4dee2-112">然后，打开终端并从保存文件的目录运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="4dee2-112">Then, open a terminal and run the following commands from the directory where the file was saved.</span></span> <span data-ttu-id="4dee2-113">根据下载内容，存档文件名称可能不同。</span><span class="sxs-lookup"><span data-stu-id="4dee2-113">The archive file name may be different depending on what you downloaded.</span></span>

<span data-ttu-id="4dee2-114">**使用以下命令来提取运行时**：</span><span class="sxs-lookup"><span data-stu-id="4dee2-114">**Use the following command to extract the runtime**:</span></span>

```bash
mkdir -p "$HOME/dotnet" && tar zxf aspnetcore-runtime-5.0.0-linux-x64.tar.gz -C "$HOME/dotnet"
export DOTNET_ROOT=$HOME/dotnet
export PATH=$PATH:$HOME/dotnet
```

<span data-ttu-id="4dee2-115">**使用以下命令来提取 SDK**：</span><span class="sxs-lookup"><span data-stu-id="4dee2-115">**Use the following command to extract the SDK**:</span></span>

```bash
mkdir -p "$HOME/dotnet" && tar zxf dotnet-sdk-5.0.100-linux-x64.tar.gz -C "$HOME/dotnet"
export DOTNET_ROOT=$HOME/dotnet
export PATH=$PATH:$HOME/dotnet
```

> [!TIP]
> <span data-ttu-id="4dee2-116">前面的 `export` 命令只会使 .NET CLI 命令对运行它的终端会话可用。</span><span class="sxs-lookup"><span data-stu-id="4dee2-116">The preceding `export` commands only make the .NET CLI commands available for the terminal session in which it was run.</span></span>
>
> <span data-ttu-id="4dee2-117">你可以编辑 shell 配置文件，永久地添加这些命令。</span><span class="sxs-lookup"><span data-stu-id="4dee2-117">You can edit your shell profile to permanently add the commands.</span></span> <span data-ttu-id="4dee2-118">Linux 提供了许多不同的 shell，每个都有不同的配置文件。</span><span class="sxs-lookup"><span data-stu-id="4dee2-118">There are a number of different shells available for Linux and each has a different profile.</span></span> <span data-ttu-id="4dee2-119">例如：</span><span class="sxs-lookup"><span data-stu-id="4dee2-119">For example:</span></span>
>
> - <span data-ttu-id="4dee2-120">**Bash Shell**：~/.bash_profile、~/.bashrc</span><span class="sxs-lookup"><span data-stu-id="4dee2-120">**Bash Shell**: *~/.bash_profile*, *~/.bashrc*</span></span>
> - <span data-ttu-id="4dee2-121">**Korn Shell**：~/.kshrc 或 .profile</span><span class="sxs-lookup"><span data-stu-id="4dee2-121">**Korn Shell**: *~/.kshrc* or *.profile*</span></span>
> - <span data-ttu-id="4dee2-122">**Z Shell**：~/.zshrc 或 .zprofile</span><span class="sxs-lookup"><span data-stu-id="4dee2-122">**Z Shell**: *~/.zshrc* or *.zprofile*</span></span>
>
> <span data-ttu-id="4dee2-123">为 shell 编辑相应的源文件，并将 `:$HOME/dotnet` 添加到现有 `PATH` 语句的末尾。</span><span class="sxs-lookup"><span data-stu-id="4dee2-123">Edit the appropriate source file for your shell and add `:$HOME/dotnet` to the end of the existing `PATH` statement.</span></span> <span data-ttu-id="4dee2-124">如果不包含 `PATH` 语句，则使用 `export PATH=$PATH:$HOME/dotnet` 添加新行。</span><span class="sxs-lookup"><span data-stu-id="4dee2-124">If no `PATH` statement is included, add a new line with `export PATH=$PATH:$HOME/dotnet`.</span></span>
>
> <span data-ttu-id="4dee2-125">另外，将 `export DOTNET_ROOT=$HOME/dotnet` 添加至文件的末尾。</span><span class="sxs-lookup"><span data-stu-id="4dee2-125">Also, add `export DOTNET_ROOT=$HOME/dotnet` to the end of the file.</span></span>

<span data-ttu-id="4dee2-126">使用此方法可以将不同的版本安装到不同的位置，并明确选择应用程序要使用的对应版本。</span><span class="sxs-lookup"><span data-stu-id="4dee2-126">This approach lets you install different versions into separate locations and choose explicitly which one to use by which application.</span></span>
