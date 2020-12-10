---
title: 使用 Visual Studio for Mac 创建 .NET 类库
description: 了解如何使用 Visual Studio for Mac 创建 .NET 类库。
ms.date: 11/30/2020
ms.openlocfilehash: 1b6b26de06d18d505fa6dde3ff9779a3dab3f1e6
ms.sourcegitcommit: 9d525bb8109216ca1dc9e39c149d4902f4b43da5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/04/2020
ms.locfileid: "96599288"
---
# <a name="tutorial-create-a-net-class-library-using-visual-studio-for-mac"></a><span data-ttu-id="376e3-103">教程：使用 Visual Studio for Mac 创建 .NET 类库</span><span class="sxs-lookup"><span data-stu-id="376e3-103">Tutorial: Create a .NET class library using Visual Studio for Mac</span></span>

<span data-ttu-id="376e3-104">在本教程中，将创建包含一个字符串处理方法的类库。</span><span class="sxs-lookup"><span data-stu-id="376e3-104">In this tutorial, you create a class library that contains a single string-handling method.</span></span>

<span data-ttu-id="376e3-105">类库定义的是可以由应用程序调用的类型和方法。</span><span class="sxs-lookup"><span data-stu-id="376e3-105">A *class library* defines types and methods that are called by an application.</span></span> <span data-ttu-id="376e3-106">如果库以 .NET Standard 2.0 为目标，则支持 .NET Standard 2.0 的任何 .NET 实现（包括 .NET Framework）均可调用该库。</span><span class="sxs-lookup"><span data-stu-id="376e3-106">If the library targets .NET Standard 2.0, it can be called by any .NET implementation (including .NET Framework) that supports .NET Standard 2.0.</span></span> <span data-ttu-id="376e3-107">如果库以 .NET 5 为目标，则以 .NET 5 为目标的任何应用程序均可调用该库。</span><span class="sxs-lookup"><span data-stu-id="376e3-107">If the library targets .NET 5, it can be called by any application that targets .NET 5.</span></span> <span data-ttu-id="376e3-108">本教程演示如何以 .NET 5 为目标。</span><span class="sxs-lookup"><span data-stu-id="376e3-108">This tutorial shows how to target .NET 5.</span></span>

