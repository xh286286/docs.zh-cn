---
ms.openlocfilehash: 83808f2f3a05333ed5d9e3809cbc2fd6e230d02c
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031748"
---

[<span data-ttu-id="28694-101">.NET Core 可以从 Snap Store 中获取。</span><span class="sxs-lookup"><span data-stu-id="28694-101">.NET Core is available from the Snap Store.</span></span>](https://snapcraft.io/dotnet-sdk)

<span data-ttu-id="28694-102">Snap 是应用及其依赖项的捆绑包，无需修改即可在多个不同的 Linux 发行版中正常运行。</span><span class="sxs-lookup"><span data-stu-id="28694-102">A snap is a bundle of an app and its dependencies that works without modification across many different Linux distributions.</span></span> <span data-ttu-id="28694-103">可以从 Snap Store 中发现和安装 Snap。</span><span class="sxs-lookup"><span data-stu-id="28694-103">Snaps are discoverable and installable from the Snap Store.</span></span> <span data-ttu-id="28694-104">若要详细了解 Snap，请参阅[开始使用 Snap](https://snapcraft.io/docs/getting-started)。</span><span class="sxs-lookup"><span data-stu-id="28694-104">For more information about Snap, see [Getting started with Snap](https://snapcraft.io/docs/getting-started).</span></span>

<span data-ttu-id="28694-105">只有受支持的 .NET Core 版本，才能通过 Snap 获取。</span><span class="sxs-lookup"><span data-stu-id="28694-105">Only supported versions of .NET Core are available through Snap.</span></span>

### <a name="install-the-sdk"></a><span data-ttu-id="28694-106">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="28694-106">Install the SDK</span></span>

<span data-ttu-id="28694-107">适用于 .NET SDK 的 Snap 包都是在同一标识符（即 `dotnet-sdk`）下发布的。</span><span class="sxs-lookup"><span data-stu-id="28694-107">Snap packages for .NET SDK are all published under the same identifier: `dotnet-sdk`.</span></span> <span data-ttu-id="28694-108">可以通过指定通道来安装特定版本的 SDK。</span><span class="sxs-lookup"><span data-stu-id="28694-108">A specific version of the SDK can be installed by specifying the channel.</span></span> <span data-ttu-id="28694-109">SDK 包括相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="28694-109">The SDK includes the corresponding runtime.</span></span> <span data-ttu-id="28694-110">下表列出了通道：</span><span class="sxs-lookup"><span data-stu-id="28694-110">The following table lists the channels:</span></span>

| <span data-ttu-id="28694-111">.NET 版本</span><span class="sxs-lookup"><span data-stu-id="28694-111">.NET version</span></span> | <span data-ttu-id="28694-112">Snap 包</span><span class="sxs-lookup"><span data-stu-id="28694-112">Snap package</span></span>             |
|--------------|--------------------------|
| <span data-ttu-id="28694-113">5.0</span><span class="sxs-lookup"><span data-stu-id="28694-113">5.0</span></span>          | <span data-ttu-id="28694-114">`5.0` 或 `latest/stable`</span><span class="sxs-lookup"><span data-stu-id="28694-114">`5.0` or `latest/stable`</span></span> |
| <span data-ttu-id="28694-115">3.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="28694-115">3.1 (LTS)</span></span>    | <span data-ttu-id="28694-116">`3.1` 或 `lts/stable`</span><span class="sxs-lookup"><span data-stu-id="28694-116">`3.1` or `lts/stable`</span></span>    |
| <span data-ttu-id="28694-117">2.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="28694-117">2.1 (LTS)</span></span>    | `2.1`                    |

<span data-ttu-id="28694-118">若要安装适用于 .NET SDK 的 Snap 包，请运行 `snap install` 命令。</span><span class="sxs-lookup"><span data-stu-id="28694-118">Use the `snap install` command to install a .NET SDK snap package.</span></span> <span data-ttu-id="28694-119">使用 `--channel` 参数来指明要安装哪个版本。</span><span class="sxs-lookup"><span data-stu-id="28694-119">Use the `--channel` parameter to indicate which version to install.</span></span> <span data-ttu-id="28694-120">如果省略此参数，则使用 `latest/stable`。</span><span class="sxs-lookup"><span data-stu-id="28694-120">If this parameter is omitted, `latest/stable` is used.</span></span> <span data-ttu-id="28694-121">在下面的示例中，指定的是 `5.0`：</span><span class="sxs-lookup"><span data-stu-id="28694-121">In this example, `5.0` is specified:</span></span>

```bash
sudo snap install dotnet-sdk --classic --channel=5.0
```

<span data-ttu-id="28694-122">接下来，使用 `snap alias` 命令为系统注册 `dotnet` 命令：</span><span class="sxs-lookup"><span data-stu-id="28694-122">Next, register the `dotnet` command for the system with the `snap alias` command:</span></span>

```bash
sudo snap alias dotnet-sdk.dotnet dotnet
```

<span data-ttu-id="28694-123">此命令的格式为 `sudo snap alias {package}.{command} {alias}`。</span><span class="sxs-lookup"><span data-stu-id="28694-123">This command is formatted as: `sudo snap alias {package}.{command} {alias}`.</span></span> <span data-ttu-id="28694-124">可以选择所需的任何 `{alias}` 名称。</span><span class="sxs-lookup"><span data-stu-id="28694-124">You can choose any `{alias}` name you would like.</span></span> <span data-ttu-id="28694-125">例如，可以根据 Snap 安装的特定版本来命名此命令：`sudo snap alias dotnet-sdk.dotnet dotnet50`。</span><span class="sxs-lookup"><span data-stu-id="28694-125">For example, you could name the command after the specific version installed by snap: `sudo snap alias dotnet-sdk.dotnet dotnet50`.</span></span> <span data-ttu-id="28694-126">运行命令 `dotnet50` 时，将调用这一特定版本的 .NET。</span><span class="sxs-lookup"><span data-stu-id="28694-126">When you use the command `dotnet50`, you'll invoke this specific version of .NET.</span></span> <span data-ttu-id="28694-127">但这与大多数教程和示例不兼容，因为它们需要使用 `dotnet` 命令。</span><span class="sxs-lookup"><span data-stu-id="28694-127">But this is incompatible with most tutorials and examples as they expect a `dotnet` command to be available.</span></span>

### <a name="install-the-runtime"></a><span data-ttu-id="28694-128">安装运行时</span><span class="sxs-lookup"><span data-stu-id="28694-128">Install the runtime</span></span>

<span data-ttu-id="28694-129">适用于 .NET Core Runtime 的 Snap 包都是在各自的包标识符下发布的。</span><span class="sxs-lookup"><span data-stu-id="28694-129">Snap packages for .NET Core Runtime are each published under their own package identifier.</span></span> <span data-ttu-id="28694-130">下表列出了这些包标识符：</span><span class="sxs-lookup"><span data-stu-id="28694-130">The following table lists the package identifiers:</span></span>

| <span data-ttu-id="28694-131">.NET 版本</span><span class="sxs-lookup"><span data-stu-id="28694-131">.NET version</span></span>      | <span data-ttu-id="28694-132">Snap 包</span><span class="sxs-lookup"><span data-stu-id="28694-132">Snap package</span></span>        |
|-------------------|---------------------|
| <span data-ttu-id="28694-133">5.0</span><span class="sxs-lookup"><span data-stu-id="28694-133">5.0</span></span>               | `dotnet-runtime-50` |
| <span data-ttu-id="28694-134">3.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="28694-134">3.1 (LTS)</span></span>         | `dotnet-runtime-31` |
| <span data-ttu-id="28694-135">3.0</span><span class="sxs-lookup"><span data-stu-id="28694-135">3.0</span></span>               | `dotnet-runtime-30` |
| <span data-ttu-id="28694-136">2.2</span><span class="sxs-lookup"><span data-stu-id="28694-136">2.2</span></span>               | `dotnet-runtime-22` |
| <span data-ttu-id="28694-137">2.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="28694-137">2.1 (LTS)</span></span>         | `dotnet-runtime-21` |

<span data-ttu-id="28694-138">若要安装适用于 .NET Runtime 的 Snap 包，请运行 `snap install` 命令。</span><span class="sxs-lookup"><span data-stu-id="28694-138">Use the `snap install` command to install a .NET Runtime snap package.</span></span> <span data-ttu-id="28694-139">在下面的示例中，安装的是 .NET 5.0：</span><span class="sxs-lookup"><span data-stu-id="28694-139">In this example, .NET 5.0 is installed:</span></span>

```bash
sudo snap install dotnet-runtime-50 --classic
```

<span data-ttu-id="28694-140">接下来，使用 `snap alias` 命令为系统注册 `dotnet` 命令：</span><span class="sxs-lookup"><span data-stu-id="28694-140">Next, register the `dotnet` command for the system with the `snap alias` command:</span></span>

```bash
sudo snap alias dotnet-runtime-50.dotnet dotnet
```

<span data-ttu-id="28694-141">此命令的格式为 `sudo snap alias {package}.{command} {alias}`。</span><span class="sxs-lookup"><span data-stu-id="28694-141">This command is formatted as: `sudo snap alias {package}.{command} {alias}`.</span></span> <span data-ttu-id="28694-142">可以选择所需的任何 `{alias}` 名称。</span><span class="sxs-lookup"><span data-stu-id="28694-142">You can choose any `{alias}` name you would like.</span></span> <span data-ttu-id="28694-143">例如，可以根据 Snap 安装的特定版本来命名此命令：`sudo snap alias dotnet-runtime-50.dotnet dotnet50`。</span><span class="sxs-lookup"><span data-stu-id="28694-143">For example, you could name the command after the specific version installed by snap: `sudo snap alias dotnet-runtime-50.dotnet dotnet50`.</span></span> <span data-ttu-id="28694-144">运行命令 `dotnet50` 时，将调用这一特定版本的 .NET。</span><span class="sxs-lookup"><span data-stu-id="28694-144">When you use the command `dotnet50`, you'll invoke this specific version of .NET.</span></span> <span data-ttu-id="28694-145">但这与大多数教程和示例不兼容，因为它们需要使用 `dotnet` 命令。</span><span class="sxs-lookup"><span data-stu-id="28694-145">But this is incompatible with most tutorials and examples as they expect a `dotnet` command to be available.</span></span>

### <a name="ssl-certificate-errors"></a><span data-ttu-id="28694-146">SSL 证书错误</span><span class="sxs-lookup"><span data-stu-id="28694-146">SSL Certificate errors</span></span>

<span data-ttu-id="28694-147">通过 Snap 安装 .NET 后，可能会在某些发行版上找不到 .NET SSL 证书，并且可能会在 `restore` 期间看到如下错误：</span><span class="sxs-lookup"><span data-stu-id="28694-147">When .NET is installed through Snap, it's possible that on some distros the .NET SSL certificates may not be found and you may receive an error similar to the following during `restore`:</span></span>

```bash
Processing post-creation actions...
Running 'dotnet restore' on /home/myhome/test/test.csproj...
  Restoring packages for /home/myhome/test/test.csproj...
/snap/dotnet-sdk/27/sdk/2.2.103/NuGet.targets(114,5): error : Unable to load the service index for source https://api.nuget.org/v3/index.json. [/home/myhome/test/test.csproj]
/snap/dotnet-sdk/27/sdk/2.2.103/NuGet.targets(114,5): error :   The SSL connection could not be established, see inner exception. [/home/myhome/test/test.csproj]
/snap/dotnet-sdk/27/sdk/2.2.103/NuGet.targets(114,5): error :   The remote certificate is invalid according to the validation procedure. [/home/myhome/test/test.csproj]
```

<span data-ttu-id="28694-148">若要解决此问题，请设置一些环境变量：</span><span class="sxs-lookup"><span data-stu-id="28694-148">To resolve this issue, set a few environment variables:</span></span>

```bash
export SSL_CERT_FILE=[path-to-certificate-file]
export SSL_CERT_DIR=/dev/null
```

<span data-ttu-id="28694-149">证书位置因发行版而异。</span><span class="sxs-lookup"><span data-stu-id="28694-149">The certificate location will vary by distro.</span></span> <span data-ttu-id="28694-150">下面是我们在发行版中遇到此问题的位置。</span><span class="sxs-lookup"><span data-stu-id="28694-150">Here are the locations for the distros where we have experienced the issue.</span></span>

* <span data-ttu-id="28694-151">Fedora - `/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem`</span><span class="sxs-lookup"><span data-stu-id="28694-151">Fedora - `/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem`</span></span>
* <span data-ttu-id="28694-152">OpenSUSE - `/etc/ssl/ca-bundle.pem`</span><span class="sxs-lookup"><span data-stu-id="28694-152">OpenSUSE - `/etc/ssl/ca-bundle.pem`</span></span>
* <span data-ttu-id="28694-153">Solus - `/etc/ssl/certs/ca-certificates.crt`</span><span class="sxs-lookup"><span data-stu-id="28694-153">Solus - `/etc/ssl/certs/ca-certificates.crt`</span></span>
