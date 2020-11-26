---
title: System.ServiceModel.MessageProcessingPaused
ms.date: 03/30/2017
ms.assetid: 36b5302a-93cc-478a-9bb2-8a1601fba1df
ms.openlocfilehash: e4c8040d2350e3824b5d68dc6f32376007792a7f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96235111"
---
# <a name="systemservicemodelmessageprocessingpaused"></a><span data-ttu-id="79512-102">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="79512-102">System.ServiceModel.MessageProcessingPaused</span></span>

<span data-ttu-id="79512-103">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="79512-103">System.ServiceModel.MessageProcessingPaused</span></span>  
  
## <a name="description"></a><span data-ttu-id="79512-104">描述</span><span class="sxs-lookup"><span data-stu-id="79512-104">Description</span></span>  

 <span data-ttu-id="79512-105">线程在处理消息时切换。</span><span class="sxs-lookup"><span data-stu-id="79512-105">The threads were switched while processing a message.</span></span>  
  
 <span data-ttu-id="79512-106">消息处理可以因为以下原因而暂停：</span><span class="sxs-lookup"><span data-stu-id="79512-106">Message processing can be paused by the following reasons:</span></span>  
  
- <span data-ttu-id="79512-107">ConcurrencyMode 为 single 或 reentrant，并且服务正在处理另一条消息。</span><span class="sxs-lookup"><span data-stu-id="79512-107">ConcurrencyMode is single or reentrant, and the service is processing another message.</span></span>  
  
- <span data-ttu-id="79512-108">启用了事务，并且服务正在处理另一个事务。</span><span class="sxs-lookup"><span data-stu-id="79512-108">Transaction is enabled and the service is processing another transaction.</span></span>  
  
- <span data-ttu-id="79512-109">同步上下文不是最新。</span><span class="sxs-lookup"><span data-stu-id="79512-109">Synchronization context is not current.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79512-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79512-110">See also</span></span>

- [<span data-ttu-id="79512-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="79512-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="79512-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="79512-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="79512-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="79512-113">Administration and Diagnostics</span></span>](../index.md)
