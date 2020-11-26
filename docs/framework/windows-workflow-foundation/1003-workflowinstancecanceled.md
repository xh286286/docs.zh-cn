---
title: 1003 - WorkflowInstanceCanceled
ms.date: 03/30/2017
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
ms.openlocfilehash: bd8abf173ab6588d4a35ba59c6cd14fb53445e9f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239895"
---
# <a name="1003---workflowinstancecanceled"></a><span data-ttu-id="5028b-102">1003 - WorkflowInstanceCanceled</span><span class="sxs-lookup"><span data-stu-id="5028b-102">1003 - WorkflowInstanceCanceled</span></span>

## <a name="properties"></a><span data-ttu-id="5028b-103">属性</span><span class="sxs-lookup"><span data-stu-id="5028b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5028b-104">ID</span><span class="sxs-lookup"><span data-stu-id="5028b-104">ID</span></span>|<span data-ttu-id="5028b-105">1003</span><span class="sxs-lookup"><span data-stu-id="5028b-105">1003</span></span>|  
|<span data-ttu-id="5028b-106">关键字</span><span class="sxs-lookup"><span data-stu-id="5028b-106">Keywords</span></span>|<span data-ttu-id="5028b-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5028b-107">WFRuntime</span></span>|  
|<span data-ttu-id="5028b-108">Level</span><span class="sxs-lookup"><span data-stu-id="5028b-108">Level</span></span>|<span data-ttu-id="5028b-109">信息</span><span class="sxs-lookup"><span data-stu-id="5028b-109">Information</span></span>|  
|<span data-ttu-id="5028b-110">通道</span><span class="sxs-lookup"><span data-stu-id="5028b-110">Channel</span></span>|<span data-ttu-id="5028b-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="5028b-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5028b-112">描述</span><span class="sxs-lookup"><span data-stu-id="5028b-112">Description</span></span>  

 <span data-ttu-id="5028b-113">指示工作流实例在“已取消”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="5028b-113">Indicates a workflow instance has completed in the Canceled state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5028b-114">消息</span><span class="sxs-lookup"><span data-stu-id="5028b-114">Message</span></span>  

 <span data-ttu-id="5028b-115">WorkflowInstance Id“%1”在“已取消”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="5028b-115">WorkflowInstance Id: '%1' has completed in the Canceled state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5028b-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="5028b-116">Details</span></span>  
  
|<span data-ttu-id="5028b-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="5028b-117">Data Item Name</span></span>|<span data-ttu-id="5028b-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="5028b-118">Data Item Type</span></span>|<span data-ttu-id="5028b-119">描述</span><span class="sxs-lookup"><span data-stu-id="5028b-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5028b-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="5028b-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="5028b-121">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="5028b-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="5028b-122">应用程序域</span><span class="sxs-lookup"><span data-stu-id="5028b-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="5028b-123">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="5028b-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
