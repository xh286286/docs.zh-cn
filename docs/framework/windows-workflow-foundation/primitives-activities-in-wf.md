---
title: WF 中的基元活动
ms.date: 03/30/2017
ms.assetid: 8e9009d1-236e-4d8e-86fc-e43132bf6dfc
ms.openlocfilehash: 4f2c20c109d67a35ccc9c363c0a3631922161d2c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96246070"
---
# <a name="primitives-activities-in-wf"></a><span data-ttu-id="27186-102">WF 中的基元活动</span><span class="sxs-lookup"><span data-stu-id="27186-102">Primitives Activities in WF</span></span>

[!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] <span data-ttu-id="27186-103">提供了多个系统提供的活动，这些活动提供了一个用于执行常规任务的方便机制。</span><span class="sxs-lookup"><span data-stu-id="27186-103">provides several system-provided activities that provide a convenient mechanism for performing common tasks.</span></span>  
  
|<span data-ttu-id="27186-104">活动</span><span class="sxs-lookup"><span data-stu-id="27186-104">Activity</span></span>|<span data-ttu-id="27186-105">说明</span><span class="sxs-lookup"><span data-stu-id="27186-105">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.Activities.Statements.Assign>|<span data-ttu-id="27186-106">将值分配给当前范围中的变量。</span><span class="sxs-lookup"><span data-stu-id="27186-106">Assigns a value to a variable at the current scope.</span></span>|  
|<xref:System.Activities.Statements.Delay>|<span data-ttu-id="27186-107">将一个执行路径置于空闲状态，可能允许卸载工作流。</span><span class="sxs-lookup"><span data-stu-id="27186-107">Puts one path of execution into an idle state, possibly allowing the workflow to be unloaded.</span></span>|  
|<xref:System.Activities.Statements.InvokeDelegate>|<span data-ttu-id="27186-108">执行派生自 <xref:System.Activities.ActivityDelegate> 的委托并且作为属性公开。</span><span class="sxs-lookup"><span data-stu-id="27186-108">Executes a delegate that derives from <xref:System.Activities.ActivityDelegate> and is exposed as a property.</span></span>|  
|<xref:System.Activities.Statements.InvokeMethod>|<span data-ttu-id="27186-109">执行 CLR 对象的公共方法。</span><span class="sxs-lookup"><span data-stu-id="27186-109">Executes a public method of a CLR object.</span></span>|  
|<xref:System.Activities.Statements.WriteLine>|<span data-ttu-id="27186-110">将指定的字符串写入控制台或指定的 <xref:System.IO.TextWriter> 对象。</span><span class="sxs-lookup"><span data-stu-id="27186-110">Writes a specified string to the console or a specified <xref:System.IO.TextWriter> object.</span></span>|
