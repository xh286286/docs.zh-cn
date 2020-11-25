---
title: IHostThreadPoolManager::GetAvailableThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetAvailableThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetAvailableThreads
helpviewer_keywords:
- GetAvailableThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
- IHostThreadPoolManager::GetAvailableThreads method [.NET Framework hosting]
ms.assetid: 61d26dfd-7f24-4e7d-a63e-b30a463f08e1
topic_type:
- apiref
ms.openlocfilehash: 64d5ba9ad5557f99b175c277d48003529d77861c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730794"
---
# <a name="ihostthreadpoolmanagergetavailablethreads-method"></a><span data-ttu-id="6c473-102">IHostThreadPoolManager::GetAvailableThreads 方法</span><span class="sxs-lookup"><span data-stu-id="6c473-102">IHostThreadPoolManager::GetAvailableThreads Method</span></span>

<span data-ttu-id="6c473-103">获取线程池中当前未处理工作项的线程的数目。</span><span class="sxs-lookup"><span data-stu-id="6c473-103">Gets the number of threads in the thread pool that are not currently processing work items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c473-104">语法</span><span class="sxs-lookup"><span data-stu-id="6c473-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAvailableThreads (  
    [out] DWORD *pdwAvailableWorkerThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6c473-105">参数</span><span class="sxs-lookup"><span data-stu-id="6c473-105">Parameters</span></span>  

 `pdwAvailableWorkerThreads`  
 <span data-ttu-id="6c473-106">弄一个指针，指向线程池中当前未处理工作项的线程数。</span><span class="sxs-lookup"><span data-stu-id="6c473-106">[out] Pointer to the number of threads in the thread pool that are not currently processing work items.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6c473-107">返回值</span><span class="sxs-lookup"><span data-stu-id="6c473-107">Return Value</span></span>  
  
|<span data-ttu-id="6c473-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6c473-108">HRESULT</span></span>|<span data-ttu-id="6c473-109">说明</span><span class="sxs-lookup"><span data-stu-id="6c473-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6c473-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c473-110">S_OK</span></span>|<span data-ttu-id="6c473-111">`GetAvailableThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="6c473-111">`GetAvailableThreads` returned successfully.</span></span>|  
|<span data-ttu-id="6c473-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6c473-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6c473-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="6c473-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6c473-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6c473-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6c473-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="6c473-115">The call timed out.</span></span>|  
|<span data-ttu-id="6c473-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6c473-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6c473-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="6c473-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6c473-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6c473-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6c473-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="6c473-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6c473-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6c473-120">E_FAIL</span></span>|<span data-ttu-id="6c473-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="6c473-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6c473-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="6c473-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6c473-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="6c473-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="6c473-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="6c473-124">E_NOTIMPL</span></span>|<span data-ttu-id="6c473-125">宿主不提供的实现 `GetAvailableThreads` 。</span><span class="sxs-lookup"><span data-stu-id="6c473-125">The host does not provide an implementation of `GetAvailableThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6c473-126">注解</span><span class="sxs-lookup"><span data-stu-id="6c473-126">Remarks</span></span>  

 <span data-ttu-id="6c473-127">如果主机未提供的实现 `GetAvailableThreads` ，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="6c473-127">If the host does not provide an implementation of `GetAvailableThreads`, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c473-128">要求</span><span class="sxs-lookup"><span data-stu-id="6c473-128">Requirements</span></span>  

 <span data-ttu-id="6c473-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c473-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c473-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6c473-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6c473-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6c473-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6c473-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c473-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c473-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c473-133">See also</span></span>

- <xref:System.Threading.ThreadPool.GetAvailableThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="6c473-134">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="6c473-134">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
