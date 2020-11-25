---
title: IHostThreadPoolManager::SetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.SetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::SetMaxThreads
helpviewer_keywords:
- IHostThreadPoolManager::SetMaxThreads method [.NET Framework hosting]
- SetMaxThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: 77cfd347-95c2-4425-b807-4ecc2a8d4578
topic_type:
- apiref
ms.openlocfilehash: 68e806daa63d13ad6c1f3b5de634c20ca02e8eb4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730705"
---
# <a name="ihostthreadpoolmanagersetmaxthreads-method"></a><span data-ttu-id="ec27f-102">IHostThreadPoolManager::SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="ec27f-102">IHostThreadPoolManager::SetMaxThreads Method</span></span>

<span data-ttu-id="ec27f-103">设置宿主可在线程池中维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="ec27f-103">Sets the maximum number of threads that the host can maintain in the thread pool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec27f-104">语法</span><span class="sxs-lookup"><span data-stu-id="ec27f-104">Syntax</span></span>  
  
```cpp  
HRESULT SetMaxThreads (  
    [in] DWORD MaxThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec27f-105">参数</span><span class="sxs-lookup"><span data-stu-id="ec27f-105">Parameters</span></span>  

 `MaxThreads`  
 <span data-ttu-id="ec27f-106">线程池中辅助线程的最大数目。</span><span class="sxs-lookup"><span data-stu-id="ec27f-106">The maximum number of worker threads in the thread pool.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ec27f-107">返回值</span><span class="sxs-lookup"><span data-stu-id="ec27f-107">Return Value</span></span>  
  
|<span data-ttu-id="ec27f-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ec27f-108">HRESULT</span></span>|<span data-ttu-id="ec27f-109">说明</span><span class="sxs-lookup"><span data-stu-id="ec27f-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ec27f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec27f-110">S_OK</span></span>|<span data-ttu-id="ec27f-111">`SetMaxThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ec27f-111">`SetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="ec27f-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ec27f-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ec27f-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ec27f-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ec27f-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ec27f-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ec27f-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ec27f-115">The call timed out.</span></span>|  
|<span data-ttu-id="ec27f-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ec27f-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ec27f-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ec27f-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ec27f-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ec27f-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ec27f-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ec27f-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ec27f-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ec27f-120">E_FAIL</span></span>|<span data-ttu-id="ec27f-121">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ec27f-121">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="ec27f-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ec27f-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ec27f-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ec27f-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ec27f-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="ec27f-124">E_NOTIMPL</span></span>|<span data-ttu-id="ec27f-125">宿主不提供的实现 `SetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="ec27f-125">The host does not provide an implementation of `SetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ec27f-126">注解</span><span class="sxs-lookup"><span data-stu-id="ec27f-126">Remarks</span></span>  

 <span data-ttu-id="ec27f-127">宿主无需允许 CLR 配置线程池的大小。</span><span class="sxs-lookup"><span data-stu-id="ec27f-127">A host is not required to allow the CLR to configure the size of the thread pool.</span></span> <span data-ttu-id="ec27f-128">出于实现、性能或可伸缩性等原因，某些主机可能需要对线程池进行独占控制。</span><span class="sxs-lookup"><span data-stu-id="ec27f-128">Some hosts might want exclusive control over the thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="ec27f-129">在这种情况下，主机应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="ec27f-129">In this case, a host should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec27f-130">要求</span><span class="sxs-lookup"><span data-stu-id="ec27f-130">Requirements</span></span>  

 <span data-ttu-id="ec27f-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ec27f-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec27f-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ec27f-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ec27f-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ec27f-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ec27f-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec27f-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec27f-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ec27f-135">See also</span></span>

- <xref:System.Threading.ThreadPool.SetMaxThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="ec27f-136">GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="ec27f-136">GetMaxThreads Method</span></span>](ihostthreadpoolmanager-getmaxthreads-method.md)
- [<span data-ttu-id="ec27f-137">SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="ec27f-137">SetMinThreads Method</span></span>](ihostthreadpoolmanager-setminthreads-method.md)
- [<span data-ttu-id="ec27f-138">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="ec27f-138">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
