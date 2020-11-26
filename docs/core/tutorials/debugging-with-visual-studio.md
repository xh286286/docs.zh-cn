---
title: 使用 Visual Studio 调试 .NET 控制台应用程序
description: 了解如何使用 Visual Studio 调试 .NET 控制台应用。
ms.date: 06/08/2020
dev_langs:
- csharp
- vb
ms.custom: vs-dotnet
ms.openlocfilehash: 8a914dc6cf069c011ea5b077ada514bf8cec331d
ms.sourcegitcommit: 5114e7847e0ff8ddb8c266802d47af78567949cf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/19/2020
ms.locfileid: "94916180"
---
# <a name="tutorial-debug-a-net-console-application-using-visual-studio"></a><span data-ttu-id="6bd0f-103">教程：使用 Visual Studio 调试 .NET 控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="6bd0f-103">Tutorial: Debug a .NET console application using Visual Studio</span></span>

<span data-ttu-id="6bd0f-104">本教程介绍了 Visual Studio 中提供的调试工具。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-104">This tutorial introduces the debugging tools available in Visual Studio.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6bd0f-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="6bd0f-105">Prerequisites</span></span>

- <span data-ttu-id="6bd0f-106">本教程适用于在[使用 Visual Studio 创建 .NET 控制台应用程序](with-visual-studio.md)中创建的控制台应用。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-106">This tutorial works with the console app that you create in [Create a .NET console application using Visual Studio](with-visual-studio.md).</span></span>

## <a name="use-debug-build-configuration"></a><span data-ttu-id="6bd0f-107">使用“调试”生成配置</span><span class="sxs-lookup"><span data-stu-id="6bd0f-107">Use Debug build configuration</span></span>

<span data-ttu-id="6bd0f-108">“调试”和“发布”是 Visual Studio 的内置生成配置 。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-108">*Debug* and *Release* are Visual Studio's built-in build configurations.</span></span> <span data-ttu-id="6bd0f-109">可使用“调试”生成配置进行调试，使用“发布”配置进行最终版本分发。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-109">You use the Debug build configuration for debugging and the Release configuration for the final release distribution.</span></span>

<span data-ttu-id="6bd0f-110">在“调试”配置中，程序使用完整符号调试信息编译，且不进行优化。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-110">In the Debug configuration, a program compiles with full symbolic debug information and no optimization.</span></span> <span data-ttu-id="6bd0f-111">优化会使调试复杂化，因为源代码和生成的指令之间的关系更加复杂。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-111">Optimization complicates debugging, because the relationship between source code and generated instructions is more complex.</span></span> <span data-ttu-id="6bd0f-112">程序的发布配置进行了完全优化，且不包含任何符号调试信息。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-112">The release configuration of a program has no symbolic debug information and is fully optimized.</span></span>

 <span data-ttu-id="6bd0f-113">默认情况下，Visual Studio 使用“调试”生成配置，因此不需要在调试之前对其进行更改。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-113">By default, Visual Studio uses the Debug build configuration, so you don't need to change it before debugging.</span></span>

1. <span data-ttu-id="6bd0f-114">启动 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-114">Start Visual Studio.</span></span>

1. <span data-ttu-id="6bd0f-115">打开在[使用 Visual Studio 创建 .NET 控制台应用程序](with-visual-studio.md)中创建的项目。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-115">Open the project that you created in [Create a .NET console application using Visual Studio](with-visual-studio.md).</span></span>

   <span data-ttu-id="6bd0f-116">当前的生成配置显示在工具栏上。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-116">The current build configuration is shown on the toolbar.</span></span> <span data-ttu-id="6bd0f-117">下面的工具栏图像显示 Visual Studio 配置为编译应用的“调试”版本：</span><span class="sxs-lookup"><span data-stu-id="6bd0f-117">The following toolbar image shows that Visual Studio is configured to compile the Debug version of the app:</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/visual-studio-toolbar-debug.png" alt-text="突出显示“调试”的 Visual Studio 工具栏":::

## <a name="set-a-breakpoint"></a><span data-ttu-id="6bd0f-119">设置断点</span><span class="sxs-lookup"><span data-stu-id="6bd0f-119">Set a breakpoint</span></span>

<span data-ttu-id="6bd0f-120">断点会在执行包含断点的代码行之前暂时中断执行应用程序。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-120">A *breakpoint* temporarily interrupts the execution of the application before the line with the breakpoint is executed.</span></span>

