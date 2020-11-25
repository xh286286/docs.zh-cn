---
title: IHostSyncManager::CreateSemaphore 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateSemaphore
helpviewer_keywords:
- CreateSemaphore method [.NET Framework hosting]
- IHostSyncManager::CreateSemaphore method [.NET Framework hosting]
ms.assetid: 37679e94-5ff9-4173-8fa5-457febeb89bf
topic_type:
- apiref
ms.openlocfilehash: 9af38a58ce8786c56d9f50089605dc994167497e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722123"
---
# <a name="ihostsyncmanagercreatesemaphore-method"></a><span data-ttu-id="784ad-102">IHostSyncManager::CreateSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="784ad-102">IHostSyncManager::CreateSemaphore Method</span></span>

<span data-ttu-id="784ad-103">为公共语言运行时 (CLR) 创建一个 [IHostSemaphore](ihostsemaphore-interface.md) 对象，该对象用作等待事件的信号量。</span><span class="sxs-lookup"><span data-stu-id="784ad-103">Creates an [IHostSemaphore](ihostsemaphore-interface.md) object for the common language runtime (CLR) to use as a semaphore for wait events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="784ad-104">语法</span><span class="sxs-lookup"><span data-stu-id="784ad-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateSemaphore (  
    [in]  DWORD dwInitial,  
    [in]  DWORD dwMax,  
    [out] IHostSemaphore **ppSemaphore  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="784ad-105">参数</span><span class="sxs-lookup"><span data-stu-id="784ad-105">Parameters</span></span>  

 `dwInitial`  
 <span data-ttu-id="784ad-106">中的初始计数 `ppSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="784ad-106">[in] The initial count for `ppSemaphore`.</span></span>  
  
 `dwMax`  
 <span data-ttu-id="784ad-107">中的最大计数 `ppSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="784ad-107">[in] The maximum count for `ppSemaphore`.</span></span>  
  
 `ppSemaphore`  
 <span data-ttu-id="784ad-108">弄指向实例的地址的指针 `IHostSemaphore` ; 如果无法创建信号量，则为 null。</span><span class="sxs-lookup"><span data-stu-id="784ad-108">[out] A pointer to the address of an `IHostSemaphore` instance, or null if the semaphore could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="784ad-109">返回值</span><span class="sxs-lookup"><span data-stu-id="784ad-109">Return Value</span></span>  
  
|<span data-ttu-id="784ad-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="784ad-110">HRESULT</span></span>|<span data-ttu-id="784ad-111">说明</span><span class="sxs-lookup"><span data-stu-id="784ad-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="784ad-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="784ad-112">S_OK</span></span>|<span data-ttu-id="784ad-113">`CreateSemaphore` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="784ad-113">`CreateSemaphore` returned successfully.</span></span>|  
|<span data-ttu-id="784ad-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="784ad-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="784ad-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="784ad-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="784ad-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="784ad-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="784ad-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="784ad-117">The call timed out.</span></span>|  
|<span data-ttu-id="784ad-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="784ad-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="784ad-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="784ad-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="784ad-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="784ad-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="784ad-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="784ad-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="784ad-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="784ad-122">E_FAIL</span></span>|<span data-ttu-id="784ad-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="784ad-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="784ad-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="784ad-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="784ad-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="784ad-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="784ad-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="784ad-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="784ad-127">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="784ad-127">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="784ad-128">注解</span><span class="sxs-lookup"><span data-stu-id="784ad-128">Remarks</span></span>  

 <span data-ttu-id="784ad-129">`CreateSemaphore` 镜像同名的 Win32 函数。</span><span class="sxs-lookup"><span data-stu-id="784ad-129">`CreateSemaphore` mirrors the Win32 function that has the same name.</span></span> <span data-ttu-id="784ad-130">`dwInitial`和 `dwMax` 参数分别对信号量和参数使用相同的语义 `lInitialCount` `lMaximumCount` 。</span><span class="sxs-lookup"><span data-stu-id="784ad-130">The `dwInitial` and `dwMax` parameters use the same semantics for the semaphore count as the Win32 `lInitialCount` and `lMaximumCount` parameters, respectively.</span></span> <span data-ttu-id="784ad-131">`dwInitial` 必须介于零和 `dwMax` （含）之间。</span><span class="sxs-lookup"><span data-stu-id="784ad-131">`dwInitial` must be between zero and `dwMax`, inclusive.</span></span> <span data-ttu-id="784ad-132">`dwMax` 必须大于零。</span><span class="sxs-lookup"><span data-stu-id="784ad-132">`dwMax` must be greater than zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="784ad-133">要求</span><span class="sxs-lookup"><span data-stu-id="784ad-133">Requirements</span></span>  

 <span data-ttu-id="784ad-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="784ad-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="784ad-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="784ad-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="784ad-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="784ad-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="784ad-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="784ad-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="784ad-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="784ad-138">See also</span></span>

- [<span data-ttu-id="784ad-139">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="784ad-139">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="784ad-140">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="784ad-140">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="784ad-141">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="784ad-141">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
