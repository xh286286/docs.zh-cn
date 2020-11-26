---
title: 使用 DynamicActivity 在运行时创建活动
description: DynamicActivity 是一个具有公共构造函数的具体的密封类。 使用类可在运行时使用活动 DOM 组装活动功能。
ms.date: 03/30/2017
ms.assetid: 1af85cc6-912d-449e-90c5-c5db3eca5ace
ms.openlocfilehash: b65d7e385690b77d44c73e7a8a4ed38b04f30ea6
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96242092"
---
# <a name="creating-an-activity-at-runtime-with-dynamicactivity"></a><span data-ttu-id="e82f1-104">使用 DynamicActivity 在运行时创建活动</span><span class="sxs-lookup"><span data-stu-id="e82f1-104">Creating an Activity at Runtime with DynamicActivity</span></span>

<span data-ttu-id="e82f1-105"><xref:System.Activities.DynamicActivity> 是一个带有公共构造函数的具体的密封类。</span><span class="sxs-lookup"><span data-stu-id="e82f1-105"><xref:System.Activities.DynamicActivity> is a concrete, sealed class with a public constructor.</span></span> <span data-ttu-id="e82f1-106">通过使用活动 DOM，<xref:System.Activities.DynamicActivity> 可用于在运行时组合活动功能。</span><span class="sxs-lookup"><span data-stu-id="e82f1-106"><xref:System.Activities.DynamicActivity> can be used to assemble activity functionality at runtime using an activity DOM.</span></span>  
  
## <a name="dynamicactivity-features"></a><span data-ttu-id="e82f1-107">DynamicActivity 功能</span><span class="sxs-lookup"><span data-stu-id="e82f1-107">DynamicActivity Features</span></span>  

 <span data-ttu-id="e82f1-108"><xref:System.Activities.DynamicActivity> 有权访问执行属性、自变量和变量，但无权访问运行时服务（例如安排子活动或跟踪）。</span><span class="sxs-lookup"><span data-stu-id="e82f1-108"><xref:System.Activities.DynamicActivity> has access to execution properties, arguments and variables, but no access to run-time services such as scheduling child activities or tracking.</span></span>  
  
 <span data-ttu-id="e82f1-109">使用工作流 <xref:System.Activities.Argument> 对象可以设置顶级属性。</span><span class="sxs-lookup"><span data-stu-id="e82f1-109">Top-level properties can be set using workflow <xref:System.Activities.Argument> objects.</span></span> <span data-ttu-id="e82f1-110">在命令性代码中，使用新类型的 CLR 属性创建这些参数。</span><span class="sxs-lookup"><span data-stu-id="e82f1-110">In imperative code, these arguments are created using CLR properties on a new type.</span></span> <span data-ttu-id="e82f1-111">在 XAML 中，使用 `x:Class` 和 `x:Member` 标记声明这些参数。</span><span class="sxs-lookup"><span data-stu-id="e82f1-111">In XAML, they are declared using `x:Class` and `x:Member` tags.</span></span>  
  
 <span data-ttu-id="e82f1-112">使用 <xref:System.Activities.DynamicActivity> 构造的活动使用 <xref:System.ComponentModel.ICustomTypeDescriptor> 与设计器交互。</span><span class="sxs-lookup"><span data-stu-id="e82f1-112">Activities constructed using <xref:System.Activities.DynamicActivity> interface with the designer using <xref:System.ComponentModel.ICustomTypeDescriptor>.</span></span> <span data-ttu-id="e82f1-113">可以使用 <xref:System.Activities.XamlIntegration.ActivityXamlServices.Load%2A> 动态加载在设计器中创建的活动，如下面的过程所示。</span><span class="sxs-lookup"><span data-stu-id="e82f1-113">Activities created in the designer can be loaded dynamically using <xref:System.Activities.XamlIntegration.ActivityXamlServices.Load%2A>, as demonstrated in the following procedure.</span></span>  
  
#### <a name="to-create-an-activity-at-runtime-using-imperative-code"></a><span data-ttu-id="e82f1-114">使用命令性代码在运行时创建活动</span><span class="sxs-lookup"><span data-stu-id="e82f1-114">To create an activity at runtime using imperative code</span></span>  
  
1. <span data-ttu-id="e82f1-115">OpenVisual Studio 2010。</span><span class="sxs-lookup"><span data-stu-id="e82f1-115">OpenVisual Studio 2010.</span></span>  
  
