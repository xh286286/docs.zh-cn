---
title: System.ServiceModel.Channels.ConnectionPoolCloseException
ms.date: 03/30/2017
ms.assetid: 8358898e-129e-4fac-a6bf-bf3aa4293ae2
ms.openlocfilehash: d8edb8e916578247e62e3a3eb3b11b80f93416cd
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96286950"
---
# <a name="systemservicemodelchannelsconnectionpoolcloseexception"></a><span data-ttu-id="2d25a-102">System.ServiceModel.Channels.ConnectionPoolCloseException</span><span class="sxs-lookup"><span data-stu-id="2d25a-102">System.ServiceModel.Channels.ConnectionPoolCloseException</span></span>

<span data-ttu-id="2d25a-103">关闭此连接池中的连接时发生异常。</span><span class="sxs-lookup"><span data-stu-id="2d25a-103">An exception occurred while closing the connections in this connection pool.</span></span>  
  
## <a name="description"></a><span data-ttu-id="2d25a-104">描述</span><span class="sxs-lookup"><span data-stu-id="2d25a-104">Description</span></span>  

 <span data-ttu-id="2d25a-105">此错误级别跟踪表明关闭 Windows Communication Foundation (WCF) 的连接池功能所使用的连接池时出错。</span><span class="sxs-lookup"><span data-stu-id="2d25a-105">This error level trace indicates that an error has occurred while closing the connection pools used by Windows Communication Foundation (WCF)’s connection pooling feature.</span></span> <span data-ttu-id="2d25a-106">一种可能的原因是一个池连接或一组池连接在 CloseTimeout 内未成功关闭。</span><span class="sxs-lookup"><span data-stu-id="2d25a-106">One possible reason for this is an unsuccessful closure of a pooled connection, or a set of pooled connections within the CloseTimeout.</span></span> <span data-ttu-id="2d25a-107">当引发此异常时，将中止该池内所有剩余的未关闭连接，并放弃其他池内的未关闭连接。</span><span class="sxs-lookup"><span data-stu-id="2d25a-107">When this exception is thrown, any remaining unclosed connections within that pool are aborted; unclosed connections within other pools are abandoned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d25a-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d25a-108">See also</span></span>

- [<span data-ttu-id="2d25a-109">跟踪</span><span class="sxs-lookup"><span data-stu-id="2d25a-109">Tracing</span></span>](index.md)
- [<span data-ttu-id="2d25a-110">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="2d25a-110">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="2d25a-111">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="2d25a-111">Administration and Diagnostics</span></span>](../index.md)
