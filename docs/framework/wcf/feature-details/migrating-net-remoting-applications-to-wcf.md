---
title: 将 .NET 远程处理应用程序迁移到 WCF
ms.date: 03/30/2017
helpviewer_keywords:
- ',NET remoting [WCF]'
ms.assetid: 24793465-65ae-4308-8c12-dce4fd12a583
ms.openlocfilehash: 2cfaebd064d10e5b331412d177929ecb20117a07
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96248209"
---
# <a name="migrating-net-remoting-applications-to-wcf"></a><span data-ttu-id="6b79a-102">将 .NET 远程处理应用程序迁移到 WCF</span><span class="sxs-lookup"><span data-stu-id="6b79a-102">Migrating .NET Remoting Applications to WCF</span></span>

<span data-ttu-id="6b79a-103">**本主题特定于旧技术，保留该技术是为了向后兼容现有应用程序，不建议用于新的开发。现在应使用 WCF 开发分布式应用程序。**</span><span class="sxs-lookup"><span data-stu-id="6b79a-103">**This topic is specific to a legacy technology that is retained for backward compatibility with existing applications and is not recommended for new development. Distributed applications should now be developed using WCF.**</span></span>  
  
 <span data-ttu-id="6b79a-104">可以通过两种方法来利用 WCF 和现有的 .NET 远程处理应用程序：集成和迁移。</span><span class="sxs-lookup"><span data-stu-id="6b79a-104">There are two ways to take advantage of WCF with existing .NET Remoting applications: integration and migration.</span></span> <span data-ttu-id="6b79a-105">集成使你能够并行运行 .NET 远程处理2.0 和 WCF，使你可以同时在这两种技术上公开相同的业务对象，而无需修改现有的 .NET 远程处理2.0 代码。</span><span class="sxs-lookup"><span data-stu-id="6b79a-105">Integration allows you to have .NET Remoting 2.0 and WCF running side by side, letting you expose the same business objects over both technologies simultaneously without having to modify your existing .NET Remoting 2.0 code.</span></span> <span data-ttu-id="6b79a-106">集成要求在 .NET Framework 2.0 或更高版本上运行。</span><span class="sxs-lookup"><span data-stu-id="6b79a-106">Integration requires that you are running on .NET Framework 2.0 or greater.</span></span> <span data-ttu-id="6b79a-107">如果你想要利用 WCF 功能，并且不需要与远程处理2.0 系统之间的网络兼容性，则可以将整个服务迁移到 WCF。</span><span class="sxs-lookup"><span data-stu-id="6b79a-107">If you want to take advantage of WCF features and do not need wire compatibility with Remoting 2.0 systems, you can migrate your entire service to WCF.</span></span> <span data-ttu-id="6b79a-108">从 .NET 远程处理2.0 迁移到 WCF 需要更改远程对象的接口及其配置设置。</span><span class="sxs-lookup"><span data-stu-id="6b79a-108">Migration from .NET Remoting 2.0 to WCF requires changes to the remote object's interface and its configuration settings.</span></span> <span data-ttu-id="6b79a-109">[从远程处理到 Windows Communication Foundation](/previous-versions/aa730857(v=vs.80))中介绍了这两个主题。</span><span class="sxs-lookup"><span data-stu-id="6b79a-109">Both of these topics are covered in [From Remoting to the Windows Communication Foundation](/previous-versions/aa730857(v=vs.80)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b79a-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6b79a-110">See also</span></span>

- [<span data-ttu-id="6b79a-111">概念性概述</span><span class="sxs-lookup"><span data-stu-id="6b79a-111">Conceptual Overview</span></span>](../conceptual-overview.md)
