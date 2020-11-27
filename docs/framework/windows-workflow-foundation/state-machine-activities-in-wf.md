---
title: WF 中的状态机活动
ms.date: 03/30/2017
ms.assetid: 93312eaf-07e0-4a55-b4f7-4cdbbc4dee2d
ms.openlocfilehash: dd0bfae1f24ecd9f98c0a2f04265581f880202a7
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96261717"
---
# <a name="state-machine-activities-in-wf"></a><span data-ttu-id="8a197-102">WF 中的状态机活动</span><span class="sxs-lookup"><span data-stu-id="8a197-102">State Machine Activities in WF</span></span>

<span data-ttu-id="8a197-103">.NET Framework 4.5 提供多个系统提供的活动和活动设计器，用于创建状态机工作流。</span><span class="sxs-lookup"><span data-stu-id="8a197-103">.NET Framework 4.5 provides several system-provided activities and activity designers for creating state machine workflows.</span></span>  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.StateMachine>|<span data-ttu-id="8a197-104">使用熟悉的状态机范例执行包含的活动。</span><span class="sxs-lookup"><span data-stu-id="8a197-104">Executes contained activities using the familiar state machine paradigm.</span></span>|  
|<xref:System.Activities.Statements.State>|<span data-ttu-id="8a197-105">代表状态机中的状态。</span><span class="sxs-lookup"><span data-stu-id="8a197-105">Represents a state in a state machine.</span></span>|  
|<xref:System.Activities.Core.Presentation.FinalState>|<span data-ttu-id="8a197-106">表示状态机中的终止状态。</span><span class="sxs-lookup"><span data-stu-id="8a197-106">Represents a terminating state in a state machine.</span></span> <span data-ttu-id="8a197-107"><xref:System.Activities.Core.Presentation.FinalState> 是在创建预配置为终止状态的 <xref:System.Activities.Statements.State> 时所使用的活动设计器。</span><span class="sxs-lookup"><span data-stu-id="8a197-107"><xref:System.Activities.Core.Presentation.FinalState> is an activity designer that when used creates a <xref:System.Activities.Statements.State> preconfigured as a terminating state.</span></span> <span data-ttu-id="8a197-108">有关详细信息，请参阅 [FinalState 活动设计器](/visualstudio/workflow-designer/finalstate-activity-designer)。</span><span class="sxs-lookup"><span data-stu-id="8a197-108">For more information, see [FinalState Activity Designer](/visualstudio/workflow-designer/finalstate-activity-designer).</span></span>|  
|<xref:System.Activities.Statements.Transition>|<span data-ttu-id="8a197-109">表示两个状态间的转换。</span><span class="sxs-lookup"><span data-stu-id="8a197-109">Represents the transition between two states.</span></span> <span data-ttu-id="8a197-110">没有用于的 **工具箱** 项 <xref:System.Activities.Statements.Transition> ; 通过在两个状态之间拖放线条，或在一个状态悬停在另一个状态上时，在工作流设计器上创建转换。</span><span class="sxs-lookup"><span data-stu-id="8a197-110">There is no **Toolbox** item for <xref:System.Activities.Statements.Transition>; transitions are created on the workflow designer by dragging and dropping a line between two states, or by dropping a state on the triangles that appear when one state is hovered over another.</span></span> <span data-ttu-id="8a197-111">有关详细信息，请参阅 [转变活动设计器](/visualstudio/workflow-designer/transition-activity-designer)。</span><span class="sxs-lookup"><span data-stu-id="8a197-111">For more information, see [Transition Activity Designer](/visualstudio/workflow-designer/transition-activity-designer).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8a197-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a197-112">See also</span></span>

- [<span data-ttu-id="8a197-113">入门教程</span><span class="sxs-lookup"><span data-stu-id="8a197-113">Getting Started Tutorial</span></span>](getting-started-tutorial.md)
