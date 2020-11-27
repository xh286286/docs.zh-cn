---
title: 1027 - StartTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 116ae5ec-b9d5-4231-824e-270d00eea7b8
ms.openlocfilehash: cb5671ce7a30a7096104ba0ca6c4f36bed6b93f9
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275227"
---
# <a name="1027---starttransactioncontextworkitem"></a><span data-ttu-id="ab4d9-102">1027 - StartTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="ab4d9-102">1027 - StartTransactionContextWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="ab4d9-103">属性</span><span class="sxs-lookup"><span data-stu-id="ab4d9-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ab4d9-104">ID</span><span class="sxs-lookup"><span data-stu-id="ab4d9-104">ID</span></span>|<span data-ttu-id="ab4d9-105">1027</span><span class="sxs-lookup"><span data-stu-id="ab4d9-105">1027</span></span>|  
|<span data-ttu-id="ab4d9-106">关键字</span><span class="sxs-lookup"><span data-stu-id="ab4d9-106">Keywords</span></span>|<span data-ttu-id="ab4d9-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ab4d9-107">WFRuntime</span></span>|  
|<span data-ttu-id="ab4d9-108">级别</span><span class="sxs-lookup"><span data-stu-id="ab4d9-108">Level</span></span>|<span data-ttu-id="ab4d9-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="ab4d9-109">Verbose</span></span>|  
|<span data-ttu-id="ab4d9-110">通道</span><span class="sxs-lookup"><span data-stu-id="ab4d9-110">Channel</span></span>|<span data-ttu-id="ab4d9-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="ab4d9-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ab4d9-112">描述</span><span class="sxs-lookup"><span data-stu-id="ab4d9-112">Description</span></span>  

 <span data-ttu-id="ab4d9-113">指示 TransactionContextWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="ab4d9-113">Indicates a TransactionContextWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ab4d9-114">消息</span><span class="sxs-lookup"><span data-stu-id="ab4d9-114">Message</span></span>  

 <span data-ttu-id="ab4d9-115">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行 TransactionContextWorkItem。</span><span class="sxs-lookup"><span data-stu-id="ab4d9-115">Starting execution of a TransactionContextWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ab4d9-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="ab4d9-116">Details</span></span>  
  
|<span data-ttu-id="ab4d9-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="ab4d9-117">Data Item Name</span></span>|<span data-ttu-id="ab4d9-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="ab4d9-118">Data Item Type</span></span>|<span data-ttu-id="ab4d9-119">描述</span><span class="sxs-lookup"><span data-stu-id="ab4d9-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ab4d9-120">活动</span><span class="sxs-lookup"><span data-stu-id="ab4d9-120">Activity</span></span>|<span data-ttu-id="ab4d9-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ab4d9-121">xs:string</span></span>|<span data-ttu-id="ab4d9-122">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="ab4d9-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="ab4d9-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ab4d9-123">DisplayName</span></span>|<span data-ttu-id="ab4d9-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="ab4d9-124">xs:string</span></span>|<span data-ttu-id="ab4d9-125">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ab4d9-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="ab4d9-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="ab4d9-126">InstanceId</span></span>|<span data-ttu-id="ab4d9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="ab4d9-127">xs:string</span></span>|<span data-ttu-id="ab4d9-128">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="ab4d9-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="ab4d9-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="ab4d9-129">AppDomain</span></span>|<span data-ttu-id="ab4d9-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="ab4d9-130">xs:string</span></span>|<span data-ttu-id="ab4d9-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="ab4d9-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
