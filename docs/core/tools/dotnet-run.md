---
title: dotnet run 命令
description: dotnet run 命令可便于使用源代码运行应用程序。
ms.date: 02/19/2020
ms.openlocfilehash: c80f290c75e3bac65ae73fe8edada53db4ce86f8
ms.sourcegitcommit: b201d177e01480a139622f3bf8facd367657a472
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2020
ms.locfileid: "94634411"
---
# <a name="dotnet-run"></a><span data-ttu-id="0b24a-103">dotnet run</span><span class="sxs-lookup"><span data-stu-id="0b24a-103">dotnet run</span></span>

<span data-ttu-id="0b24a-104">**本文适用于：** ✔️ .NET Core 2.x SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="0b24a-104">**This article applies to:** ✔️ .NET Core 2.x SDK and later versions</span></span>

## <a name="name"></a><span data-ttu-id="0b24a-105">“属性”</span><span class="sxs-lookup"><span data-stu-id="0b24a-105">Name</span></span>

<span data-ttu-id="0b24a-106">`dotnet run` - 无需任何显式编译或启动命令即可运行源代码。</span><span class="sxs-lookup"><span data-stu-id="0b24a-106">`dotnet run` - Runs source code without any explicit compile or launch commands.</span></span>

## <a name="synopsis"></a><span data-ttu-id="0b24a-107">摘要</span><span class="sxs-lookup"><span data-stu-id="0b24a-107">Synopsis</span></span>

```dotnetcli
dotnet run [-c|--configuration <CONFIGURATION>] [-f|--framework <FRAMEWORK>]
    [--force] [--interactive] [--launch-profile <NAME>] [--no-build]
    [--no-dependencies] [--no-launch-profile] [--no-restore]
    [-p|--project <PATH>] [-r|--runtime <RUNTIME_IDENTIFIER>]
    [-v|--verbosity <LEVEL>] [[--] [application arguments]]

dotnet run -h|--help
```

## <a name="description"></a><span data-ttu-id="0b24a-108">描述</span><span class="sxs-lookup"><span data-stu-id="0b24a-108">Description</span></span>

<span data-ttu-id="0b24a-109">`dotnet run` 命令为从源代码使用一个命令运行应用程序提供了一个方便的选项。</span><span class="sxs-lookup"><span data-stu-id="0b24a-109">The `dotnet run` command provides a convenient option to run your application from the source code with one command.</span></span> <span data-ttu-id="0b24a-110">这对从命令行中进行快速迭代开发很有帮助。</span><span class="sxs-lookup"><span data-stu-id="0b24a-110">It's useful for fast iterative development from the command line.</span></span> <span data-ttu-id="0b24a-111">命令取决于生成代码的 [`dotnet build`](dotnet-build.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="0b24a-111">The command depends on the [`dotnet build`](dotnet-build.md) command to build the code.</span></span> <span data-ttu-id="0b24a-112">对于此生成的任何要求，例如项目必须首先还原，同样适用于 `dotnet run`。</span><span class="sxs-lookup"><span data-stu-id="0b24a-112">Any requirements for the build, such as that the project must be restored first, apply to `dotnet run` as well.</span></span>

<span data-ttu-id="0b24a-113">输出文件会写入到默认位置，即 `bin/<configuration>/<target>`。</span><span class="sxs-lookup"><span data-stu-id="0b24a-113">Output files are written into the default location, which is `bin/<configuration>/<target>`.</span></span> <span data-ttu-id="0b24a-114">例如，如果具有 `netcoreapp2.1` 应用程序并且运行 `dotnet run`，则输出置于 `bin/Debug/netcoreapp2.1`。</span><span class="sxs-lookup"><span data-stu-id="0b24a-114">For example if you have a `netcoreapp2.1` application and you run `dotnet run`, the output is placed in `bin/Debug/netcoreapp2.1`.</span></span> <span data-ttu-id="0b24a-115">将根据需要覆盖文件。</span><span class="sxs-lookup"><span data-stu-id="0b24a-115">Files are overwritten as needed.</span></span> <span data-ttu-id="0b24a-116">临时文件将置于 `obj` 目录。</span><span class="sxs-lookup"><span data-stu-id="0b24a-116">Temporary files are placed in the `obj` directory.</span></span>

