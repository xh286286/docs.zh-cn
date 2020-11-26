---
title: MSMQ
ms.date: 03/30/2017
ms.assetid: d9fca29f-fa44-4ec4-bb48-b10800694500
ms.openlocfilehash: 7ef31a188e1564da47ea1e7323cdd4cd5ef5be60
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96236671"
---
# <a name="msmq"></a><span data-ttu-id="83b7c-102">MSMQ</span><span class="sxs-lookup"><span data-stu-id="83b7c-102">MSMQ</span></span>

<span data-ttu-id="83b7c-103">在 MSMQ 应用程序中，不会在 MSMQ 与队列通道之间传输任何额外活动。</span><span class="sxs-lookup"><span data-stu-id="83b7c-103">In an MSMQ application, no additional activity is transferred from the queued channel to MSMQ and from MSMQ to the queued channel.</span></span>  
  
 <span data-ttu-id="83b7c-104">另外，在执行 Send（发送）操作和 Receive（接收）操作时，还将 MSMQ 消息 ID 和 SOAP 消息 ID（连同活动 ID，如果存在）</span><span class="sxs-lookup"><span data-stu-id="83b7c-104">In addition, MSMQ Message ID and SOAP message ID (along with Activity ID, if one exists) are traced as part of queued channel traces on a Send operation.</span></span>  
  
 <span data-ttu-id="83b7c-105">作为队列通道跟踪的一部分来跟踪。</span><span class="sxs-lookup"><span data-stu-id="83b7c-105">MSMQ Message ID and SOAP message ID (along with activity ID, if one exists) are traced as part of queued channel traces on a Receive operation.</span></span>  
  
 <span data-ttu-id="83b7c-106">接收操作所需的传输的执行方式类似于任何其他传输 (接收字节->处理消息 > 操作) 。</span><span class="sxs-lookup"><span data-stu-id="83b7c-106">The required transfers on the Receive operation are executed similarly to any other transport (receive bytes->Process message-> operation).</span></span>
