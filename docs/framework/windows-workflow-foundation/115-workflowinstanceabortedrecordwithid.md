---
title: 115 - WorkflowInstanceAbortedRecordWithId
ms.date: 03/30/2017
ms.assetid: 0293dd4e-e6ae-473a-b3d6-c2d38f9bd875
ms.openlocfilehash: 69c0c58de36a7fff916b11deba888b7cef7c626e
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96285143"
---
# <a name="115---workflowinstanceabortedrecordwithid"></a><span data-ttu-id="e6011-102">115 - WorkflowInstanceAbortedRecordWithId</span><span class="sxs-lookup"><span data-stu-id="e6011-102">115 - WorkflowInstanceAbortedRecordWithId</span></span>

## <a name="properties"></a><span data-ttu-id="e6011-103">属性</span><span class="sxs-lookup"><span data-stu-id="e6011-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e6011-104">ID</span><span class="sxs-lookup"><span data-stu-id="e6011-104">ID</span></span>|<span data-ttu-id="e6011-105">115</span><span class="sxs-lookup"><span data-stu-id="e6011-105">115</span></span>|  
|<span data-ttu-id="e6011-106">关键字</span><span class="sxs-lookup"><span data-stu-id="e6011-106">Keywords</span></span>|<span data-ttu-id="e6011-107">HealthMonitoring、WFTracking</span><span class="sxs-lookup"><span data-stu-id="e6011-107">HealthMonitoring, WFTracking</span></span>|  
|<span data-ttu-id="e6011-108">Level</span><span class="sxs-lookup"><span data-stu-id="e6011-108">Level</span></span>|<span data-ttu-id="e6011-109">警告</span><span class="sxs-lookup"><span data-stu-id="e6011-109">Warning</span></span>|  
|<span data-ttu-id="e6011-110">通道</span><span class="sxs-lookup"><span data-stu-id="e6011-110">Channel</span></span>|<span data-ttu-id="e6011-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="e6011-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e6011-112">描述</span><span class="sxs-lookup"><span data-stu-id="e6011-112">Description</span></span>  

 <span data-ttu-id="e6011-113">当工作流实例发出 WorkflowInstanceAbortedRecord 时，ETW 跟踪参与者将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="e6011-113">This event is emitted by the ETW tracking participant when a workflow instance emits WorkflowInstanceAbortedRecord.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e6011-114">消息</span><span class="sxs-lookup"><span data-stu-id="e6011-114">Message</span></span>  

 <span data-ttu-id="e6011-115">TrackRecord = WorkflowInstanceAbortedRecord，InstanceID = %1，RecordNumber = %2，EventTime = %3，ActivityDefinitionId = %4，Reason = %5，Annotations = %6，ProfileName = %7，WorkflowDefinitionIdentity = %8</span><span class="sxs-lookup"><span data-stu-id="e6011-115">TrackRecord = WorkflowInstanceAbortedRecord, InstanceID = %1, RecordNumber = %2, EventTime = %3, ActivityDefinitionId = %4, Reason = %5,  Annotations = %6, ProfileName = %7, WorkflowDefinitionIdentity = %8</span></span>  
  
## <a name="details"></a><span data-ttu-id="e6011-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="e6011-116">Details</span></span>  
  
