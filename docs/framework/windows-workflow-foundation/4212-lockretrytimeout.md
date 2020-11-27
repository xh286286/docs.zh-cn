---
title: 4212 - LockRetryTimeout
ms.date: 03/30/2017
ms.assetid: d4ad415a-9871-49fc-85b8-8ee2ea149b1d
ms.openlocfilehash: 43ec434064f768fc976232c6d3013f17c80fe053
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96267164"
---
# <a name="4212---lockretrytimeout"></a><span data-ttu-id="20bd3-102">4212 - LockRetryTimeout</span><span class="sxs-lookup"><span data-stu-id="20bd3-102">4212 - LockRetryTimeout</span></span>

## <a name="properties"></a><span data-ttu-id="20bd3-103">属性</span><span class="sxs-lookup"><span data-stu-id="20bd3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="20bd3-104">ID</span><span class="sxs-lookup"><span data-stu-id="20bd3-104">ID</span></span>|<span data-ttu-id="20bd3-105">4212</span><span class="sxs-lookup"><span data-stu-id="20bd3-105">4212</span></span>|  
|<span data-ttu-id="20bd3-106">关键字</span><span class="sxs-lookup"><span data-stu-id="20bd3-106">Keywords</span></span>|<span data-ttu-id="20bd3-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="20bd3-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="20bd3-108">Level</span><span class="sxs-lookup"><span data-stu-id="20bd3-108">Level</span></span>|<span data-ttu-id="20bd3-109">警告</span><span class="sxs-lookup"><span data-stu-id="20bd3-109">Warning</span></span>|  
|<span data-ttu-id="20bd3-110">通道</span><span class="sxs-lookup"><span data-stu-id="20bd3-110">Channel</span></span>|<span data-ttu-id="20bd3-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="20bd3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="20bd3-112">描述</span><span class="sxs-lookup"><span data-stu-id="20bd3-112">Description</span></span>  

 <span data-ttu-id="20bd3-113">尝试获取实例锁时 SQL 提供程序遇到了超时。</span><span class="sxs-lookup"><span data-stu-id="20bd3-113">SQL provider encountered a timeout trying to acquire the instance lock.</span></span>  
  
## <a name="message"></a><span data-ttu-id="20bd3-114">消息</span><span class="sxs-lookup"><span data-stu-id="20bd3-114">Message</span></span>  

 <span data-ttu-id="20bd3-115">尝试获取实例锁时超时。</span><span class="sxs-lookup"><span data-stu-id="20bd3-115">Timeout trying to acquire the instance lock.</span></span>  <span data-ttu-id="20bd3-116">操作在分配的超时 %1 内没有完成。</span><span class="sxs-lookup"><span data-stu-id="20bd3-116">The operation did not complete within the allotted timeout of %1.</span></span> <span data-ttu-id="20bd3-117">分配给此操作的时间可能是更长超时的一部分。</span><span class="sxs-lookup"><span data-stu-id="20bd3-117">The time allotted to this operation may have been a portion of a longer timeout.</span></span>  
  
## <a name="details"></a><span data-ttu-id="20bd3-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="20bd3-118">Details</span></span>  
  
|<span data-ttu-id="20bd3-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="20bd3-119">Data Item Name</span></span>|<span data-ttu-id="20bd3-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="20bd3-120">Data Item Type</span></span>|<span data-ttu-id="20bd3-121">描述</span><span class="sxs-lookup"><span data-stu-id="20bd3-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="20bd3-122">延迟</span><span class="sxs-lookup"><span data-stu-id="20bd3-122">Delay</span></span>|<span data-ttu-id="20bd3-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="20bd3-123">xs:string</span></span>|<span data-ttu-id="20bd3-124">重试之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="20bd3-124">The delay between retries.</span></span>|  
|<span data-ttu-id="20bd3-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="20bd3-125">AppDomain</span></span>|<span data-ttu-id="20bd3-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="20bd3-126">xs:string</span></span>|<span data-ttu-id="20bd3-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="20bd3-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
