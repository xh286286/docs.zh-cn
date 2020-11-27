---
title: 3552 - MaxPendingMessagesPerChannelExceeded
ms.date: 03/30/2017
ms.assetid: fc8309d9-eb3a-4636-a6f0-dd0018c1361d
ms.openlocfilehash: bd3e7539922e6c430c4ffe5bd96ef1ac7dbd098f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96261158"
---
# <a name="3552---maxpendingmessagesperchannelexceeded"></a><span data-ttu-id="9c1e5-102">3552 - MaxPendingMessagesPerChannelExceeded</span><span class="sxs-lookup"><span data-stu-id="9c1e5-102">3552 - MaxPendingMessagesPerChannelExceeded</span></span>

## <a name="properties"></a><span data-ttu-id="9c1e5-103">属性</span><span class="sxs-lookup"><span data-stu-id="9c1e5-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9c1e5-104">ID</span><span class="sxs-lookup"><span data-stu-id="9c1e5-104">ID</span></span>|<span data-ttu-id="9c1e5-105">3552</span><span class="sxs-lookup"><span data-stu-id="9c1e5-105">3552</span></span>|  
|<span data-ttu-id="9c1e5-106">关键字</span><span class="sxs-lookup"><span data-stu-id="9c1e5-106">Keywords</span></span>|<span data-ttu-id="9c1e5-107">配额、WFServices</span><span class="sxs-lookup"><span data-stu-id="9c1e5-107">Quota, WFServices</span></span>|  
|<span data-ttu-id="9c1e5-108">Level</span><span class="sxs-lookup"><span data-stu-id="9c1e5-108">Level</span></span>|<span data-ttu-id="9c1e5-109">警告</span><span class="sxs-lookup"><span data-stu-id="9c1e5-109">Warning</span></span>|  
|<span data-ttu-id="9c1e5-110">通道</span><span class="sxs-lookup"><span data-stu-id="9c1e5-110">Channel</span></span>|<span data-ttu-id="9c1e5-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="9c1e5-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9c1e5-112">描述</span><span class="sxs-lookup"><span data-stu-id="9c1e5-112">Description</span></span>  

 <span data-ttu-id="9c1e5-113">指示达到了中止值“MaxPendingMessagesPerChannel”。</span><span class="sxs-lookup"><span data-stu-id="9c1e5-113">Indicates the throttle 'MaxPendingMessagesPerChannel' limit was hit.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9c1e5-114">消息</span><span class="sxs-lookup"><span data-stu-id="9c1e5-114">Message</span></span>  

 <span data-ttu-id="9c1e5-115">达到了“%1”的中止值“MaxPendingMessagesPerChannel”。</span><span class="sxs-lookup"><span data-stu-id="9c1e5-115">The throttle 'MaxPendingMessagesPerChannel' limit of  '%1' was hit.</span></span> <span data-ttu-id="9c1e5-116">若要增加此限制，请调整 BufferedReceiveServiceBehavior 中的 MaxPendingMessagesPerChannel 属性。</span><span class="sxs-lookup"><span data-stu-id="9c1e5-116">To increase this limit, adjust the MaxPendingMessagesPerChannel property on BufferedReceiveServiceBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9c1e5-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="9c1e5-117">Details</span></span>  
  
|<span data-ttu-id="9c1e5-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9c1e5-118">Data Item Name</span></span>|<span data-ttu-id="9c1e5-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9c1e5-119">Data Item Type</span></span>|<span data-ttu-id="9c1e5-120">描述</span><span class="sxs-lookup"><span data-stu-id="9c1e5-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9c1e5-121">限制</span><span class="sxs-lookup"><span data-stu-id="9c1e5-121">Limit</span></span>|<span data-ttu-id="9c1e5-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="9c1e5-122">xs:string</span></span>|<span data-ttu-id="9c1e5-123">中止值 MaxPendingMessagesPerChannel。</span><span class="sxs-lookup"><span data-stu-id="9c1e5-123">The limit of the MaxPendingMessagesPerChannel throttle.</span></span>|  
|<span data-ttu-id="9c1e5-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9c1e5-124">AppDomain</span></span>|<span data-ttu-id="9c1e5-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="9c1e5-125">xs:string</span></span>|<span data-ttu-id="9c1e5-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9c1e5-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
