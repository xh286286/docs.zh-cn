---
title: 使用 Activity 类的工作流活动创作
ms.date: 03/30/2017
ms.assetid: 7b7b1c66-f093-43c3-b4d1-7173b46516da
ms.openlocfilehash: 21f1c8b1249d41029fa7a19360e96ad866c823a7
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96293840"
---
# <a name="workflow-activity-authoring-using-the-activity-class"></a><span data-ttu-id="f2090-102">使用 Activity 类的工作流活动创作</span><span class="sxs-lookup"><span data-stu-id="f2090-102">Workflow Activity Authoring Using the Activity Class</span></span>

<span data-ttu-id="f2090-103">使用 Windows Workflow Foundation (WF) 创建活动的最基本方法 [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] 是创建一个继承自的类，该类 <xref:System.Activities.Activity> 通过从 [内置活动库](net-framework-4-5-built-in-activity-library.md)中组合自定义活动或活动来创建功能。</span><span class="sxs-lookup"><span data-stu-id="f2090-103">The most basic way to create an activity using Windows Workflow Foundation (WF) in [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] is to create a class that inherits from <xref:System.Activities.Activity> that creates functionality by assembling custom activities or activities from the [Built-In Activity Library](net-framework-4-5-built-in-activity-library.md).</span></span> <span data-ttu-id="f2090-104">本主题演示如何创建向控制台写入两个消息的活动。</span><span class="sxs-lookup"><span data-stu-id="f2090-104">This topic demonstrates how to create an activity that writes two messages to the console.</span></span>

### <a name="to-create-a-custom-activity-using-the-activity-designer"></a><span data-ttu-id="f2090-105">使用活动设计器创建自定义活动</span><span class="sxs-lookup"><span data-stu-id="f2090-105">To create a custom Activity using the activity designer</span></span>

1. <span data-ttu-id="f2090-106">打开 Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="f2090-106">Open Visual Studio 2012.</span></span>

2. <span data-ttu-id="f2090-107">依次选择“文件”、“新建”和“项目”。</span><span class="sxs-lookup"><span data-stu-id="f2090-107">Select File, New, Project.</span></span> <span data-ttu-id="f2090-108">在 "**项目类型**" 窗口中的 " **Visual c #** " 下选择 " **Workflow 4.0** "，然后选择 " **v2010** " 节点。</span><span class="sxs-lookup"><span data-stu-id="f2090-108">Select **Workflow 4.0** under **Visual C#** in the **Project Types** window, and select the **v2010** node.</span></span> <span data-ttu-id="f2090-109">在 "**模板**" 窗口中选择 "**活动库**"。</span><span class="sxs-lookup"><span data-stu-id="f2090-109">Select **Activity Library** in the **Templates** window.</span></span> <span data-ttu-id="f2090-110">将新项目命名为 HelloActivity。</span><span class="sxs-lookup"><span data-stu-id="f2090-110">Name the new project HelloActivity.</span></span>

3. <span data-ttu-id="f2090-111">打开新的活动。</span><span class="sxs-lookup"><span data-stu-id="f2090-111">Open the new activity.</span></span>  <span data-ttu-id="f2090-112">将 <xref:System.Activities.Statements.Sequence> 活动从工具箱拖到设计器图面。</span><span class="sxs-lookup"><span data-stu-id="f2090-112">Drag a <xref:System.Activities.Statements.Sequence> activity from the toolbox onto the designer surface.</span></span>

4. <span data-ttu-id="f2090-113">将 <xref:System.Activities.Statements.WriteLine> 活动拖到 <xref:System.Activities.Statements.Sequence> 活动中。</span><span class="sxs-lookup"><span data-stu-id="f2090-113">Drag a <xref:System.Activities.Statements.WriteLine> activity into the <xref:System.Activities.Statements.Sequence> activity.</span></span> <span data-ttu-id="f2090-114">`"Hello World"`在 "**文本**" 字段中输入引号)  (。</span><span class="sxs-lookup"><span data-stu-id="f2090-114">Enter `"Hello World"` (with quotes) into the **Text** field.</span></span>

5. <span data-ttu-id="f2090-115">将第二个 <xref:System.Activities.Statements.WriteLine> 活动拖到 <xref:System.Activities.Statements.Sequence> 活动中并将其放置在第一个活动的下面。</span><span class="sxs-lookup"><span data-stu-id="f2090-115">Drag a second <xref:System.Activities.Statements.WriteLine> activity into the <xref:System.Activities.Statements.Sequence> activity, below the first one.</span></span> <span data-ttu-id="f2090-116">`"Goodbye"`在 "**文本**" 字段中输入引号)  (。</span><span class="sxs-lookup"><span data-stu-id="f2090-116">Enter `"Goodbye"` (with quotes) into the **Text** field.</span></span>
