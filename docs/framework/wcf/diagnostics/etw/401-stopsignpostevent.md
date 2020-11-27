---
title: 401- StopSignPostEvent
ms.date: 03/30/2017
ms.assetid: e033d03a-510d-4300-aa65-ef02cb4807f2
ms.openlocfilehash: e549a8aabd0a54022000515050cde19dc4f20dd3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294061"
---
# <a name="401--stopsignpostevent"></a><span data-ttu-id="7aa74-102">401- StopSignPostEvent</span><span class="sxs-lookup"><span data-stu-id="7aa74-102">401- StopSignPostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="7aa74-103">属性</span><span class="sxs-lookup"><span data-stu-id="7aa74-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7aa74-104">ID</span><span class="sxs-lookup"><span data-stu-id="7aa74-104">ID</span></span>|<span data-ttu-id="7aa74-105">401</span><span class="sxs-lookup"><span data-stu-id="7aa74-105">401</span></span>|  
|<span data-ttu-id="7aa74-106">关键字</span><span class="sxs-lookup"><span data-stu-id="7aa74-106">Keywords</span></span>|<span data-ttu-id="7aa74-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="7aa74-107">Troubleshooting</span></span>|  
|<span data-ttu-id="7aa74-108">Level</span><span class="sxs-lookup"><span data-stu-id="7aa74-108">Level</span></span>|<span data-ttu-id="7aa74-109">信息</span><span class="sxs-lookup"><span data-stu-id="7aa74-109">Information</span></span>|  
|<span data-ttu-id="7aa74-110">通道</span><span class="sxs-lookup"><span data-stu-id="7aa74-110">Channel</span></span>|<span data-ttu-id="7aa74-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="7aa74-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7aa74-112">描述</span><span class="sxs-lookup"><span data-stu-id="7aa74-112">Description</span></span>  

 <span data-ttu-id="7aa74-113">此事件标记端对端活动的结束，</span><span class="sxs-lookup"><span data-stu-id="7aa74-113">This event marks the end of an end-to-end activity.</span></span> <span data-ttu-id="7aa74-114">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="7aa74-114">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7aa74-115">消息</span><span class="sxs-lookup"><span data-stu-id="7aa74-115">Message</span></span>  

 <span data-ttu-id="7aa74-116">活动边界。</span><span class="sxs-lookup"><span data-stu-id="7aa74-116">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7aa74-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="7aa74-117">Details</span></span>  
  
|<span data-ttu-id="7aa74-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="7aa74-118">Data Item Name</span></span>|<span data-ttu-id="7aa74-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="7aa74-119">Data Item Type</span></span>|<span data-ttu-id="7aa74-120">描述</span><span class="sxs-lookup"><span data-stu-id="7aa74-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7aa74-121">扩展数据</span><span class="sxs-lookup"><span data-stu-id="7aa74-121">Extended Data</span></span>|`xs:string`|<span data-ttu-id="7aa74-122">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="7aa74-122">The name of the activity.</span></span>|  
|<span data-ttu-id="7aa74-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="7aa74-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="7aa74-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="7aa74-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
