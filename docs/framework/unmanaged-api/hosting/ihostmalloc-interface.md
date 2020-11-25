---
title: IHostMalloc 接口
ms.date: 03/30/2017
api_name:
- IHostMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc
helpviewer_keywords:
- IHostMAlloc interface [.NET Framework hosting]
ms.assetid: e3c6643b-6fc7-4a99-959d-4b7b4e63fdee
topic_type:
- apiref
ms.openlocfilehash: 2530c7fcd63f81b566d6623a533bd8e2af084047
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702155"
---
# <a name="ihostmalloc-interface"></a><span data-ttu-id="898ba-102">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="898ba-102">IHostMalloc Interface</span></span>

<span data-ttu-id="898ba-103">提供一些方法，这些方法允许公共语言运行时 (CLR) 通过宿主请求从堆进行细化分配。</span><span class="sxs-lookup"><span data-stu-id="898ba-103">Provides methods that allow the common language runtime (CLR) to request fine-grained allocations from the heap through the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="898ba-104">方法</span><span class="sxs-lookup"><span data-stu-id="898ba-104">Methods</span></span>  
  
|<span data-ttu-id="898ba-105">方法</span><span class="sxs-lookup"><span data-stu-id="898ba-105">Method</span></span>|<span data-ttu-id="898ba-106">说明</span><span class="sxs-lookup"><span data-stu-id="898ba-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="898ba-107">Alloc 方法</span><span class="sxs-lookup"><span data-stu-id="898ba-107">Alloc Method</span></span>](ihostmalloc-alloc-method.md)|<span data-ttu-id="898ba-108">请求宿主从堆分配请求的内存量。</span><span class="sxs-lookup"><span data-stu-id="898ba-108">Requests that the host allocate the requested amount of memory from the heap.</span></span>|  
|[<span data-ttu-id="898ba-109">DebugAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="898ba-109">DebugAlloc Method</span></span>](ihostmalloc-debugalloc-method.md)|<span data-ttu-id="898ba-110">请求宿主从堆分配请求的内存量，并另外跟踪内存的分配位置。</span><span class="sxs-lookup"><span data-stu-id="898ba-110">Requests that the host allocate the requested amount of memory from the heap, and additionally track where the memory was allocated.</span></span>|  
|[<span data-ttu-id="898ba-111">Free 方法</span><span class="sxs-lookup"><span data-stu-id="898ba-111">Free Method</span></span>](ihostmalloc-free-method.md)|<span data-ttu-id="898ba-112">释放通过使用方法分配的内存 `Alloc` 。</span><span class="sxs-lookup"><span data-stu-id="898ba-112">Frees memory that was allocated by using the `Alloc` method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="898ba-113">注解</span><span class="sxs-lookup"><span data-stu-id="898ba-113">Remarks</span></span>  

 <span data-ttu-id="898ba-114">CLR `IHostMalloc` 通过调用 [IHostMemoryManager：： CreateMalloc](ihostmemorymanager-createmalloc-method.md) 方法获取指向实例的接口指针。</span><span class="sxs-lookup"><span data-stu-id="898ba-114">The CLR gets an interface pointer to an `IHostMalloc` instance by calling the [IHostMemoryManager::CreateMalloc](ihostmemorymanager-createmalloc-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="898ba-115">要求</span><span class="sxs-lookup"><span data-stu-id="898ba-115">Requirements</span></span>  

 <span data-ttu-id="898ba-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="898ba-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="898ba-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="898ba-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="898ba-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="898ba-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="898ba-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="898ba-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="898ba-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="898ba-120">See also</span></span>

- [<span data-ttu-id="898ba-121">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="898ba-121">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="898ba-122">承载接口</span><span class="sxs-lookup"><span data-stu-id="898ba-122">Hosting Interfaces</span></span>](hosting-interfaces.md)
