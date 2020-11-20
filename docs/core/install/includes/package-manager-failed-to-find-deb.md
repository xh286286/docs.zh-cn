---
ms.openlocfilehash: aba7b473af7685aa45f7e093a2f75311687593df
ms.sourcegitcommit: bc9c63541c3dc756d48a7ce9d22b5583a18cf7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2020
ms.locfileid: "94506948"
---

<span data-ttu-id="63e6b-101">如果收到类似于“找不到包 {dotnet-package}”或“无法安装某些包”的错误消息，请运行以下命令 。</span><span class="sxs-lookup"><span data-stu-id="63e6b-101">If you receive an error message similar to **Unable to locate package {dotnet-package}** or **Some packages could not be installed**, run the following commands.</span></span>

<span data-ttu-id="63e6b-102">以下命令组中有两个占位符。</span><span class="sxs-lookup"><span data-stu-id="63e6b-102">There are two placeholders in the following set of commands.</span></span>

- `{dotnet-package}`\
<span data-ttu-id="63e6b-103">此项表示要安装的 .NET 包，如 `aspnetcore-runtime-3.1`。</span><span class="sxs-lookup"><span data-stu-id="63e6b-103">This represents the .NET package you're installing, such as `aspnetcore-runtime-3.1`.</span></span> <span data-ttu-id="63e6b-104">它在以下 `sudo apt-get install` 命令中使用。</span><span class="sxs-lookup"><span data-stu-id="63e6b-104">This is used in the following `sudo apt-get install` command.</span></span>

- `{os-version}`\
<span data-ttu-id="63e6b-105">此项表示你所使用的 Linux 版本。</span><span class="sxs-lookup"><span data-stu-id="63e6b-105">This represents the Linux version you are on.</span></span> <span data-ttu-id="63e6b-106">此项在以下 `wget` 命令中使用。</span><span class="sxs-lookup"><span data-stu-id="63e6b-106">This is used in the `wget` command below.</span></span>

<span data-ttu-id="63e6b-107">首先，尝试清除包列表：</span><span class="sxs-lookup"><span data-stu-id="63e6b-107">First, try purging the package list:</span></span>

```bash
sudo dpkg --purge packages-microsoft-prod && sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get update
```

<span data-ttu-id="63e6b-108">然后，再次尝试安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="63e6b-108">Then, try to install .NET again.</span></span> <span data-ttu-id="63e6b-109">如果这不起作用，可使用以下命令运行手动安装：</span><span class="sxs-lookup"><span data-stu-id="63e6b-109">If that doesn't work, you can run a manual install with the following commands:</span></span>
