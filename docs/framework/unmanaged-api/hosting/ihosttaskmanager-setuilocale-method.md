---
title: IHostTaskManager::SetUILocale 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.SetUILocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::SetUILocale
helpviewer_keywords:
- SetUILocale method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::SetUILocale method [.NET Framework hosting]
ms.assetid: d0c87a9c-ea81-4237-a16b-c22b36ec9dc8
topic_type:
- apiref
ms.openlocfilehash: bd1a1d7d2f7f945f345e8af802b881392d6d93e5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724216"
---
# <a name="ihosttaskmanagersetuilocale-method"></a><span data-ttu-id="7a8b3-102">IHostTaskManager::SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="7a8b3-102">IHostTaskManager::SetUILocale Method</span></span>

<span data-ttu-id="7a8b3-103">向宿主通知公共语言运行时 (CLR) 已更改当前正在执行的任务的用户界面 (UI) 区域设置或区域性。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-103">Notifies the host that the common language runtime (CLR) has changed the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a8b3-104">语法</span><span class="sxs-lookup"><span data-stu-id="7a8b3-104">Syntax</span></span>  
  
```cpp  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7a8b3-105">参数</span><span class="sxs-lookup"><span data-stu-id="7a8b3-105">Parameters</span></span>  

 `lcid`  
 <span data-ttu-id="7a8b3-106">中映射到新分配的地理区域和语言的区域设置标识符值。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-106">[in] The locale identifier value that maps to the newly assigned geographical culture and language.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7a8b3-107">返回值</span><span class="sxs-lookup"><span data-stu-id="7a8b3-107">Return Value</span></span>  
  
|<span data-ttu-id="7a8b3-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7a8b3-108">HRESULT</span></span>|<span data-ttu-id="7a8b3-109">说明</span><span class="sxs-lookup"><span data-stu-id="7a8b3-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7a8b3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a8b3-110">S_OK</span></span>|<span data-ttu-id="7a8b3-111">`SetUILocale` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-111">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="7a8b3-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7a8b3-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7a8b3-113">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7a8b3-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7a8b3-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7a8b3-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-115">The call timed out.</span></span>|  
|<span data-ttu-id="7a8b3-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7a8b3-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7a8b3-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7a8b3-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7a8b3-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7a8b3-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7a8b3-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7a8b3-120">E_FAIL</span></span>|<span data-ttu-id="7a8b3-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7a8b3-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7a8b3-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="7a8b3-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="7a8b3-124">E_NOTIMPL</span></span>|<span data-ttu-id="7a8b3-125">宿主不允许托管用户代码更改 UI 区域性。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-125">The host does not allow managed user code to change the UI culture.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a8b3-126">注解</span><span class="sxs-lookup"><span data-stu-id="7a8b3-126">Remarks</span></span>  

 <span data-ttu-id="7a8b3-127">`SetUILocale`当 <xref:System.Threading.Thread.CurrentUICulture%2A?displayProperty=nameWithType> 托管代码更改属性的值时，运行时调用。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-127">The runtime calls `SetUILocale` when the value of the <xref:System.Threading.Thread.CurrentUICulture%2A?displayProperty=nameWithType> property is changed by managed code.</span></span> <span data-ttu-id="7a8b3-128">此方法为主机提供了对区域设置同步所需的任何机制的机会。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-128">This method provides an opportunity for the host to execute any mechanisms it might have for synchronization of locales.</span></span> <span data-ttu-id="7a8b3-129">如果主机不允许从托管代码更改 UI 区域设置，或未实现同步区域设置的机制，则它应从此方法返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-129">If a host does not allow the UI locale to be changed from managed code, or does not implement a mechanism to synchronize locales, it should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a8b3-130">要求</span><span class="sxs-lookup"><span data-stu-id="7a8b3-130">Requirements</span></span>  

 <span data-ttu-id="7a8b3-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a8b3-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a8b3-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7a8b3-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7a8b3-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7a8b3-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7a8b3-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a8b3-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a8b3-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a8b3-135">See also</span></span>

- [<span data-ttu-id="7a8b3-136">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="7a8b3-136">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="7a8b3-137">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="7a8b3-137">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="7a8b3-138">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="7a8b3-138">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="7a8b3-139">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="7a8b3-139">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="7a8b3-140">SetLocale 方法</span><span class="sxs-lookup"><span data-stu-id="7a8b3-140">SetLocale Method</span></span>](ihosttaskmanager-setlocale-method.md)