1. <span data-ttu-id="6bd0f-121">单击该行代码窗口的左边缘，在显示名称、日期和时间的行上设置断点。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-121">Set a *breakpoint* on the line that displays the name, date, and time, by clicking in the left margin of the code window on that line.</span></span> <span data-ttu-id="6bd0f-122">左边缘在行号的左侧。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-122">The left margin is to the left of the line numbers.</span></span>  <span data-ttu-id="6bd0f-123">设置断点的其他方法是，通过将光标置于代码行中，然后按 <kbd>F9</kbd> 或从菜单栏中选择“调试” > “切换断点”来进行设置 。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-123">Other ways to set a breakpoint are by placing the cursor in the line of code and then pressing <kbd>F9</kbd> or choosing **Debug** > **Toggle Breakpoint** from the menu bar.</span></span>

   <span data-ttu-id="6bd0f-124">如下图所示，Visual Studio 通过突出显示此代码行并在左边缘显示红点来指示设置了断点的行。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-124">As the following image shows, Visual Studio indicates the line on which the breakpoint is set by highlighting it and displaying a red dot in the left margin.</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/set-breakpoint-in-editor.png" alt-text="设置断点后的 Visual Studio 程序窗口":::

1. <span data-ttu-id="6bd0f-126">按 <kbd>F5</kbd>，在调试模式下运行程序。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-126">Press <kbd>F5</kbd> to run the program in Debug mode.</span></span> <span data-ttu-id="6bd0f-127">启动调试的另一种方法是从菜单中选择“调试” > “启动调试”。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-127">Another way to start debugging is by choosing **Debug** > **Start Debugging** from the menu.</span></span>

1. <span data-ttu-id="6bd0f-128">当程序提示输入名称时，在控制台窗口中输入字符串，然后按 Enter<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-128">Enter a string in the console window when the program prompts for a name, and then press <kbd>Enter</kbd>.</span></span>

1. <span data-ttu-id="6bd0f-129">到达断点时，程序停止执行，然后执行 `Console.WriteLine` 方法。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-129">Program execution stops when it reaches the breakpoint and before the `Console.WriteLine` method executes.</span></span> <span data-ttu-id="6bd0f-130">“局部变量”窗口显示当前正在执行的方法中定义的变量值。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-130">The **Locals** window displays the values of variables that are defined in the currently executing method.</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/breakpoint-hit.png" alt-text="Visual Studio 中断点的屏幕截图":::

## <a name="use-the-immediate-window"></a><span data-ttu-id="6bd0f-132">使用“即时”窗口</span><span class="sxs-lookup"><span data-stu-id="6bd0f-132">Use the Immediate window</span></span>

<span data-ttu-id="6bd0f-133">在“即时”窗口中，可以与正在调试的应用程序进行交互。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-133">The **Immediate** window lets you interact with the application you're debugging.</span></span> <span data-ttu-id="6bd0f-134">可以通过交互方式更改变量值，看看这样会对程序产生哪些影响。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-134">You can interactively change the value of variables to see how it affects your program.</span></span>

1. <span data-ttu-id="6bd0f-135">如果“即时”窗口不可见，请选择“调试” > “Windows” > “即时”来显示它。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-135">If the **Immediate** window is not visible, display it by choosing **Debug** > **Windows** > **Immediate**.</span></span>

1. <span data-ttu-id="6bd0f-136">在“即时”窗口中输入 `name = "Gracie"`，然后按 Enter<kbd></kbd> 键。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-136">Enter `name = "Gracie"` in the **Immediate** window and press the <kbd>Enter</kbd> key.</span></span>

1. <span data-ttu-id="6bd0f-137">在“即时”窗口中输入 `date = DateTime.Parse("2019-11-16T17:25:00Z").ToUniversalTime()`，然后按 Enter<kbd></kbd> 键。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-137">Enter `date = DateTime.Parse("2019-11-16T17:25:00Z").ToUniversalTime()` in the **Immediate** window and press the <kbd>Enter</kbd> key.</span></span>

   <span data-ttu-id="6bd0f-138">“即时”窗口显示字符串变量的值和 <xref:System.DateTime> 值的属性。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-138">The **Immediate** window displays the value of the string variable and the properties of the <xref:System.DateTime> value.</span></span> <span data-ttu-id="6bd0f-139">此外，“局部变量”窗口中也会更新变量值。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-139">In addition, the values of the variables are updated in the **Locals** window.</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/locals-immediate-window.png" alt-text="Visual Studio 2019 中的“局部变量”和“即时”窗口":::

