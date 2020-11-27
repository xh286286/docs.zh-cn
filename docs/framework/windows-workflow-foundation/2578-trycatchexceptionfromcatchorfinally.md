---
title: 2578 - TryCatchExceptionFromCatchOrFinally
ms.date: 03/30/2017
ms.assetid: 4803fee6-b8d8-4937-9907-d5c5fd5299db
ms.openlocfilehash: 92503b13f59556fa21d058578982c3fa7b7a6b96
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96271186"
---
# <a name="2578---trycatchexceptionfromcatchorfinally"></a><span data-ttu-id="0a920-102">2578 - TryCatchExceptionFromCatchOrFinally</span><span class="sxs-lookup"><span data-stu-id="0a920-102">2578 - TryCatchExceptionFromCatchOrFinally</span></span>

## <a name="properties"></a><span data-ttu-id="0a920-103">属性</span><span class="sxs-lookup"><span data-stu-id="0a920-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0a920-104">ID</span><span class="sxs-lookup"><span data-stu-id="0a920-104">ID</span></span>|<span data-ttu-id="0a920-105">2578</span><span class="sxs-lookup"><span data-stu-id="0a920-105">2578</span></span>|  
|<span data-ttu-id="0a920-106">关键字</span><span class="sxs-lookup"><span data-stu-id="0a920-106">Keywords</span></span>|<span data-ttu-id="0a920-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="0a920-107">WFActivities</span></span>|  
|<span data-ttu-id="0a920-108">Level</span><span class="sxs-lookup"><span data-stu-id="0a920-108">Level</span></span>|<span data-ttu-id="0a920-109">警告</span><span class="sxs-lookup"><span data-stu-id="0a920-109">Warning</span></span>|  
|<span data-ttu-id="0a920-110">通道</span><span class="sxs-lookup"><span data-stu-id="0a920-110">Channel</span></span>|<span data-ttu-id="0a920-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0a920-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0a920-112">描述</span><span class="sxs-lookup"><span data-stu-id="0a920-112">Description</span></span>  

 <span data-ttu-id="0a920-113">指示 Catch 或 Finally 活动引发了异常。</span><span class="sxs-lookup"><span data-stu-id="0a920-113">Indicates a Catch or Finally activity has thrown an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0a920-114">消息</span><span class="sxs-lookup"><span data-stu-id="0a920-114">Message</span></span>  

 <span data-ttu-id="0a920-115">与 TryCatch 活动“%1”关联的 Catch 或 Finally 活动引发了异常。</span><span class="sxs-lookup"><span data-stu-id="0a920-115">A Catch or Finally activity that is associated with the TryCatch activity '%1' has thrown an exception.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0a920-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="0a920-116">Details</span></span>  
  
|<span data-ttu-id="0a920-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0a920-117">Data Item Name</span></span>|<span data-ttu-id="0a920-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0a920-118">Data Item Type</span></span>|<span data-ttu-id="0a920-119">说明</span><span class="sxs-lookup"><span data-stu-id="0a920-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0a920-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0a920-120">DisplayName</span></span>|<span data-ttu-id="0a920-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="0a920-121">xs:string</span></span>|<span data-ttu-id="0a920-122">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="0a920-122">The display name of the activity.</span></span>|  
|<span data-ttu-id="0a920-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0a920-123">AppDomain</span></span>|<span data-ttu-id="0a920-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="0a920-124">xs:string</span></span>|<span data-ttu-id="0a920-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0a920-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
