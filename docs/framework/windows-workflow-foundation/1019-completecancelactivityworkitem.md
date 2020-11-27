---
title: 1019 - CompleteCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 75a4a1ab-e5a3-4f4e-88e4-d19806e671d7
ms.openlocfilehash: 903b497fb3f244fd40c6888829ef71dddd455251
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275474"
---
# <a name="1019---completecancelactivityworkitem"></a><span data-ttu-id="7b0ce-102">1019 - CompleteCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="7b0ce-102">1019 - CompleteCancelActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="7b0ce-103">属性</span><span class="sxs-lookup"><span data-stu-id="7b0ce-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7b0ce-104">ID</span><span class="sxs-lookup"><span data-stu-id="7b0ce-104">ID</span></span>|<span data-ttu-id="7b0ce-105">1019</span><span class="sxs-lookup"><span data-stu-id="7b0ce-105">1019</span></span>|  
|<span data-ttu-id="7b0ce-106">关键字</span><span class="sxs-lookup"><span data-stu-id="7b0ce-106">Keywords</span></span>|<span data-ttu-id="7b0ce-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7b0ce-107">WFRuntime</span></span>|  
|<span data-ttu-id="7b0ce-108">级别</span><span class="sxs-lookup"><span data-stu-id="7b0ce-108">Level</span></span>|<span data-ttu-id="7b0ce-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="7b0ce-109">Verbose</span></span>|  
|<span data-ttu-id="7b0ce-110">通道</span><span class="sxs-lookup"><span data-stu-id="7b0ce-110">Channel</span></span>|<span data-ttu-id="7b0ce-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="7b0ce-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7b0ce-112">描述</span><span class="sxs-lookup"><span data-stu-id="7b0ce-112">Description</span></span>  

 <span data-ttu-id="7b0ce-113">指示 CancelActivityWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="7b0ce-113">Indicates a CancelActivityWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7b0ce-114">消息</span><span class="sxs-lookup"><span data-stu-id="7b0ce-114">Message</span></span>  

 <span data-ttu-id="7b0ce-115">Activity“%1”、DisplayName“%2”、InstanceId“%3”的 CancelActivityWorkItem 已经完成。</span><span class="sxs-lookup"><span data-stu-id="7b0ce-115">A CancelActivityWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7b0ce-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="7b0ce-116">Details</span></span>  
  
|<span data-ttu-id="7b0ce-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="7b0ce-117">Data Item Name</span></span>|<span data-ttu-id="7b0ce-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="7b0ce-118">Data Item Type</span></span>|<span data-ttu-id="7b0ce-119">描述</span><span class="sxs-lookup"><span data-stu-id="7b0ce-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7b0ce-120">活动</span><span class="sxs-lookup"><span data-stu-id="7b0ce-120">Activity</span></span>|<span data-ttu-id="7b0ce-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0ce-121">xs:string</span></span>|<span data-ttu-id="7b0ce-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="7b0ce-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="7b0ce-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b0ce-123">DisplayName</span></span>|<span data-ttu-id="7b0ce-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0ce-124">xs:string</span></span>|<span data-ttu-id="7b0ce-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="7b0ce-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="7b0ce-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="7b0ce-126">InstanceId</span></span>|<span data-ttu-id="7b0ce-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0ce-127">xs:string</span></span>|<span data-ttu-id="7b0ce-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="7b0ce-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="7b0ce-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="7b0ce-129">AppDomain</span></span>|<span data-ttu-id="7b0ce-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b0ce-130">xs:string</span></span>|<span data-ttu-id="7b0ce-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="7b0ce-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
