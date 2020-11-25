---
title: IHostTaskManager::BeginDelayAbort 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.BeginDelayAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::BeginDelayAbort
helpviewer_keywords:
- BeginDelayAbort method [.NET Framework hosting]
- IHostTaskManager::BeginDelayAbort method [.NET Framework hosting]
ms.assetid: 75f42a8b-ed68-4718-a030-a179cfba7d72
topic_type:
- apiref
ms.openlocfilehash: f72cc15904d098e159dd7f75f673d43ae987998d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727323"
---
# <a name="ihosttaskmanagerbegindelayabort-method"></a><span data-ttu-id="ae778-102">IHostTaskManager::BeginDelayAbort 方法</span><span class="sxs-lookup"><span data-stu-id="ae778-102">IHostTaskManager::BeginDelayAbort Method</span></span>

<span data-ttu-id="ae778-103">通知宿主托管代码输入的时间段不得中止当前任务。</span><span class="sxs-lookup"><span data-stu-id="ae778-103">Notifies the host that managed code is entering a period in which the current task must not be aborted.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae778-104">语法</span><span class="sxs-lookup"><span data-stu-id="ae778-104">Syntax</span></span>  
  
```cpp  
HRESULT BeginDelayAbort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="ae778-105">返回值</span><span class="sxs-lookup"><span data-stu-id="ae778-105">Return Value</span></span>  
  
|<span data-ttu-id="ae778-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ae778-106">HRESULT</span></span>|<span data-ttu-id="ae778-107">说明</span><span class="sxs-lookup"><span data-stu-id="ae778-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ae778-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae778-108">S_OK</span></span>|<span data-ttu-id="ae778-109">`BeginDelayAbort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ae778-109">`BeginDelayAbort` returned successfully.</span></span>|  
|<span data-ttu-id="ae778-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ae778-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ae778-111"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ae778-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ae778-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ae778-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ae778-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ae778-113">The call timed out.</span></span>|  
|<span data-ttu-id="ae778-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ae778-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ae778-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ae778-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ae778-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ae778-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ae778-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ae778-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ae778-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae778-118">E_FAIL</span></span>|<span data-ttu-id="ae778-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ae778-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ae778-120">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ae778-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ae778-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ae778-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ae778-122">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="ae778-122">E_UNEXPECTED</span></span>|<span data-ttu-id="ae778-123">`BeginDelayAbort` 已调用，但尚未接收到对 [EndDelayAbort](ihosttaskmanager-enddelayabort-method.md) 的相应调用。</span><span class="sxs-lookup"><span data-stu-id="ae778-123">`BeginDelayAbort` has already been called, but the corresponding call to [EndDelayAbort](ihosttaskmanager-enddelayabort-method.md) has not yet been received.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae778-124">注解</span><span class="sxs-lookup"><span data-stu-id="ae778-124">Remarks</span></span>  

 <span data-ttu-id="ae778-125">在调用之前，主机不得中止当前任务 `EndDelayAbort` 。</span><span class="sxs-lookup"><span data-stu-id="ae778-125">The host must not abort the current task until `EndDelayAbort` is called.</span></span> <span data-ttu-id="ae778-126">如果在没有干预调用的情况下进行了对的另一次调用 `BeginDelayAbort` `EndDelayAbort` ，主机应从返回 E_UNEXPECTED `BeginDelayAbort` ，而不应采取任何措施。</span><span class="sxs-lookup"><span data-stu-id="ae778-126">If another call to `BeginDelayAbort` is made without an intervening call to `EndDelayAbort`, the host should return E_UNEXPECTED from `BeginDelayAbort`, and should take no action.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae778-127">要求</span><span class="sxs-lookup"><span data-stu-id="ae778-127">Requirements</span></span>  

 <span data-ttu-id="ae778-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae778-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae778-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ae778-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ae778-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ae778-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ae778-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae778-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae778-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae778-132">See also</span></span>

- [<span data-ttu-id="ae778-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="ae778-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="ae778-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="ae778-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="ae778-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="ae778-135">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
