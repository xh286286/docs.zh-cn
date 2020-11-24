---
title: IHostControl::GetHostManager 方法
ms.date: 03/30/2017
api_name:
- IHostControl.GetHostManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl::GetHostManager
helpviewer_keywords:
- GetHostManager method [.NET Framework hosting]
- IHostControl::GetHostManager method [.NET Framework hosting]
ms.assetid: 0fa34bca-ed18-4626-9e78-d33684d18edb
topic_type:
- apiref
ms.openlocfilehash: e340dcb5dc093f965e6c08a24a3d65ed0aa6e07a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680815"
---
# <a name="ihostcontrolgethostmanager-method"></a><span data-ttu-id="27a3c-102">IHostControl::GetHostManager 方法</span><span class="sxs-lookup"><span data-stu-id="27a3c-102">IHostControl::GetHostManager Method</span></span>

<span data-ttu-id="27a3c-103">获取一个接口指针，该指针指向具有指定的接口的主机实现 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="27a3c-103">Gets an interface pointer to the host's implementation of the interface with the specified `IID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27a3c-104">语法</span><span class="sxs-lookup"><span data-stu-id="27a3c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetHostManager (  
    [in] REFIID riid,  
    [out, iid_is(riid)] void** ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="27a3c-105">参数</span><span class="sxs-lookup"><span data-stu-id="27a3c-105">Parameters</span></span>  

 `riid`  
 <span data-ttu-id="27a3c-106">中 `IID` 公共语言运行时 (CLR) 正在查询的接口的。</span><span class="sxs-lookup"><span data-stu-id="27a3c-106">[in] The `IID` of the interface that the common language runtime (CLR) is querying for.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="27a3c-107">弄指向宿主实现的接口的指针; 如果主机不支持此接口，则为 null。</span><span class="sxs-lookup"><span data-stu-id="27a3c-107">[out] A pointer to the host-implemented interface, or null if the host does not support this interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="27a3c-108">返回值</span><span class="sxs-lookup"><span data-stu-id="27a3c-108">Return Value</span></span>  
  
|<span data-ttu-id="27a3c-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="27a3c-109">HRESULT</span></span>|<span data-ttu-id="27a3c-110">说明</span><span class="sxs-lookup"><span data-stu-id="27a3c-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="27a3c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="27a3c-111">S_OK</span></span>|<span data-ttu-id="27a3c-112">`GetHostManager` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="27a3c-112">`GetHostManager` returned successfully.</span></span>|  
|<span data-ttu-id="27a3c-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="27a3c-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="27a3c-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="27a3c-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="27a3c-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="27a3c-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="27a3c-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="27a3c-116">The call timed out.</span></span>|  
|<span data-ttu-id="27a3c-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="27a3c-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="27a3c-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="27a3c-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="27a3c-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="27a3c-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="27a3c-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="27a3c-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="27a3c-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="27a3c-121">E_FAIL</span></span>|<span data-ttu-id="27a3c-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="27a3c-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="27a3c-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="27a3c-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="27a3c-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="27a3c-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="27a3c-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="27a3c-125">E_INVALIDARG</span></span>|<span data-ttu-id="27a3c-126">请求的无效 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="27a3c-126">The requested `IID` is not valid.</span></span>|  
|<span data-ttu-id="27a3c-127">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="27a3c-127">E_NOINTERFACE</span></span>|<span data-ttu-id="27a3c-128">不支持请求的接口。</span><span class="sxs-lookup"><span data-stu-id="27a3c-128">The requested interface is not supported.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="27a3c-129">注解</span><span class="sxs-lookup"><span data-stu-id="27a3c-129">Remarks</span></span>  

 <span data-ttu-id="27a3c-130">CLR 将查询宿主，以确定它是否支持以下一个或多个接口：</span><span class="sxs-lookup"><span data-stu-id="27a3c-130">The CLR queries the host to determine whether it supports one or more of the following interfaces:</span></span>  
  
- [<span data-ttu-id="27a3c-131">IHostMemoryManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-131">IHostMemoryManager</span></span>](ihostmemorymanager-interface.md)  
  
- [<span data-ttu-id="27a3c-132">IHostTaskManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-132">IHostTaskManager</span></span>](ihosttaskmanager-interface.md)  
  
- [<span data-ttu-id="27a3c-133">IHostThreadPoolManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-133">IHostThreadPoolManager</span></span>](ihostthreadpoolmanager-interface.md)  
  
- [<span data-ttu-id="27a3c-134">IHostIoCompletionManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-134">IHostIoCompletionManager</span></span>](ihostiocompletionmanager-interface.md)  
  
- [<span data-ttu-id="27a3c-135">IHostSyncManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-135">IHostSyncManager</span></span>](ihostsyncmanager-interface.md)  
  
- [<span data-ttu-id="27a3c-136">IHostAssemblyManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-136">IHostAssemblyManager</span></span>](ihostassemblymanager-interface.md)  
  
- [<span data-ttu-id="27a3c-137">IHostGCManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-137">IHostGCManager</span></span>](ihostgcmanager-interface.md)  
  
- [<span data-ttu-id="27a3c-138">IHostPolicyManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-138">IHostPolicyManager</span></span>](ihostpolicymanager-interface.md)  
  
- [<span data-ttu-id="27a3c-139">IHostSecurityManager</span><span class="sxs-lookup"><span data-stu-id="27a3c-139">IHostSecurityManager</span></span>](ihostsecuritymanager-interface.md)  
  
 <span data-ttu-id="27a3c-140">如果宿主支持指定的接口，它会将 `ppObject` 其设置为该接口的实现。</span><span class="sxs-lookup"><span data-stu-id="27a3c-140">If the host supports the specified interface, it sets `ppObject` to its implementation of that interface.</span></span> <span data-ttu-id="27a3c-141">否则，它将设置 `ppObject` 为 null。</span><span class="sxs-lookup"><span data-stu-id="27a3c-141">Otherwise, it sets `ppObject` to null.</span></span>  
  
 <span data-ttu-id="27a3c-142">CLR 不会对 `Release` 主机管理器调用，即使您关闭它也是如此。</span><span class="sxs-lookup"><span data-stu-id="27a3c-142">The CLR does not call `Release` on host managers, even when you shut it down.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27a3c-143">要求</span><span class="sxs-lookup"><span data-stu-id="27a3c-143">Requirements</span></span>  

 <span data-ttu-id="27a3c-144">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27a3c-144">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27a3c-145">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="27a3c-145">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="27a3c-146">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="27a3c-146">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="27a3c-147">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27a3c-147">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27a3c-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27a3c-148">See also</span></span>

- [<span data-ttu-id="27a3c-149">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="27a3c-149">IHostControl Interface</span></span>](ihostcontrol-interface.md)
