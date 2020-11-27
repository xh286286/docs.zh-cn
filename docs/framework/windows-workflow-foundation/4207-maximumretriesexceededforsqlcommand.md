---
title: 4207 - MaximumRetriesExceededForSqlCommand
ms.date: 03/30/2017
ms.assetid: 8c8bee26-9ad4-4e01-bd16-0e1fd510fb6b
ms.openlocfilehash: f724379ef2ea23dcca7aa75caab3f10f7635e419
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96251199"
---
# <a name="4207---maximumretriesexceededforsqlcommand"></a><span data-ttu-id="0f66e-102">4207 - MaximumRetriesExceededForSqlCommand</span><span class="sxs-lookup"><span data-stu-id="0f66e-102">4207 - MaximumRetriesExceededForSqlCommand</span></span>

## <a name="properties"></a><span data-ttu-id="0f66e-103">属性</span><span class="sxs-lookup"><span data-stu-id="0f66e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0f66e-104">ID</span><span class="sxs-lookup"><span data-stu-id="0f66e-104">ID</span></span>|<span data-ttu-id="0f66e-105">4207</span><span class="sxs-lookup"><span data-stu-id="0f66e-105">4207</span></span>|  
|<span data-ttu-id="0f66e-106">关键字</span><span class="sxs-lookup"><span data-stu-id="0f66e-106">Keywords</span></span>|<span data-ttu-id="0f66e-107">配额，FInstanceStore</span><span class="sxs-lookup"><span data-stu-id="0f66e-107">Quota, WFInstanceStore</span></span>|  
|<span data-ttu-id="0f66e-108">Level</span><span class="sxs-lookup"><span data-stu-id="0f66e-108">Level</span></span>|<span data-ttu-id="0f66e-109">信息</span><span class="sxs-lookup"><span data-stu-id="0f66e-109">Information</span></span>|  
|<span data-ttu-id="0f66e-110">通道</span><span class="sxs-lookup"><span data-stu-id="0f66e-110">Channel</span></span>|<span data-ttu-id="0f66e-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0f66e-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0f66e-112">描述</span><span class="sxs-lookup"><span data-stu-id="0f66e-112">Description</span></span>  

 <span data-ttu-id="0f66e-113">指示 SQL 提供程序正在放弃重试 SQL 命令，因为执行次数已达到了允许的最多重试次数。</span><span class="sxs-lookup"><span data-stu-id="0f66e-113">Indicates SQL provider is giving up retrying a SQL command as the maximum number of retries have been performed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0f66e-114">消息</span><span class="sxs-lookup"><span data-stu-id="0f66e-114">Message</span></span>  

 <span data-ttu-id="0f66e-115">正在放弃重试 SQL 命令，因为执行次数已达到了允许的最多重试次数。</span><span class="sxs-lookup"><span data-stu-id="0f66e-115">Giving up retrying a SQL command as the maximum number of retries have been performed.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0f66e-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="0f66e-116">Details</span></span>  
  
|<span data-ttu-id="0f66e-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0f66e-117">Data Item Name</span></span>|<span data-ttu-id="0f66e-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0f66e-118">Data Item Type</span></span>|<span data-ttu-id="0f66e-119">描述</span><span class="sxs-lookup"><span data-stu-id="0f66e-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0f66e-120">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0f66e-120">AppDomain</span></span>|<span data-ttu-id="0f66e-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="0f66e-121">xs:string</span></span>|<span data-ttu-id="0f66e-122">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0f66e-122">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
