---
title: 2576 - TryCatchExceptionFromTry
ms.date: 03/30/2017
ms.assetid: 47e48973-b17c-4a16-8338-c84b54aa0a6e
ms.openlocfilehash: 722d5206322c2a9abacbca554d489ba2f6efe357
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96235826"
---
# <a name="2576---trycatchexceptionfromtry"></a><span data-ttu-id="4471f-102">2576 - TryCatchExceptionFromTry</span><span class="sxs-lookup"><span data-stu-id="4471f-102">2576 - TryCatchExceptionFromTry</span></span>

## <a name="properties"></a><span data-ttu-id="4471f-103">属性</span><span class="sxs-lookup"><span data-stu-id="4471f-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4471f-104">ID</span><span class="sxs-lookup"><span data-stu-id="4471f-104">ID</span></span>|<span data-ttu-id="4471f-105">2576</span><span class="sxs-lookup"><span data-stu-id="4471f-105">2576</span></span>|  
|<span data-ttu-id="4471f-106">关键字</span><span class="sxs-lookup"><span data-stu-id="4471f-106">Keywords</span></span>|<span data-ttu-id="4471f-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="4471f-107">WFActivities</span></span>|  
|<span data-ttu-id="4471f-108">Level</span><span class="sxs-lookup"><span data-stu-id="4471f-108">Level</span></span>|<span data-ttu-id="4471f-109">信息</span><span class="sxs-lookup"><span data-stu-id="4471f-109">Information</span></span>|  
|<span data-ttu-id="4471f-110">通道</span><span class="sxs-lookup"><span data-stu-id="4471f-110">Channel</span></span>|<span data-ttu-id="4471f-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="4471f-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4471f-112">描述</span><span class="sxs-lookup"><span data-stu-id="4471f-112">Description</span></span>  

 <span data-ttu-id="4471f-113">指示 TryCatch 活动捕获了异常。</span><span class="sxs-lookup"><span data-stu-id="4471f-113">Indicates the TryCatch activity has caught an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4471f-114">消息</span><span class="sxs-lookup"><span data-stu-id="4471f-114">Message</span></span>  

 <span data-ttu-id="4471f-115">TryCatch 活动“%1”捕获了“%2”类型的异常。</span><span class="sxs-lookup"><span data-stu-id="4471f-115">The TryCatch activity '%1' has caught an exception of type '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4471f-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="4471f-116">Details</span></span>  
  
|<span data-ttu-id="4471f-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="4471f-117">Data Item Name</span></span>|<span data-ttu-id="4471f-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="4471f-118">Data Item Type</span></span>|<span data-ttu-id="4471f-119">说明</span><span class="sxs-lookup"><span data-stu-id="4471f-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4471f-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4471f-120">DisplayName</span></span>|<span data-ttu-id="4471f-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="4471f-121">xs:string</span></span>|<span data-ttu-id="4471f-122">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4471f-122">The display name of the activity.</span></span>|  
|<span data-ttu-id="4471f-123">异常</span><span class="sxs-lookup"><span data-stu-id="4471f-123">Exception</span></span>|<span data-ttu-id="4471f-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="4471f-124">xs:string</span></span>|<span data-ttu-id="4471f-125">异常的类型名称。</span><span class="sxs-lookup"><span data-stu-id="4471f-125">The type name of the exception.</span></span>|  
|<span data-ttu-id="4471f-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="4471f-126">AppDomain</span></span>|<span data-ttu-id="4471f-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="4471f-127">xs:string</span></span>|<span data-ttu-id="4471f-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="4471f-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
