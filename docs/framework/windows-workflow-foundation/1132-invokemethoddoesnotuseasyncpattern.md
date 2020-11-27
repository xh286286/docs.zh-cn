---
title: 1132 - InvokeMethodDoesNotUseAsyncPattern
ms.date: 03/30/2017
ms.assetid: 436b3767-4460-46b0-9ea3-fc2963260c11
ms.openlocfilehash: 9249bdd0fe996ee7c1b04783ac8fef2c48063cc0
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294152"
---
# <a name="1132---invokemethoddoesnotuseasyncpattern"></a><span data-ttu-id="eb420-102">1132 - InvokeMethodDoesNotUseAsyncPattern</span><span class="sxs-lookup"><span data-stu-id="eb420-102">1132 - InvokeMethodDoesNotUseAsyncPattern</span></span>

## <a name="properties"></a><span data-ttu-id="eb420-103">属性</span><span class="sxs-lookup"><span data-stu-id="eb420-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="eb420-104">ID</span><span class="sxs-lookup"><span data-stu-id="eb420-104">ID</span></span>|<span data-ttu-id="eb420-105">1132</span><span class="sxs-lookup"><span data-stu-id="eb420-105">1132</span></span>|  
|<span data-ttu-id="eb420-106">关键字</span><span class="sxs-lookup"><span data-stu-id="eb420-106">Keywords</span></span>|<span data-ttu-id="eb420-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="eb420-107">WFRuntime</span></span>|  
|<span data-ttu-id="eb420-108">Level</span><span class="sxs-lookup"><span data-stu-id="eb420-108">Level</span></span>|<span data-ttu-id="eb420-109">信息</span><span class="sxs-lookup"><span data-stu-id="eb420-109">Information</span></span>|  
|<span data-ttu-id="eb420-110">通道</span><span class="sxs-lookup"><span data-stu-id="eb420-110">Channel</span></span>|<span data-ttu-id="eb420-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="eb420-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="eb420-112">描述</span><span class="sxs-lookup"><span data-stu-id="eb420-112">Description</span></span>  

 <span data-ttu-id="eb420-113">在 CacheMetadata 步骤中，InvokeMethod 活动指示它在调用方法时未使用异步模式。</span><span class="sxs-lookup"><span data-stu-id="eb420-113">During CacheMetadata step, InvokeMethod activity indicates that it is not using the async pattern when invoking the method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="eb420-114">消息</span><span class="sxs-lookup"><span data-stu-id="eb420-114">Message</span></span>  

 <span data-ttu-id="eb420-115">InvokeMethod“%1”- 方法不使用异步模式。</span><span class="sxs-lookup"><span data-stu-id="eb420-115">InvokeMethod '%1' - method does not use asynchronous pattern.</span></span>  
  
## <a name="details"></a><span data-ttu-id="eb420-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="eb420-116">Details</span></span>  
  
|<span data-ttu-id="eb420-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="eb420-117">Data Item Name</span></span>|<span data-ttu-id="eb420-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="eb420-118">Data Item Type</span></span>|<span data-ttu-id="eb420-119">描述</span><span class="sxs-lookup"><span data-stu-id="eb420-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="eb420-120">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="eb420-120">InvokeMethod</span></span>|<span data-ttu-id="eb420-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="eb420-121">xs:string</span></span>|<span data-ttu-id="eb420-122">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="eb420-122">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="eb420-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="eb420-123">AppDomain</span></span>|<span data-ttu-id="eb420-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="eb420-124">xs:string</span></span>|<span data-ttu-id="eb420-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="eb420-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
