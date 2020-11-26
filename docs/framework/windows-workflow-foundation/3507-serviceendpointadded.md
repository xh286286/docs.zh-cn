---
title: 3507 - ServiceEndpointAdded
ms.date: 03/30/2017
ms.assetid: c068fc0e-07ee-4551-9824-ea7216e1fe37
ms.openlocfilehash: 903071e7b1f89dc3489b8d3ac05427d699a33a7e
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96240753"
---
# <a name="3507---serviceendpointadded"></a><span data-ttu-id="68c14-102">3507 - ServiceEndpointAdded</span><span class="sxs-lookup"><span data-stu-id="68c14-102">3507 - ServiceEndpointAdded</span></span>

## <a name="properties"></a><span data-ttu-id="68c14-103">属性</span><span class="sxs-lookup"><span data-stu-id="68c14-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="68c14-104">ID</span><span class="sxs-lookup"><span data-stu-id="68c14-104">ID</span></span>|<span data-ttu-id="68c14-105">3507</span><span class="sxs-lookup"><span data-stu-id="68c14-105">3507</span></span>|  
|<span data-ttu-id="68c14-106">关键字</span><span class="sxs-lookup"><span data-stu-id="68c14-106">Keywords</span></span>|<span data-ttu-id="68c14-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="68c14-107">WFServices</span></span>|  
|<span data-ttu-id="68c14-108">Level</span><span class="sxs-lookup"><span data-stu-id="68c14-108">Level</span></span>|<span data-ttu-id="68c14-109">信息</span><span class="sxs-lookup"><span data-stu-id="68c14-109">Information</span></span>|  
|<span data-ttu-id="68c14-110">通道</span><span class="sxs-lookup"><span data-stu-id="68c14-110">Channel</span></span>|<span data-ttu-id="68c14-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="68c14-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="68c14-112">描述</span><span class="sxs-lookup"><span data-stu-id="68c14-112">Description</span></span>  

 <span data-ttu-id="68c14-113">指示添加了服务终结点。</span><span class="sxs-lookup"><span data-stu-id="68c14-113">Indicates a service endpoint has been added.</span></span>  
  
## <a name="message"></a><span data-ttu-id="68c14-114">消息</span><span class="sxs-lookup"><span data-stu-id="68c14-114">Message</span></span>  

 <span data-ttu-id="68c14-115">已为地址“%1”、绑定“%2”和协定“%3”添加了服务终结点。</span><span class="sxs-lookup"><span data-stu-id="68c14-115">A service endpoint has been added for address '%1', binding '%2', and contract '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="68c14-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="68c14-116">Details</span></span>  
  
|<span data-ttu-id="68c14-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="68c14-117">Data Item Name</span></span>|<span data-ttu-id="68c14-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="68c14-118">Data Item Type</span></span>|<span data-ttu-id="68c14-119">描述</span><span class="sxs-lookup"><span data-stu-id="68c14-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="68c14-120">地址</span><span class="sxs-lookup"><span data-stu-id="68c14-120">Address</span></span>|<span data-ttu-id="68c14-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="68c14-121">xs:string</span></span>|<span data-ttu-id="68c14-122">终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="68c14-122">The address of the endpoint.</span></span>|  
|<span data-ttu-id="68c14-123">绑定</span><span class="sxs-lookup"><span data-stu-id="68c14-123">Binding</span></span>|<span data-ttu-id="68c14-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="68c14-124">xs:string</span></span>|<span data-ttu-id="68c14-125">终结点的绑定。</span><span class="sxs-lookup"><span data-stu-id="68c14-125">The binding of the endpoint.</span></span>|  
|<span data-ttu-id="68c14-126">协定</span><span class="sxs-lookup"><span data-stu-id="68c14-126">Contract</span></span>|<span data-ttu-id="68c14-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="68c14-127">xs:string</span></span>|<span data-ttu-id="68c14-128">终结点的协定。</span><span class="sxs-lookup"><span data-stu-id="68c14-128">The contract of the endpoint.</span></span>|  
|<span data-ttu-id="68c14-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="68c14-129">AppDomain</span></span>|<span data-ttu-id="68c14-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="68c14-130">xs:string</span></span>|<span data-ttu-id="68c14-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="68c14-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
