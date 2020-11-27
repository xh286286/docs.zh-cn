---
title: 1150 - CompensationState
ms.date: 03/30/2017
ms.assetid: eb015842-cc5a-47be-bce5-6af39e567723
ms.openlocfilehash: 2adb317521b8659c2419e4c04aabf4cf4499b36f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96285104"
---
# <a name="1150---compensationstate"></a><span data-ttu-id="cd42b-102">1150 - CompensationState</span><span class="sxs-lookup"><span data-stu-id="cd42b-102">1150 - CompensationState</span></span>

## <a name="properties"></a><span data-ttu-id="cd42b-103">属性</span><span class="sxs-lookup"><span data-stu-id="cd42b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="cd42b-104">ID</span><span class="sxs-lookup"><span data-stu-id="cd42b-104">ID</span></span>|<span data-ttu-id="cd42b-105">1150</span><span class="sxs-lookup"><span data-stu-id="cd42b-105">1150</span></span>|  
|<span data-ttu-id="cd42b-106">关键字</span><span class="sxs-lookup"><span data-stu-id="cd42b-106">Keywords</span></span>|<span data-ttu-id="cd42b-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="cd42b-107">WFActivities</span></span>|  
|<span data-ttu-id="cd42b-108">Level</span><span class="sxs-lookup"><span data-stu-id="cd42b-108">Level</span></span>|<span data-ttu-id="cd42b-109">信息</span><span class="sxs-lookup"><span data-stu-id="cd42b-109">Information</span></span>|  
|<span data-ttu-id="cd42b-110">通道</span><span class="sxs-lookup"><span data-stu-id="cd42b-110">Channel</span></span>|<span data-ttu-id="cd42b-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="cd42b-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="cd42b-112">描述</span><span class="sxs-lookup"><span data-stu-id="cd42b-112">Description</span></span>  

 <span data-ttu-id="cd42b-113">指示状态在 CompensableActivity 中发生更改。</span><span class="sxs-lookup"><span data-stu-id="cd42b-113">Indicates a change of state in a CompensableActivity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="cd42b-114">消息</span><span class="sxs-lookup"><span data-stu-id="cd42b-114">Message</span></span>  

 <span data-ttu-id="cd42b-115">CompensableActivity“%1”的状态为“%2”。</span><span class="sxs-lookup"><span data-stu-id="cd42b-115">CompensableActivity '%1' is in the '%2' state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="cd42b-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="cd42b-116">Details</span></span>  
  
|<span data-ttu-id="cd42b-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="cd42b-117">Data Item Name</span></span>|<span data-ttu-id="cd42b-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="cd42b-118">Data Item Type</span></span>|<span data-ttu-id="cd42b-119">说明</span><span class="sxs-lookup"><span data-stu-id="cd42b-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="cd42b-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd42b-120">DisplayName</span></span>|<span data-ttu-id="cd42b-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd42b-121">xs:string</span></span>|<span data-ttu-id="cd42b-122">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="cd42b-122">The display name of the activity.</span></span>|  
|<span data-ttu-id="cd42b-123">状态</span><span class="sxs-lookup"><span data-stu-id="cd42b-123">State</span></span>|<span data-ttu-id="cd42b-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd42b-124">xs:string</span></span>|<span data-ttu-id="cd42b-125">补偿状态。</span><span class="sxs-lookup"><span data-stu-id="cd42b-125">The compensation state.</span></span>|  
|<span data-ttu-id="cd42b-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="cd42b-126">AppDomain</span></span>|<span data-ttu-id="cd42b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd42b-127">xs:string</span></span>|<span data-ttu-id="cd42b-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="cd42b-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
