---
title: 部分信任
ms.date: 03/30/2017
ms.assetid: 489b1587-9909-4d0e-8c1a-5e83c8f8292b
ms.openlocfilehash: 844fa65bbb2858fc961091614ba581265bc08be5
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96247962"
---
# <a name="partial-trust"></a><span data-ttu-id="2fc53-102">部分信任</span><span class="sxs-lookup"><span data-stu-id="2fc53-102">Partial Trust</span></span>

<span data-ttu-id="2fc53-103">从 .NET Framework 3.5 开始，部分受信任的调用方可以访问在、和中实现的公共类型和方法 <xref:System.ServiceModel> <xref:System.Runtime.Serialization> <xref:System.ServiceModel.Web> 。</span><span class="sxs-lookup"><span data-stu-id="2fc53-103">Starting with the .NET Framework 3.5, partially trusted callers can access public types and methods implemented in <xref:System.ServiceModel>, <xref:System.Runtime.Serialization>, and <xref:System.ServiceModel.Web>.</span></span> <span data-ttu-id="2fc53-104">本部分介绍了在部分受信任的应用程序中使用 Windows Communication Foundation (WCF) 的受支持方案，以及使用降低了代码访问安全 (CA) 权限的应用程序可使用的 WCF 功能的有限子集。</span><span class="sxs-lookup"><span data-stu-id="2fc53-104">This section describes supported scenarios for using Windows Communication Foundation (WCF) within a partially trusted application as well as the limited subset of WCF functionality available to applications running with reduced code access security (CAS) permissions.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2fc53-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="2fc53-105">In This Section</span></span>  

 [<span data-ttu-id="2fc53-106">支持的部署方案</span><span class="sxs-lookup"><span data-stu-id="2fc53-106">Supported Deployment Scenarios</span></span>](supported-deployment-scenarios.md)  
 <span data-ttu-id="2fc53-107">介绍运行 WCF 的主要部分信任方案。</span><span class="sxs-lookup"><span data-stu-id="2fc53-107">Describes the main partial trust scenarios for running WCF.</span></span>  
  
 [<span data-ttu-id="2fc53-108">部分信任功能兼容性</span><span class="sxs-lookup"><span data-stu-id="2fc53-108">Partial Trust Feature Compatibility</span></span>](partial-trust-feature-compatibility.md)  
 <span data-ttu-id="2fc53-109">介绍不能用于部分信任的 WCF 功能。</span><span class="sxs-lookup"><span data-stu-id="2fc53-109">Describes the WCF features that cannot be used with partial trust.</span></span>  
  
 [<span data-ttu-id="2fc53-110">部分信任最佳实践</span><span class="sxs-lookup"><span data-stu-id="2fc53-110">Partial Trust Best Practices</span></span>](partial-trust-best-practices.md)  
 <span data-ttu-id="2fc53-111">包含在部分受信任的应用程序中使用 WCF 的最佳实践。</span><span class="sxs-lookup"><span data-stu-id="2fc53-111">Contains best practices for using WCF in partially trusted applications.</span></span>
