---
title: COR_GC_THREAD_STATS 结构
ms.date: 03/30/2017
api_name:
- COR_GC_THREAD_STATS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_THREAD_STATS
helpviewer_keywords:
- COR_GC_THREAD_STATS structure [.NET Framework hosting]
ms.assetid: 01f9a59b-7679-4d42-9ced-4a8981625c3d
topic_type:
- apiref
ms.openlocfilehash: 25a90965dc5466b7cf1a07140705424cf2ba4cd9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95699230"
---
# <a name="cor_gc_thread_stats-structure"></a><span data-ttu-id="40c18-102">COR_GC_THREAD_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="40c18-102">COR_GC_THREAD_STATS Structure</span></span>

<span data-ttu-id="40c18-103">包含与垃圾回收相关的每个线程的统计信息。</span><span class="sxs-lookup"><span data-stu-id="40c18-103">Contains per-thread statistics pertaining to garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40c18-104">语法</span><span class="sxs-lookup"><span data-stu-id="40c18-104">Syntax</span></span>  
  
```cpp  
typedef struct _COR_GC_THREAD_STATS {  
    ULONGLONG  PerThreadAllocation;
    ULONG      Flags;
} COR_GC_THREAD_STATS;  
```  
  
## <a name="members"></a><span data-ttu-id="40c18-105">成员</span><span class="sxs-lookup"><span data-stu-id="40c18-105">Members</span></span>  
  
|<span data-ttu-id="40c18-106">成员</span><span class="sxs-lookup"><span data-stu-id="40c18-106">Member</span></span>|<span data-ttu-id="40c18-107">说明</span><span class="sxs-lookup"><span data-stu-id="40c18-107">Description</span></span>|  
|------------|-----------------|  
|`PerThreadAllocation`|<span data-ttu-id="40c18-108">与当前实例关联的线程上分配的内存字节数 `COR_GC_THREAD_STATS` 。</span><span class="sxs-lookup"><span data-stu-id="40c18-108">The number of bytes of memory allocated on the thread that is associated with the current `COR_GC_THREAD_STATS` instance.</span></span> <span data-ttu-id="40c18-109">每次发生零代垃圾回收时，此数字会被清除为零。</span><span class="sxs-lookup"><span data-stu-id="40c18-109">This number is cleared to zero each time a generation-zero garbage collection occurs.</span></span>|  
|`Flags`|<span data-ttu-id="40c18-110">最近一次垃圾回收后提升为较高代的字节数。</span><span class="sxs-lookup"><span data-stu-id="40c18-110">The number of bytes promoted to a higher generation at the most recent garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="40c18-111">注解</span><span class="sxs-lookup"><span data-stu-id="40c18-111">Remarks</span></span>  

 <span data-ttu-id="40c18-112">[ICLRTask：： GetMemStats](iclrtask-getmemstats-method.md) 采用类型为的输出参数 `COR_GC_THREAD_STATS` 。</span><span class="sxs-lookup"><span data-stu-id="40c18-112">[ICLRTask::GetMemStats](iclrtask-getmemstats-method.md) takes an output parameter of type `COR_GC_THREAD_STATS`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40c18-113">要求</span><span class="sxs-lookup"><span data-stu-id="40c18-113">Requirements</span></span>  

 <span data-ttu-id="40c18-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="40c18-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40c18-115">**标头：** GCHost .idl</span><span class="sxs-lookup"><span data-stu-id="40c18-115">**Header:** GCHost.idl</span></span>  
  
 <span data-ttu-id="40c18-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="40c18-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="40c18-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40c18-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40c18-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="40c18-118">See also</span></span>

- [<span data-ttu-id="40c18-119">承载结构</span><span class="sxs-lookup"><span data-stu-id="40c18-119">Hosting Structures</span></span>](hosting-structures.md)
- [<span data-ttu-id="40c18-120">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="40c18-120">IHostTask Interface</span></span>](ihosttask-interface.md)
