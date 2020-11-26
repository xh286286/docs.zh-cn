---
title: 1041 - WorkflowApplicationPersistableIdle
ms.date: 03/30/2017
ms.assetid: 966adf2f-e21d-44df-a3ec-a8e285e0a316
ms.openlocfilehash: 9995823753fc78ca3f278cd635fcf6c7d2b84325
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96238933"
---
# <a name="1041---workflowapplicationpersistableidle"></a><span data-ttu-id="ebe47-102">1041 - WorkflowApplicationPersistableIdle</span><span class="sxs-lookup"><span data-stu-id="ebe47-102">1041 - WorkflowApplicationPersistableIdle</span></span>

## <a name="properties"></a><span data-ttu-id="ebe47-103">属性</span><span class="sxs-lookup"><span data-stu-id="ebe47-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ebe47-104">ID</span><span class="sxs-lookup"><span data-stu-id="ebe47-104">ID</span></span>|<span data-ttu-id="ebe47-105">1041</span><span class="sxs-lookup"><span data-stu-id="ebe47-105">1041</span></span>|  
|<span data-ttu-id="ebe47-106">关键字</span><span class="sxs-lookup"><span data-stu-id="ebe47-106">Keywords</span></span>|<span data-ttu-id="ebe47-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ebe47-107">WFRuntime</span></span>|  
|<span data-ttu-id="ebe47-108">Level</span><span class="sxs-lookup"><span data-stu-id="ebe47-108">Level</span></span>|<span data-ttu-id="ebe47-109">信息</span><span class="sxs-lookup"><span data-stu-id="ebe47-109">Information</span></span>|  
|<span data-ttu-id="ebe47-110">通道</span><span class="sxs-lookup"><span data-stu-id="ebe47-110">Channel</span></span>|<span data-ttu-id="ebe47-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="ebe47-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ebe47-112">描述</span><span class="sxs-lookup"><span data-stu-id="ebe47-112">Description</span></span>  

 <span data-ttu-id="ebe47-113">指示工作流应用程序空闲且可持久化。</span><span class="sxs-lookup"><span data-stu-id="ebe47-113">Indicates that a workflow application is idle and persistable.</span></span> <span data-ttu-id="ebe47-114">工作流应用程序将是空闲且可持久化的。</span><span class="sxs-lookup"><span data-stu-id="ebe47-114">The workflow application will be idled or persisted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ebe47-115">消息</span><span class="sxs-lookup"><span data-stu-id="ebe47-115">Message</span></span>  

 <span data-ttu-id="ebe47-116">WorkflowApplication Id "%1" 处于空闲和可持久状态。</span><span class="sxs-lookup"><span data-stu-id="ebe47-116">WorkflowApplication Id: '%1' is idle and persistable.</span></span>  <span data-ttu-id="ebe47-117">将执行以下操作： %2。</span><span class="sxs-lookup"><span data-stu-id="ebe47-117">The following action will be taken: %2.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ebe47-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="ebe47-118">Details</span></span>  
  
|<span data-ttu-id="ebe47-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="ebe47-119">Data Item Name</span></span>|<span data-ttu-id="ebe47-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="ebe47-120">Data Item Type</span></span>|<span data-ttu-id="ebe47-121">描述</span><span class="sxs-lookup"><span data-stu-id="ebe47-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ebe47-122">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="ebe47-122">WorkflowApplicationId</span></span>|<span data-ttu-id="ebe47-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebe47-123">xs:string</span></span>|<span data-ttu-id="ebe47-124">工作流应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="ebe47-124">The workflow application id</span></span>|  
|<span data-ttu-id="ebe47-125">ActionTaken</span><span class="sxs-lookup"><span data-stu-id="ebe47-125">ActionTaken</span></span>|<span data-ttu-id="ebe47-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebe47-126">xs:string</span></span>|<span data-ttu-id="ebe47-127">将对工作流应用程序执行的操作。</span><span class="sxs-lookup"><span data-stu-id="ebe47-127">The action that will be taken on the workflow application.</span></span>|  
|<span data-ttu-id="ebe47-128">应用程序域</span><span class="sxs-lookup"><span data-stu-id="ebe47-128">AppDomain</span></span>|<span data-ttu-id="ebe47-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ebe47-129">xs:string</span></span>|<span data-ttu-id="ebe47-130">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="ebe47-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