1. <span data-ttu-id="6bd0f-141">按 <kbd>F5</kbd> 继续执行程序。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-141">Press <kbd>F5</kbd> to continue program execution.</span></span> <span data-ttu-id="6bd0f-142">继续操作的另一种方法是从菜单中选择“调试” > “继续”。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-142">Another way to continue is by choosing **Debug** > **Continue** from the menu.</span></span>

   <span data-ttu-id="6bd0f-143">控制台窗口中显示的值对应于在“即时”窗口中所做的更改。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-143">The values displayed in the console window correspond to the changes you made in the **Immediate** window.</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/console-window.png" alt-text="显示输入值的控制台窗口":::

1. <span data-ttu-id="6bd0f-145">按任意键，退出应用程序并停止调试。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-145">Press any key to exit the application and stop debugging.</span></span>

## <a name="set-a-conditional-breakpoint"></a><span data-ttu-id="6bd0f-146">设置条件断点</span><span class="sxs-lookup"><span data-stu-id="6bd0f-146">Set a conditional breakpoint</span></span>

<span data-ttu-id="6bd0f-147">程序显示用户输入的字符串。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-147">The program displays the string that the user enters.</span></span> <span data-ttu-id="6bd0f-148">如果用户没有输入任何内容，情况又如何呢？</span><span class="sxs-lookup"><span data-stu-id="6bd0f-148">What happens if the user doesn't enter anything?</span></span> <span data-ttu-id="6bd0f-149">可以使用名为“条件断点”的有用调试功能对此进行测试。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-149">You can test this with a useful debugging feature called a *conditional breakpoint*.</span></span>

1. <span data-ttu-id="6bd0f-150">右键单击表示断点的红点。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-150">Right-click on the red dot that represents the breakpoint.</span></span> <span data-ttu-id="6bd0f-151">在上下文菜单中，选择“条件”，打开“断点设置”对话框 。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-151">In the context menu, select **Conditions** to open the **Breakpoint Settings** dialog.</span></span> <span data-ttu-id="6bd0f-152">选择“条件”框（如果尚未选择）。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-152">Select the box for **Conditions** if it's not already selected.</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/breakpoint-settings.png" alt-text="显示断点设置面板的编辑器 - C#":::

1. <span data-ttu-id="6bd0f-154">对于条件表达式，在显示测试 `x` 是否为 5 的示例代码的字段中输入以下代码。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-154">For the **Conditional Expression**, enter the following code in the field that shows example code that tests if `x` is 5.</span></span> <span data-ttu-id="6bd0f-155">如果未显示想要使用的语言，请更改页面顶部的语言选择器。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-155">If the language you want to use is not shown, change the language selector at the top of the page.</span></span>

   ```csharp
   String.IsNullOrEmpty(name)
   ```

   ```vb
   String.IsNullOrEmpty(name)
   ```

   <span data-ttu-id="6bd0f-156">每次命中断点时，调试器都会调用 `String.IsNullOrEmpty(name)` 方法，仅当该方法调用返回 `true` 时，它才会在此行上中断。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-156">Each time the breakpoint is hit, the debugger calls the `String.IsNullOrEmpty(name)` method, and it breaks on this line only if the method call returns `true`.</span></span>

   <span data-ttu-id="6bd0f-157">可以指定“命中次数”（而不是条件表达式），这样程序就会在语句的执行次数达到指定值时中断执行。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-157">Instead of a conditional expression, you can specify a *hit count*, which interrupts program execution before a statement is executed a specified number of times.</span></span> <span data-ttu-id="6bd0f-158">另一种方法是指定“筛选条件”，这样就可以根据诸如线程标识符、进程名称或线程名称之类的特性来中断程序执行。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-158">Another option is to specify a *filter condition*, which interrupts program execution based on such attributes as a thread identifier, process name, or thread name.</span></span>

1. <span data-ttu-id="6bd0f-159">选择“关闭”以关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-159">Select **Close** to close the dialog.</span></span>

