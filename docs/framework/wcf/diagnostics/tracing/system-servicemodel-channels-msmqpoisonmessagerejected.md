---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: 69da35f65e04a3cba15885c4fe6e57d63762cb1c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96260339"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a><span data-ttu-id="6fe3d-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span><span class="sxs-lookup"><span data-stu-id="6fe3d-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span></span>

<span data-ttu-id="6fe3d-103">拒绝的病毒消息。</span><span class="sxs-lookup"><span data-stu-id="6fe3d-103">Poison message rejected.</span></span>  
  
## <a name="description"></a><span data-ttu-id="6fe3d-104">描述</span><span class="sxs-lookup"><span data-stu-id="6fe3d-104">Description</span></span>  

 <span data-ttu-id="6fe3d-105">该跟踪指示遇到病毒消息并随后将其拒绝。</span><span class="sxs-lookup"><span data-stu-id="6fe3d-105">The trace indicates that a poison message was encountered and subsequently rejected.</span></span> <span data-ttu-id="6fe3d-106">当 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 属性设置为 `Reject` 时，将会出现此情况。</span><span class="sxs-lookup"><span data-stu-id="6fe3d-106">This occurs when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="6fe3d-107">拒绝的消息将传递回发送方的 [死信队列](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md)。</span><span class="sxs-lookup"><span data-stu-id="6fe3d-107">A rejected message is delivered back to the sender’s [Dead-Letter Queue](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md).</span></span>  
  
 <span data-ttu-id="6fe3d-108">若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="6fe3d-108">For more information on when messages become poison and how to configure your service to handle them appropriately, see [Poison-Message Handling](../../feature-details/poison-message-handling.md).</span></span> <span data-ttu-id="6fe3d-109">有关 MSMQ 中的拒绝消息的含义的详细信息，请参阅 [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6fe3d-109">For more information on what a rejected message means in MSMQ, see [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fe3d-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6fe3d-110">See also</span></span>

- [<span data-ttu-id="6fe3d-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="6fe3d-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="6fe3d-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="6fe3d-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="6fe3d-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="6fe3d-113">Administration and Diagnostics</span></span>](../index.md)
- [<span data-ttu-id="6fe3d-114">病毒消息处理</span><span class="sxs-lookup"><span data-stu-id="6fe3d-114">Poison-Message Handling</span></span>](../../feature-details/poison-message-handling.md)
- <span data-ttu-id="6fe3d-115">[MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6fe3d-115">[MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))</span></span>
