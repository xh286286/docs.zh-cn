---
title: IHostGCManager::SuspensionStarting 方法
ms.date: 03/30/2017
api_name:
- IHostGCManager.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager::SuspensionStarting
helpviewer_keywords:
- SuspensionStarting method, IHostGCManager interface [.NET Framework hosting]
- IHostGCManager::SuspensionStarting method [.NET Framework hosting]
ms.assetid: c381f524-94cf-4fa2-9298-50f847a03431
topic_type:
- apiref
ms.openlocfilehash: 7e610676e86dde3ab0bdea2ce2314f02b3da9976
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729494"
---
# <a name="ihostgcmanagersuspensionstarting-method"></a><span data-ttu-id="06406-102">IHostGCManager::SuspensionStarting 方法</span><span class="sxs-lookup"><span data-stu-id="06406-102">IHostGCManager::SuspensionStarting Method</span></span>

<span data-ttu-id="06406-103">向宿主通知公共语言运行时 (CLR) 正在暂停执行任务，以执行垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="06406-103">Notifies the host that the common language runtime (CLR) is suspending execution of tasks, to perform a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06406-104">语法</span><span class="sxs-lookup"><span data-stu-id="06406-104">Syntax</span></span>  
  
```cpp  
HRESULT SuspensionStarting ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="06406-105">返回值</span><span class="sxs-lookup"><span data-stu-id="06406-105">Return Value</span></span>  
  
|<span data-ttu-id="06406-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="06406-106">HRESULT</span></span>|<span data-ttu-id="06406-107">说明</span><span class="sxs-lookup"><span data-stu-id="06406-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="06406-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="06406-108">S_OK</span></span>|<span data-ttu-id="06406-109">`SuspensionStarting` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="06406-109">`SuspensionStarting` returned successfully.</span></span>|  
|<span data-ttu-id="06406-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="06406-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="06406-111">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="06406-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="06406-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="06406-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="06406-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="06406-113">The call timed out.</span></span>|  
|<span data-ttu-id="06406-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="06406-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="06406-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="06406-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="06406-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="06406-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="06406-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="06406-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="06406-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="06406-118">E_FAIL</span></span>|<span data-ttu-id="06406-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="06406-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="06406-120">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="06406-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="06406-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="06406-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06406-122">注解</span><span class="sxs-lookup"><span data-stu-id="06406-122">Remarks</span></span>  

 <span data-ttu-id="06406-123">CLR 调用 `SuspensionStarting` 来通知主机发生垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="06406-123">The CLR calls `SuspensionStarting` to inform the host that garbage collection is occurring.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="06406-124">不要重新计划此任务。</span><span class="sxs-lookup"><span data-stu-id="06406-124">Do not reschedule this task.</span></span> <span data-ttu-id="06406-125">调用 [ThreadIsBlockingForSuspension](ihostgcmanager-threadisblockingforsuspension-method.md) 时，主机必须重新安排任务。</span><span class="sxs-lookup"><span data-stu-id="06406-125">The host must reschedule a task when [ThreadIsBlockingForSuspension](ihostgcmanager-threadisblockingforsuspension-method.md) is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06406-126">要求</span><span class="sxs-lookup"><span data-stu-id="06406-126">Requirements</span></span>  

 <span data-ttu-id="06406-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06406-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06406-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="06406-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="06406-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="06406-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="06406-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06406-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06406-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06406-131">See also</span></span>

- [<span data-ttu-id="06406-132">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="06406-132">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="06406-133">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="06406-133">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="06406-134">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="06406-134">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="06406-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="06406-135">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="06406-136">IHostGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="06406-136">IHostGCManager Interface</span></span>](ihostgcmanager-interface.md)
