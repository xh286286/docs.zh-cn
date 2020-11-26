---
title: 1005 - WorkflowApplicationIdled
ms.date: 03/30/2017
ms.assetid: 74d77dfa-f20d-4fe9-a6ae-e6d1b5fe4182
ms.openlocfilehash: 3b7210246b7fb754145c8aa6128da3183cea9f91
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239856"
---
# <a name="1005---workflowapplicationidled"></a><span data-ttu-id="b9cf8-102">1005 - WorkflowApplicationIdled</span><span class="sxs-lookup"><span data-stu-id="b9cf8-102">1005 - WorkflowApplicationIdled</span></span>

## <a name="properties"></a><span data-ttu-id="b9cf8-103">属性</span><span class="sxs-lookup"><span data-stu-id="b9cf8-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b9cf8-104">ID</span><span class="sxs-lookup"><span data-stu-id="b9cf8-104">ID</span></span>|<span data-ttu-id="b9cf8-105">1005</span><span class="sxs-lookup"><span data-stu-id="b9cf8-105">1005</span></span>|  
|<span data-ttu-id="b9cf8-106">关键字</span><span class="sxs-lookup"><span data-stu-id="b9cf8-106">Keywords</span></span>|<span data-ttu-id="b9cf8-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b9cf8-107">WFRuntime</span></span>|  
|<span data-ttu-id="b9cf8-108">Level</span><span class="sxs-lookup"><span data-stu-id="b9cf8-108">Level</span></span>|<span data-ttu-id="b9cf8-109">信息</span><span class="sxs-lookup"><span data-stu-id="b9cf8-109">Information</span></span>|  
|<span data-ttu-id="b9cf8-110">通道</span><span class="sxs-lookup"><span data-stu-id="b9cf8-110">Channel</span></span>|<span data-ttu-id="b9cf8-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="b9cf8-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b9cf8-112">描述</span><span class="sxs-lookup"><span data-stu-id="b9cf8-112">Description</span></span>  

 <span data-ttu-id="b9cf8-113">指示工作流应用程序已处于空闲状态。</span><span class="sxs-lookup"><span data-stu-id="b9cf8-113">Indicates a workflow application has idled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b9cf8-114">消息</span><span class="sxs-lookup"><span data-stu-id="b9cf8-114">Message</span></span>  

 <span data-ttu-id="b9cf8-115">WorkflowApplication ID“%1”变为空闲状态。</span><span class="sxs-lookup"><span data-stu-id="b9cf8-115">WorkflowApplication Id: '%1' went idle.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b9cf8-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="b9cf8-116">Details</span></span>  
  
|<span data-ttu-id="b9cf8-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="b9cf8-117">Data Item Name</span></span>|<span data-ttu-id="b9cf8-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="b9cf8-118">Data Item Type</span></span>|<span data-ttu-id="b9cf8-119">描述</span><span class="sxs-lookup"><span data-stu-id="b9cf8-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b9cf8-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="b9cf8-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="b9cf8-121">工作流应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="b9cf8-121">The workflow application id</span></span>|  
|<span data-ttu-id="b9cf8-122">应用程序域</span><span class="sxs-lookup"><span data-stu-id="b9cf8-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="b9cf8-123">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="b9cf8-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
