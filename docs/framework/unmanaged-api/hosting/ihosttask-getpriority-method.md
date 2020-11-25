---
title: IHostTask::GetPriority 方法
ms.date: 03/30/2017
api_name:
- IHostTask.GetPriority
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::GetPriority
helpviewer_keywords:
- GetPriority method [.NET Framework hosting]
- IHostTask::GetPriority method [.NET Framework hosting]
ms.assetid: 4b463cd6-77c1-4f9a-8518-346ad8fc4b70
topic_type:
- apiref
ms.openlocfilehash: d30dcbe4e7c289c23c5af00e4bdadedc186809b4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714765"
---
# <a name="ihosttaskgetpriority-method"></a><span data-ttu-id="4afbe-102">IHostTask::GetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="4afbe-102">IHostTask::GetPriority Method</span></span>

<span data-ttu-id="4afbe-103">获取当前 [IHostTask](ihosttask-interface.md) 实例所表示的任务的线程优先级别。</span><span class="sxs-lookup"><span data-stu-id="4afbe-103">Gets the thread priority level of the task represented by the current [IHostTask](ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4afbe-104">语法</span><span class="sxs-lookup"><span data-stu-id="4afbe-104">Syntax</span></span>  
  
```cpp  
HRESULT GetPriority (  
    [out] int *pPriority  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4afbe-105">参数</span><span class="sxs-lookup"><span data-stu-id="4afbe-105">Parameters</span></span>  

 `pPriority`  
 <span data-ttu-id="4afbe-106">弄指向一个整数的指针，该整数指示当前实例所表示的任务的线程优先级别 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="4afbe-106">[out] A pointer to an integer that indicates the thread priority level of the task represented by the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4afbe-107">返回值</span><span class="sxs-lookup"><span data-stu-id="4afbe-107">Return Value</span></span>  
  
|<span data-ttu-id="4afbe-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4afbe-108">HRESULT</span></span>|<span data-ttu-id="4afbe-109">说明</span><span class="sxs-lookup"><span data-stu-id="4afbe-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4afbe-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4afbe-110">S_OK</span></span>|<span data-ttu-id="4afbe-111">`GetPriority` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="4afbe-111">`GetPriority` returned successfully.</span></span>|  
|<span data-ttu-id="4afbe-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="4afbe-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="4afbe-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="4afbe-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="4afbe-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="4afbe-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="4afbe-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="4afbe-115">The call timed out.</span></span>|  
|<span data-ttu-id="4afbe-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="4afbe-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="4afbe-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="4afbe-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="4afbe-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="4afbe-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="4afbe-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="4afbe-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="4afbe-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="4afbe-120">E_FAIL</span></span>|<span data-ttu-id="4afbe-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="4afbe-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="4afbe-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="4afbe-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="4afbe-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="4afbe-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4afbe-124">注解</span><span class="sxs-lookup"><span data-stu-id="4afbe-124">Remarks</span></span>  

 <span data-ttu-id="4afbe-125">线程优先级别值由 Win32 `SetThreadPriority` 函数定义。</span><span class="sxs-lookup"><span data-stu-id="4afbe-125">Thread priority level values are defined by the Win32 `SetThreadPriority` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4afbe-126">要求</span><span class="sxs-lookup"><span data-stu-id="4afbe-126">Requirements</span></span>  

 <span data-ttu-id="4afbe-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4afbe-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4afbe-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="4afbe-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4afbe-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4afbe-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4afbe-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4afbe-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4afbe-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4afbe-131">See also</span></span>

- [<span data-ttu-id="4afbe-132">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="4afbe-132">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="4afbe-133">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="4afbe-133">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="4afbe-134">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="4afbe-134">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="4afbe-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="4afbe-135">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
