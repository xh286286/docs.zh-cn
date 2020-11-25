---
title: ICLRTask::LocksHeld 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.LocksHeld
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::LocksHeld
helpviewer_keywords:
- LocksHeld method [.NET Framework hosting]
- ICLRTask::LocksHeld method [.NET Framework hosting]
ms.assetid: e88a4dc3-02cc-4703-a474-292b71c40657
topic_type:
- apiref
ms.openlocfilehash: 755dfed4107a602390a4402a2dde83e08986b623
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731691"
---
# <a name="iclrtasklocksheld-method"></a><span data-ttu-id="411ab-102">ICLRTask::LocksHeld 方法</span><span class="sxs-lookup"><span data-stu-id="411ab-102">ICLRTask::LocksHeld Method</span></span>

<span data-ttu-id="411ab-103">获取任务当前持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="411ab-103">Gets the number of locks currently held on the task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="411ab-104">语法</span><span class="sxs-lookup"><span data-stu-id="411ab-104">Syntax</span></span>  
  
```cpp  
HRESULT LocksHeld (  
    [out] SIZE_T *pLockCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="411ab-105">参数</span><span class="sxs-lookup"><span data-stu-id="411ab-105">Parameters</span></span>  

 `pLockCount`  
 <span data-ttu-id="411ab-106">弄在调用方法时任务中持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="411ab-106">[out] The number of locks held on the task at the time of the method call.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="411ab-107">返回值</span><span class="sxs-lookup"><span data-stu-id="411ab-107">Return Value</span></span>  
  
|<span data-ttu-id="411ab-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="411ab-108">HRESULT</span></span>|<span data-ttu-id="411ab-109">说明</span><span class="sxs-lookup"><span data-stu-id="411ab-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="411ab-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="411ab-110">S_OK</span></span>|<span data-ttu-id="411ab-111">`LocksHeld` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="411ab-111">`LocksHeld` returned successfully.</span></span>|  
|<span data-ttu-id="411ab-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="411ab-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="411ab-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="411ab-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="411ab-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="411ab-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="411ab-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="411ab-115">The call timed out.</span></span>|  
|<span data-ttu-id="411ab-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="411ab-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="411ab-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="411ab-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="411ab-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="411ab-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="411ab-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="411ab-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="411ab-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="411ab-120">E_FAIL</span></span>|<span data-ttu-id="411ab-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="411ab-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="411ab-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="411ab-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="411ab-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="411ab-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="411ab-124">要求</span><span class="sxs-lookup"><span data-stu-id="411ab-124">Requirements</span></span>  

 <span data-ttu-id="411ab-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="411ab-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="411ab-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="411ab-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="411ab-127">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="411ab-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="411ab-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="411ab-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="411ab-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="411ab-129">See also</span></span>

- [<span data-ttu-id="411ab-130">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="411ab-130">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="411ab-131">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="411ab-131">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="411ab-132">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="411ab-132">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="411ab-133">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="411ab-133">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
