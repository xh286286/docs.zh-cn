---
title: 1017 - ScheduleCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 864546ab-d65c-4989-8fcb-537ba03a3cdd
ms.openlocfilehash: 6aed9773aa45251075520a0f955e9d71234f1357
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275614"
---
# <a name="1017---schedulecancelactivityworkitem"></a><span data-ttu-id="9af2a-102">1017 - ScheduleCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="9af2a-102">1017 - ScheduleCancelActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="9af2a-103">属性</span><span class="sxs-lookup"><span data-stu-id="9af2a-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9af2a-104">ID</span><span class="sxs-lookup"><span data-stu-id="9af2a-104">ID</span></span>|<span data-ttu-id="9af2a-105">1017</span><span class="sxs-lookup"><span data-stu-id="9af2a-105">1017</span></span>|  
|<span data-ttu-id="9af2a-106">关键字</span><span class="sxs-lookup"><span data-stu-id="9af2a-106">Keywords</span></span>|<span data-ttu-id="9af2a-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="9af2a-107">WFRuntime</span></span>|  
|<span data-ttu-id="9af2a-108">级别</span><span class="sxs-lookup"><span data-stu-id="9af2a-108">Level</span></span>|<span data-ttu-id="9af2a-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="9af2a-109">Verbose</span></span>|  
|<span data-ttu-id="9af2a-110">通道</span><span class="sxs-lookup"><span data-stu-id="9af2a-110">Channel</span></span>|<span data-ttu-id="9af2a-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="9af2a-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9af2a-112">描述</span><span class="sxs-lookup"><span data-stu-id="9af2a-112">Description</span></span>  

 <span data-ttu-id="9af2a-113">指示已安排 CancelActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="9af2a-113">Indicates a CancelActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9af2a-114">消息</span><span class="sxs-lookup"><span data-stu-id="9af2a-114">Message</span></span>  

 <span data-ttu-id="9af2a-115">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了 CancelActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="9af2a-115">A CancelActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9af2a-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="9af2a-116">Details</span></span>  
  
|<span data-ttu-id="9af2a-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9af2a-117">Data Item Name</span></span>|<span data-ttu-id="9af2a-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9af2a-118">Data Item Type</span></span>|<span data-ttu-id="9af2a-119">描述</span><span class="sxs-lookup"><span data-stu-id="9af2a-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9af2a-120">活动</span><span class="sxs-lookup"><span data-stu-id="9af2a-120">Activity</span></span>|<span data-ttu-id="9af2a-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="9af2a-121">xs:string</span></span>|<span data-ttu-id="9af2a-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="9af2a-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="9af2a-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="9af2a-123">DisplayName</span></span>|<span data-ttu-id="9af2a-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="9af2a-124">xs:string</span></span>|<span data-ttu-id="9af2a-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="9af2a-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="9af2a-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="9af2a-126">InstanceId</span></span>|<span data-ttu-id="9af2a-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="9af2a-127">xs:string</span></span>|<span data-ttu-id="9af2a-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="9af2a-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="9af2a-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9af2a-129">AppDomain</span></span>|<span data-ttu-id="9af2a-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="9af2a-130">xs:string</span></span>|<span data-ttu-id="9af2a-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9af2a-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