<span data-ttu-id="0b24a-117">如果该项目指定多个框架，在不使用 `-f|--framework <FRAMEWORK>` 选项指定框架时，执行 `dotnet run` 将导致错误。</span><span class="sxs-lookup"><span data-stu-id="0b24a-117">If the project specifies multiple frameworks, executing `dotnet run` results in an error unless the `-f|--framework <FRAMEWORK>` option is used to specify the framework.</span></span>

<span data-ttu-id="0b24a-118">在项目上下文，而不是生成程序集中使用 `dotnet run` 命令。</span><span class="sxs-lookup"><span data-stu-id="0b24a-118">The `dotnet run` command is used in the context of projects, not built assemblies.</span></span> <span data-ttu-id="0b24a-119">如果尝试改为运行依赖于框架的应用程序 DLL，则必须在不使用命令的情况下使用 [dotnet](dotnet.md)。</span><span class="sxs-lookup"><span data-stu-id="0b24a-119">If you're trying to run a framework-dependent application DLL instead, you must use [dotnet](dotnet.md) without a command.</span></span> <span data-ttu-id="0b24a-120">例如，若要运行 `myapp.dll`，请使用：</span><span class="sxs-lookup"><span data-stu-id="0b24a-120">For example, to run `myapp.dll`, use:</span></span>

```dotnetcli
dotnet myapp.dll
```

<span data-ttu-id="0b24a-121">有关 `dotnet` 驱动程序的详细信息，请参阅 [.NET 命令行工具 (CLI)](index.md) 主题。</span><span class="sxs-lookup"><span data-stu-id="0b24a-121">For more information on the `dotnet` driver, see the [.NET Command Line Tools (CLI)](index.md) topic.</span></span>

<span data-ttu-id="0b24a-122">若要运行应用程序，`dotnet run` 命令需从 NuGet 缓存解析共享运行时之外的应用程序依赖项。</span><span class="sxs-lookup"><span data-stu-id="0b24a-122">To run the application, the `dotnet run` command resolves the dependencies of the application that are outside of the shared runtime from the NuGet cache.</span></span> <span data-ttu-id="0b24a-123">因为它使用缓存的依赖项，因此，不推荐在生产中使用 `dotnet run` 来运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="0b24a-123">Because it uses cached dependencies, it's not recommended to use `dotnet run` to run applications in production.</span></span> <span data-ttu-id="0b24a-124">相反，使用 [`dotnet publish`](dotnet-publish.md)[ 命令创建部署](../deploying/index.md)，并部署已发布的输出。</span><span class="sxs-lookup"><span data-stu-id="0b24a-124">Instead, [create a deployment](../deploying/index.md) using the [`dotnet publish`](dotnet-publish.md) command and deploy the published output.</span></span>

### <a name="implicit-restore"></a><span data-ttu-id="0b24a-125">隐式还原</span><span class="sxs-lookup"><span data-stu-id="0b24a-125">Implicit restore</span></span>

[!INCLUDE[dotnet restore note + options](~/includes/dotnet-restore-note-options.md)]

## <a name="options"></a><span data-ttu-id="0b24a-126">选项</span><span class="sxs-lookup"><span data-stu-id="0b24a-126">Options</span></span>

- **`--`**

  <span data-ttu-id="0b24a-127">将参数分隔到正在运行的应用程序的参数的 `dotnet run`。</span><span class="sxs-lookup"><span data-stu-id="0b24a-127">Delimits arguments to `dotnet run` from arguments for the application being run.</span></span> <span data-ttu-id="0b24a-128">在此分隔符后的所有参数均传递给已运行的应用程序。</span><span class="sxs-lookup"><span data-stu-id="0b24a-128">All arguments after this delimiter are passed to the application run.</span></span>

