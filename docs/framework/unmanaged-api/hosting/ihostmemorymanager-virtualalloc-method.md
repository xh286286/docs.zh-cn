---
title: IHostMemoryManager::VirtualAlloc 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualAlloc
helpviewer_keywords:
- VirtualAlloc method [.NET Framework hosting]
- IHostMemoryManager::VirtualAlloc method [.NET Framework hosting]
ms.assetid: 4dff3646-a050-4bd9-ac31-fe307e8637ec
topic_type:
- apiref
ms.openlocfilehash: a2deabc5f1c7ea0f42b6d8ec3944d984854ae571
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731275"
---
# <a name="ihostmemorymanagervirtualalloc-method"></a><span data-ttu-id="0d877-102">IHostMemoryManager::VirtualAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="0d877-102">IHostMemoryManager::VirtualAlloc Method</span></span>

<span data-ttu-id="0d877-103">用作相应 Win32 函数的逻辑包装。</span><span class="sxs-lookup"><span data-stu-id="0d877-103">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="0d877-104">的 Win32 实现 `VirtualAlloc` 保留或提交调用进程的虚拟地址空间中的页面区域。</span><span class="sxs-lookup"><span data-stu-id="0d877-104">The Win32 implementation of `VirtualAlloc` reserves or commits a region of pages in the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d877-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d877-105">Syntax</span></span>  
  
```cpp  
HRESULT VirtualAlloc (  
    [in]  void*   pAddress,  
    [in]  SIZE_T  dwSize,  
    [in]  DWORD   flAllocationType,  
    [in]  DWORD   flProtect,  
    [in]  EMemoryCriticalLevel dwCriticalLevel,  
    [out] void**  ppMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d877-106">参数</span><span class="sxs-lookup"><span data-stu-id="0d877-106">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="0d877-107">中指向要分配的区域的起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="0d877-107">[in] A pointer to the starting address of the region to allocate.</span></span>  
  
 `dwSize`  
 <span data-ttu-id="0d877-108">中区域的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0d877-108">[in] The size, in bytes, of the region.</span></span>  
  
 `flAllocationType`  
 <span data-ttu-id="0d877-109">中内存分配的类型。</span><span class="sxs-lookup"><span data-stu-id="0d877-109">[in] The type of memory allocation.</span></span>  
  
 `flProtect`  
 <span data-ttu-id="0d877-110">中要分配的页面区域的内存保护。</span><span class="sxs-lookup"><span data-stu-id="0d877-110">[in] Memory protection for the region of pages to be allocated.</span></span>  
  
 `dwCriticalLevel`  
 <span data-ttu-id="0d877-111">中指示分配失败的影响的 [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) 值。</span><span class="sxs-lookup"><span data-stu-id="0d877-111">[in] An [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) value that indicates the impact of an allocation failure.</span></span>  
  
 `ppMem`  
 <span data-ttu-id="0d877-112">弄指向分配的内存的起始地址的指针; 如果无法满足请求，则为 null。</span><span class="sxs-lookup"><span data-stu-id="0d877-112">[out] Pointer to the starting address of the allocated memory, or null if the request could not be satisfied.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0d877-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0d877-113">Return Value</span></span>  
  
|<span data-ttu-id="0d877-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0d877-114">HRESULT</span></span>|<span data-ttu-id="0d877-115">说明</span><span class="sxs-lookup"><span data-stu-id="0d877-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0d877-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d877-116">S_OK</span></span>|<span data-ttu-id="0d877-117">`VirtualAlloc` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="0d877-117">`VirtualAlloc` returned successfully.</span></span>|  
|<span data-ttu-id="0d877-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0d877-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0d877-119"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="0d877-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0d877-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0d877-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0d877-121">调用超时。</span><span class="sxs-lookup"><span data-stu-id="0d877-121">The call timed out.</span></span>|  
|<span data-ttu-id="0d877-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0d877-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0d877-123">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="0d877-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0d877-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0d877-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0d877-125">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="0d877-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0d877-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0d877-126">E_FAIL</span></span>|<span data-ttu-id="0d877-127">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="0d877-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0d877-128">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="0d877-128">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0d877-129">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="0d877-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="0d877-130">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="0d877-130">E_OUTOFMEMORY</span></span>|<span data-ttu-id="0d877-131">没有足够的可用内存来完成分配请求</span><span class="sxs-lookup"><span data-stu-id="0d877-131">Not enough memory was available to complete the allocation request</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0d877-132">注解</span><span class="sxs-lookup"><span data-stu-id="0d877-132">Remarks</span></span>  

 <span data-ttu-id="0d877-133">可以通过调用在进程的地址空间中保留区域 `VirtualAlloc` 。</span><span class="sxs-lookup"><span data-stu-id="0d877-133">You reserve a region in the address space of your process by calling `VirtualAlloc`.</span></span> <span data-ttu-id="0d877-134">`pAddress`参数包含所需内存块的起始地址。</span><span class="sxs-lookup"><span data-stu-id="0d877-134">The `pAddress` parameter contains the beginning address of the memory block you want.</span></span> <span data-ttu-id="0d877-135">此参数通常设置为 null。</span><span class="sxs-lookup"><span data-stu-id="0d877-135">This parameter is typically set to null.</span></span> <span data-ttu-id="0d877-136">操作系统会保留可用于进程的免费地址范围记录。</span><span class="sxs-lookup"><span data-stu-id="0d877-136">The operating system keeps a record of free address ranges available to your process.</span></span> <span data-ttu-id="0d877-137">如果 `pAddress` 值为 null，则指示系统在其认为合适的位置保留区域。</span><span class="sxs-lookup"><span data-stu-id="0d877-137">A `pAddress` value of null instructs the system to reserve the region wherever it sees fit.</span></span> <span data-ttu-id="0d877-138">或者，您可以为内存块提供特定的起始地址。</span><span class="sxs-lookup"><span data-stu-id="0d877-138">Alternatively, you can provide a specific starting address for the memory block.</span></span> <span data-ttu-id="0d877-139">在这两种情况下，output 参数 `ppMem` 将作为指向已分配内存的指针返回。</span><span class="sxs-lookup"><span data-stu-id="0d877-139">In both cases, the output parameter `ppMem` is returned as a pointer to the allocated memory.</span></span> <span data-ttu-id="0d877-140">函数本身返回 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="0d877-140">The function itself returns an HRESULT value.</span></span>  
  
 <span data-ttu-id="0d877-141">Win32 `VirtualAlloc` 函数没有 `ppMem` 参数，而是返回指向分配的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="0d877-141">The Win32 `VirtualAlloc` function does not have a `ppMem` parameter, and returns the pointer to the allocated memory instead.</span></span> <span data-ttu-id="0d877-142">有关详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="0d877-142">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d877-143">要求</span><span class="sxs-lookup"><span data-stu-id="0d877-143">Requirements</span></span>  

 <span data-ttu-id="0d877-144">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0d877-144">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d877-145">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0d877-145">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0d877-146">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0d877-146">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0d877-147">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d877-147">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d877-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d877-148">See also</span></span>

- [<span data-ttu-id="0d877-149">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="0d877-149">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