1. <span data-ttu-id="6bd0f-160">通过按 F5<kbd></kbd> 调试来启动程序。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-160">Start the program with debugging by pressing <kbd>F5</kbd>.</span></span>

1. <span data-ttu-id="6bd0f-161">在控制台窗口中，在看到输入名称的提示时按 Enter<kbd></kbd> 键。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-161">In the console window, press the <kbd>Enter</kbd> key when prompted to enter your name.</span></span>

1. <span data-ttu-id="6bd0f-162">由于符合指定的条件（`name` 为 `null` 或 <xref:System.String.Empty?displayProperty=nameWithType>），因此程序会在到达断点时以及在 `Console.WriteLine` 方法执行之前停止执行。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-162">Because the condition you specified (`name` is either `null` or <xref:System.String.Empty?displayProperty=nameWithType>) has been satisfied, program execution stops when it reaches the breakpoint and before the `Console.WriteLine` method executes.</span></span>

1. <span data-ttu-id="6bd0f-163">选择“局部变量”窗口，其中显示当前正在执行的方法的局部变量值。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-163">Select the **Locals** window, which shows the values of variables that are local to the currently executing method.</span></span> <span data-ttu-id="6bd0f-164">在这种情况下，`Main` 是当前正在执行的方法。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-164">In this case, `Main` is the currently executing method.</span></span> <span data-ttu-id="6bd0f-165">请注意，`name` 变量的值为 `""` 或 <xref:System.String.Empty?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-165">Observe that the value of the `name` variable is `""`, or <xref:System.String.Empty?displayProperty=nameWithType>.</span></span>

