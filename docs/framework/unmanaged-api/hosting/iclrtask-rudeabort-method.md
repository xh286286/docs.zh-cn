---
title: ICLRTask::RudeAbort 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.RudeAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::RudeAbort
helpviewer_keywords:
- RudeAbort method, ICLRTask interface [.NET Framework hosting]
- ICLRTask::RudeAbort method [.NET Framework hosting]
ms.assetid: b5785468-fcd7-4cc3-8a5d-8796337b53fc
topic_type:
- apiref
ms.openlocfilehash: 5b0e2265810b00fe0760d4e25c0f9904a96d9f2a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95691040"
---
# <a name="iclrtaskrudeabort-method"></a><span data-ttu-id="8fe13-102">ICLRTask::RudeAbort 方法</span><span class="sxs-lookup"><span data-stu-id="8fe13-102">ICLRTask::RudeAbort Method</span></span>

<span data-ttu-id="8fe13-103">指示公共语言运行时 (CLR) 立即和无条件中止当前 [ICLRTask 接口](iclrtask-interface.md) 实例表示的任务。</span><span class="sxs-lookup"><span data-stu-id="8fe13-103">Instructs the common language runtime (CLR) to abort the task represented by the current [ICLRTask Interface](iclrtask-interface.md) instance immediately and unconditionally.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fe13-104">语法</span><span class="sxs-lookup"><span data-stu-id="8fe13-104">Syntax</span></span>  
  
```cpp  
HRESULT RudeAbort ();
```  
  
## <a name="return-value"></a><span data-ttu-id="8fe13-105">返回值</span><span class="sxs-lookup"><span data-stu-id="8fe13-105">Return Value</span></span>  
  
|<span data-ttu-id="8fe13-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8fe13-106">HRESULT</span></span>|<span data-ttu-id="8fe13-107">说明</span><span class="sxs-lookup"><span data-stu-id="8fe13-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8fe13-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fe13-108">S_OK</span></span>|<span data-ttu-id="8fe13-109">`RudeAbort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="8fe13-109">`RudeAbort` returned successfully.</span></span>|  
|<span data-ttu-id="8fe13-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8fe13-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8fe13-111">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="8fe13-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8fe13-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8fe13-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8fe13-113">调用超时。</span><span class="sxs-lookup"><span data-stu-id="8fe13-113">The call timed out.</span></span>|  
|<span data-ttu-id="8fe13-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8fe13-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8fe13-115">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="8fe13-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8fe13-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8fe13-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8fe13-117">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="8fe13-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8fe13-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8fe13-118">E_FAIL</span></span>|<span data-ttu-id="8fe13-119">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="8fe13-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8fe13-120">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="8fe13-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8fe13-121">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="8fe13-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8fe13-122">注解</span><span class="sxs-lookup"><span data-stu-id="8fe13-122">Remarks</span></span>  

 <span data-ttu-id="8fe13-123">宿主调用 `RudeAbort` 立即中止任务。</span><span class="sxs-lookup"><span data-stu-id="8fe13-123">A host calls `RudeAbort` to abort a task immediately.</span></span> <span data-ttu-id="8fe13-124">不保证会执行终结器和异常处理例程。</span><span class="sxs-lookup"><span data-stu-id="8fe13-124">Finalizers and exception handling routines are not guaranteed to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fe13-125">要求</span><span class="sxs-lookup"><span data-stu-id="8fe13-125">Requirements</span></span>  

 <span data-ttu-id="8fe13-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8fe13-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fe13-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8fe13-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8fe13-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8fe13-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8fe13-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8fe13-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fe13-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fe13-130">See also</span></span>

- [<span data-ttu-id="8fe13-131">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="8fe13-131">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="8fe13-132">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="8fe13-132">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="8fe13-133">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="8fe13-133">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="8fe13-134">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="8fe13-134">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
