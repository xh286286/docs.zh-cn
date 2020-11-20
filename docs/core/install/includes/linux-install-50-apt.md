---
ms.openlocfilehash: 87c7abf6a20dd8e9769f3b3b3cbe271d32fd62c3
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506951"
---

### <a name="install-the-sdk"></a><span data-ttu-id="8b2c1-101">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="8b2c1-101">Install the SDK</span></span>

<span data-ttu-id="8b2c1-102">.NET SDK 使你可以通过 .NET 开发应用。</span><span class="sxs-lookup"><span data-stu-id="8b2c1-102">The .NET SDK allows you to develop apps with .NET.</span></span> <span data-ttu-id="8b2c1-103">如果安装 .NET SDK，则无需安装相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="8b2c1-103">If you install the .NET SDK, you don't need to install the corresponding runtime.</span></span> <span data-ttu-id="8b2c1-104">若要安装 .NET SDK，请运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="8b2c1-104">To install the .NET SDK, run the following commands:</span></span>

```bash
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-5.0
```

> [!IMPORTANT]
> <span data-ttu-id="8b2c1-105">如果收到类似于“找不到包 dotnet-sdk-5.0”的错误消息，请参阅 [APT 疑难解答](#apt-troubleshooting)部分。</span><span class="sxs-lookup"><span data-stu-id="8b2c1-105">If you receive an error message similar to **Unable to locate package dotnet-sdk-5.0**, see the [APT troubleshooting](#apt-troubleshooting) section.</span></span>

### <a name="install-the-runtime"></a><span data-ttu-id="8b2c1-106">安装运行时</span><span class="sxs-lookup"><span data-stu-id="8b2c1-106">Install the runtime</span></span>

<span data-ttu-id="8b2c1-107">通过 ASP.NET Core 运行时，可以运行使用 .NET 开发且未提供运行时的应用。</span><span class="sxs-lookup"><span data-stu-id="8b2c1-107">The ASP.NET Core Runtime allows you to run apps that were made with .NET that didn't provide the runtime.</span></span> <span data-ttu-id="8b2c1-108">以下命令将安装 ASP.NET Core 运行时，这是与 .NET 最兼容的运行时。</span><span class="sxs-lookup"><span data-stu-id="8b2c1-108">The following commands install the ASP.NET Core Runtime, which is the most compatible runtime for .NET.</span></span> <span data-ttu-id="8b2c1-109">在终端中，运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="8b2c1-109">In your terminal, run the following commands:</span></span>

```bash
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y aspnetcore-runtime-5.0
```

> [!IMPORTANT]
> <span data-ttu-id="8b2c1-110">如果收到类似于“找不到包 aspnetcore-runtime-5.0”的错误消息，请参阅 [APT 疑难解答](#apt-troubleshooting)部分。</span><span class="sxs-lookup"><span data-stu-id="8b2c1-110">If you receive an error message similar to **Unable to locate package aspnetcore-runtime-5.0**, see the [APT troubleshooting](#apt-troubleshooting) section.</span></span>

<span data-ttu-id="8b2c1-111">作为 ASP.NET Core 运行时的一种替代方法，你可以安装不包含 ASP.NET Core 支持的 .NET 运行时：将上一命令中的 `aspnetcore-runtime-5.0` 替换为 `dotnet-runtime-5.0`：</span><span class="sxs-lookup"><span data-stu-id="8b2c1-111">As an alternative to the ASP.NET Core Runtime, you can install the .NET Runtime, which doesn't include ASP.NET Core support: replace `aspnetcore-runtime-5.0` in the previous command with `dotnet-runtime-5.0`:</span></span>

```bash
sudo apt-get install -y dotnet-runtime-5.0
```