2. <span data-ttu-id="e82f1-116">选择 " **文件**"、" **新建**"、" **项目**"。</span><span class="sxs-lookup"><span data-stu-id="e82f1-116">Select **File**, **New**, **Project**.</span></span> <span data-ttu-id="e82f1-117">在 "**项目类型**" 窗口中的 " **Visual c #** " 下选择 " **Workflow 4.0** "，然后选择 " **v2010** " 节点。</span><span class="sxs-lookup"><span data-stu-id="e82f1-117">Select **Workflow 4.0** under **Visual C#** in the **Project Types** window, and select the **v2010** node.</span></span> <span data-ttu-id="e82f1-118">在 "**模板**" 窗口中选择 "**顺序工作流控制台应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="e82f1-118">Select **Sequential Workflow Console Application** in the **Templates** window.</span></span> <span data-ttu-id="e82f1-119">将新项目命名为 DynamicActivitySample。</span><span class="sxs-lookup"><span data-stu-id="e82f1-119">Name the new project DynamicActivitySample.</span></span>  
  
3. <span data-ttu-id="e82f1-120">右键单击击 helloactivity 项目中的 Workflow1.xaml，然后选择 " **删除**"。</span><span class="sxs-lookup"><span data-stu-id="e82f1-120">Right-click Workflow1.xaml in the HelloActivity project and select **Delete**.</span></span>  
  
4. <span data-ttu-id="e82f1-121">打开 Program.cs。</span><span class="sxs-lookup"><span data-stu-id="e82f1-121">Open Program.cs.</span></span> <span data-ttu-id="e82f1-122">将下面的指令添加到文件的顶部。</span><span class="sxs-lookup"><span data-stu-id="e82f1-122">Add the following directive to the top of the file.</span></span>  
  
    ```csharp  
    using System.Collections.Generic;  
    ```  
  
5. <span data-ttu-id="e82f1-123">将 `Main` 方法的内容替换为以下代码，这会创建一个包含单个 <xref:System.Activities.Statements.Sequence> 活动的 <xref:System.Activities.Statements.WriteLine> 活动，并将后者赋给新动态活动的 <xref:System.Activities.DynamicActivity.Implementation%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="e82f1-123">Replace the contents of the `Main` method with the following code, which creates a <xref:System.Activities.Statements.Sequence> activity that contains a single <xref:System.Activities.Statements.WriteLine> activity and assigns it to the <xref:System.Activities.DynamicActivity.Implementation%2A> property of a new dynamic activity.</span></span>  
  
    ```csharp  
    //Define the input argument for the activity  
    var textOut = new InArgument<string>();  
    //Create the activity, property, and implementation  
                Activity dynamicWorkflow = new DynamicActivity()  
                {  
                    Properties =
                    {  
                        new DynamicActivityProperty  
                        {  
                            Name = "Text",  
                            Type = typeof(InArgument<String>),  
                            Value = textOut  
                        }  
                    },  
                    Implementation = () => new Sequence()  
                    {  
                        Activities =
                        {  
                            new WriteLine()  
                            {  
                                Text = new InArgument<string>(env => textOut.Get(env))  
                            }  
                        }  
                    }  
                };  
    //Execute the activity with a parameter dictionary  
                WorkflowInvoker.Invoke(dynamicWorkflow, new Dictionary<string, object> { { "Text", "Hello World!" } });  
                Console.ReadLine();  
    ```  
  
6. <span data-ttu-id="e82f1-124">执行应用程序。</span><span class="sxs-lookup"><span data-stu-id="e82f1-124">Execute the application.</span></span> <span data-ttu-id="e82f1-125">带有文本 "Hello World！" 的控制台窗口</span><span class="sxs-lookup"><span data-stu-id="e82f1-125">A console window with the text "Hello World!"</span></span> <span data-ttu-id="e82f1-126">显示.</span><span class="sxs-lookup"><span data-stu-id="e82f1-126">displays.</span></span>  
  
#### <a name="to-create-an-activity-at-runtime-using-xaml"></a><span data-ttu-id="e82f1-127">使用 XAML 在运行时创建活动</span><span class="sxs-lookup"><span data-stu-id="e82f1-127">To create an activity at runtime using XAML</span></span>  
  
1. <span data-ttu-id="e82f1-128">打开 Visual Studio 2010。</span><span class="sxs-lookup"><span data-stu-id="e82f1-128">Open Visual Studio 2010.</span></span>  
  
