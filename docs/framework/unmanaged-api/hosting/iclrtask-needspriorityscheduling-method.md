---
title: ICLRTask::NeedsPriorityScheduling 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.NeedsPriorityScheduling
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::NeedsPriorityScheduling
helpviewer_keywords:
- ICLRTask::NeedsPriorityScheduling method [.NET Framework hosting]
- NeedsPriorityScheduling method [.NET Framework hosting]
ms.assetid: 9c9db3f3-26bf-4317-88de-5eb926a22a1d
topic_type:
- apiref
ms.openlocfilehash: 86e0899b883f09f2e7b27c0f957e943deb73bb66
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95690793"
---
# <a name="iclrtaskneedspriorityscheduling-method"></a><span data-ttu-id="418cb-102">ICLRTask::NeedsPriorityScheduling 方法</span><span class="sxs-lookup"><span data-stu-id="418cb-102">ICLRTask::NeedsPriorityScheduling Method</span></span>

<span data-ttu-id="418cb-103">获取一个值，该值指示当前要切换的任务是否需要标记为高优先级才能进行重新计划。</span><span class="sxs-lookup"><span data-stu-id="418cb-103">Gets a value that indicates whether the current task, which is being switched out, needs to be marked as a high priority for rescheduling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="418cb-104">语法</span><span class="sxs-lookup"><span data-stu-id="418cb-104">Syntax</span></span>  
  
```cpp  
HRESULT NeedsPriorityScheduling (  
    [out] BOOL *pbNeedsPriorityScheduling  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="418cb-105">参数</span><span class="sxs-lookup"><span data-stu-id="418cb-105">Parameters</span></span>  

 `pbNeedsPriorityRescheduling`  
 <span data-ttu-id="418cb-106">[out] `true` 如果宿主应尽快尝试重新计划当前任务实例，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="418cb-106">[out] `true`, if the host should attempt to reschedule the current task instance as soon as possible; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="418cb-107">返回值</span><span class="sxs-lookup"><span data-stu-id="418cb-107">Return Value</span></span>  
  
|<span data-ttu-id="418cb-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="418cb-108">HRESULT</span></span>|<span data-ttu-id="418cb-109">说明</span><span class="sxs-lookup"><span data-stu-id="418cb-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="418cb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="418cb-110">S_OK</span></span>|<span data-ttu-id="418cb-111">`NeedsPriorityRescheduling` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="418cb-111">`NeedsPriorityRescheduling` returned successfully.</span></span>|  
|<span data-ttu-id="418cb-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="418cb-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="418cb-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="418cb-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="418cb-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="418cb-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="418cb-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="418cb-115">The call timed out.</span></span>|  
|<span data-ttu-id="418cb-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="418cb-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="418cb-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="418cb-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="418cb-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="418cb-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="418cb-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="418cb-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="418cb-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="418cb-120">E_FAIL</span></span>|<span data-ttu-id="418cb-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="418cb-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="418cb-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="418cb-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="418cb-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="418cb-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="418cb-124">注解</span><span class="sxs-lookup"><span data-stu-id="418cb-124">Remarks</span></span>  

 <span data-ttu-id="418cb-125">在任务接近垃圾回收器收集的情况下，CLR 将的值设置 `pbNeedsPriorityScheduling` 为 `true` ，以指示高优先级重新计划。</span><span class="sxs-lookup"><span data-stu-id="418cb-125">In situations where the task is close to being collected by the garbage collector, the CLR sets the value of `pbNeedsPriorityScheduling` to `true`, indicating high-priority rescheduling.</span></span> <span data-ttu-id="418cb-126">这使主机可以快速重新计划任务，从而最大程度地减少垃圾回收延迟的可能性，并使宿主和运行时能够在保存内存资源时进行合作。</span><span class="sxs-lookup"><span data-stu-id="418cb-126">This allows the host to reschedule the task quickly, thereby minimizing the potential for delays in garbage collection, and enabling the host and the runtime to cooperate in conserving memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="418cb-127">要求</span><span class="sxs-lookup"><span data-stu-id="418cb-127">Requirements</span></span>  

 <span data-ttu-id="418cb-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="418cb-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="418cb-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="418cb-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="418cb-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="418cb-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="418cb-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="418cb-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="418cb-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="418cb-132">See also</span></span>

- [<span data-ttu-id="418cb-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="418cb-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="418cb-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="418cb-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="418cb-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="418cb-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="418cb-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="418cb-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
