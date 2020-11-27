---
title: 使用 ETW 进行分析跟踪
ms.date: 03/30/2017
helpviewer_keywords:
- diagnostics [WCF], analytic tracing
- administration [WCF], analytic tracing
- analytic tracing [WCF]
ms.assetid: 1d518e47-a38d-41e8-93d7-8c3b361f6a56
ms.openlocfilehash: 4bb31eeac7c5d3c8c30f66090b07de9f8af4d5a4
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96274616"
---
# <a name="analytic-tracing-with-etw"></a><span data-ttu-id="3d97c-102">使用 ETW 进行分析跟踪</span><span class="sxs-lookup"><span data-stu-id="3d97c-102">Analytic Tracing with ETW</span></span>

<span data-ttu-id="3d97c-103">Windows Communication Foundation (WCF) 分析跟踪提供一种在执行 WCF 服务的过程中捕获诊断信息的方法。</span><span class="sxs-lookup"><span data-stu-id="3d97c-103">Windows Communication Foundation (WCF) analytic tracing offers a way to capture diagnostic information during the execution of a WCF service.</span></span> <span data-ttu-id="3d97c-104">在 WCF 堆栈中的关键点处发出 WCF 分析跟踪事件，以允许在生产环境中对 WCF 服务进行故障排除。</span><span class="sxs-lookup"><span data-stu-id="3d97c-104">WCF analytic tracing events are emitted at key points in the WCF stack to allow troubleshooting of WCF services in a production environment.</span></span> <span data-ttu-id="3d97c-105">WCF 服务的分析跟踪对承载 wcf 服务的产品服务器的性能的影响最小， [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] 因为这些事件非常有效地发出到 Windows (ETW) 会话的事件跟踪。</span><span class="sxs-lookup"><span data-stu-id="3d97c-105">Analytic tracing for WCF services has minimal impact on the performance of a product server that hosts [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] WCF services as these events are very efficiently emitted to an Event Tracing for Windows (ETW) session.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3d97c-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="3d97c-106">In This Section</span></span>  

 [<span data-ttu-id="3d97c-107">分析跟踪概述</span><span class="sxs-lookup"><span data-stu-id="3d97c-107">Analytic Tracing Overview</span></span>](analytic-tracing-overview.md)  
 <span data-ttu-id="3d97c-108">讨论 WCF 分析跟踪在中的工作方式 [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="3d97c-108">Discusses how WCF analytic tracing works in [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].</span></span>  
  
 [<span data-ttu-id="3d97c-109">动态启用分析跟踪</span><span class="sxs-lookup"><span data-stu-id="3d97c-109">Dynamically Enabling Analytic Tracing</span></span>](dynamically-enabling-analytic-tracing.md)  
 <span data-ttu-id="3d97c-110">讨论如何使用 ETW 动态启用或禁用跟踪。</span><span class="sxs-lookup"><span data-stu-id="3d97c-110">Discusses how to enable or disable tracing dynamically using ETW.</span></span>  
  
 [<span data-ttu-id="3d97c-111">配置消息流跟踪</span><span class="sxs-lookup"><span data-stu-id="3d97c-111">Configuring Message Flow Tracing</span></span>](configuring-message-flow-tracing.md)  
 <span data-ttu-id="3d97c-112">描述如何配置消息流跟踪。</span><span class="sxs-lookup"><span data-stu-id="3d97c-112">Describes how to configure message flow tracing.</span></span>  
  
 [<span data-ttu-id="3d97c-113">分析跟踪事件参考</span><span class="sxs-lookup"><span data-stu-id="3d97c-113">Analytic Trace Event Reference</span></span>](analytic-trace-event-reference.md)  
 <span data-ttu-id="3d97c-114">显示一张表，其中包括事件 ID 及其事件级别、事件消息和关键字。</span><span class="sxs-lookup"><span data-stu-id="3d97c-114">Shows a table of event IDs with their event levels, event messages and keywords.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d97c-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d97c-115">See also</span></span>

- [<span data-ttu-id="3d97c-116">针对 Windows 的 WCF 服务和事件跟踪</span><span class="sxs-lookup"><span data-stu-id="3d97c-116">WCF Services and Event Tracing for Windows</span></span>](../../samples/wcf-services-and-event-tracing-for-windows.md)
- [<span data-ttu-id="3d97c-117">在 Windows 事件跟踪中跟踪事件</span><span class="sxs-lookup"><span data-stu-id="3d97c-117">Tracking Events into Event Tracing in Windows</span></span>](../../../windows-workflow-foundation/samples/tracking-events-into-event-tracing-in-windows.md)
