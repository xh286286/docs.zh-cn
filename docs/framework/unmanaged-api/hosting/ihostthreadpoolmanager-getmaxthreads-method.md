---
title: IHostThreadPoolManager::GetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetMaxThreads
helpviewer_keywords:
- IHostThreadPoolManager::GetMaxThreads method [.NET Framework hosting]
- GetMaxThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: db268876-6178-4a81-aca3-318ee7f96001
topic_type:
- apiref
ms.openlocfilehash: 3aecebe2803d3a795db801491d0f60a5eb7c00ce
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730781"
---
# <a name="ihostthreadpoolmanagergetmaxthreads-method"></a><span data-ttu-id="007ba-102">IHostThreadPoolManager::GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="007ba-102">IHostThreadPoolManager::GetMaxThreads Method</span></span>

<span data-ttu-id="007ba-103">获取主机在线程池中并发维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="007ba-103">Gets the maximum number of threads that the host maintains concurrently in the thread pool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="007ba-104">语法</span><span class="sxs-lookup"><span data-stu-id="007ba-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMaxThreads (  
    [out] DWORD *pdwMaxWorkerThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="007ba-105">参数</span><span class="sxs-lookup"><span data-stu-id="007ba-105">Parameters</span></span>  

 `pdwMaxWorkerThreads`  
 <span data-ttu-id="007ba-106">弄一个指针，它指向主机在线程池中维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="007ba-106">[out] A pointer to the maximum number of threads that the host maintains in the thread pool.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="007ba-107">返回值</span><span class="sxs-lookup"><span data-stu-id="007ba-107">Return Value</span></span>  
  
|<span data-ttu-id="007ba-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="007ba-108">HRESULT</span></span>|<span data-ttu-id="007ba-109">说明</span><span class="sxs-lookup"><span data-stu-id="007ba-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="007ba-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="007ba-110">S_OK</span></span>|<span data-ttu-id="007ba-111">`GetMaxThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="007ba-111">`GetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="007ba-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="007ba-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="007ba-113"> (CLR ( 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="007ba-113">The common language runtime (CLR( has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="007ba-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="007ba-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="007ba-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="007ba-115">The call timed out.</span></span>|  
|<span data-ttu-id="007ba-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="007ba-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="007ba-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="007ba-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="007ba-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="007ba-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="007ba-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="007ba-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="007ba-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="007ba-120">E_FAIL</span></span>|<span data-ttu-id="007ba-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="007ba-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="007ba-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="007ba-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="007ba-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="007ba-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="007ba-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="007ba-124">E_NOTIMPL</span></span>|<span data-ttu-id="007ba-125">宿主不提供的实现 `GetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="007ba-125">The host does not provide an implementation of `GetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="007ba-126">注解</span><span class="sxs-lookup"><span data-stu-id="007ba-126">Remarks</span></span>  

 <span data-ttu-id="007ba-127">CLR 调用 `GetMaxThreads` 来确定线程池中线程的总数。</span><span class="sxs-lookup"><span data-stu-id="007ba-127">The CLR calls `GetMaxThreads` to determine the total number of threads in the thread pool.</span></span> <span data-ttu-id="007ba-128">[GetAvailableThreads](ihostthreadpoolmanager-getavailablethreads-method.md)方法获取当前未处理工作项的线程数。</span><span class="sxs-lookup"><span data-stu-id="007ba-128">The [GetAvailableThreads](ihostthreadpoolmanager-getavailablethreads-method.md) method gets the number of threads that are not currently processing work items.</span></span> <span data-ttu-id="007ba-129">所有超出参数返回值的请求将 `pdwMaxWorkerThreads` 保持排队状态，直到线程变为可用。</span><span class="sxs-lookup"><span data-stu-id="007ba-129">All requests above the returned value of the `pdwMaxWorkerThreads` parameter remain queued until threads become available.</span></span>  
  
 <span data-ttu-id="007ba-130">如果主机未提供的实现 `GetMaxThreads` ，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="007ba-130">If the host does not provide an implementation of `GetMaxThreads`, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="007ba-131">要求</span><span class="sxs-lookup"><span data-stu-id="007ba-131">Requirements</span></span>  

 <span data-ttu-id="007ba-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="007ba-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="007ba-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="007ba-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="007ba-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="007ba-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="007ba-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="007ba-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="007ba-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="007ba-136">See also</span></span>

- <xref:System.Threading.ThreadPool.GetMaxThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="007ba-137">GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="007ba-137">GetMinThreads Method</span></span>](ihostthreadpoolmanager-getminthreads-method.md)
- [<span data-ttu-id="007ba-138">SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="007ba-138">SetMaxThreads Method</span></span>](ihostthreadpoolmanager-setmaxthreads-method.md)
- [<span data-ttu-id="007ba-139">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="007ba-139">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
