---
title: 将 .NET 应用部署到 Raspberry Pi
description: 了解如何将 .NET 应用部署到 Raspberry Pi。
author: camsoper
ms.author: casoper
ms.date: 11/13/2020
ms.topic: how-to
ms.prod: dotnet
ms.openlocfilehash: 4da558e2cdfc283d21f2a5497cb71dc746109614
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96591085"
---
# <a name="deploy-net-apps-to-raspberry-pi"></a><span data-ttu-id="56230-103">将 .NET 应用部署到 Raspberry Pi</span><span class="sxs-lookup"><span data-stu-id="56230-103">Deploy .NET apps to Raspberry Pi</span></span>

<span data-ttu-id="56230-104">将 .NET 应用程序部署到 Raspberry Pi 与任何其他平台相同。</span><span class="sxs-lookup"><span data-stu-id="56230-104">Deployment of .NET apps to Raspberry Pi is identical to that of any other platform.</span></span> <span data-ttu-id="56230-105">您的应用程序可以作为 *独立* 或 *依赖于框架的* 部署模式运行。</span><span class="sxs-lookup"><span data-stu-id="56230-105">Your app can run as *self-contained* or *framework-dependent* deployment modes.</span></span> <span data-ttu-id="56230-106">每个策略都有一些优点。</span><span class="sxs-lookup"><span data-stu-id="56230-106">There are advantages to each strategy.</span></span> <span data-ttu-id="56230-107">有关详细信息，请参阅 [.net 应用程序发布概述](../core/deploying/index.md)。</span><span class="sxs-lookup"><span data-stu-id="56230-107">For more information, see [.NET application publishing overview](../core/deploying/index.md).</span></span>

## <a name="deploying-a-framework-dependent-app"></a><span data-ttu-id="56230-108">部署依赖框架的应用</span><span class="sxs-lookup"><span data-stu-id="56230-108">Deploying a framework-dependent app</span></span>

<span data-ttu-id="56230-109">若要将应用部署为依赖框架的应用，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="56230-109">To deploy your app as a framework-dependent app, complete the following steps:</span></span>

1. [!INCLUDE [ensure-ssh](includes/ensure-ssh.md)]

1. <span data-ttu-id="56230-110">使用 [dotnet 脚本](../core/tools/dotnet-install-script.md)在 Raspberry Pi 上安装 .net。</span><span class="sxs-lookup"><span data-stu-id="56230-110">Install .NET on the Raspberry Pi using the [dotnet-install scripts](../core/tools/dotnet-install-script.md).</span></span> <span data-ttu-id="56230-111">在 Raspberry Pi 上的 Bash 提示符 (本地或 SSH) 完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="56230-111">Complete the following steps from a Bash prompt on the Raspberry Pi (local or SSH):</span></span>
    1. <span data-ttu-id="56230-112">运行以下命令以安装 .NET：</span><span class="sxs-lookup"><span data-stu-id="56230-112">Run the following command to install .NET:</span></span>

        ```bash
        curl -sSL https://dot.net/v1/dotnet-install.sh | bash /dev/stdin
        ```

        > [!NOTE]
        > <span data-ttu-id="56230-113">这会安装最新版本。</span><span class="sxs-lookup"><span data-stu-id="56230-113">This installs the latest version.</span></span> <span data-ttu-id="56230-114">如果需要特定版本，请将添加 `--version <VERSION>` 到末尾，其中 `<VERSION>` 是特定的生成版本。</span><span class="sxs-lookup"><span data-stu-id="56230-114">If you need a specific version, add `--version <VERSION>` to the end, where `<VERSION>` is the specific build version.</span></span>

    1. <span data-ttu-id="56230-115">若要简化路径解析，请添加 `DOTNET_ROOT` 环境变量，并使用以下命令将 *dotnet* 目录添加到 `$PATH` ：</span><span class="sxs-lookup"><span data-stu-id="56230-115">To simplify path resolution, add a `DOTNET_ROOT` environment variable and add the *.dotnet* directory to `$PATH` with the following commands:</span></span>

        ```bash
        echo 'export DOTNET_ROOT=$HOME/.dotnet' >> ~/.bashrc
        echo 'export PATH=$PATH:$HOME/.dotnet' >> ~/.bashrc
        source ~/.bashrc
        ```

    1. <span data-ttu-id="56230-116">用以下命令验证 .NET 安装：</span><span class="sxs-lookup"><span data-stu-id="56230-116">Verify the .NET installation with the following command:</span></span>

        ```dotnetcli
        dotnet --version
        ```

        <span data-ttu-id="56230-117">验证显示的版本是否与安装的版本匹配。</span><span class="sxs-lookup"><span data-stu-id="56230-117">Verify the displayed version matches the version you installed.</span></span>

