---
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: d4fbbeaaa1daeea62b5495d0b30c37d0297ccd75
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96249912"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a><span data-ttu-id="dbf68-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span><span class="sxs-lookup"><span data-stu-id="dbf68-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span></span>

<span data-ttu-id="dbf68-103">消息的入站接收速率过高。</span><span class="sxs-lookup"><span data-stu-id="dbf68-103">The inbound receive rate of messages is too high.</span></span>  
  
## <a name="description"></a><span data-ttu-id="dbf68-104">描述</span><span class="sxs-lookup"><span data-stu-id="dbf68-104">Description</span></span>  

 <span data-ttu-id="dbf68-105">此跟踪在尝试处理入站消息时发生。</span><span class="sxs-lookup"><span data-stu-id="dbf68-105">This trace occurs when attempting to process inbound messages.</span></span> <span data-ttu-id="dbf68-106">无法将消息转发给特定的邻居，因为已经超过了为该邻居设置的配额。</span><span class="sxs-lookup"><span data-stu-id="dbf68-106">A message could not be forwarded to a specific neighbor because the quota set for that neighbor has been exceeded.</span></span> <span data-ttu-id="dbf68-107">当无响应邻居无法清除为该邻居挂起的积压工作 (backlog) 消息时会发生此情况。</span><span class="sxs-lookup"><span data-stu-id="dbf68-107">This occurs when an unresponsive neighbor fails to clear a backlog of messages pending for that neighbor.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="dbf68-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="dbf68-108">Troubleshooting</span></span>  

 <span data-ttu-id="dbf68-109">降低在网格中发送消息的速率。</span><span class="sxs-lookup"><span data-stu-id="dbf68-109">Reduce the rate at which messages are sent within the mesh.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbf68-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbf68-110">See also</span></span>

- [<span data-ttu-id="dbf68-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="dbf68-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="dbf68-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="dbf68-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="dbf68-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="dbf68-113">Administration and Diagnostics</span></span>](../index.md)
