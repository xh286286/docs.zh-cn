---
title: IHostSemaphore::Wait 方法
ms.date: 03/30/2017
api_name:
- IHostSemaphore.Wait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore::Wait
helpviewer_keywords:
- IHostSemaphore::Wait method [.NET Framework hosting]
- Wait method, IHostSemaphore interface [.NET Framework hosting]
ms.assetid: 0da962a3-ce55-44dd-ab7a-14ad7105af4a
topic_type:
- apiref
ms.openlocfilehash: 69b2338e6992c386a3cd34a632d69b73a67f14fa
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95682999"
---
# <a name="ihostsemaphorewait-method"></a><span data-ttu-id="6040e-102">IHostSemaphore::Wait 方法</span><span class="sxs-lookup"><span data-stu-id="6040e-102">IHostSemaphore::Wait Method</span></span>

<span data-ttu-id="6040e-103">导致当前 [IHostSemaphore](ihostsemaphore-interface.md) 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="6040e-103">Causes the current [IHostSemaphore](ihostsemaphore-interface.md) instance to wait until it is owned or the specified amount of time elapses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6040e-104">语法</span><span class="sxs-lookup"><span data-stu-id="6040e-104">Syntax</span></span>  
  
```cpp  
HRESULT Wait (  
    [in] DWORD dwMilliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6040e-105">参数</span><span class="sxs-lookup"><span data-stu-id="6040e-105">Parameters</span></span>  

 `dwMilliseconds`  
 <span data-ttu-id="6040e-106">中如果当前实例不属于，则返回前等待的毫秒数 `IHostSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="6040e-106">[in] The number of milliseconds to wait before returning, if the current `IHostSemaphore` instance is not owned.</span></span>  
  
 `option`  
 <span data-ttu-id="6040e-107">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一，指定主机在此操作阻止的情况下应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="6040e-107">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values, specifying what action the host should take if this operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6040e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="6040e-108">Return Value</span></span>  
  
|<span data-ttu-id="6040e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6040e-109">HRESULT</span></span>|<span data-ttu-id="6040e-110">说明</span><span class="sxs-lookup"><span data-stu-id="6040e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6040e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6040e-111">S_OK</span></span>|<span data-ttu-id="6040e-112">`Wait` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="6040e-112">`Wait` returned successfully.</span></span>|  
|<span data-ttu-id="6040e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6040e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6040e-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="6040e-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6040e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6040e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6040e-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="6040e-116">The call timed out.</span></span>|  
|<span data-ttu-id="6040e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6040e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6040e-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="6040e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6040e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6040e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6040e-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="6040e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6040e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6040e-121">E_FAIL</span></span>|<span data-ttu-id="6040e-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="6040e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6040e-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="6040e-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6040e-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="6040e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="6040e-125">HOST_E_DEADLOCK</span><span class="sxs-lookup"><span data-stu-id="6040e-125">HOST_E_DEADLOCK</span></span>|<span data-ttu-id="6040e-126">主机在等待间隔期间检测到死锁，并将当前 `IHostSemaphore` 实例选择为死锁牺牲品。</span><span class="sxs-lookup"><span data-stu-id="6040e-126">The host detected a deadlock during the wait interval, and chose the current `IHostSemaphore` instance as a deadlock victim.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6040e-127">要求</span><span class="sxs-lookup"><span data-stu-id="6040e-127">Requirements</span></span>  

 <span data-ttu-id="6040e-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6040e-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6040e-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6040e-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6040e-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6040e-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6040e-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6040e-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6040e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6040e-132">See also</span></span>

- [<span data-ttu-id="6040e-133">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="6040e-133">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="6040e-134">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="6040e-134">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="6040e-135">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="6040e-135">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="6040e-136">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="6040e-136">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="6040e-137">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="6040e-137">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
