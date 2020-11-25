---
title: ICLRTask::YieldTask 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.YieldTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::YieldTask
helpviewer_keywords:
- ICLRTask::YieldTask method [.NET Framework hosting]
- YieldTask method [.NET Framework hosting]
ms.assetid: b8eb4095-3a8f-4be3-9446-63e9893dce7d
topic_type:
- apiref
ms.openlocfilehash: 7b9b47daa96ffcb1f66b462ff8e227250c5a81ca
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720270"
---
# <a name="iclrtaskyieldtask-method"></a><span data-ttu-id="beeb1-102">ICLRTask::YieldTask 方法</span><span class="sxs-lookup"><span data-stu-id="beeb1-102">ICLRTask::YieldTask Method</span></span>

<span data-ttu-id="beeb1-103">请求公共语言运行时 (CLR) 放置当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务，并使处理器时间可供其他任务使用。</span><span class="sxs-lookup"><span data-stu-id="beeb1-103">Requests that the common language runtime (CLR) put aside the task that the current [ICLRTask](iclrtask-interface.md) instance represents, and make the processor time available to other tasks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="beeb1-104">语法</span><span class="sxs-lookup"><span data-stu-id="beeb1-104">Syntax</span></span>  
  
```cpp  
HRESULT YieldTask ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="beeb1-105">返回值</span><span class="sxs-lookup"><span data-stu-id="beeb1-105">Return Value</span></span>  
  
|<span data-ttu-id="beeb1-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="beeb1-106">HRESULT</span></span>|<span data-ttu-id="beeb1-107">说明</span><span class="sxs-lookup"><span data-stu-id="beeb1-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="beeb1-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="beeb1-108">S_OK</span></span>|<span data-ttu-id="beeb1-109">`YieldTask` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="beeb1-109">`YieldTask` returned successfully.</span></span>|  
|<span data-ttu-id="beeb1-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="beeb1-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="beeb1-111">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="beeb1-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="beeb1-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="beeb1-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="beeb1-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="beeb1-113">The call timed out.</span></span>|  
|<span data-ttu-id="beeb1-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="beeb1-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="beeb1-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="beeb1-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="beeb1-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="beeb1-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="beeb1-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="beeb1-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="beeb1-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beeb1-118">E_FAIL</span></span>|<span data-ttu-id="beeb1-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="beeb1-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="beeb1-120">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="beeb1-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="beeb1-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="beeb1-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="beeb1-122">注解</span><span class="sxs-lookup"><span data-stu-id="beeb1-122">Remarks</span></span>  

 <span data-ttu-id="beeb1-123">主机调用 `YieldTask` 来请求其他任务或进程的处理器资源。</span><span class="sxs-lookup"><span data-stu-id="beeb1-123">A host calls `YieldTask` to request processor resources for other tasks or processes.</span></span> <span data-ttu-id="beeb1-124">此方法主要用于允许长时间运行的代码放弃 CPU 时间。</span><span class="sxs-lookup"><span data-stu-id="beeb1-124">This method is primarily intended to allow long-running code to give up CPU time.</span></span> <span data-ttu-id="beeb1-125">运行时尝试将当前实例表示的任务置于 `ICLRTask` 可产生处理时间的状态，但不保证成功。</span><span class="sxs-lookup"><span data-stu-id="beeb1-125">The runtime attempts to put the task that the current `ICLRTask` instance represents in a state where it can yield processing time, but makes no guarantee of success.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="beeb1-126">要求</span><span class="sxs-lookup"><span data-stu-id="beeb1-126">Requirements</span></span>  

 <span data-ttu-id="beeb1-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="beeb1-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="beeb1-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="beeb1-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="beeb1-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="beeb1-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="beeb1-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="beeb1-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="beeb1-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="beeb1-131">See also</span></span>

- [<span data-ttu-id="beeb1-132">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="beeb1-132">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="beeb1-133">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="beeb1-133">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="beeb1-134">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="beeb1-134">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="beeb1-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="beeb1-135">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
