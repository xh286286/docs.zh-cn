---
title: 删除 .NET 运行时和 SDK
description: 本文介绍如何确定当前所安装 .NET 运行时和 SDK 的版本，以及如何在 Windows、Mac 和 Linux 上删除它们。
author: adegeo
ms.author: adegeo
ms.date: 11/20/2020
zone_pivot_groups: operating-systems-set-one
ms.openlocfilehash: f07a9acdc5be310d38da18602dde2ebf678e9a1b
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031717"
---
# <a name="how-to-remove-the-net-runtime-and-sdk"></a><span data-ttu-id="bc11c-103">如何删除 .NET 运行时和 SDK</span><span class="sxs-lookup"><span data-stu-id="bc11c-103">How to remove the .NET Runtime and SDK</span></span>

<span data-ttu-id="bc11c-104">经过一段时间后，在安装 .NET 运行时和 SDK 的更新版本时，你可能需要从计算机中删除过时的 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-104">Over time, as you install updated versions of the .NET runtime and SDK, you may want to remove outdated versions of .NET from your machine.</span></span> <span data-ttu-id="bc11c-105">如 [.NET 版本选择](../versions/selection.md)一文中详述，删除旧版运行时可能会更改为运行共享框架应用程序所选择的运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-105">Removing older versions of the runtime may change the runtime chosen to run shared framework applications, as detailed in the article on [.NET version selection](../versions/selection.md).</span></span>

## <a name="should-i-remove-a-version"></a><span data-ttu-id="bc11c-106">是否应删除某个版本？</span><span class="sxs-lookup"><span data-stu-id="bc11c-106">Should I remove a version?</span></span>

<span data-ttu-id="bc11c-107">借助 [.NET 版本选择](../versions/selection.md)行为和 .NET 各个更新之间的运行时兼容性，可安全地删除以前的版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-107">The [.NET version selection](../versions/selection.md) behaviors and the runtime compatibility of .NET across updates enables safe removal of previous versions.</span></span> <span data-ttu-id="bc11c-108">.NET 运行时更新在主版本“区段”（如 1.x 和 2.x）中兼容。</span><span class="sxs-lookup"><span data-stu-id="bc11c-108">.NET runtime updates are compatible within a major version **band** such as 1.x and 2.x.</span></span> <span data-ttu-id="bc11c-109">此外，较新版本的 .NET SDK 通常能够兼容地生成面向运行时早期版本的应用程序。</span><span class="sxs-lookup"><span data-stu-id="bc11c-109">Additionally, newer releases of the .NET SDK generally maintain the ability to build applications that target previous versions of the runtime in a compatible manner.</span></span>

<span data-ttu-id="bc11c-110">通常，只需要应用程序所需的最新 SDK 和运行时的最新补丁版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-110">In general, you only need the latest SDK and latest patch version of the runtimes required for your application.</span></span> <span data-ttu-id="bc11c-111">需要保留旧版 SDK 或运行时版本的实例包括维护基于 project.json 的应用程序  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-111">Instances where you might want to keep older SDK or runtime versions include maintaining *project.json*-based applications.</span></span> <span data-ttu-id="bc11c-112">除非应用程序有需保留早期 SDK 或运行时的特定原因，否则可以安全地删除旧版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-112">Unless your application has specific reasons for earlier SDKs or runtimes, you may safely remove older versions.</span></span>

## <a name="determine-what-is-installed"></a><span data-ttu-id="bc11c-113">确定安装内容</span><span class="sxs-lookup"><span data-stu-id="bc11c-113">Determine what is installed</span></span>

<span data-ttu-id="bc11c-114">.NET CLI 提供了相关的选项，你可以使用它们来列出计算机上安装的 SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-114">The .NET CLI has options you can use to list the versions of the SDK and runtime that are installed on your machine.</span></span>  <span data-ttu-id="bc11c-115">使用 [`dotnet --list-sdks`](../tools/dotnet.md#options) 查看计算机上安装的 SDK 列表。</span><span class="sxs-lookup"><span data-stu-id="bc11c-115">Use [`dotnet --list-sdks`](../tools/dotnet.md#options) to see the list of SDKs installed on your machine.</span></span> <span data-ttu-id="bc11c-116">使用 [`dotnet --list-runtimes`](../tools/dotnet.md#options) 查看计算机上安装的运行时列表。</span><span class="sxs-lookup"><span data-stu-id="bc11c-116">Use [`dotnet --list-runtimes`](../tools/dotnet.md#options) to see the list of runtimes installed on your machine.</span></span> <span data-ttu-id="bc11c-117">有关详细信息，请参阅[如何检查是否已安装 .NET](how-to-detect-installed-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="bc11c-117">For more information, see [How to check that .NET is already installed](how-to-detect-installed-versions.md).</span></span>

