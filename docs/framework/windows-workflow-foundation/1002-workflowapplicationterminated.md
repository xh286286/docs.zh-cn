---
title: 1002 - WorkflowApplicationTerminated
ms.date: 03/30/2017
ms.assetid: 4e8b111f-79dc-4898-bb4a-e9b36f69420f
ms.openlocfilehash: e7c92dcc9ce472c50af6f0aa26c59f55d62fbb9f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239934"
---
# <a name="1002---workflowapplicationterminated"></a><span data-ttu-id="cdeff-102">1002 - WorkflowApplicationTerminated</span><span class="sxs-lookup"><span data-stu-id="cdeff-102">1002 - WorkflowApplicationTerminated</span></span>

## <a name="properties"></a><span data-ttu-id="cdeff-103">属性</span><span class="sxs-lookup"><span data-stu-id="cdeff-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="cdeff-104">ID</span><span class="sxs-lookup"><span data-stu-id="cdeff-104">ID</span></span>|<span data-ttu-id="cdeff-105">1002</span><span class="sxs-lookup"><span data-stu-id="cdeff-105">1002</span></span>|  
|<span data-ttu-id="cdeff-106">关键字</span><span class="sxs-lookup"><span data-stu-id="cdeff-106">Keywords</span></span>|<span data-ttu-id="cdeff-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="cdeff-107">WFRuntime</span></span>|  
|<span data-ttu-id="cdeff-108">Level</span><span class="sxs-lookup"><span data-stu-id="cdeff-108">Level</span></span>|<span data-ttu-id="cdeff-109">信息</span><span class="sxs-lookup"><span data-stu-id="cdeff-109">Information</span></span>|  
|<span data-ttu-id="cdeff-110">通道</span><span class="sxs-lookup"><span data-stu-id="cdeff-110">Channel</span></span>|<span data-ttu-id="cdeff-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="cdeff-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="cdeff-112">描述</span><span class="sxs-lookup"><span data-stu-id="cdeff-112">Description</span></span>  

 <span data-ttu-id="cdeff-113">指示工作流应用程序因出现异常而在“出错”状态下终止。</span><span class="sxs-lookup"><span data-stu-id="cdeff-113">Indicates a workflow application has terminated in the Faulted state with an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="cdeff-114">消息</span><span class="sxs-lookup"><span data-stu-id="cdeff-114">Message</span></span>  

 <span data-ttu-id="cdeff-115">WorkflowApplication Id“%1”已终止。</span><span class="sxs-lookup"><span data-stu-id="cdeff-115">WorkflowApplication Id: '%1' was terminated.</span></span> <span data-ttu-id="cdeff-116">该应用程序因出现异常而在“出错”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="cdeff-116">It has completed in the Faulted state with an exception.</span></span>  
  
## <a name="details"></a><span data-ttu-id="cdeff-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="cdeff-117">Details</span></span>  
  
|<span data-ttu-id="cdeff-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="cdeff-118">Data Item Name</span></span>|<span data-ttu-id="cdeff-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="cdeff-119">Data Item Type</span></span>|<span data-ttu-id="cdeff-120">描述</span><span class="sxs-lookup"><span data-stu-id="cdeff-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="cdeff-121">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="cdeff-121">WorkflowApplicationId</span></span>|`xs:string`|<span data-ttu-id="cdeff-122">工作流应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="cdeff-122">The workflow application id</span></span>|  
|<span data-ttu-id="cdeff-123">异常</span><span class="sxs-lookup"><span data-stu-id="cdeff-123">Exception</span></span>|`xs:string`|<span data-ttu-id="cdeff-124">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="cdeff-124">The exception details for the exception</span></span>|  
|<span data-ttu-id="cdeff-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="cdeff-125">AppDomain</span></span>|`xs:string`|<span data-ttu-id="cdeff-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="cdeff-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
