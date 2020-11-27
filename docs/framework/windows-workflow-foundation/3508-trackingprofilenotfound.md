---
title: 3508 - TrackingProfileNotFound
ms.date: 03/30/2017
ms.assetid: 4cee3c4a-0490-4c94-aa19-ef7ce7287c02
ms.openlocfilehash: 23262427c3da730eaf930a8b483c7c4d4ec3a3a4
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96289836"
---
# <a name="3508---trackingprofilenotfound"></a><span data-ttu-id="fe421-102">3508 - TrackingProfileNotFound</span><span class="sxs-lookup"><span data-stu-id="fe421-102">3508 - TrackingProfileNotFound</span></span>

## <a name="properties"></a><span data-ttu-id="fe421-103">属性</span><span class="sxs-lookup"><span data-stu-id="fe421-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fe421-104">ID</span><span class="sxs-lookup"><span data-stu-id="fe421-104">ID</span></span>|<span data-ttu-id="fe421-105">3508</span><span class="sxs-lookup"><span data-stu-id="fe421-105">3508</span></span>|  
|<span data-ttu-id="fe421-106">关键字</span><span class="sxs-lookup"><span data-stu-id="fe421-106">Keywords</span></span>|<span data-ttu-id="fe421-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="fe421-107">WFServices</span></span>|  
|<span data-ttu-id="fe421-108">级别</span><span class="sxs-lookup"><span data-stu-id="fe421-108">Level</span></span>|<span data-ttu-id="fe421-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="fe421-109">Verbose</span></span>|  
|<span data-ttu-id="fe421-110">通道</span><span class="sxs-lookup"><span data-stu-id="fe421-110">Channel</span></span>|<span data-ttu-id="fe421-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="fe421-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fe421-112">描述</span><span class="sxs-lookup"><span data-stu-id="fe421-112">Description</span></span>  

 <span data-ttu-id="fe421-113">指示在配置文件中找不到 TrackingProfile，或 ActivityDefinitionId 与配置文件不匹配。</span><span class="sxs-lookup"><span data-stu-id="fe421-113">Indicates either a TrackingProfile is not found in the config file or the ActivityDefinitionId does not match the profile.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fe421-114">消息</span><span class="sxs-lookup"><span data-stu-id="fe421-114">Message</span></span>  

 <span data-ttu-id="fe421-115">未找到 ActivityDefinitionId“%2”的 TrackingProfile“%1”。</span><span class="sxs-lookup"><span data-stu-id="fe421-115">TrackingProfile '%1' for the ActivityDefinitionId '%2' not found.</span></span> <span data-ttu-id="fe421-116">在配置文件中找不到 TrackingProfile，或 ActivityDefinitionId 不匹配。</span><span class="sxs-lookup"><span data-stu-id="fe421-116">Either the TrackingProfile is not found in the config file or the ActivityDefinitionId does not match.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fe421-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="fe421-117">Details</span></span>  
  
|<span data-ttu-id="fe421-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="fe421-118">Data Item Name</span></span>|<span data-ttu-id="fe421-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="fe421-119">Data Item Type</span></span>|<span data-ttu-id="fe421-120">描述</span><span class="sxs-lookup"><span data-stu-id="fe421-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fe421-121">TrackingProfile</span><span class="sxs-lookup"><span data-stu-id="fe421-121">TrackingProfile</span></span>|<span data-ttu-id="fe421-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe421-122">xs:string</span></span>|<span data-ttu-id="fe421-123">跟踪配置文件的名称。</span><span class="sxs-lookup"><span data-stu-id="fe421-123">The name of the tracking profile.</span></span>|  
|<span data-ttu-id="fe421-124">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fe421-124">ActivityDefinitionId</span></span>|<span data-ttu-id="fe421-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe421-125">xs:string</span></span>|<span data-ttu-id="fe421-126">活动定义 ID。</span><span class="sxs-lookup"><span data-stu-id="fe421-126">The activity definition id.</span></span>|  
|<span data-ttu-id="fe421-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="fe421-127">AppDomain</span></span>|<span data-ttu-id="fe421-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe421-128">xs:string</span></span>|<span data-ttu-id="fe421-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="fe421-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
