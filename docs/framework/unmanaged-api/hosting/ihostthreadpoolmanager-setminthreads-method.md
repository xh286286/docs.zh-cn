---
title: IHostThreadPoolManager::SetMinThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.SetMinThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::SetMinThreads
helpviewer_keywords:
- SetMinThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
- IHostThreadPoolManager::SetMinThreads method [.NET Framework hosting]
ms.assetid: 10409db9-9fd2-4e4d-b8cd-cf6fec0afaa2
topic_type:
- apiref
ms.openlocfilehash: d6f56f689a35fa025a924be0db67c893f160fc7f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730729"
---
# <a name="ihostthreadpoolmanagersetminthreads-method"></a><span data-ttu-id="2339a-102">IHostThreadPoolManager::SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="2339a-102">IHostThreadPoolManager::SetMinThreads Method</span></span>

<span data-ttu-id="2339a-103">设置主机在预期请求中必须保持的空闲线程的最小数目。</span><span class="sxs-lookup"><span data-stu-id="2339a-103">Sets the minimum number of idle threads that the host must maintain in anticipation of requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2339a-104">语法</span><span class="sxs-lookup"><span data-stu-id="2339a-104">Syntax</span></span>  
  
```cpp  
HRESULT SetMinThreads (  
    [in] DWORD MinThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2339a-105">参数</span><span class="sxs-lookup"><span data-stu-id="2339a-105">Parameters</span></span>  

 `MinThreads`  
 <span data-ttu-id="2339a-106">中宿主必须维持的新最小线程数。</span><span class="sxs-lookup"><span data-stu-id="2339a-106">[in] The new minimum number of threads that the host must maintain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2339a-107">返回值</span><span class="sxs-lookup"><span data-stu-id="2339a-107">Return Value</span></span>  
  
|<span data-ttu-id="2339a-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2339a-108">HRESULT</span></span>|<span data-ttu-id="2339a-109">说明</span><span class="sxs-lookup"><span data-stu-id="2339a-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2339a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2339a-110">S_OK</span></span>|<span data-ttu-id="2339a-111">`SetMinThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="2339a-111">`SetMinThreads` returned successfully.</span></span>|  
|<span data-ttu-id="2339a-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2339a-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2339a-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="2339a-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2339a-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2339a-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2339a-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="2339a-115">The call timed out.</span></span>|  
|<span data-ttu-id="2339a-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2339a-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2339a-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="2339a-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2339a-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2339a-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2339a-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="2339a-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2339a-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2339a-120">E_FAIL</span></span>|<span data-ttu-id="2339a-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="2339a-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2339a-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="2339a-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2339a-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="2339a-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="2339a-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="2339a-124">E_NOTIMPL</span></span>|<span data-ttu-id="2339a-125">宿主不提供的实现 `SetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="2339a-125">The host does not provide an implementation of `SetMinThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2339a-126">注解</span><span class="sxs-lookup"><span data-stu-id="2339a-126">Remarks</span></span>  

 <span data-ttu-id="2339a-127">不要求主机提供的实现 `SetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="2339a-127">A host is not required to provide an implementation of `SetMinThreads`.</span></span> <span data-ttu-id="2339a-128">在这种情况下，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="2339a-128">In this case, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2339a-129">要求</span><span class="sxs-lookup"><span data-stu-id="2339a-129">Requirements</span></span>  

 <span data-ttu-id="2339a-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2339a-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2339a-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2339a-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2339a-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2339a-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2339a-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2339a-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2339a-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2339a-134">See also</span></span>

- <xref:System.Threading.ThreadPool.SetMinThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="2339a-135">GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="2339a-135">GetMinThreads Method</span></span>](ihostthreadpoolmanager-getminthreads-method.md)
- [<span data-ttu-id="2339a-136">SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="2339a-136">SetMaxThreads Method</span></span>](ihostthreadpoolmanager-setmaxthreads-method.md)
- [<span data-ttu-id="2339a-137">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="2339a-137">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
