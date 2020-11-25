---
title: IHostSyncManager::CreateManualEvent 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateManualEvent
helpviewer_keywords:
- CreateManualEvent method [.NET Framework hosting]
- IHostSyncManager::CreateManualEvent method [.NET Framework hosting]
ms.assetid: 68661fbd-09cf-46dc-890b-e694f8a3880a
topic_type:
- apiref
ms.openlocfilehash: 67af8f125b2be39138bac5d51148215f3a3acf86
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723865"
---
# <a name="ihostsyncmanagercreatemanualevent-method"></a><span data-ttu-id="e6935-102">IHostSyncManager::CreateManualEvent 方法</span><span class="sxs-lookup"><span data-stu-id="e6935-102">IHostSyncManager::CreateManualEvent Method</span></span>

<span data-ttu-id="e6935-103">创建手动重置的事件对象。</span><span class="sxs-lookup"><span data-stu-id="e6935-103">Creates a manual-reset event object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6935-104">语法</span><span class="sxs-lookup"><span data-stu-id="e6935-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateManualEvent (  
    [in]  BOOL bInitialState,  
    [out] IHostManualEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6935-105">参数</span><span class="sxs-lookup"><span data-stu-id="e6935-105">Parameters</span></span>  

 `bInitialState`  
 <span data-ttu-id="e6935-106">[in] `true` ，如果对象已终止，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="e6935-106">[in] `true`, if the object is signaled; otherwise, `false`.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="e6935-107">弄指向 [IHostManualEvent](ihostmanualevent-interface.md) 实例的地址的指针; 如果未能创建该事件，则为 null。</span><span class="sxs-lookup"><span data-stu-id="e6935-107">[out] A pointer to the address of an [IHostManualEvent](ihostmanualevent-interface.md) instance, or null if the event could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e6935-108">返回值</span><span class="sxs-lookup"><span data-stu-id="e6935-108">Return Value</span></span>  
  
|<span data-ttu-id="e6935-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e6935-109">HRESULT</span></span>|<span data-ttu-id="e6935-110">说明</span><span class="sxs-lookup"><span data-stu-id="e6935-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e6935-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6935-111">S_OK</span></span>|<span data-ttu-id="e6935-112">`CreateManualEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="e6935-112">`CreateManualEvent` returned successfully.</span></span>|  
|<span data-ttu-id="e6935-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e6935-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e6935-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="e6935-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e6935-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e6935-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e6935-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="e6935-116">The call timed out.</span></span>|  
|<span data-ttu-id="e6935-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e6935-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e6935-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="e6935-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e6935-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e6935-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e6935-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="e6935-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e6935-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e6935-121">E_FAIL</span></span>|<span data-ttu-id="e6935-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="e6935-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e6935-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="e6935-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e6935-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="e6935-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="e6935-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e6935-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="e6935-126">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="e6935-126">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e6935-127">注解</span><span class="sxs-lookup"><span data-stu-id="e6935-127">Remarks</span></span>  

 <span data-ttu-id="e6935-128">`CreateManualEvent` 创建一个 `IHostManualEvent` 手动重置事件对象，该对象需要调用 [IHostManualEvent：： reset](ihostmanualevent-reset-method.md) 方法，以将其设置为非终止状态。</span><span class="sxs-lookup"><span data-stu-id="e6935-128">`CreateManualEvent` creates an `IHostManualEvent`, a manual-reset event object that requires a call to the [IHostManualEvent::Reset](ihostmanualevent-reset-method.md) method to set it to a non-signaled state.</span></span> <span data-ttu-id="e6935-129">`CreateManualEvent``CreateEvent`使用 `true` 为参数指定的值镜像 Win32 函数 `bManualReset` 。</span><span class="sxs-lookup"><span data-stu-id="e6935-129">`CreateManualEvent` mirrors the Win32 `CreateEvent` function with a value of `true` specified for the `bManualReset` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6935-130">要求</span><span class="sxs-lookup"><span data-stu-id="e6935-130">Requirements</span></span>  

 <span data-ttu-id="e6935-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e6935-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6935-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e6935-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e6935-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e6935-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e6935-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6935-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6935-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6935-135">See also</span></span>

- [<span data-ttu-id="e6935-136">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="e6935-136">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="e6935-137">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="e6935-137">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="e6935-138">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="e6935-138">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
