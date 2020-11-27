---
title: 1026 - ScheduleTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 0d5f86ba-ec21-4129-a726-5432e425384c
ms.openlocfilehash: 7ba2ada1fbd5217592b4e4e3cffd813ffbe978ac
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275240"
---
# <a name="1026---scheduletransactioncontextworkitem"></a><span data-ttu-id="ed137-102">1026 - ScheduleTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="ed137-102">1026 - ScheduleTransactionContextWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="ed137-103">属性</span><span class="sxs-lookup"><span data-stu-id="ed137-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ed137-104">ID</span><span class="sxs-lookup"><span data-stu-id="ed137-104">ID</span></span>|<span data-ttu-id="ed137-105">1026</span><span class="sxs-lookup"><span data-stu-id="ed137-105">1026</span></span>|  
|<span data-ttu-id="ed137-106">关键字</span><span class="sxs-lookup"><span data-stu-id="ed137-106">Keywords</span></span>|<span data-ttu-id="ed137-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ed137-107">WFRuntime</span></span>|  
|<span data-ttu-id="ed137-108">级别</span><span class="sxs-lookup"><span data-stu-id="ed137-108">Level</span></span>|<span data-ttu-id="ed137-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="ed137-109">Verbose</span></span>|  
|<span data-ttu-id="ed137-110">通道</span><span class="sxs-lookup"><span data-stu-id="ed137-110">Channel</span></span>|<span data-ttu-id="ed137-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="ed137-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ed137-112">描述</span><span class="sxs-lookup"><span data-stu-id="ed137-112">Description</span></span>  

 <span data-ttu-id="ed137-113">指示已安排 TransactionContextWorkItem。</span><span class="sxs-lookup"><span data-stu-id="ed137-113">Indicates a TransactionContextWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ed137-114">消息</span><span class="sxs-lookup"><span data-stu-id="ed137-114">Message</span></span>  

 <span data-ttu-id="ed137-115">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了 TransactionContextWorkItem。</span><span class="sxs-lookup"><span data-stu-id="ed137-115">A TransactionContextWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ed137-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="ed137-116">Details</span></span>  
  
|<span data-ttu-id="ed137-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="ed137-117">Data Item Name</span></span>|<span data-ttu-id="ed137-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="ed137-118">Data Item Type</span></span>|<span data-ttu-id="ed137-119">描述</span><span class="sxs-lookup"><span data-stu-id="ed137-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ed137-120">活动</span><span class="sxs-lookup"><span data-stu-id="ed137-120">Activity</span></span>|<span data-ttu-id="ed137-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ed137-121">xs:string</span></span>|<span data-ttu-id="ed137-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="ed137-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="ed137-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed137-123">DisplayName</span></span>|<span data-ttu-id="ed137-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="ed137-124">xs:string</span></span>|<span data-ttu-id="ed137-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ed137-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="ed137-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="ed137-126">InstanceId</span></span>|<span data-ttu-id="ed137-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="ed137-127">xs:string</span></span>|<span data-ttu-id="ed137-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="ed137-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="ed137-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="ed137-129">AppDomain</span></span>|<span data-ttu-id="ed137-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="ed137-130">xs:string</span></span>|<span data-ttu-id="ed137-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="ed137-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
