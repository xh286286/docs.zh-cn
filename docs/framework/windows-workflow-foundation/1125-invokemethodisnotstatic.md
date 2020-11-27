---
title: 1125 - InvokeMethodIsNotStatic
ms.date: 03/30/2017
ms.assetid: ea2b3827-63da-497b-b2c3-d5cebefe57a1
ms.openlocfilehash: 0405b4e1207db5c056fbd478b98c408258daf0c3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294204"
---
# <a name="1125---invokemethodisnotstatic"></a><span data-ttu-id="b2edb-102">1125 - InvokeMethodIsNotStatic</span><span class="sxs-lookup"><span data-stu-id="b2edb-102">1125 - InvokeMethodIsNotStatic</span></span>

## <a name="properties"></a><span data-ttu-id="b2edb-103">属性</span><span class="sxs-lookup"><span data-stu-id="b2edb-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b2edb-104">ID</span><span class="sxs-lookup"><span data-stu-id="b2edb-104">ID</span></span>|<span data-ttu-id="b2edb-105">1125</span><span class="sxs-lookup"><span data-stu-id="b2edb-105">1125</span></span>|  
|<span data-ttu-id="b2edb-106">关键字</span><span class="sxs-lookup"><span data-stu-id="b2edb-106">Keywords</span></span>|<span data-ttu-id="b2edb-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b2edb-107">WFRuntime</span></span>|  
|<span data-ttu-id="b2edb-108">Level</span><span class="sxs-lookup"><span data-stu-id="b2edb-108">Level</span></span>|<span data-ttu-id="b2edb-109">信息</span><span class="sxs-lookup"><span data-stu-id="b2edb-109">Information</span></span>|  
|<span data-ttu-id="b2edb-110">通道</span><span class="sxs-lookup"><span data-stu-id="b2edb-110">Channel</span></span>|<span data-ttu-id="b2edb-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="b2edb-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b2edb-112">描述</span><span class="sxs-lookup"><span data-stu-id="b2edb-112">Description</span></span>  

 <span data-ttu-id="b2edb-113">在 CacheMetadata 步骤中，InvokeMethod 活动指示要调用的方法是非静态的。</span><span class="sxs-lookup"><span data-stu-id="b2edb-113">During CacheMetadata step, InvokeMethod activity indicates the method to be invoked is not static.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b2edb-114">消息</span><span class="sxs-lookup"><span data-stu-id="b2edb-114">Message</span></span>  

 <span data-ttu-id="b2edb-115">InvokeMethod“%1”- 方法非静态。</span><span class="sxs-lookup"><span data-stu-id="b2edb-115">InvokeMethod '%1' - method is not Static.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b2edb-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="b2edb-116">Details</span></span>  
  
|<span data-ttu-id="b2edb-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="b2edb-117">Data Item Name</span></span>|<span data-ttu-id="b2edb-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="b2edb-118">Data Item Type</span></span>|<span data-ttu-id="b2edb-119">描述</span><span class="sxs-lookup"><span data-stu-id="b2edb-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b2edb-120">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="b2edb-120">InvokeMethod</span></span>|<span data-ttu-id="b2edb-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="b2edb-121">xs:string</span></span>|<span data-ttu-id="b2edb-122">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b2edb-122">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="b2edb-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="b2edb-123">AppDomain</span></span>|<span data-ttu-id="b2edb-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="b2edb-124">xs:string</span></span>|<span data-ttu-id="b2edb-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="b2edb-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