- **`-c|--configuration <CONFIGURATION>`**

  <span data-ttu-id="0b24a-129">定义生成配置。</span><span class="sxs-lookup"><span data-stu-id="0b24a-129">Defines the build configuration.</span></span> <span data-ttu-id="0b24a-130">大多数项目的默认配置为 `Debug`，但你可以覆盖项目中的生成配置设置。</span><span class="sxs-lookup"><span data-stu-id="0b24a-130">The default for most projects is `Debug`, but you can override the build configuration settings in your project.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="0b24a-131">使用指定[框架](../../standard/frameworks.md)生成并运行应用。</span><span class="sxs-lookup"><span data-stu-id="0b24a-131">Builds and runs the app using the specified [framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="0b24a-132">框架必须在项目文件中进行指定。</span><span class="sxs-lookup"><span data-stu-id="0b24a-132">The framework must be specified in the project file.</span></span>

- **`--force`**

  <span data-ttu-id="0b24a-133">强制解析所有依赖项，即使上次还原已成功，也不例外。</span><span class="sxs-lookup"><span data-stu-id="0b24a-133">Forces all dependencies to be resolved even if the last restore was successful.</span></span> <span data-ttu-id="0b24a-134">指定此标记等同于删除 project.assets.json 文件  。</span><span class="sxs-lookup"><span data-stu-id="0b24a-134">Specifying this flag is the same as deleting the *project.assets.json* file.</span></span>

- **`-h|--help`**

  <span data-ttu-id="0b24a-135">打印出有关命令的简短帮助。</span><span class="sxs-lookup"><span data-stu-id="0b24a-135">Prints out a short help for the command.</span></span>

- **`--interactive`**

  <span data-ttu-id="0b24a-136">允许命令停止并等待用户输入或操作（例如，完成身份验证）。</span><span class="sxs-lookup"><span data-stu-id="0b24a-136">Allows the command to stop and wait for user input or action (for example, to complete authentication).</span></span> <span data-ttu-id="0b24a-137">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="0b24a-137">Available since .NET Core 3.0 SDK.</span></span>

- **`--launch-profile <NAME>`**

  <span data-ttu-id="0b24a-138">启动应用程序时要使用的启动配置文件（若有）的名称。</span><span class="sxs-lookup"><span data-stu-id="0b24a-138">The name of the launch profile (if any) to use when launching the application.</span></span> <span data-ttu-id="0b24a-139">启动配置文件在 launchSettings.json 文件中进行定义，通常称为 `Development`、`Staging` 和 `Production` 。</span><span class="sxs-lookup"><span data-stu-id="0b24a-139">Launch profiles are defined in the *launchSettings.json* file and are typically called `Development`, `Staging`, and `Production`.</span></span> <span data-ttu-id="0b24a-140">有关详细信息，请参阅[使用多个环境](/aspnet/core/fundamentals/environments)。</span><span class="sxs-lookup"><span data-stu-id="0b24a-140">For more information, see [Working with multiple environments](/aspnet/core/fundamentals/environments).</span></span>

- **`--no-build`**

  <span data-ttu-id="0b24a-141">运行前不生成项目。</span><span class="sxs-lookup"><span data-stu-id="0b24a-141">Doesn't build the project before running.</span></span> <span data-ttu-id="0b24a-142">还隐式设置 `--no-restore` 标记。</span><span class="sxs-lookup"><span data-stu-id="0b24a-142">It also implicit sets the `--no-restore` flag.</span></span>

- **`--no-dependencies`**

  <span data-ttu-id="0b24a-143">当使用项目到项目 (P2P) 引用还原项目时，还原根项目，不还原引用。</span><span class="sxs-lookup"><span data-stu-id="0b24a-143">When restoring a project with project-to-project (P2P) references, restores the root project and not the references.</span></span>

- **`--no-launch-profile`**

  <span data-ttu-id="0b24a-144">不尝试使用 launchSettings.json 配置应用程序  。</span><span class="sxs-lookup"><span data-stu-id="0b24a-144">Doesn't try to use *launchSettings.json* to configure the application.</span></span>

- **`--no-restore`**

  <span data-ttu-id="0b24a-145">运行此命令时不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="0b24a-145">Doesn't execute an implicit restore when running the command.</span></span>

- **`-p|--project <PATH>`**

  <span data-ttu-id="0b24a-146">指定要运行的项目文件的路径（文件夹名称或完整路径）。</span><span class="sxs-lookup"><span data-stu-id="0b24a-146">Specifies the path of the project file to run (folder name or full path).</span></span> <span data-ttu-id="0b24a-147">如果未指定，则默认为当前目录。</span><span class="sxs-lookup"><span data-stu-id="0b24a-147">If not specified, it defaults to the current directory.</span></span>

- **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="0b24a-148">指定要为其还原包的目标运行时。</span><span class="sxs-lookup"><span data-stu-id="0b24a-148">Specifies the target runtime to restore packages for.</span></span> <span data-ttu-id="0b24a-149">有关运行时标识符 (RID) 的列表，请参阅 [RID 目录](../rid-catalog.md)。</span><span class="sxs-lookup"><span data-stu-id="0b24a-149">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span> <span data-ttu-id="0b24a-150">自 .NET Core 3.0 SDK 起可用的 `-r` 简短选项。</span><span class="sxs-lookup"><span data-stu-id="0b24a-150">`-r` short option available since .NET Core 3.0 SDK.</span></span>

- **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="0b24a-151">设置命令的详细级别。</span><span class="sxs-lookup"><span data-stu-id="0b24a-151">Sets the verbosity level of the command.</span></span> <span data-ttu-id="0b24a-152">允许使用的值为 `q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]` 和 `diag[nostic]`。</span><span class="sxs-lookup"><span data-stu-id="0b24a-152">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="0b24a-153">默认值为 `m`。</span><span class="sxs-lookup"><span data-stu-id="0b24a-153">The default value is `m`.</span></span> <span data-ttu-id="0b24a-154">自 .NET Core 2.1 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="0b24a-154">Available since .NET Core 2.1 SDK.</span></span>

## <a name="examples"></a><span data-ttu-id="0b24a-155">示例</span><span class="sxs-lookup"><span data-stu-id="0b24a-155">Examples</span></span>

- <span data-ttu-id="0b24a-156">运行当前目录中的项目：</span><span class="sxs-lookup"><span data-stu-id="0b24a-156">Run the project in the current directory:</span></span>

  ```dotnetcli
  dotnet run
  ```

- <span data-ttu-id="0b24a-157">运行指定的项目：</span><span class="sxs-lookup"><span data-stu-id="0b24a-157">Run the specified project:</span></span>

  ```dotnetcli
  dotnet run --project ./projects/proj1/proj1.csproj
  ```

- <span data-ttu-id="0b24a-158">运行当前目录中的项目（在本例中，`--help` 参数被传递到应用程序，因为使用了空白的 `--` 选项）：</span><span class="sxs-lookup"><span data-stu-id="0b24a-158">Run the project in the current directory (the `--help` argument in this example is passed to the application, since the blank `--` option is used):</span></span>

  ```dotnetcli
  dotnet run --configuration Release -- --help
  ```

- <span data-ttu-id="0b24a-159">在仅显示最小输出的当前目录中还原项目的依赖项和工具，然后运行项目：</span><span class="sxs-lookup"><span data-stu-id="0b24a-159">Restore dependencies and tools for the project in the current directory only showing minimal output and then run the project:</span></span>

  ```dotnetcli
  dotnet run --verbosity m
  ```
