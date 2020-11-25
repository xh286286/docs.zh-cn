---
title: ICLRTaskManager::GetCurrentTask 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTask
helpviewer_keywords:
- GetCurrentTask method, ICLRTaskManager interface [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTask method [.NET Framework hosting]
ms.assetid: c0b82a9f-edc6-4878-9c81-48de53c02142
topic_type:
- apiref
ms.openlocfilehash: af855e3ba47dc329a4fb722c3e13d5f1816beba4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723267"
---
# <a name="iclrtaskmanagergetcurrenttask-method"></a><span data-ttu-id="f3862-102">ICLRTaskManager::GetCurrentTask 方法</span><span class="sxs-lookup"><span data-stu-id="f3862-102">ICLRTaskManager::GetCurrentTask Method</span></span>

<span data-ttu-id="f3862-103">获取当前在该方法调用所源自的操作系统线程上运行的 [ICLRTask](iclrtask-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="f3862-103">Gets the [ICLRTask](iclrtask-interface.md) instance that is currently running on the operating system thread from which the method call originated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3862-104">语法</span><span class="sxs-lookup"><span data-stu-id="f3862-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentTask (  
    [out] ICLRTask **ppTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f3862-105">参数</span><span class="sxs-lookup"><span data-stu-id="f3862-105">Parameters</span></span>  

 `ppTask`  
 <span data-ttu-id="f3862-106">弄一个指针 `ICLRTask` ，指向从其发出调用的操作系统线程上当前正在执行的实例的地址，如果此线程上当前未执行任何任务，则为 null。</span><span class="sxs-lookup"><span data-stu-id="f3862-106">[out] A pointer to the address of an `ICLRTask` instance that is currently executing on the operating system thread from which the call originated, or null if no task is currently executing on this thread.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f3862-107">返回值</span><span class="sxs-lookup"><span data-stu-id="f3862-107">Return Value</span></span>  
  
|<span data-ttu-id="f3862-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f3862-108">HRESULT</span></span>|<span data-ttu-id="f3862-109">说明</span><span class="sxs-lookup"><span data-stu-id="f3862-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f3862-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3862-110">S_OK</span></span>|<span data-ttu-id="f3862-111">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f3862-111">The method returned successfully.</span></span>|  
|<span data-ttu-id="f3862-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f3862-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f3862-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f3862-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f3862-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f3862-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f3862-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f3862-115">The call timed out.</span></span>|  
|<span data-ttu-id="f3862-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f3862-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f3862-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f3862-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f3862-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f3862-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f3862-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f3862-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f3862-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3862-120">E_FAIL</span></span>|<span data-ttu-id="f3862-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f3862-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f3862-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f3862-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f3862-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f3862-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f3862-124">注解</span><span class="sxs-lookup"><span data-stu-id="f3862-124">Remarks</span></span>  

 <span data-ttu-id="f3862-125">`ICLRTask`参数指向的实例 `ppTask` 表示 CLR 当前正在执行的任务。</span><span class="sxs-lookup"><span data-stu-id="f3862-125">The `ICLRTask` instance that the `ppTask` parameter points to represents the currently executing task for the CLR.</span></span> <span data-ttu-id="f3862-126">`ICLRTask`实例与表示宿主任务的相应[IHostTask](ihosttask-interface.md)实例相关联。</span><span class="sxs-lookup"><span data-stu-id="f3862-126">The `ICLRTask` instance is associated with a corresponding [IHostTask](ihosttask-interface.md) instance that represents the task for the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3862-127">要求</span><span class="sxs-lookup"><span data-stu-id="f3862-127">Requirements</span></span>  

 <span data-ttu-id="f3862-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f3862-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3862-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f3862-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f3862-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f3862-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f3862-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3862-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3862-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3862-132">See also</span></span>

- [<span data-ttu-id="f3862-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="f3862-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="f3862-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f3862-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="f3862-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="f3862-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="f3862-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f3862-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
