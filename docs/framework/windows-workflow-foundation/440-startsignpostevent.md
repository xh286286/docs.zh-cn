---
title: 440 - StartSignpostEvent1
ms.date: 03/30/2017
ms.assetid: 27b551b5-ae76-49f8-bab8-6300009eb4c1
ms.openlocfilehash: 1e0278d665a961afab21445ab8490e3e5a94987c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96293450"
---
# <a name="440---startsignpostevent1"></a><span data-ttu-id="3c52a-102">440 - StartSignpostEvent1</span><span class="sxs-lookup"><span data-stu-id="3c52a-102">440 - StartSignpostEvent1</span></span>

## <a name="properties"></a><span data-ttu-id="3c52a-103">属性</span><span class="sxs-lookup"><span data-stu-id="3c52a-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3c52a-104">ID</span><span class="sxs-lookup"><span data-stu-id="3c52a-104">ID</span></span>|<span data-ttu-id="3c52a-105">440</span><span class="sxs-lookup"><span data-stu-id="3c52a-105">440</span></span>|  
|<span data-ttu-id="3c52a-106">关键字</span><span class="sxs-lookup"><span data-stu-id="3c52a-106">Keywords</span></span>|<span data-ttu-id="3c52a-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="3c52a-107">Troubleshooting</span></span>|  
|<span data-ttu-id="3c52a-108">Level</span><span class="sxs-lookup"><span data-stu-id="3c52a-108">Level</span></span>|<span data-ttu-id="3c52a-109">信息</span><span class="sxs-lookup"><span data-stu-id="3c52a-109">Information</span></span>|  
|<span data-ttu-id="3c52a-110">通道</span><span class="sxs-lookup"><span data-stu-id="3c52a-110">Channel</span></span>|<span data-ttu-id="3c52a-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="3c52a-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3c52a-112">描述</span><span class="sxs-lookup"><span data-stu-id="3c52a-112">Description</span></span>  

 <span data-ttu-id="3c52a-113">在活动跟踪中，指示消息是否已开始跨越发送或接收中的活动边界。</span><span class="sxs-lookup"><span data-stu-id="3c52a-113">In activity tracing, indicates a message has started crossing an activity boundary in send or receive.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3c52a-114">消息</span><span class="sxs-lookup"><span data-stu-id="3c52a-114">Message</span></span>  

 <span data-ttu-id="3c52a-115">活动边界。</span><span class="sxs-lookup"><span data-stu-id="3c52a-115">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3c52a-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="3c52a-116">Details</span></span>  
  
|<span data-ttu-id="3c52a-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="3c52a-117">Data Item Name</span></span>|<span data-ttu-id="3c52a-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="3c52a-118">Data Item Type</span></span>|<span data-ttu-id="3c52a-119">描述</span><span class="sxs-lookup"><span data-stu-id="3c52a-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3c52a-120">ExtendedData</span><span class="sxs-lookup"><span data-stu-id="3c52a-120">ExtendedData</span></span>|`xs:string`|<span data-ttu-id="3c52a-121">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="3c52a-121">The name of the activity.</span></span>|  
|<span data-ttu-id="3c52a-122">应用程序域</span><span class="sxs-lookup"><span data-stu-id="3c52a-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="3c52a-123">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="3c52a-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
