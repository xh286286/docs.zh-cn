---
title: IHostMemoryManager::CreateMAlloc 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.CreateMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::CreateMAlloc
helpviewer_keywords:
- CreateAlloc method [.NET Framework hosting]
- IHostMemoryManager::CreateMAlloc method [.NET Framework hosting]
ms.assetid: 9ee6e052-bef7-4350-9e4f-edfffd99ad6f
topic_type:
- apiref
ms.openlocfilehash: 79580170d544cd3763992a4bc67fd20e3446bb1d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95685716"
---
# <a name="ihostmemorymanagercreatemalloc-method"></a><span data-ttu-id="d51da-102">IHostMemoryManager::CreateMAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="d51da-102">IHostMemoryManager::CreateMAlloc Method</span></span>

<span data-ttu-id="d51da-103">获取一个接口指针，该指针指向用于从主机创建的堆发出分配请求的 [IHostMAlloc](ihostmalloc-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="d51da-103">Gets an interface pointer to an [IHostMAlloc](ihostmalloc-interface.md) instance that is used to make allocation requests from a heap created by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d51da-104">语法</span><span class="sxs-lookup"><span data-stu-id="d51da-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateMalloc (  
    [in]  DWORD         dwMallocType,  
    [out] IHostMalloc **ppMalloc  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d51da-105">参数</span><span class="sxs-lookup"><span data-stu-id="d51da-105">Parameters</span></span>  

 `dwMallocType`  
 <span data-ttu-id="d51da-106">中 [MALLOC_TYPE](malloc-type-enumeration.md) 标志的组合，这些标志指定正在分配的内存的特征。</span><span class="sxs-lookup"><span data-stu-id="d51da-106">[in] A combination of [MALLOC_TYPE](malloc-type-enumeration.md) flags that specifies the characteristics of the memory that is being allocated.</span></span>  
  
 `ppMAlloc`  
 <span data-ttu-id="d51da-107">弄指向主机提供的实例的地址的指针 `IHostMAlloc` 。</span><span class="sxs-lookup"><span data-stu-id="d51da-107">[out] A pointer to the address of an `IHostMAlloc` instance provided by the host.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d51da-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d51da-108">Return Value</span></span>  
  
|<span data-ttu-id="d51da-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d51da-109">HRESULT</span></span>|<span data-ttu-id="d51da-110">说明</span><span class="sxs-lookup"><span data-stu-id="d51da-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d51da-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d51da-111">S_OK</span></span>|<span data-ttu-id="d51da-112">`CreateMAlloc` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d51da-112">`CreateMAlloc` returned successfully.</span></span>|  
|<span data-ttu-id="d51da-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d51da-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d51da-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d51da-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d51da-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d51da-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d51da-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="d51da-116">The call timed out.</span></span>|  
|<span data-ttu-id="d51da-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d51da-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d51da-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d51da-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d51da-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d51da-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d51da-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="d51da-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d51da-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d51da-121">E_FAIL</span></span>|<span data-ttu-id="d51da-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d51da-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d51da-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="d51da-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d51da-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d51da-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d51da-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d51da-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="d51da-126">没有足够的物理内存可用于完成分配请求。</span><span class="sxs-lookup"><span data-stu-id="d51da-126">Not enough physical memory was available to complete the allocation request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d51da-127">注解</span><span class="sxs-lookup"><span data-stu-id="d51da-127">Remarks</span></span>  

 <span data-ttu-id="d51da-128">`CreateMAlloc` 返回一个对象，该对象允许 CLR 通过主机发出分配请求，而不是使用标准的 Win32 函数。</span><span class="sxs-lookup"><span data-stu-id="d51da-128">`CreateMAlloc` returns an object that allows the CLR to make allocation requests through the host instead of using the standard Win32 functions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d51da-129">要求</span><span class="sxs-lookup"><span data-stu-id="d51da-129">Requirements</span></span>  

 <span data-ttu-id="d51da-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d51da-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d51da-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d51da-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d51da-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d51da-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d51da-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d51da-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d51da-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d51da-134">See also</span></span>

- [<span data-ttu-id="d51da-135">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="d51da-135">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)
- [<span data-ttu-id="d51da-136">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="d51da-136">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
