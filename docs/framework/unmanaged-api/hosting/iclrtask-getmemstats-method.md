---
title: ICLRTask::GetMemStats 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.GetMemStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::GetMemStats
helpviewer_keywords:
- ICLRTask::GetMemStats method [.NET Framework hosting]
- GetMemStats method [.NET Framework hosting]
ms.assetid: c9e07657-1682-4c30-a336-f8658ff1a125
topic_type:
- apiref
ms.openlocfilehash: 5d57bc742ebcba00f9fbe569a4be27b82a5f8055
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726504"
---
# <a name="iclrtaskgetmemstats-method"></a><span data-ttu-id="7e71e-102">ICLRTask::GetMemStats 方法</span><span class="sxs-lookup"><span data-stu-id="7e71e-102">ICLRTask::GetMemStats Method</span></span>

<span data-ttu-id="7e71e-103">获取与当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务相关的统计内存使用情况信息。</span><span class="sxs-lookup"><span data-stu-id="7e71e-103">Gets statistical memory usage information related to the task that the current [ICLRTask](iclrtask-interface.md) instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e71e-104">语法</span><span class="sxs-lookup"><span data-stu-id="7e71e-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMemStats (  
    [out] COR_GC_THREAD_STATS *pMemUsage  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7e71e-105">参数</span><span class="sxs-lookup"><span data-stu-id="7e71e-105">Parameters</span></span>  

 `pMemUsage`  
 <span data-ttu-id="7e71e-106">弄一个指向 [COR_GC_THREAD_STATS](cor-gc-thread-stats-structure.md) 实例的指针，其中包含有关该任务的内存使用情况的详细信息，包括已分配的字节数。</span><span class="sxs-lookup"><span data-stu-id="7e71e-106">[out] A pointer to a [COR_GC_THREAD_STATS](cor-gc-thread-stats-structure.md) instance that contains details about the memory usage of the task, including the number of bytes allocated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7e71e-107">返回值</span><span class="sxs-lookup"><span data-stu-id="7e71e-107">Return Value</span></span>  
  
|<span data-ttu-id="7e71e-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7e71e-108">HRESULT</span></span>|<span data-ttu-id="7e71e-109">说明</span><span class="sxs-lookup"><span data-stu-id="7e71e-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7e71e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e71e-110">S_OK</span></span>|<span data-ttu-id="7e71e-111">`GetMemStats` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="7e71e-111">`GetMemStats` returned successfully.</span></span>|  
|<span data-ttu-id="7e71e-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7e71e-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7e71e-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7e71e-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7e71e-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7e71e-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7e71e-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="7e71e-115">The call timed out.</span></span>|  
|<span data-ttu-id="7e71e-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7e71e-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7e71e-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="7e71e-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7e71e-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7e71e-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7e71e-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="7e71e-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7e71e-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7e71e-120">E_FAIL</span></span>|<span data-ttu-id="7e71e-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7e71e-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7e71e-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7e71e-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7e71e-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7e71e-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7e71e-124">要求</span><span class="sxs-lookup"><span data-stu-id="7e71e-124">Requirements</span></span>  

 <span data-ttu-id="7e71e-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7e71e-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e71e-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7e71e-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7e71e-127">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7e71e-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7e71e-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e71e-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e71e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e71e-129">See also</span></span>

- [<span data-ttu-id="7e71e-130">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="7e71e-130">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="7e71e-131">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="7e71e-131">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="7e71e-132">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="7e71e-132">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="7e71e-133">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="7e71e-133">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