> [!NOTE]
> <span data-ttu-id="376e3-109">你的反馈非常有价值。</span><span class="sxs-lookup"><span data-stu-id="376e3-109">Your feedback is highly valued.</span></span> <span data-ttu-id="376e3-110">有两种方法可以向开发团队提供有关 Visual Studio for Mac 的反馈：</span><span class="sxs-lookup"><span data-stu-id="376e3-110">There are two ways you can provide feedback to the development team on Visual Studio for Mac:</span></span>
>
> - <span data-ttu-id="376e3-111">在 Visual Studio for Mac 中，从菜单选择“帮助” > “报告问题”，或从欢迎屏幕中选择“报告问题”，将打开一个窗口，以供填写 bug 报告。</span><span class="sxs-lookup"><span data-stu-id="376e3-111">In Visual Studio for Mac, select **Help** > **Report a Problem** from the menu or **Report a Problem** from the Welcome screen, which opens a window for filing a bug report.</span></span> <span data-ttu-id="376e3-112">可在[开发人员社区](https://aka.ms/feedback/report?space=41)门户中跟踪自己的反馈。</span><span class="sxs-lookup"><span data-stu-id="376e3-112">You can track your feedback in the [Developer Community](https://aka.ms/feedback/report?space=41) portal.</span></span>
> - <span data-ttu-id="376e3-113">若要提出建议，从菜单中选择“帮助” > “提供建议”，或从欢迎屏幕中选择“提供建议”，转到 [Visual Studio for Mac 开发人员社区网页](https://aka.ms/feedback/suggest?space=41)。</span><span class="sxs-lookup"><span data-stu-id="376e3-113">To make a suggestion, select **Help** > **Provide a Suggestion** from the menu or **Provide a Suggestion** from the Welcome screen, which takes you to the [Visual Studio for Mac Developer Community webpage](https://aka.ms/feedback/suggest?space=41).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="376e3-114">先决条件</span><span class="sxs-lookup"><span data-stu-id="376e3-114">Prerequisites</span></span>

* <span data-ttu-id="376e3-115">[安装 Visual Studio for Mac 版本 8.8 或更高版本](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link)。</span><span class="sxs-lookup"><span data-stu-id="376e3-115">[Install Visual Studio for Mac version 8.8 or later](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link).</span></span> <span data-ttu-id="376e3-116">选择用于安装 .NET Core 的选项。</span><span class="sxs-lookup"><span data-stu-id="376e3-116">Select the option to install .NET Core.</span></span> <span data-ttu-id="376e3-117">安装 Xamarin 对于 .NET 开发而言是可选项。</span><span class="sxs-lookup"><span data-stu-id="376e3-117">Installing Xamarin is optional for .NET development.</span></span> <span data-ttu-id="376e3-118">有关更多信息，请参见以下资源：</span><span class="sxs-lookup"><span data-stu-id="376e3-118">For more information, see the following resources:</span></span>

  * <span data-ttu-id="376e3-119">[教程：安装 Visual Studio for Mac](/visualstudio/mac/installation)。</span><span class="sxs-lookup"><span data-stu-id="376e3-119">[Tutorial: Install Visual Studio for Mac](/visualstudio/mac/installation).</span></span>
  * <span data-ttu-id="376e3-120">[支持的 macOS 版本](../install/macos.md)。</span><span class="sxs-lookup"><span data-stu-id="376e3-120">[Supported macOS versions](../install/macos.md).</span></span>
  * <span data-ttu-id="376e3-121">[Visual Studio for Mac 支持的 .NET 版本](/visualstudio/mac/net-core-support)。</span><span class="sxs-lookup"><span data-stu-id="376e3-121">[.NET versions supported by Visual Studio for Mac](/visualstudio/mac/net-core-support).</span></span>

## <a name="create-a-solution-with-a-class-library-project"></a><span data-ttu-id="376e3-122">创建包含类库项目的解决方案</span><span class="sxs-lookup"><span data-stu-id="376e3-122">Create a solution with a class library project</span></span>

<span data-ttu-id="376e3-123">Visual Studio 解决方案用作一个或多个项目的容器。</span><span class="sxs-lookup"><span data-stu-id="376e3-123">A Visual Studio solution serves as a container for one or more projects.</span></span> <span data-ttu-id="376e3-124">创建解决方案和解决方案中的类库项目。</span><span class="sxs-lookup"><span data-stu-id="376e3-124">Create a solution and a class library project in the solution.</span></span> <span data-ttu-id="376e3-125">稍后将其他相关项目添加到同一个解决方案中。</span><span class="sxs-lookup"><span data-stu-id="376e3-125">You'll add additional, related projects to the same solution later.</span></span>

1. <span data-ttu-id="376e3-126">启动 Visual Studio for Mac。</span><span class="sxs-lookup"><span data-stu-id="376e3-126">Start Visual Studio for Mac.</span></span>

1. <span data-ttu-id="376e3-127">在“开始”窗口中，选择“新建项目”。</span><span class="sxs-lookup"><span data-stu-id="376e3-127">In the start window, select **New Project**.</span></span>

1. <span data-ttu-id="376e3-128">在“为新项目选择一个模板”对话框中选择“Web 和控制台” > “库” > “类库”然后选择“下一步”。</span><span class="sxs-lookup"><span data-stu-id="376e3-128">In the **Choose a template for your new project** dialog select **Web and Console** > **Library** > **Class Library**, and then select **Next**.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/visual-studio-mac-new-project.png" alt-text="“新建项目”对话框":::

1. <span data-ttu-id="376e3-130">在“配置新的类库”对话框中，选择“.NET 5.0”，然后选择“下一步”。</span><span class="sxs-lookup"><span data-stu-id="376e3-130">In the **Configure your new Class Library** dialog, choose **.NET 5.0**, and select **Next**.</span></span>

1. <span data-ttu-id="376e3-131">将项目命名为“StringLibrary”，并将解决方案命名为“ClassLibraryProjects”。</span><span class="sxs-lookup"><span data-stu-id="376e3-131">Name the project "StringLibrary" and the solution "ClassLibraryProjects".</span></span> <span data-ttu-id="376e3-132">使“在解决方案目录中创建项目目录”保持选中状态。</span><span class="sxs-lookup"><span data-stu-id="376e3-132">Leave **Create a project directory within the solution directory** selected.</span></span> <span data-ttu-id="376e3-133">选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="376e3-133">Select **Create**.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/visual-studio-mac-new-project-options.png" alt-text="Visual Studio for Mac“新建项目”对话框选项":::

1. <span data-ttu-id="376e3-135">从主菜单中，选择“视图” > “解决方案”，然后选择“停靠”图标使边栏保持打开状态。</span><span class="sxs-lookup"><span data-stu-id="376e3-135">From the main menu, select **View** > **Solution**, and select the dock icon to keep the pad open.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/solution-dock-icon.png" alt-text="“解决方案”边栏的“停靠”图标":::

1. <span data-ttu-id="376e3-137">在“解决方案”边栏中，展开 `StringLibrary` 节点以显示模板提供的类文件 *Class1.cs*。</span><span class="sxs-lookup"><span data-stu-id="376e3-137">In the **Solution** pad, expand the `StringLibrary` node to reveal the class file provided by the template, *Class1.cs*.</span></span> <span data-ttu-id="376e3-138">按住 <kbd>Ctrl</kbd> 并单击该文件，从上下文菜单中选择“重命名”，然后将该文件重命名为“StringLibrary.cs”。</span><span class="sxs-lookup"><span data-stu-id="376e3-138"><kbd>ctrl</kbd>-click the file, select **Rename** from the context menu, and rename the file to *StringLibrary.cs*.</span></span> <span data-ttu-id="376e3-139">打开文件并将内容替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="376e3-139">Open the file and replace the contents with the following code:</span></span>

   :::code language="csharp" source="./snippets/library-with-visual-studio/csharp/StringLibrary/Class1.cs":::

1. <span data-ttu-id="376e3-140">按 <kbd>⌘</kbd><kbd>S</kbd> (<kbd>command</kbd>+<kbd>S</kbd>) 以保存文件。</span><span class="sxs-lookup"><span data-stu-id="376e3-140">Press <kbd>⌘</kbd><kbd>S</kbd> (<kbd>command</kbd>+<kbd>S</kbd>) to save the file.</span></span>

1. <span data-ttu-id="376e3-141">在 IDE 窗口底部边距处选择“错误”，打开“错误”面板。</span><span class="sxs-lookup"><span data-stu-id="376e3-141">Select **Errors** in the margin at the bottom of the IDE window to open the **Errors** panel.</span></span> <span data-ttu-id="376e3-142">选择“生成输出”按钮。</span><span class="sxs-lookup"><span data-stu-id="376e3-142">Select the **Build Output** button.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/visual-studio-mac-error-button.png" alt-text="显示“错误”按钮的 Visual Studio Mac IDE 底部边距处":::

1. <span data-ttu-id="376e3-144">从菜单中选择“生成” > “生成所有”。</span><span class="sxs-lookup"><span data-stu-id="376e3-144">Select **Build** > **Build All** from the menu.</span></span>

   <span data-ttu-id="376e3-145">生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="376e3-145">The solution builds.</span></span> <span data-ttu-id="376e3-146">生成输出面板显示生成成功。</span><span class="sxs-lookup"><span data-stu-id="376e3-146">The build output panel shows that the build is successful.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/visual-studio-mac-build-panel.png" alt-text="“错误”面板的 Visual Studio Mac 生成输出面板，其中显示生成成功消息":::

## <a name="add-a-console-app-to-the-solution"></a><span data-ttu-id="376e3-148">向解决方案添加控制台应用</span><span class="sxs-lookup"><span data-stu-id="376e3-148">Add a console app to the solution</span></span>

<span data-ttu-id="376e3-149">添加使用类库的控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="376e3-149">Add a console application that uses the class library.</span></span> <span data-ttu-id="376e3-150">应用将提示用户输入字符串，并报告字符串是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="376e3-150">The app will prompt the user to enter a string and report whether the string begins with an uppercase character.</span></span>

1. <span data-ttu-id="376e3-151">在“解决方案”边栏中，按住 <kbd>Ctrl</kbd> 并单击 `ClassLibraryProjects` 解决方案。</span><span class="sxs-lookup"><span data-stu-id="376e3-151">In the **Solution** pad, <kbd>ctrl</kbd>-click the `ClassLibraryProjects` solution.</span></span> <span data-ttu-id="376e3-152">通过从“Web 和控制台” > “应用”模板中选择模板来添加新的“控制台应用程序”项目，然后选择“下一步”。</span><span class="sxs-lookup"><span data-stu-id="376e3-152">Add a new **Console Application** project by selecting the template from the **Web and Console** > **App** templates, and select **Next**.</span></span>

1. <span data-ttu-id="376e3-153">选择“.NET Core 5.0”作为“目标框架”，然后选择“下一步”。</span><span class="sxs-lookup"><span data-stu-id="376e3-153">Select **.NET 5.0** as the **Target Framework** and select **Next**.</span></span>

1. <span data-ttu-id="376e3-154">将项目命名为“ShowCase”。</span><span class="sxs-lookup"><span data-stu-id="376e3-154">Name the project **ShowCase**.</span></span> <span data-ttu-id="376e3-155">选择“创建”以在解决方案中创建项目。</span><span class="sxs-lookup"><span data-stu-id="376e3-155">Select **Create** to create the project in the solution.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/add-showcase-project.png" alt-text="添加 ShowCase 项目":::

1. <span data-ttu-id="376e3-157">打开 *Program.cs* 文件。</span><span class="sxs-lookup"><span data-stu-id="376e3-157">Open the *Program.cs* file.</span></span> <span data-ttu-id="376e3-158">将代码替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="376e3-158">Replace the code with the following code:</span></span>

   :::code language="csharp" source="./snippets/library-with-visual-studio/csharp/ShowCase/Program.cs":::

   <span data-ttu-id="376e3-159">该程序会提示用户输入字符串。</span><span class="sxs-lookup"><span data-stu-id="376e3-159">The program prompts the user to enter a string.</span></span> <span data-ttu-id="376e3-160">它会指明字符串是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="376e3-160">It indicates whether the string starts with an uppercase character.</span></span> <span data-ttu-id="376e3-161">如果用户没有输入字符串就按 <kbd>Enter</kbd> 键，那么应用程序会终止，控制台窗口会关闭。</span><span class="sxs-lookup"><span data-stu-id="376e3-161">If the user presses the <kbd>enter</kbd> key without entering a string, the application ends, and the console window closes.</span></span>

   <span data-ttu-id="376e3-162">该代码使用 `row` 变量来维护写入到控制台窗口的数据行数计数。</span><span class="sxs-lookup"><span data-stu-id="376e3-162">The code uses the `row` variable to maintain a count of the number of rows of data written to the console window.</span></span> <span data-ttu-id="376e3-163">如果大于或等于 25，该代码将清除控制台窗口，并向用户显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="376e3-163">Whenever it's greater than or equal to 25, the code clears the console window and displays a message to the user.</span></span>

## <a name="add-a-project-reference"></a><span data-ttu-id="376e3-164">添加项目引用</span><span class="sxs-lookup"><span data-stu-id="376e3-164">Add a project reference</span></span>

<span data-ttu-id="376e3-165">最初，新的控制台应用项目无权访问类库。</span><span class="sxs-lookup"><span data-stu-id="376e3-165">Initially, the new console app project doesn't have access to the class library.</span></span> <span data-ttu-id="376e3-166">若要允许该项目调用类库中的方法，可以创建对类库项目的项目引用。</span><span class="sxs-lookup"><span data-stu-id="376e3-166">To allow it to call methods in the class library, create a project reference to the class library project.</span></span>

1. <span data-ttu-id="376e3-167">在“解决方案”边栏中，按住 <kbd>Ctrl</kbd> 并单击新“ShowCase”项目的“依赖项”节点。</span><span class="sxs-lookup"><span data-stu-id="376e3-167">In the **Solutions** pad, <kbd>ctrl</kbd>-click the **Dependencies** node of the new **ShowCase** project.</span></span> <span data-ttu-id="376e3-168">在上下文菜单中，选择“添加引用”。</span><span class="sxs-lookup"><span data-stu-id="376e3-168">In the context menu, select **Add Reference**.</span></span>

1. <span data-ttu-id="376e3-169">在“引用”对话框中，选择“StringLibrary”，然后选择“确定”。</span><span class="sxs-lookup"><span data-stu-id="376e3-169">In the **References** dialog, select **StringLibrary** and select **OK**.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="376e3-170">运行应用</span><span class="sxs-lookup"><span data-stu-id="376e3-170">Run the app</span></span>

1. <span data-ttu-id="376e3-171">按住 Ctrl<kbd></kbd> 并单击 ShowCase 项目，然后从上下文菜单中选择“运行项目”。</span><span class="sxs-lookup"><span data-stu-id="376e3-171"><kbd>ctrl</kbd>-click the **ShowCase** project and select **Run project** from the context menu.</span></span>

1. <span data-ttu-id="376e3-172">输入字符串并按 <kbd>Enter</kbd> 以试用程序，然后按 <kbd>Enter</kbd> 退出。</span><span class="sxs-lookup"><span data-stu-id="376e3-172">Try out the program by entering strings and pressing <kbd>enter</kbd>, then press <kbd>enter</kbd> to exit.</span></span>

   :::image type="content" source="media/library-with-visual-studio-mac/visual-studio-mac-console-window.png" alt-text="Visual Studio for Mac 控制台窗口，显示正在运行的应用":::

## <a name="additional-resources"></a><span data-ttu-id="376e3-174">其他资源</span><span class="sxs-lookup"><span data-stu-id="376e3-174">Additional resources</span></span>

* [<span data-ttu-id="376e3-175">使用 .NET CLI 开发库</span><span class="sxs-lookup"><span data-stu-id="376e3-175">Develop libraries with the .NET CLI</span></span>](libraries.md)
* [<span data-ttu-id="376e3-176">Visual Studio 2019 for Mac 发行说明</span><span class="sxs-lookup"><span data-stu-id="376e3-176">Visual Studio 2019 for Mac Release Notes</span></span>](/visualstudio/releasenotes/vs2019-mac-relnotes)
* <span data-ttu-id="376e3-177">[.NET Standard 版本及其支持的平台](../../standard/net-standard.md)。</span><span class="sxs-lookup"><span data-stu-id="376e3-177">[.NET Standard versions and the platforms they support](../../standard/net-standard.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="376e3-178">后续步骤</span><span class="sxs-lookup"><span data-stu-id="376e3-178">Next steps</span></span>

<span data-ttu-id="376e3-179">在本教程中，你创建了一个解决方案和一个库项目，并添加了一个使用该库的控制台应用项目。</span><span class="sxs-lookup"><span data-stu-id="376e3-179">In this tutorial, you created a solution and a library project, and added a console app project that uses the library.</span></span> <span data-ttu-id="376e3-180">在下一教程中，将向解决方案中添加单元测试项目。</span><span class="sxs-lookup"><span data-stu-id="376e3-180">In the next tutorial, you add a unit test project to the solution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="376e3-181">使用 Visual Studio for Mac 测试 .NET 类库</span><span class="sxs-lookup"><span data-stu-id="376e3-181">Test a .NET class library using Visual Studio for Mac</span></span>](testing-library-with-visual-studio-mac.md)