## <a name="uninstall-net"></a><span data-ttu-id="bc11c-118">卸载 .NET</span><span class="sxs-lookup"><span data-stu-id="bc11c-118">Uninstall .NET</span></span>

::: zone pivot="os-windows"

<span data-ttu-id="bc11c-119">.NET 使用 Windows“应用和功能”对话框来删除各版 .NET 运行时和 SDK。</span><span class="sxs-lookup"><span data-stu-id="bc11c-119">.NET uses the Windows **Apps & features** dialog to remove versions of the .NET runtime and SDK.</span></span> <span data-ttu-id="bc11c-120">下图显示了“应用和功能”对话框  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-120">The following figure shows the **Apps & features** dialog.</span></span> <span data-ttu-id="bc11c-121">你可以搜索 core sdk 或 .net sdk 来筛选和显示安装的 .NET 版本 。</span><span class="sxs-lookup"><span data-stu-id="bc11c-121">You can search for **core sdk** or **.net sdk** to filter and show installed versions of .NET.</span></span>

![使用“添加/删除程序”来删除 .NET](./media/remove-runtime-sdk-versions/programs-and-features.png)

<span data-ttu-id="bc11c-123">选择要从计算机中删除的任何版本，然后单击“卸载”  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-123">Select any versions you want to remove from your machine and click **Uninstall**.</span></span>

::: zone-end

::: zone pivot="os-linux"

<span data-ttu-id="bc11c-124">Linux 还提供其他选项来卸载 .NET（SDK 或运行时）。</span><span class="sxs-lookup"><span data-stu-id="bc11c-124">There are more options to uninstall .NET (either SDK or runtime) on Linux.</span></span> <span data-ttu-id="bc11c-125">卸载 .NET 的最佳方法是镜像用来安装 .NET 的操作。</span><span class="sxs-lookup"><span data-stu-id="bc11c-125">The best way for you to uninstall .NET is to mirror the action you used to install .NET.</span></span> <span data-ttu-id="bc11c-126">具体取决于所选择的分发和安装方法。</span><span class="sxs-lookup"><span data-stu-id="bc11c-126">The specifics depend on your chosen distribution and the installation method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc11c-127">有关 Red Hat 安装，请参阅 [Red Hat Product Documentation for .NET](https://access.redhat.com/documentation/en-us/net/5.0/)（Red Hat .NET 产品文档）。</span><span class="sxs-lookup"><span data-stu-id="bc11c-127">For Red Hat installations, consult the [Red Hat Product Documentation for .NET](https://access.redhat.com/documentation/en-us/net/5.0/).</span></span>

<span data-ttu-id="bc11c-128">除非从预览版本进行升级，否则使用包管理器升级时无需卸载 .NET SDK。</span><span class="sxs-lookup"><span data-stu-id="bc11c-128">There's no need to uninstall the .NET SDK when upgrading it using a package manager, unless you're upgrading from a preview version.</span></span> <span data-ttu-id="bc11c-129">包管理器 `update` 或 `refresh` 命令将在成功安装较新版本后自动删除旧版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-129">The package manager `update` or `refresh` commands will automatically remove the older version upon the successful installation of a newer version.</span></span> <span data-ttu-id="bc11c-130">如果已安装预览版本，请卸载该版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-130">If you have a preview version installed, uninstall it.</span></span>

<span data-ttu-id="bc11c-131">如果使用包管理器安装 .NET，则使用同一包管理器来卸载 .NET SDK 或运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-131">If you installed .NET using a package manager, use that same package manager to uninstall the .NET SDK or runtime.</span></span> <span data-ttu-id="bc11c-132">.NET 安装支持常用的包管理器。</span><span class="sxs-lookup"><span data-stu-id="bc11c-132">.NET installations support most popular package managers.</span></span> <span data-ttu-id="bc11c-133">有关环境中的精确语法，请查阅分发的包管理器文档：</span><span class="sxs-lookup"><span data-stu-id="bc11c-133">Consult the documentation for your distribution's package manager for the precise syntax in your environment:</span></span>

