---
title: 使用 Visual Studio Code 创建 .NET 类库
description: 了解如何使用 Visual Studio Code 创建 .NET 类库。
ms.date: 11/18/2020
ms.openlocfilehash: 4473163b76060623b364d7dabf7366c3575e3dcd
ms.sourcegitcommit: 9d525bb8109216ca1dc9e39c149d4902f4b43da5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/04/2020
ms.locfileid: "96599494"
---
# <a name="tutorial-create-a-net-class-library-using-visual-studio-code"></a><span data-ttu-id="e02ab-103">教程：使用 Visual Studio Code 创建 .NET 类库</span><span class="sxs-lookup"><span data-stu-id="e02ab-103">Tutorial: Create a .NET class library using Visual Studio Code</span></span>

<span data-ttu-id="e02ab-104">在本教程中，将创建包含一个字符串处理方法的简单实用工具库。</span><span class="sxs-lookup"><span data-stu-id="e02ab-104">In this tutorial, you create a simple utility library that contains a single string-handling method.</span></span>

<span data-ttu-id="e02ab-105">类库定义的是可以由应用程序调用的类型和方法。</span><span class="sxs-lookup"><span data-stu-id="e02ab-105">A *class library* defines types and methods that are called by an application.</span></span> <span data-ttu-id="e02ab-106">如果库以 .NET Standard 2.0 为目标，则支持 .NET Standard 2.0 的任何 .NET 实现（包括 .NET Framework）均可调用该库。</span><span class="sxs-lookup"><span data-stu-id="e02ab-106">If the library targets .NET Standard 2.0, it can be called by any .NET implementation (including .NET Framework) that supports .NET Standard 2.0.</span></span> <span data-ttu-id="e02ab-107">如果库以 .NET 5 为目标，则以 .NET 5 为目标的任何应用程序均可调用该库。</span><span class="sxs-lookup"><span data-stu-id="e02ab-107">If the library targets .NET 5, it can be called by any application that targets .NET 5.</span></span> <span data-ttu-id="e02ab-108">本教程演示如何以 .NET 5 为目标。</span><span class="sxs-lookup"><span data-stu-id="e02ab-108">This tutorial shows how to target .NET 5.</span></span>

<span data-ttu-id="e02ab-109">创建类库后，可将其作为第三方组件进行分发，也可将其作为与一个或多个应用程序捆绑在一起的组件进行分发。</span><span class="sxs-lookup"><span data-stu-id="e02ab-109">When you create a class library, you can distribute it as a third-party component or as a bundled component with one or more applications.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e02ab-110">先决条件</span><span class="sxs-lookup"><span data-stu-id="e02ab-110">Prerequisites</span></span>

