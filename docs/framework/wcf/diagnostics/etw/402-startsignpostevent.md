---
title: 402 - StartSignpostEvent
ms.date: 03/30/2017
ms.assetid: 5e5be126-765d-4ac9-88e7-008e9ef4f0e5
ms.openlocfilehash: ff32c900f4e357b7f1eca669a0ea60f80ea24b19
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96258317"
---
# <a name="402---startsignpostevent"></a><span data-ttu-id="8323c-102">402 - StartSignpostEvent</span><span class="sxs-lookup"><span data-stu-id="8323c-102">402 - StartSignpostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="8323c-103">属性</span><span class="sxs-lookup"><span data-stu-id="8323c-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8323c-104">ID</span><span class="sxs-lookup"><span data-stu-id="8323c-104">ID</span></span>|<span data-ttu-id="8323c-105">402</span><span class="sxs-lookup"><span data-stu-id="8323c-105">402</span></span>|  
|<span data-ttu-id="8323c-106">关键字</span><span class="sxs-lookup"><span data-stu-id="8323c-106">Keywords</span></span>|<span data-ttu-id="8323c-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="8323c-107">Troubleshooting</span></span>|  
|<span data-ttu-id="8323c-108">Level</span><span class="sxs-lookup"><span data-stu-id="8323c-108">Level</span></span>|<span data-ttu-id="8323c-109">信息</span><span class="sxs-lookup"><span data-stu-id="8323c-109">Information</span></span>|  
|<span data-ttu-id="8323c-110">通道</span><span class="sxs-lookup"><span data-stu-id="8323c-110">Channel</span></span>|<span data-ttu-id="8323c-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="8323c-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8323c-112">描述</span><span class="sxs-lookup"><span data-stu-id="8323c-112">Description</span></span>  

 <span data-ttu-id="8323c-113">此事件标记端对端活动的开始。</span><span class="sxs-lookup"><span data-stu-id="8323c-113">This event marks the beginning of an end-to-end activity.</span></span> <span data-ttu-id="8323c-114">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="8323c-114">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8323c-115">消息</span><span class="sxs-lookup"><span data-stu-id="8323c-115">Message</span></span>  

 <span data-ttu-id="8323c-116">活动边界。</span><span class="sxs-lookup"><span data-stu-id="8323c-116">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="8323c-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="8323c-117">Details</span></span>  
  
|<span data-ttu-id="8323c-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="8323c-118">Data Item Name</span></span>|<span data-ttu-id="8323c-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="8323c-119">Data Item Type</span></span>|<span data-ttu-id="8323c-120">描述</span><span class="sxs-lookup"><span data-stu-id="8323c-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8323c-121">扩展数据</span><span class="sxs-lookup"><span data-stu-id="8323c-121">Extended Data</span></span>|`xs:string`|<span data-ttu-id="8323c-122">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="8323c-122">The name of the activity.</span></span>|  
|<span data-ttu-id="8323c-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="8323c-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="8323c-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="8323c-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
