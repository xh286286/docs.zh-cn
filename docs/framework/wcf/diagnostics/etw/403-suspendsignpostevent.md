---
title: 403 - SuspendSignpostEvent
ms.date: 03/30/2017
ms.assetid: fb2e6f29-e556-47b4-b4c1-acd6b8879702
ms.openlocfilehash: 66251141cdf66c18ad0c1334f6f3e6c0629b4b33
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96241052"
---
# <a name="403---suspendsignpostevent"></a><span data-ttu-id="7cf6f-102">403 - SuspendSignpostEvent</span><span class="sxs-lookup"><span data-stu-id="7cf6f-102">403 - SuspendSignpostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="7cf6f-103">属性</span><span class="sxs-lookup"><span data-stu-id="7cf6f-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7cf6f-104">ID</span><span class="sxs-lookup"><span data-stu-id="7cf6f-104">ID</span></span>|<span data-ttu-id="7cf6f-105">403</span><span class="sxs-lookup"><span data-stu-id="7cf6f-105">403</span></span>|  
|<span data-ttu-id="7cf6f-106">关键字</span><span class="sxs-lookup"><span data-stu-id="7cf6f-106">Keywords</span></span>|<span data-ttu-id="7cf6f-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="7cf6f-107">Troubleshooting</span></span>|  
|<span data-ttu-id="7cf6f-108">Level</span><span class="sxs-lookup"><span data-stu-id="7cf6f-108">Level</span></span>|<span data-ttu-id="7cf6f-109">信息</span><span class="sxs-lookup"><span data-stu-id="7cf6f-109">Information</span></span>|  
|<span data-ttu-id="7cf6f-110">通道</span><span class="sxs-lookup"><span data-stu-id="7cf6f-110">Channel</span></span>|<span data-ttu-id="7cf6f-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="7cf6f-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7cf6f-112">描述</span><span class="sxs-lookup"><span data-stu-id="7cf6f-112">Description</span></span>  

 <span data-ttu-id="7cf6f-113">此事件标记端对端活动的挂起，</span><span class="sxs-lookup"><span data-stu-id="7cf6f-113">This event marks the suspension of an end-to-end activity.</span></span> <span data-ttu-id="7cf6f-114">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="7cf6f-114">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7cf6f-115">消息</span><span class="sxs-lookup"><span data-stu-id="7cf6f-115">Message</span></span>  

 <span data-ttu-id="7cf6f-116">活动边界。</span><span class="sxs-lookup"><span data-stu-id="7cf6f-116">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7cf6f-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="7cf6f-117">Details</span></span>  
  
|<span data-ttu-id="7cf6f-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="7cf6f-118">Data Item Name</span></span>|<span data-ttu-id="7cf6f-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="7cf6f-119">Data Item Type</span></span>|<span data-ttu-id="7cf6f-120">描述</span><span class="sxs-lookup"><span data-stu-id="7cf6f-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7cf6f-121">扩展数据</span><span class="sxs-lookup"><span data-stu-id="7cf6f-121">Extended Data</span></span>|`xs:string`|<span data-ttu-id="7cf6f-122">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="7cf6f-122">The name of the activity.</span></span>|  
|<span data-ttu-id="7cf6f-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="7cf6f-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="7cf6f-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="7cf6f-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