1. <span data-ttu-id="e02ab-111">已安装 [C# 扩展](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) 的 [Visual Studio Code](https://code.visualstudio.com/)。</span><span class="sxs-lookup"><span data-stu-id="e02ab-111">[Visual Studio Code](https://code.visualstudio.com/) with the [C# extension](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) installed.</span></span> <span data-ttu-id="e02ab-112">有关如何在 Visual Studio Code 上安装扩展的信息，请访问 [VS Code 扩展市场](https://code.visualstudio.com/docs/editor/extension-gallery)。</span><span class="sxs-lookup"><span data-stu-id="e02ab-112">For information about how to install extensions on Visual Studio Code, see [VS Code Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery).</span></span>
2. <span data-ttu-id="e02ab-113">[.NET 5.0 SDK 或更高版本](https://dotnet.microsoft.com/download)</span><span class="sxs-lookup"><span data-stu-id="e02ab-113">The [.NET 5.0 SDK or later](https://dotnet.microsoft.com/download)</span></span>

## <a name="create-a-solution"></a><span data-ttu-id="e02ab-114">创建解决方案</span><span class="sxs-lookup"><span data-stu-id="e02ab-114">Create a solution</span></span>

<span data-ttu-id="e02ab-115">首先，创建一个空白解决方案来放置类库项目。</span><span class="sxs-lookup"><span data-stu-id="e02ab-115">Start by creating a blank solution to put the class library project in.</span></span> <span data-ttu-id="e02ab-116">解决方案用作一个或多个项目的容器。</span><span class="sxs-lookup"><span data-stu-id="e02ab-116">A solution serves as a container for one or more projects.</span></span> <span data-ttu-id="e02ab-117">将其他相关项目添加到同一个解决方案中。</span><span class="sxs-lookup"><span data-stu-id="e02ab-117">You'll add additional, related projects to the same solution.</span></span>

1. <span data-ttu-id="e02ab-118">启动 Visual Studio Code。</span><span class="sxs-lookup"><span data-stu-id="e02ab-118">Start Visual Studio Code.</span></span>

1. <span data-ttu-id="e02ab-119">从主菜单中选择“文件” > “打开文件夹”（在 macOS 上为“打开...”）</span><span class="sxs-lookup"><span data-stu-id="e02ab-119">Select **File** > **Open Folder** (**Open...** on macOS) from the main menu</span></span>

1. <span data-ttu-id="e02ab-120">在“打开文件夹”对话框中，创建“ClassLibraryProjects”文件夹，然后单击“选择文件夹”（在 macOS 上为“打开”）。</span><span class="sxs-lookup"><span data-stu-id="e02ab-120">In the **Open Folder** dialog, create a *ClassLibraryProjects* folder and click **Select Folder** (**Open** on macOS).</span></span>

1. <span data-ttu-id="e02ab-121">在主菜单中选择“视图” > “终端”，从 Visual Studio Code 中打开“终端”  。</span><span class="sxs-lookup"><span data-stu-id="e02ab-121">Open the **Terminal** in Visual Studio Code by selecting **View** > **Terminal** from the main menu.</span></span>

   <span data-ttu-id="e02ab-122">“终端”在“ClassLibraryProjects”文件夹中连同命令提示符一起打开。</span><span class="sxs-lookup"><span data-stu-id="e02ab-122">The **Terminal** opens with the command prompt in the *ClassLibraryProjects* folder.</span></span>

1. <span data-ttu-id="e02ab-123">在“终端”中输入以下命令：</span><span class="sxs-lookup"><span data-stu-id="e02ab-123">In the **Terminal**, enter the following command:</span></span>

   ```dotnetcli
   dotnet new sln
   ```

   <span data-ttu-id="e02ab-124">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-124">The terminal output looks like the following example:</span></span>

   ```output
   The template "Solution File" was created successfully.
   ```

## <a name="create-a-class-library-project"></a><span data-ttu-id="e02ab-125">创建类库项目</span><span class="sxs-lookup"><span data-stu-id="e02ab-125">Create a class library project</span></span>

<span data-ttu-id="e02ab-126">将名为“StringLibrary”的新 .NET 类库项目添加到解决方案。</span><span class="sxs-lookup"><span data-stu-id="e02ab-126">Add a new .NET class library project named "StringLibrary" to the solution.</span></span>

1. <span data-ttu-id="e02ab-127">在终端中，运行以下命令创建库项目：</span><span class="sxs-lookup"><span data-stu-id="e02ab-127">In the terminal, run the following command to create the library project:</span></span>

   ```dotnetcli
   dotnet new classlib -o StringLibrary
   ```

   <span data-ttu-id="e02ab-128">`-o` 或 `--output` 命令指定用于放置生成的输出的位置。</span><span class="sxs-lookup"><span data-stu-id="e02ab-128">The `-o` or `--output` command specifies the location to place the generated output.</span></span>

   <span data-ttu-id="e02ab-129">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-129">The terminal output looks like the following example:</span></span>

   ```output
   The template "Class library" was created successfully.
   Processing post-creation actions...
   Running 'dotnet restore' on StringLibrary\StringLibrary.csproj...
     Determining projects to restore...
     Restored C:\Projects\ClassLibraryProjects\StringLibrary\StringLibrary.csproj (in 328 ms).
   Restore succeeded.
   ```

1. <span data-ttu-id="e02ab-130">运行以下命令，向解决方案添加库项目：</span><span class="sxs-lookup"><span data-stu-id="e02ab-130">Run the following command to add the library project to the solution:</span></span>

   ```dotnetcli
   dotnet sln add StringLibrary/StringLibrary.csproj
   ```

   <span data-ttu-id="e02ab-131">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-131">The terminal output looks like the following example:</span></span>

   ```output
   Project `StringLibrary\StringLibrary.csproj` added to the solution.
   ```

1. <span data-ttu-id="e02ab-132">检查以确保该库以 .NET 5 为目标。</span><span class="sxs-lookup"><span data-stu-id="e02ab-132">Check to make sure that the library targets .NET 5.</span></span> <span data-ttu-id="e02ab-133">在资源管理器中，打开 StringLibrary/StringLibrary.csproj。</span><span class="sxs-lookup"><span data-stu-id="e02ab-133">In **Explorer**, open *StringLibrary/StringLibrary.csproj*.</span></span>

   <span data-ttu-id="e02ab-134">`TargetFramework` 元素表明项目以 .NET 5.0 为目标。</span><span class="sxs-lookup"><span data-stu-id="e02ab-134">The `TargetFramework` element shows that the project targets .NET 5.0.</span></span>

   ```xml
   <Project Sdk="Microsoft.NET.Sdk">

     <PropertyGroup>
       <TargetFramework>net5.0</TargetFramework>
     </PropertyGroup>

   </Project>
   ```

1. <span data-ttu-id="e02ab-135">打开 Class1.cs 并将代码替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="e02ab-135">Open *Class1.cs* and replace the code with the following code.</span></span>

   :::code language="csharp" source="./snippets/library-with-visual-studio/csharp/StringLibrary/Class1.cs":::

   <span data-ttu-id="e02ab-136">类库 `UtilityLibraries.StringLibrary`包含一个名为 `StartsWithUpper` 的方法。</span><span class="sxs-lookup"><span data-stu-id="e02ab-136">The class library, `UtilityLibraries.StringLibrary`, contains a method named `StartsWithUpper`.</span></span> <span data-ttu-id="e02ab-137">此方法会返回 <xref:System.Boolean> 值，以指明当前字符串实例是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="e02ab-137">This method returns a <xref:System.Boolean> value that indicates whether the current string instance begins with an uppercase character.</span></span> <span data-ttu-id="e02ab-138">Unicode 标准会区分大小写字符。</span><span class="sxs-lookup"><span data-stu-id="e02ab-138">The Unicode standard distinguishes uppercase characters from lowercase characters.</span></span> <span data-ttu-id="e02ab-139">如果为大写字符，<xref:System.Char.IsUpper(System.Char)?displayProperty=nameWithType> 方法返回 `true`。</span><span class="sxs-lookup"><span data-stu-id="e02ab-139">The <xref:System.Char.IsUpper(System.Char)?displayProperty=nameWithType> method returns `true` if a character is uppercase.</span></span>

1. <span data-ttu-id="e02ab-140">保存该文件。</span><span class="sxs-lookup"><span data-stu-id="e02ab-140">Save the file.</span></span>

1. <span data-ttu-id="e02ab-141">运行以下命令以生成解决方案，并验证项目是否正确编译。</span><span class="sxs-lookup"><span data-stu-id="e02ab-141">Run the following command to build the solution and verify that the project compiles without error.</span></span>

   ```dotnetcli
   dotnet build
   ```

   <span data-ttu-id="e02ab-142">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-142">The terminal output looks like the following example:</span></span>

   ```output
   Microsoft (R) Build Engine version 16.7.0+b89cb5fde for .NET
   Copyright (C) Microsoft Corporation. All rights reserved.
     Determining projects to restore...
     All projects are up-to-date for restore.
     StringLibrary -> C:\Projects\ClassLibraryProjects\StringLibrary\bin\Debug\net5.0\StringLibrary.dll
   Build succeeded.
       0 Warning(s)
       0 Error(s)
   Time Elapsed 00:00:02.78
   ```

## <a name="add-a-console-app-to-the-solution"></a><span data-ttu-id="e02ab-143">向解决方案添加控制台应用</span><span class="sxs-lookup"><span data-stu-id="e02ab-143">Add a console app to the solution</span></span>

<span data-ttu-id="e02ab-144">添加使用类库的控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="e02ab-144">Add a console application that uses the class library.</span></span> <span data-ttu-id="e02ab-145">应用将提示用户输入字符串，并报告字符串是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="e02ab-145">The app will prompt the user to enter a string and report whether the string begins with an uppercase character.</span></span>

1. <span data-ttu-id="e02ab-146">在终端中，运行以下命令创建控制台应用项目：</span><span class="sxs-lookup"><span data-stu-id="e02ab-146">In the terminal, run the following command to create the console app project:</span></span>

   ```dotnetcli
   dotnet new console -o ShowCase
   ```

   <span data-ttu-id="e02ab-147">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-147">The terminal output looks like the following example:</span></span>

   ```output
   The template "Console Application" was created successfully.
   Processing post-creation actions...
   Running 'dotnet restore' on ShowCase\ShowCase.csproj...  
     Determining projects to restore...
     Restored C:\Projects\ClassLibraryProjects\ShowCase\ShowCase.csproj (in 210 ms).
   Restore succeeded.
   ```

1. <span data-ttu-id="e02ab-148">运行以下命令，向解决方案添加控制台应用项目：</span><span class="sxs-lookup"><span data-stu-id="e02ab-148">Run the following command to add the console app project to the solution:</span></span>

   ```dotnetcli
   dotnet sln add ShowCase/ShowCase.csproj
   ```

   <span data-ttu-id="e02ab-149">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-149">The terminal output looks like the following example:</span></span>

   ```output
   Project `ShowCase\ShowCase.csproj` added to the solution.
   ```

1. <span data-ttu-id="e02ab-150">打开 ShowCase/Program.cs 并将所有代码替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="e02ab-150">Open *ShowCase/Program.cs* and replace all of the code with the following code.</span></span>

   :::code language="csharp" source="./snippets/library-with-visual-studio/csharp/ShowCase/Program.cs":::

   <span data-ttu-id="e02ab-151">该代码使用 `row` 变量来维护写入到控制台窗口的数据行数计数。</span><span class="sxs-lookup"><span data-stu-id="e02ab-151">The code uses the `row` variable to maintain a count of the number of rows of data written to the console window.</span></span> <span data-ttu-id="e02ab-152">如果大于或等于 25，该代码将清除控制台窗口，并向用户显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="e02ab-152">Whenever it's greater than or equal to 25, the code clears the console window and displays a message to the user.</span></span>

   <span data-ttu-id="e02ab-153">该程序会提示用户输入字符串。</span><span class="sxs-lookup"><span data-stu-id="e02ab-153">The program prompts the user to enter a string.</span></span> <span data-ttu-id="e02ab-154">它会指明字符串是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="e02ab-154">It indicates whether the string starts with an uppercase character.</span></span> <span data-ttu-id="e02ab-155">如果用户没有输入字符串就按 <kbd>Enter</kbd> 键，那么应用程序会终止，控制台窗口会关闭。</span><span class="sxs-lookup"><span data-stu-id="e02ab-155">If the user presses the <kbd>Enter</kbd> key without entering a string, the application ends, and the console window closes.</span></span>

1. <span data-ttu-id="e02ab-156">保存更改。</span><span class="sxs-lookup"><span data-stu-id="e02ab-156">Save your changes.</span></span>

## <a name="add-a-project-reference"></a><span data-ttu-id="e02ab-157">添加项目引用</span><span class="sxs-lookup"><span data-stu-id="e02ab-157">Add a project reference</span></span>

<span data-ttu-id="e02ab-158">最初，新的控制台应用项目无权访问类库。</span><span class="sxs-lookup"><span data-stu-id="e02ab-158">Initially, the new console app project doesn't have access to the class library.</span></span> <span data-ttu-id="e02ab-159">若要允许该项目调用类库中的方法，可以创建对类库项目的项目引用。</span><span class="sxs-lookup"><span data-stu-id="e02ab-159">To allow it to call methods in the class library, create a project reference to the class library project.</span></span>

1. <span data-ttu-id="e02ab-160">运行下面的命令：</span><span class="sxs-lookup"><span data-stu-id="e02ab-160">Run the following command:</span></span>

   ```dotnetcli
   dotnet add ShowCase/ShowCase.csproj reference StringLibrary/StringLibrary.csproj
   ```

   <span data-ttu-id="e02ab-161">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-161">The terminal output looks like the following example:</span></span>

   ```output
   Reference `..\StringLibrary\StringLibrary.csproj` added to the project.
   ```

## <a name="run-the-app"></a><span data-ttu-id="e02ab-162">运行应用</span><span class="sxs-lookup"><span data-stu-id="e02ab-162">Run the app</span></span>

1. <span data-ttu-id="e02ab-163">在终端中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e02ab-163">Run the following command in the terminal:</span></span>

   ```dotnetcli
   dotnet run --project ShowCase/ShowCase.csproj
   ```

1. <span data-ttu-id="e02ab-164">输入字符串并按 Enter 以试用程序，然后按 Enter 退出<kbd></kbd><kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="e02ab-164">Try out the program by entering strings and pressing <kbd>Enter</kbd>, then press <kbd>Enter</kbd> to exit.</span></span>

   <span data-ttu-id="e02ab-165">终端输出如以下示例所示：</span><span class="sxs-lookup"><span data-stu-id="e02ab-165">The terminal output looks like the following example:</span></span>

   ```output
   Press <Enter> only to exit; otherwise, enter a string and press <Enter>:

   A string that starts with an uppercase letter
   Input: A string that starts with an uppercase letter
   Begins with uppercase? : Yes

   a string that starts with a lowercase letter
   Input: a string that starts with a lowercase letter
   Begins with uppercase? : No
   ```

## <a name="additional-resources"></a><span data-ttu-id="e02ab-166">其他资源</span><span class="sxs-lookup"><span data-stu-id="e02ab-166">Additional resources</span></span>

* [<span data-ttu-id="e02ab-167">使用 .NET CLI 开发库</span><span class="sxs-lookup"><span data-stu-id="e02ab-167">Develop libraries with the .NET CLI</span></span>](libraries.md)
* <span data-ttu-id="e02ab-168">[.NET Standard 版本及其支持的平台](../../standard/net-standard.md)。</span><span class="sxs-lookup"><span data-stu-id="e02ab-168">[.NET Standard versions and the platforms they support](../../standard/net-standard.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="e02ab-169">后续步骤</span><span class="sxs-lookup"><span data-stu-id="e02ab-169">Next steps</span></span>

<span data-ttu-id="e02ab-170">在本教程中，你创建了一个解决方案，添加了一个库项目，并添加了一个使用该库的控制台应用项目。</span><span class="sxs-lookup"><span data-stu-id="e02ab-170">In this tutorial, you created a solution, added a library project, and added a console app project that uses the library.</span></span> <span data-ttu-id="e02ab-171">在下一教程中，将向解决方案中添加单元测试项目。</span><span class="sxs-lookup"><span data-stu-id="e02ab-171">In the next tutorial, you add a unit test project to the solution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e02ab-172">使用 Visual Studio Code 通过 .NET 测试 .NET 类库</span><span class="sxs-lookup"><span data-stu-id="e02ab-172">Test a .NET class library with .NET using Visual Studio Code</span></span>](testing-library-with-visual-studio-code.md)