1. <span data-ttu-id="6bd0f-166">在“即时”窗口中输入下面的语句并按 Enter<kbd></kbd>，确认值为空字符串。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-166">Confirm the value is an empty string by entering the following statement in the **Immediate** window and pressing <kbd>Enter</kbd>.</span></span> <span data-ttu-id="6bd0f-167">结果为 `true`。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-167">The result is `true`.</span></span>

   ```csharp
   ? name == String.Empty
   ```

   ```vb
   ? String.IsNullOrEmpty(name)
   ```

   <span data-ttu-id="6bd0f-168">问号指示即时窗口[计算表达式](/visualstudio/ide/reference/immediate-window#enter-commands)。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-168">The question mark directs the immediate window to [evaluate an expression](/visualstudio/ide/reference/immediate-window#enter-commands).</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/immediate-window-output.png" alt-text="在执行语句后返回值 true 的即时窗口 - C#":::

1. <span data-ttu-id="6bd0f-170">按 <kbd>F5</kbd> 继续执行程序。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-170">Press <kbd>F5</kbd> to continue program execution.</span></span>

1. <span data-ttu-id="6bd0f-171">按任意键，关闭控制台窗口并停止调试。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-171">Press any key to close the console window and stop debugging.</span></span>

1. <span data-ttu-id="6bd0f-172">单击代码窗口左边缘上的点，清除断点。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-172">Clear the breakpoint by clicking on the dot in the left margin of the code window.</span></span> <span data-ttu-id="6bd0f-173">清除断点的其他方法是在选中代码行时按 <kbd>F9</kbd> 或选择“调试”>“切换断点”。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-173">Other ways to clear a breakpoint are by pressing <kbd>F9</kbd> or choosing **Debug > Toggle Breakpoint** while the line of code is selected.</span></span>

## <a name="step-through-a-program"></a><span data-ttu-id="6bd0f-174">单步执行程序</span><span class="sxs-lookup"><span data-stu-id="6bd0f-174">Step through a program</span></span>

<span data-ttu-id="6bd0f-175">使用 Visual Studio，还可以单步执行程序，并监视其执行情况。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-175">Visual Studio also allows you to step line by line through a program and monitor its execution.</span></span> <span data-ttu-id="6bd0f-176">通常可以设置断点，并通过程序代码的一小部分执行程序流。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-176">Ordinarily, you'd set a breakpoint and follow program flow through a small part of your program code.</span></span> <span data-ttu-id="6bd0f-177">由于此程序很小，因此可以单步执行整个程序。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-177">Since this program is small, you can step through the entire program.</span></span>

1. <span data-ttu-id="6bd0f-178">选择“调试” > “单步执行” 。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-178">Choose **Debug** > **Step Into**.</span></span> <span data-ttu-id="6bd0f-179">一次调试一个语句的另一种方法是按 F11<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-179">Another way to debug one statement at a time is by pressing <kbd>F11</kbd>.</span></span>

   <span data-ttu-id="6bd0f-180">Visual Studio 会在要执行的下一行旁边突出显示一个箭头。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-180">Visual Studio highlights and displays an arrow beside the next line of execution.</span></span>

   <span data-ttu-id="6bd0f-181">C#</span><span class="sxs-lookup"><span data-stu-id="6bd0f-181">C#</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/step-into-method.png" alt-text="Visual Studio 单步执行方法 - C#":::

   <span data-ttu-id="6bd0f-183">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6bd0f-183">Visual Basic</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/vb-step-into-method.png" alt-text="Visual Studio 单步执行方法 - Visual Basic":::

   <span data-ttu-id="6bd0f-185">此时，“局部变量”窗口显示 `args` 数组为空，`name` 和 `date` 具有默认值。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-185">At this point, the **Locals** window shows that the `args` array is empty, and `name` and `date` have default values.</span></span> <span data-ttu-id="6bd0f-186">此外，Visual Studio 还打开了一个空白控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-186">In addition, Visual Studio has opened a blank console window.</span></span>

1. <span data-ttu-id="6bd0f-187">按下 F11<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-187">Press <kbd>F11</kbd>.</span></span> <span data-ttu-id="6bd0f-188">Visual Studio 现在突出显示要执行的下一行。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-188">Visual Studio now highlights the next line of execution.</span></span> <span data-ttu-id="6bd0f-189">“局部变量”窗口保持不变，控制台窗口仍为空白。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-189">The **Locals** window is unchanged, and the console window remains blank.</span></span>

   <span data-ttu-id="6bd0f-190">C#</span><span class="sxs-lookup"><span data-stu-id="6bd0f-190">C#</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/step-into-source-method.png" alt-text="Visual Studio 单步执行方法源 - C#":::

   <span data-ttu-id="6bd0f-192">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6bd0f-192">Visual Basic</span></span>

   :::image type="content" source="./media/debugging-with-visual-studio/vb-step-into-source-method.png" alt-text="Visual Studio 单步执行方法源 - Visual Basic":::

1. <span data-ttu-id="6bd0f-194">按下 F11<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-194">Press <kbd>F11</kbd>.</span></span> <span data-ttu-id="6bd0f-195">Visual Studio 突出显示包含 `name` 变量赋值的语句。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-195">Visual Studio highlights the statement that includes the `name` variable assignment.</span></span> <span data-ttu-id="6bd0f-196">“局部变量”窗口显示 `name` 为 `null`，控制台窗口显示字符串“What is your name?”。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-196">The **Locals** window shows that `name` is `null`, and the console window displays the string "What is your name?".</span></span>

1. <span data-ttu-id="6bd0f-197">在控制台窗口中输入字符串，然后按 Enter<kbd></kbd>，从而响应提示。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-197">Respond to the prompt by entering a string in the console window and pressing <kbd>Enter</kbd>.</span></span> <span data-ttu-id="6bd0f-198">控制台无响应，输入的字符串未显示在控制台窗口中，但 <xref:System.Console.ReadLine%2A?displayProperty=nameWithType> 方法将捕获输入。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-198">The console is unresponsive, and the string you entered isn't displayed in the console window, but the <xref:System.Console.ReadLine%2A?displayProperty=nameWithType> method will nevertheless capture your input.</span></span>

1. <span data-ttu-id="6bd0f-199">按下 F11<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-199">Press <kbd>F11</kbd>.</span></span> <span data-ttu-id="6bd0f-200">Visual Studio 突出显示包含 `date` 变量赋值（在 Visual Basic 中为 `currentDate`）的语句。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-200">Visual Studio highlights the statement that includes the `date` variable assignment (`currentDate` in Visual Basic).</span></span> <span data-ttu-id="6bd0f-201">“局部变量”窗口显示 <xref:System.Console.ReadLine%2A?displayProperty=nameWithType> 方法调用返回的值。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-201">The **Locals** window shows the value returned by the call to the <xref:System.Console.ReadLine%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="6bd0f-202">控制台窗口还显示在提示符处输入的字符串。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-202">The console window also displays the string you entered at the prompt.</span></span>

1. <span data-ttu-id="6bd0f-203">按下 F11<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-203">Press <kbd>F11</kbd>.</span></span> <span data-ttu-id="6bd0f-204">“局部变量”窗口显示通过 <xref:System.DateTime.Now?displayProperty=nameWithType> 属性赋值后的 `date` 变量值。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-204">The **Locals** window shows the value of the `date` variable after the assignment from the <xref:System.DateTime.Now?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="6bd0f-205">控制台窗口保持不变。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-205">The console window is unchanged.</span></span>

1. <span data-ttu-id="6bd0f-206">按下 F11<kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-206">Press <kbd>F11</kbd>.</span></span> <span data-ttu-id="6bd0f-207">Visual Studio 调用 <xref:System.Console.WriteLine(System.String,System.Object,System.Object)?displayProperty=nameWithType> 方法。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-207">Visual Studio calls the <xref:System.Console.WriteLine(System.String,System.Object,System.Object)?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="6bd0f-208">控制台窗口会显示格式化的字符串。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-208">The console window displays the formatted string.</span></span>

1. <span data-ttu-id="6bd0f-209">选择“调试” > “跳出” 。停止分步执行的另一种方法是按 Shift+F11<kbd></kbd><kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-209">Choose **Debug** > **Step Out**. Another way to stop step-by-step execution is by pressing <kbd>Shift</kbd>+<kbd>F11</kbd>.</span></span>

   <span data-ttu-id="6bd0f-210">控制台窗口会显示一条消息，并等待用户按任意键。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-210">The console window displays a message and waits for you to press a key.</span></span>

1. <span data-ttu-id="6bd0f-211">按任意键，关闭控制台窗口并停止调试。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-211">Press any key to close the console window and stop debugging.</span></span>

## <a name="use-release-build-configuration"></a><span data-ttu-id="6bd0f-212">使用“发布”生成配置</span><span class="sxs-lookup"><span data-stu-id="6bd0f-212">Use Release build configuration</span></span>

<span data-ttu-id="6bd0f-213">测试应用程序的“调试”版本后，还应该编译并测试“发布”版本。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-213">Once you've tested the Debug version of your application, you should also compile and test the Release version.</span></span> <span data-ttu-id="6bd0f-214">发布版本包含编译器优化，有时可能会对应用程序的行为产生不良影响。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-214">The Release version incorporates compiler optimizations that can sometimes negatively affect the behavior of an application.</span></span> <span data-ttu-id="6bd0f-215">例如，旨在提升性能的编译器优化可能会在多线程应用程序中创建争用条件。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-215">For example, compiler optimizations that are designed to improve performance can create race conditions in multithreaded applications.</span></span>

<span data-ttu-id="6bd0f-216">若要生成和测试控制台应用程序的发布版本，请将工具栏上的生成配置从“调试”更改为“发布”。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-216">To build and test the Release version of your console application, change the build configuration on the toolbar from **Debug** to **Release**.</span></span>

:::image type="content" source="./media/debugging-with-visual-studio/visual-studio-toolbar-release.png" alt-text="突出显示版本的默认 Visual Studio 工具栏":::

<span data-ttu-id="6bd0f-218">按 F5<kbd></kbd> 或选择“生成”菜单中的“生成解决方案”后，Visual Studio 会编译应用程序的“发布”版本。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-218">When you press <kbd>F5</kbd> or choose **Build Solution** from the **Build** menu, Visual Studio compiles the Release version of the application.</span></span> <span data-ttu-id="6bd0f-219">可像测试“调试”版本一样测试“发布”版本。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-219">You can test it as you did the Debug version.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6bd0f-220">后续步骤</span><span class="sxs-lookup"><span data-stu-id="6bd0f-220">Next steps</span></span>

<span data-ttu-id="6bd0f-221">在本教程中，你使用了 Visual Studio 调试工具。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-221">In this tutorial, you used Visual Studio debugging tools.</span></span> <span data-ttu-id="6bd0f-222">在下一教程中，你将发布应用的可部署版本。</span><span class="sxs-lookup"><span data-stu-id="6bd0f-222">In the next tutorial, you publish a deployable version of the app.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="6bd0f-223">使用 Visual Studio 发布 .NET 控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="6bd0f-223">Publish a .NET console application using Visual Studio</span></span>](publishing-with-visual-studio.md)
