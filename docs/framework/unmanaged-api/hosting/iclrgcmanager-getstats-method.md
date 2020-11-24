---
title: ICLRGCManager::GetStats 方法
ms.date: 03/30/2017
api_name:
- ICLRGCManager.GetStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager::GetStats
helpviewer_keywords:
- GetStats method, ICLRGCManager interface [.NET Framework hosting]
- ICLRGCManager::GetStats method [.NET Framework hosting]
ms.assetid: ce259d1d-cd81-4490-a7a1-0d0ea0804872
topic_type:
- apiref
ms.openlocfilehash: 70fe8b132f03925c41b6bc7aae8e60fea1b05202
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95678267"
---
# <a name="iclrgcmanagergetstats-method"></a><span data-ttu-id="dc3da-102">ICLRGCManager::GetStats 方法</span><span class="sxs-lookup"><span data-stu-id="dc3da-102">ICLRGCManager::GetStats Method</span></span>

<span data-ttu-id="dc3da-103">获取有关公共语言运行时的垃圾回收系统的当前统计信息集。</span><span class="sxs-lookup"><span data-stu-id="dc3da-103">Gets a set of current statistics about the common language runtime's garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc3da-104">语法</span><span class="sxs-lookup"><span data-stu-id="dc3da-104">Syntax</span></span>  
  
```cpp  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc3da-105">参数</span><span class="sxs-lookup"><span data-stu-id="dc3da-105">Parameters</span></span>  

 `pStats`  
 <span data-ttu-id="dc3da-106">[in，out]一个 [COR_GC_STATS](cor-gc-stats-structure.md) 实例，其中包含请求的统计信息。</span><span class="sxs-lookup"><span data-stu-id="dc3da-106">[in, out] A [COR_GC_STATS](cor-gc-stats-structure.md) instance that contains the requested statistics.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dc3da-107">返回值</span><span class="sxs-lookup"><span data-stu-id="dc3da-107">Return Value</span></span>  
  
|<span data-ttu-id="dc3da-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="dc3da-108">HRESULT</span></span>|<span data-ttu-id="dc3da-109">说明</span><span class="sxs-lookup"><span data-stu-id="dc3da-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="dc3da-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc3da-110">S_OK</span></span>|<span data-ttu-id="dc3da-111">`GetStats` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="dc3da-111">`GetStats` returned successfully.</span></span>|  
|<span data-ttu-id="dc3da-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="dc3da-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="dc3da-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="dc3da-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="dc3da-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="dc3da-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="dc3da-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="dc3da-115">The call timed out.</span></span>|  
|<span data-ttu-id="dc3da-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="dc3da-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="dc3da-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="dc3da-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="dc3da-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="dc3da-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="dc3da-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="dc3da-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="dc3da-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dc3da-120">E_FAIL</span></span>|<span data-ttu-id="dc3da-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="dc3da-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="dc3da-122">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="dc3da-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="dc3da-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="dc3da-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dc3da-124">注解</span><span class="sxs-lookup"><span data-stu-id="dc3da-124">Remarks</span></span>  

 <span data-ttu-id="dc3da-125">CLR 只计算和返回由的字段指定的统计信息 `Flags` `pStats` 。</span><span class="sxs-lookup"><span data-stu-id="dc3da-125">The CLR calculates and returns only those statistics that are specified by the `Flags` field of `pStats`.</span></span>  
  
 <span data-ttu-id="dc3da-126">将 `Flags` 字段设置为一个或多个 [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) 枚举的值，以指定要设置 [COR_GC_STATS](cor-gc-stats-structure.md) 结构中的哪些统计信息。</span><span class="sxs-lookup"><span data-stu-id="dc3da-126">Set the `Flags` field to one or more values of the [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) enumeration to specify which statistics in the [COR_GC_STATS](cor-gc-stats-structure.md) structure are to be set.</span></span>  
  
 <span data-ttu-id="dc3da-127">用法的示例如下所示：</span><span class="sxs-lookup"><span data-stu-id="dc3da-127">An example of the usage is as follows:</span></span>  
  
```cpp  
COR_GC_STATS GCStats;  
GCStats.Flags = COR_GC_COUNTS | COR_GC_MEMORYUSAGE;  
pCLRGCManager->GetStats(&GCStats);  
```  
  
## <a name="requirements"></a><span data-ttu-id="dc3da-128">要求</span><span class="sxs-lookup"><span data-stu-id="dc3da-128">Requirements</span></span>  

 <span data-ttu-id="dc3da-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dc3da-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc3da-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="dc3da-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dc3da-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dc3da-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dc3da-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc3da-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc3da-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc3da-133">See also</span></span>

- [<span data-ttu-id="dc3da-134">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="dc3da-134">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="dc3da-135">COR_GC_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="dc3da-135">COR_GC_STATS Structure</span></span>](cor-gc-stats-structure.md)
- [<span data-ttu-id="dc3da-136">COR_GC_STAT_TYPES 枚举</span><span class="sxs-lookup"><span data-stu-id="dc3da-136">COR_GC_STAT_TYPES Enumeration</span></span>](cor-gc-stat-types-enumeration.md)
- [<span data-ttu-id="dc3da-137">垃圾回收</span><span class="sxs-lookup"><span data-stu-id="dc3da-137">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
- [<span data-ttu-id="dc3da-138">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="dc3da-138">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="dc3da-139">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="dc3da-139">ICLRGCManager Interface</span></span>](iclrgcmanager-interface.md)
- [<span data-ttu-id="dc3da-140">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="dc3da-140">CLR Hosting Interfaces</span></span>](clr-hosting-interfaces.md)
- [<span data-ttu-id="dc3da-141">承载接口</span><span class="sxs-lookup"><span data-stu-id="dc3da-141">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="dc3da-142">承载</span><span class="sxs-lookup"><span data-stu-id="dc3da-142">Hosting</span></span>](index.md)