|<span data-ttu-id="e6011-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e6011-117">Data Item Name</span></span>|<span data-ttu-id="e6011-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e6011-118">Data Item Type</span></span>|<span data-ttu-id="e6011-119">描述</span><span class="sxs-lookup"><span data-stu-id="e6011-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e6011-120">InstanceId</span><span class="sxs-lookup"><span data-stu-id="e6011-120">InstanceId</span></span>|<span data-ttu-id="e6011-121">xs:GUID</span><span class="sxs-lookup"><span data-stu-id="e6011-121">xs:GUID</span></span>|<span data-ttu-id="e6011-122">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="e6011-122">The instance id for the workflow</span></span>|  
|<span data-ttu-id="e6011-123">RecordNumber</span><span class="sxs-lookup"><span data-stu-id="e6011-123">RecordNumber</span></span>|<span data-ttu-id="e6011-124">xs:long</span><span class="sxs-lookup"><span data-stu-id="e6011-124">xs:long</span></span>|<span data-ttu-id="e6011-125">发出的记录的序列号</span><span class="sxs-lookup"><span data-stu-id="e6011-125">The sequence number of the emitted record</span></span>|  
|<span data-ttu-id="e6011-126">EventTime</span><span class="sxs-lookup"><span data-stu-id="e6011-126">EventTime</span></span>|<span data-ttu-id="e6011-127">xs:dateTime</span><span class="sxs-lookup"><span data-stu-id="e6011-127">xs:dateTime</span></span>|<span data-ttu-id="e6011-128">发出该事件时的 UTC 时间</span><span class="sxs-lookup"><span data-stu-id="e6011-128">The time in UTC when the event was emitted</span></span>|  
|<span data-ttu-id="e6011-129">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e6011-129">ActivityDefinitionId</span></span>|<span data-ttu-id="e6011-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6011-130">xs:string</span></span>|<span data-ttu-id="e6011-131">工作流中根活动的名称</span><span class="sxs-lookup"><span data-stu-id="e6011-131">The name of the root activity in the workflow</span></span>|  
|<span data-ttu-id="e6011-132">状态</span><span class="sxs-lookup"><span data-stu-id="e6011-132">State</span></span>|<span data-ttu-id="e6011-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6011-133">xs:string</span></span>|<span data-ttu-id="e6011-134">工作流的当前状态。</span><span class="sxs-lookup"><span data-stu-id="e6011-134">The current state of the Workflow.</span></span>|  
|<span data-ttu-id="e6011-135">批注</span><span class="sxs-lookup"><span data-stu-id="e6011-135">Annotations</span></span>|<span data-ttu-id="e6011-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6011-136">xs:string</span></span>|<span data-ttu-id="e6011-137">已添加到此事件中的批注。</span><span class="sxs-lookup"><span data-stu-id="e6011-137">The annotations that were added to this event.</span></span> <span data-ttu-id="e6011-138">值存储在 xml 元素中，格式为 \<items> \< item name = "annotationName" type="System.String"> a \</item> \</items> 。</span><span class="sxs-lookup"><span data-stu-id="e6011-138">The values are stored in an xml element in the format \<items>\< item name = "annotationName" type="System.String">annotationValue\</item>\</items>.</span></span> <span data-ttu-id="e6011-139">如果未指定任何批注，则该字符串包含 \<items/> 。</span><span class="sxs-lookup"><span data-stu-id="e6011-139">If no annotations are specified then the string contains \<items/>.</span></span> <span data-ttu-id="e6011-140">ETW 事件大小受到 ETW 缓冲区大小或 ETW 事件最大负载的限制。</span><span class="sxs-lookup"><span data-stu-id="e6011-140">The ETW event size is limited by the ETW buffer size or the max payload for an ETW event.</span></span> <span data-ttu-id="e6011-141">如果事件的大小超过 ETW 限制，则通过删除批注并将批注值替换为 ... 来截断事件。 \<items> \</items></span><span class="sxs-lookup"><span data-stu-id="e6011-141">If the size of the event exceeds the ETW limits, then the event is truncated by dropping the annotations and replacing the annotation value with \<items>...\</items>.</span></span>|  
|<span data-ttu-id="e6011-142">ProfileName</span><span class="sxs-lookup"><span data-stu-id="e6011-142">ProfileName</span></span>|<span data-ttu-id="e6011-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6011-143">xs:string</span></span>|<span data-ttu-id="e6011-144">导致发出此事件的跟踪配置文件的名称</span><span class="sxs-lookup"><span data-stu-id="e6011-144">The name or the tracking profile that resulted in this event being emitted</span></span>|  
|<span data-ttu-id="e6011-145">WorkflowDefinitionIdentity</span><span class="sxs-lookup"><span data-stu-id="e6011-145">WorkflowDefinitionIdentity</span></span>|<span data-ttu-id="e6011-146">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6011-146">xs:string</span></span>|<span data-ttu-id="e6011-147">工作流定义 ID</span><span class="sxs-lookup"><span data-stu-id="e6011-147">The workflow definition id</span></span>|  
|<span data-ttu-id="e6011-148">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e6011-148">AppDomain</span></span>|<span data-ttu-id="e6011-149">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6011-149">xs:string</span></span>|<span data-ttu-id="e6011-150">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e6011-150">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