1. <span data-ttu-id="56230-118">按照以下步骤，在开发计算机上发布应用程序，具体取决于开发环境。</span><span class="sxs-lookup"><span data-stu-id="56230-118">Publish the app on the development computer as follows, depending on development environment.</span></span>
    - <span data-ttu-id="56230-119">如果使用的是 **Visual Studio**，请将 [应用程序部署到本地文件夹](/visualstudio/deployment/quickstart-deploy-to-local-folder?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="56230-119">If using **Visual Studio**, [deploy the app to a local folder](/visualstudio/deployment/quickstart-deploy-to-local-folder?view=vs-2019).</span></span> <span data-ttu-id="56230-120">在发布之前，在 "发布配置文件摘要" 中选择 " **编辑** "，然后选择 " **设置** " 选项卡。确保将 **部署模式** 设置为 " *依赖于框架* "，并将 " **目标运行时** " 设置为 " *可移植*"。</span><span class="sxs-lookup"><span data-stu-id="56230-120">Before publishing, select **Edit** in the publish profile summary and select the **Settings** tab. Ensure that **Deployment mode** is set to *Framework-dependent* and **Target runtime** is set to *Portable*.</span></span>
    - <span data-ttu-id="56230-121">如果使用 **.NET CLI**，请使用 [dotnet publish](../core/tools/dotnet-publish.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="56230-121">If using the **.NET CLI**, use the [dotnet publish](../core/tools/dotnet-publish.md) command.</span></span> <span data-ttu-id="56230-122">不需要其他参数。</span><span class="sxs-lookup"><span data-stu-id="56230-122">No additional arguments are required.</span></span>

1. [!INCLUDE [sftp-client](includes/sftp-client.md)]

1. <span data-ttu-id="56230-123">在 Raspberry Pi 上的 Bash 提示符 (本地或 SSH) 上，运行应用。</span><span class="sxs-lookup"><span data-stu-id="56230-123">From a Bash prompt on the Raspberry Pi (local or SSH), run the app.</span></span> <span data-ttu-id="56230-124">为此，请将部署文件夹设置为当前目录，并执行以下命令 (其中 *HelloWorld.dll* 是应用) 的入口点：</span><span class="sxs-lookup"><span data-stu-id="56230-124">To do this, set the deployment folder as the current directory and execute the following command (where *HelloWorld.dll* is the entry point of the app):</span></span>

    ```dotnetcli
    dotnet HelloWorld.dll
    ```

## <a name="deploying-a-self-contained-app"></a><span data-ttu-id="56230-125">部署自包含应用</span><span class="sxs-lookup"><span data-stu-id="56230-125">Deploying a self-contained app</span></span>

<span data-ttu-id="56230-126">若要将应用部署为自包含应用，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="56230-126">To deploy your app as a self-contained app, complete the following steps:</span></span>

1. [!INCLUDE [ensure-ssh](includes/ensure-ssh.md)]

1. <span data-ttu-id="56230-127">按照以下步骤，在开发计算机上发布应用程序，具体取决于开发环境。</span><span class="sxs-lookup"><span data-stu-id="56230-127">Publish the app on the development computer as follows, depending on development environment.</span></span>
    - <span data-ttu-id="56230-128">如果使用的是 **Visual Studio**，请将 [应用程序部署到本地文件夹](/visualstudio/deployment/quickstart-deploy-to-local-folder?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="56230-128">If using **Visual Studio**, [deploy the app to a local folder](/visualstudio/deployment/quickstart-deploy-to-local-folder?view=vs-2019).</span></span> <span data-ttu-id="56230-129">在发布之前，在 "发布配置文件摘要" 中选择 " **编辑** "，然后选择 " **设置** " 选项卡。确保将 " **部署模式** " 设置为 " *自包含* "，并将 " **目标运行时** " 设置为 " *linux-arm*"。</span><span class="sxs-lookup"><span data-stu-id="56230-129">Before publishing, select **Edit** in the publish profile summary and select the **Settings** tab. Ensure that **Deployment mode** is set to *Self-contained* and **Target runtime** is set to *linux-arm*.</span></span>
    - <span data-ttu-id="56230-130">如果使用的是 **.NET CLI**，请将 [dotnet publish](../core/tools/dotnet-publish.md) 命令与 `-r linux-arm` 参数一起使用：</span><span class="sxs-lookup"><span data-stu-id="56230-130">If using the **.NET CLI**, use the [dotnet publish](../core/tools/dotnet-publish.md) command with the `-r linux-arm` argument:</span></span>

        ```dotnetcli
        dotnet publish -r linux-arm
        ```

1. [!INCLUDE [sftp-client](includes/sftp-client.md)]

1. <span data-ttu-id="56230-131">在 Raspberry Pi 上的 Bash 提示符 (本地或 SSH) 上，运行应用。</span><span class="sxs-lookup"><span data-stu-id="56230-131">From a Bash prompt on the Raspberry Pi (local or SSH), run the app.</span></span> <span data-ttu-id="56230-132">为此，请将当前目录设置为部署位置并完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="56230-132">To do this, set the current directory to the deployment location and complete the following steps:</span></span>
    1. <span data-ttu-id="56230-133">为 *可执行* 文件 (指定) 的可执行 `HelloWorld` 文件的名称。</span><span class="sxs-lookup"><span data-stu-id="56230-133">Give the executable *execute* permission (where `HelloWorld` is the executable file name).</span></span>

        ```bash
        chmod +x HelloWorld
        ```

    1. <span data-ttu-id="56230-134">运行可执行文件。</span><span class="sxs-lookup"><span data-stu-id="56230-134">Run the executable.</span></span>

        ```bash
        ./HelloWorld
        ```