2. <span data-ttu-id="e82f1-129">选择 " **文件**"、" **新建**"、" **项目**"。</span><span class="sxs-lookup"><span data-stu-id="e82f1-129">Select **File**, **New**, **Project**.</span></span> <span data-ttu-id="e82f1-130">在 "**项目类型**" 窗口中的 " **Visual c #** " 下选择 " **Workflow 4.0** "，然后选择 " **v2010** " 节点。</span><span class="sxs-lookup"><span data-stu-id="e82f1-130">Select **Workflow 4.0** under **Visual C#** in the **Project Types** window, and select the **v2010** node.</span></span> <span data-ttu-id="e82f1-131">在 "**模板**" 窗口中选择 "**工作流控制台应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="e82f1-131">Select  **Workflow Console Application** in the **Templates** window.</span></span> <span data-ttu-id="e82f1-132">将新项目命名为 DynamicActivitySample。</span><span class="sxs-lookup"><span data-stu-id="e82f1-132">Name the new project DynamicActivitySample.</span></span>  
  
3. <span data-ttu-id="e82f1-133">在 HelloActivity 项目中打开 Workflow1.xaml。</span><span class="sxs-lookup"><span data-stu-id="e82f1-133">Open Workflow1.xaml in the HelloActivity project.</span></span> <span data-ttu-id="e82f1-134">单击设计器底部的 " **自变量** " 选项。</span><span class="sxs-lookup"><span data-stu-id="e82f1-134">Click the **Arguments** option at the bottom of the designer.</span></span> <span data-ttu-id="e82f1-135">创建一个 `In` 类型的新 `TextToWrite` 自变量，并将其命名为 `String`。</span><span class="sxs-lookup"><span data-stu-id="e82f1-135">Create a new `In` argument called `TextToWrite` of type `String`.</span></span>  
  
4. <span data-ttu-id="e82f1-136">将 " **WriteLine** " 活动从 "工具箱" 的 " **基元** " 部分拖到设计器图面上。</span><span class="sxs-lookup"><span data-stu-id="e82f1-136">Drag a **WriteLine** activity from the **Primitives** section of the toolbox onto the designer surface.</span></span> <span data-ttu-id="e82f1-137">将值分配 `TextToWrite` 给活动的 " **Text** " 属性。</span><span class="sxs-lookup"><span data-stu-id="e82f1-137">Assign the value `TextToWrite` to the **Text** property of the activity.</span></span>  
  
5. <span data-ttu-id="e82f1-138">打开 Program.cs。</span><span class="sxs-lookup"><span data-stu-id="e82f1-138">Open Program.cs.</span></span> <span data-ttu-id="e82f1-139">将下面的指令添加到文件的顶部。</span><span class="sxs-lookup"><span data-stu-id="e82f1-139">Add the following directive to the top of the file.</span></span>  
  
    ```csharp  
    using System.Activities.XamlIntegration;  
    ```  
  
6. <span data-ttu-id="e82f1-140">将 `Main` 方法的内容替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="e82f1-140">Replace the contents of the `Main` method with the following code.</span></span>  
  
    ```csharp  
    Activity act2 = ActivityXamlServices.Load(@"Workflow1.xaml");  
                    results = WorkflowInvoker.Invoke(act2, new Dictionary<string, object> { { "TextToWrite", "HelloWorld!" } });  
    Console.ReadLine();  
    ```  
  
7. <span data-ttu-id="e82f1-141">执行应用程序。</span><span class="sxs-lookup"><span data-stu-id="e82f1-141">Execute the application.</span></span> <span data-ttu-id="e82f1-142">带有文本 "Hello World！" 的控制台窗口</span><span class="sxs-lookup"><span data-stu-id="e82f1-142">A console window with the text "Hello World!"</span></span> <span data-ttu-id="e82f1-143"> 将出现。</span><span class="sxs-lookup"><span data-stu-id="e82f1-143">appears.</span></span>  
  
8. <span data-ttu-id="e82f1-144">在 **解决方案资源管理器** 中右键单击 "workflow1.xaml" 文件，然后选择 " **查看代码**"。</span><span class="sxs-lookup"><span data-stu-id="e82f1-144">Right-click the Workflow1.xaml file in the **Solution Explorer** and select **View Code**.</span></span> <span data-ttu-id="e82f1-145">请注意，活动类使用 `x:Class` 创建，属性使用 `x:Property` 创建。</span><span class="sxs-lookup"><span data-stu-id="e82f1-145">Note that the activity class is created with `x:Class` and the property is created with `x:Property`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e82f1-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e82f1-146">See also</span></span>

- [<span data-ttu-id="e82f1-147">使用命令性代码创作工作流、活动和表达式</span><span class="sxs-lookup"><span data-stu-id="e82f1-147">Authoring Workflows, Activities, and Expressions Using Imperative Code</span></span>](authoring-workflows-activities-and-expressions-using-imperative-code.md)