- <span data-ttu-id="bc11c-134">[apt-get(8)](https://linux.die.net/man/8/apt-get) 由基于 Debian 的系统（包括 Ubuntu）使用。</span><span class="sxs-lookup"><span data-stu-id="bc11c-134">[apt-get(8)](https://linux.die.net/man/8/apt-get) is used by Debian based systems, including Ubuntu.</span></span>
- <span data-ttu-id="bc11c-135">[yum(8)](https://linux.die.net/man/8/yum) 用于 Fedora、CentOS 和 Oracle Linux。</span><span class="sxs-lookup"><span data-stu-id="bc11c-135">[yum(8)](https://linux.die.net/man/8/yum) is used on Fedora, CentOS, and Oracle Linux.</span></span>
- <span data-ttu-id="bc11c-136">[zypper(8)](https://en.opensuse.org/SDB:Zypper_manual_(plain)) 用于 openSUSE 和 SUSE Linux Enterprise System (SLES)。</span><span class="sxs-lookup"><span data-stu-id="bc11c-136">[zypper(8)](https://en.opensuse.org/SDB:Zypper_manual_(plain)) is used on openSUSE and SUSE Linux Enterprise System (SLES).</span></span>
- <span data-ttu-id="bc11c-137">[dnf(8)](https://dnf.readthedocs.io/en/latest/command_ref.html) 用于 Fedora。</span><span class="sxs-lookup"><span data-stu-id="bc11c-137">[dnf(8)](https://dnf.readthedocs.io/en/latest/command_ref.html) is used on Fedora.</span></span>

<span data-ttu-id="bc11c-138">几乎在所有情况下，删除包的命令都是 `remove`。</span><span class="sxs-lookup"><span data-stu-id="bc11c-138">In almost all cases, the command to remove a package is `remove`.</span></span>

<span data-ttu-id="bc11c-139">大多数包管理器的 .NET SDK 安装包名称为 `dotnet-sdk`，后跟版本号。</span><span class="sxs-lookup"><span data-stu-id="bc11c-139">The package name for the .NET SDK installation for most package managers is `dotnet-sdk`, followed by the version number.</span></span> <span data-ttu-id="bc11c-140">从 2.1.300 版 .NET SDK 和 `2.1` 版运行时开始，只需要主版本号和次版本号：例如，可将 .NET SDK 2.1.300 版引用为包 `dotnet-sdk-2.1`。</span><span class="sxs-lookup"><span data-stu-id="bc11c-140">Starting with the version 2.1.300 of the .NET SDK and version `2.1` of the runtime, only the major and minor version numbers are necessary: for example, the .NET SDK version 2.1.300 can be referenced as the package `dotnet-sdk-2.1`.</span></span> <span data-ttu-id="bc11c-141">以前的版本则需要整个版本字符串：例如，2.1.200 版 .NET SDK 需要 `dotnet-sdk-2.1.200`。</span><span class="sxs-lookup"><span data-stu-id="bc11c-141">Prior versions require the entire version string: for example, `dotnet-sdk-2.1.200` would be required for version 2.1.200 of the .NET SDK.</span></span>

<span data-ttu-id="bc11c-142">对于仅安装了运行时而未安装 SDK 的计算机，.NET 运行时的包名称为 `dotnet-runtime-<version>`，整个运行时堆栈的包名称为 `aspnetcore-runtime-<version>`。</span><span class="sxs-lookup"><span data-stu-id="bc11c-142">For machines that have installed only the runtime, and not the SDK, the package name is `dotnet-runtime-<version>` for the .NET runtime, and `aspnetcore-runtime-<version>` for the entire runtime stack.</span></span>

> [!TIP]
> <span data-ttu-id="bc11c-143">使用包管理器卸载 SDK 时，2.0 之前的 .NET Core 安装不会卸载主机应用程序。</span><span class="sxs-lookup"><span data-stu-id="bc11c-143">.NET Core installations earlier than 2.0 didn't uninstall the host application when the SDK was uninstalled using the package manager.</span></span> <span data-ttu-id="bc11c-144">使用 `apt-get`，该命令为：</span><span class="sxs-lookup"><span data-stu-id="bc11c-144">Using `apt-get`, the command is:</span></span>
>
> ```bash
> apt-get remove dotnet-host
> ```
>
> <span data-ttu-id="bc11c-145">没有版本附加到 `dotnet-host`。</span><span class="sxs-lookup"><span data-stu-id="bc11c-145">There's no version attached to `dotnet-host`.</span></span>

<span data-ttu-id="bc11c-146">如果使用 tarball 安装，则必须手动删除 .NET。</span><span class="sxs-lookup"><span data-stu-id="bc11c-146">If you installed using a tarball, you must remove .NET using the manual method.</span></span>

<span data-ttu-id="bc11c-147">在 Linux 上，必须通过删除进行版本控制的目录，分别删除 SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-147">On Linux, you must remove the SDKs and runtimes separately, by removing the versioned directories.</span></span> <span data-ttu-id="bc11c-148">删除它们会从磁盘中删除 SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-148">Removing them deletes the SDK and runtime from disk.</span></span> <span data-ttu-id="bc11c-149">例如，要删除 1.0.1 SDK 和运行时，可使用以下 bash 命令：</span><span class="sxs-lookup"><span data-stu-id="bc11c-149">For example, to remove the 1.0.1 SDK and runtime, you would use the following bash commands:</span></span>

```bash
version="1.0.1"
sudo rm -rf /usr/local/share/dotnet/sdk/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.NETCore.App/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.All/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.App/$version
sudo rm -rf /usr/local/share/dotnet/host/fxr/$version
```

<span data-ttu-id="bc11c-150">SDK 和运行时的父目录列在 `dotnet --list-sdks` 和 `dotnet --list-runtimes` 命令的输出中，如上表所示。</span><span class="sxs-lookup"><span data-stu-id="bc11c-150">The parent directories for the SDK and runtime are listed in the output from the `dotnet --list-sdks` and `dotnet --list-runtimes` command, as shown in the earlier table.</span></span>

::: zone-end

::: zone pivot="os-macos"

<span data-ttu-id="bc11c-151">在 Mac 上，必须通过删除进行版本控制的目录，分别删除 SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-151">On Mac, you must remove the SDKs and runtimes separately, by removing the versioned directories.</span></span> <span data-ttu-id="bc11c-152">删除它们会从磁盘中删除 SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-152">Removing them deletes the SDK and runtime from disk.</span></span> <span data-ttu-id="bc11c-153">例如，要删除 1.0.1 SDK 和运行时，可使用以下 bash 命令：</span><span class="sxs-lookup"><span data-stu-id="bc11c-153">For example, to remove the 1.0.1 SDK and runtime, you would use the following bash commands:</span></span>

```bash
version="1.0.1"
sudo rm -rf /usr/local/share/dotnet/sdk/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.NETCore.App/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.All/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.App/$version
sudo rm -rf /usr/local/share/dotnet/host/fxr/$version
```

<span data-ttu-id="bc11c-154">SDK 和运行时的父目录列在 `dotnet --list-sdks` 和 `dotnet --list-runtimes` 命令的输出中，如上表所示。</span><span class="sxs-lookup"><span data-stu-id="bc11c-154">The parent directories for the SDK and runtime are listed in the output from the `dotnet --list-sdks` and `dotnet --list-runtimes` command, as shown in the earlier table.</span></span>

::: zone-end

## <a name="net-uninstall-tool"></a><span data-ttu-id="bc11c-155">.NET 卸载工具</span><span class="sxs-lookup"><span data-stu-id="bc11c-155">.NET Uninstall Tool</span></span>

<span data-ttu-id="bc11c-156">你可以使用 [.NET 卸载工具](../additional-tools/uninstall-tool.md) (`dotnet-core-uninstall`) 从系统中删除 .NET SDK 和运行时。</span><span class="sxs-lookup"><span data-stu-id="bc11c-156">The [.NET Uninstall Tool](../additional-tools/uninstall-tool.md) (`dotnet-core-uninstall`) lets you remove .NET SDKs and runtimes from a system.</span></span> <span data-ttu-id="bc11c-157">可使用选项集合来指定应卸载的版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-157">A collection of options is available to specify which versions should be uninstalled.</span></span>

## <a name="visual-studio-dependency-on-net-core-sdk-versions"></a><span data-ttu-id="bc11c-158">.NET Core SDK 版本的 Visual Studio 依赖项</span><span class="sxs-lookup"><span data-stu-id="bc11c-158">Visual Studio dependency on .NET Core SDK versions</span></span>

<span data-ttu-id="bc11c-159">在 Visual Studio 2019 版本 16.3 之前，Visual Studio 安装程序称为独立的 .NET Core SDK 安装程序。</span><span class="sxs-lookup"><span data-stu-id="bc11c-159">Before Visual Studio 2019 version 16.3, Visual Studio installers called the standalone .NET Core SDK installer.</span></span> <span data-ttu-id="bc11c-160">因此，SDK 版本显示在 Windows“应用和功能”对话框中  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-160">As a result, the SDK versions appear in the Windows **Apps & features** dialog.</span></span> <span data-ttu-id="bc11c-161">使用独立安装程序删除 Visual Studio 安装的 .NET Core SDK 可能会破坏 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="bc11c-161">Removing .NET Core SDKs that were installed by Visual Studio using the standalone installer may break Visual Studio.</span></span> <span data-ttu-id="bc11c-162">如果 Visual Studio 在卸载 SDK 之后出现问题，请在该特定版本的 Visual Studio 上运行修复。</span><span class="sxs-lookup"><span data-stu-id="bc11c-162">If Visual Studio has problems after you uninstall SDKs, run Repair on that specific version of Visual Studio.</span></span> <span data-ttu-id="bc11c-163">下表显示了 .NET Core SDK 版本的一些 Visual Studio 依赖项：</span><span class="sxs-lookup"><span data-stu-id="bc11c-163">The following table shows some of the Visual Studio dependencies on .NET Core SDK versions:</span></span>

| <span data-ttu-id="bc11c-164">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="bc11c-164">Visual Studio version</span></span>           | <span data-ttu-id="bc11c-165">.NET Core SDK 版本</span><span class="sxs-lookup"><span data-stu-id="bc11c-165">.NET Core SDK version</span></span>          |
|---------------------------------|--------------------------------|
| <span data-ttu-id="bc11c-166">Visual Studio 2019 版本 16.2</span><span class="sxs-lookup"><span data-stu-id="bc11c-166">Visual Studio 2019 version 16.2</span></span> | <span data-ttu-id="bc11c-167">.NET Core SDK 2.2.4xx、2.1.8xx</span><span class="sxs-lookup"><span data-stu-id="bc11c-167">.NET Core SDK 2.2.4xx, 2.1.8xx</span></span> |
| <span data-ttu-id="bc11c-168">Visual Studio 2019 版本 16.1</span><span class="sxs-lookup"><span data-stu-id="bc11c-168">Visual Studio 2019 version 16.1</span></span> | <span data-ttu-id="bc11c-169">.NET Core SDK 2.2.3xx、2.1.7xx</span><span class="sxs-lookup"><span data-stu-id="bc11c-169">.NET Core SDK 2.2.3xx, 2.1.7xx</span></span> |
| <span data-ttu-id="bc11c-170">Visual Studio 2019 版本 16.0</span><span class="sxs-lookup"><span data-stu-id="bc11c-170">Visual Studio 2019 version 16.0</span></span> | <span data-ttu-id="bc11c-171">.NET Core SDK 2.2.2xx、2.1.6xx</span><span class="sxs-lookup"><span data-stu-id="bc11c-171">.NET Core SDK 2.2.2xx, 2.1.6xx</span></span> |
| <span data-ttu-id="bc11c-172">Visual Studio 2017 版本 15.9</span><span class="sxs-lookup"><span data-stu-id="bc11c-172">Visual Studio 2017 version 15.9</span></span> | <span data-ttu-id="bc11c-173">.NET Core SDK 2.2.1xx、2.1.5xx</span><span class="sxs-lookup"><span data-stu-id="bc11c-173">.NET Core SDK 2.2.1xx, 2.1.5xx</span></span> |
| <span data-ttu-id="bc11c-174">Visual Studio 2017 版本 15.8</span><span class="sxs-lookup"><span data-stu-id="bc11c-174">Visual Studio 2017 version 15.8</span></span> | <span data-ttu-id="bc11c-175">.NET Core SDK 2.1.4xx</span><span class="sxs-lookup"><span data-stu-id="bc11c-175">.NET Core SDK 2.1.4xx</span></span>          |

<span data-ttu-id="bc11c-176">从 Visual Studio 2019 16.3 版开始，Visual Studio 负责其自己的 .NET SDK 副本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-176">Starting with Visual Studio 2019 version 16.3, Visual Studio is in charge of its own copy of the .NET SDK.</span></span> <span data-ttu-id="bc11c-177">因此，“应用和功能”对话框中将不再显示这些 SDK 版本  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-177">For that reason, you no longer see those SDK versions in the **Apps & features** dialog.</span></span>

## <a name="remove-the-nuget-fallback-folder"></a><span data-ttu-id="bc11c-178">删除 NuGet 回退文件夹</span><span class="sxs-lookup"><span data-stu-id="bc11c-178">Remove the NuGet fallback folder</span></span>

<span data-ttu-id="bc11c-179">在 .NET Core 3.0 SDK 之前，.NET Core SDK 安装程序使用名为 NuGetFallbackFolder 的文件夹存储 NuGet 包的缓存  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-179">Before .NET Core 3.0 SDK, the .NET Core SDK installers used a folder named *NuGetFallbackFolder* to store a cache of NuGet packages.</span></span> <span data-ttu-id="bc11c-180">此缓存在操作期间（如 `dotnet restore` 或 `dotnet build /t:Restore`）使用。</span><span class="sxs-lookup"><span data-stu-id="bc11c-180">This cache was used during operations such as `dotnet restore` or `dotnet build /t:Restore`.</span></span> <span data-ttu-id="bc11c-181">NuGetFallbackFolder 在 Windows 上位于 C:\Program Files\dotnet\sdk，在 macOS 上位于 /usr/local/share/dotnet/sdk    。</span><span class="sxs-lookup"><span data-stu-id="bc11c-181">The *NuGetFallbackFolder* is located at *C:\Program Files\dotnet\sdk* on Windows and at */usr/local/share/dotnet/sdk* on macOS.</span></span>

<span data-ttu-id="bc11c-182">如果是以下情况，则可能需要删除此文件夹：</span><span class="sxs-lookup"><span data-stu-id="bc11c-182">You may want to remove this folder, if:</span></span>

- <span data-ttu-id="bc11c-183">仅使用 .NET Core 3.0 SDK 或 .NET 5.0（或更高版本）进行开发。</span><span class="sxs-lookup"><span data-stu-id="bc11c-183">You're only developing using .NET Core 3.0 SDK or .NET 5.0 or later versions.</span></span>
- <span data-ttu-id="bc11c-184">你使用早于 3.0 的 .NET Core SDK 版本进行开发，但可以联机工作。</span><span class="sxs-lookup"><span data-stu-id="bc11c-184">You're developing using .NET Core SDK versions earlier than 3.0, but you can work online.</span></span>

<span data-ttu-id="bc11c-185">如果要删除 NuGet 回退文件夹，可以将其删除，但需要管理员权限才能执行此操作。</span><span class="sxs-lookup"><span data-stu-id="bc11c-185">If you want to remove the NuGet fallback folder, you can delete it, but you'll need admin privileges to do so.</span></span>

<span data-ttu-id="bc11c-186">建议不要删除 dotnet  文件夹。</span><span class="sxs-lookup"><span data-stu-id="bc11c-186">It's not recommended to delete the *dotnet* folder.</span></span> <span data-ttu-id="bc11c-187">这样做会删除以前安装的所有全局工具。</span><span class="sxs-lookup"><span data-stu-id="bc11c-187">Doing so would remove any global tools you've previously installed.</span></span> <span data-ttu-id="bc11c-188">此外，在 Windows 上：</span><span class="sxs-lookup"><span data-stu-id="bc11c-188">Also, on Windows:</span></span>

- <span data-ttu-id="bc11c-189">你将中断 Visual Studio 2019 版本 16.3 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="bc11c-189">You'll break Visual Studio 2019 version 16.3 and later versions.</span></span> <span data-ttu-id="bc11c-190">可以运行“修复”  来恢复。</span><span class="sxs-lookup"><span data-stu-id="bc11c-190">You can run **Repair** to recover.</span></span>
- <span data-ttu-id="bc11c-191">如果“应用和功能”对话框中存在 .NET Core SDK 条目，它们将是孤立的  。</span><span class="sxs-lookup"><span data-stu-id="bc11c-191">If there are .NET Core SDK entries in the **Apps & features** dialog, they'll be orphaned.</span></span>
