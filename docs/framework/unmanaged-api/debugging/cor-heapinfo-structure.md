---
title: COR_HEAPINFO 结构
ms.date: 03/30/2017
api_name:
- COR_HEAPINFO
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_HEAPINFO
helpviewer_keywords:
- COR_HEAPINFO structure [.NET Framework debugging]
ms.assetid: bfb2cd39-3e0b-4d51-ba0c-f009755c1456
topic_type:
- apiref
ms.openlocfilehash: 5400350e1c489ec4c2ff3cddf83a4f1a8a0c7947
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726595"
---
# <a name="cor_heapinfo-structure"></a><span data-ttu-id="a32db-102">COR_HEAPINFO 结构</span><span class="sxs-lookup"><span data-stu-id="a32db-102">COR_HEAPINFO Structure</span></span>

<span data-ttu-id="a32db-103">提供有关垃圾回收堆的常规信息，包括它是否是可枚举的。</span><span class="sxs-lookup"><span data-stu-id="a32db-103">Provides general information about the garbage collection heap, including whether it is enumerable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a32db-104">语法</span><span class="sxs-lookup"><span data-stu-id="a32db-104">Syntax</span></span>  
  
```cpp  
typedef struct _COR_HEAPINFO {  
    BOOL areGCStructuresValid;
    DWORD pointerSize;
    DWORD numHeaps;  
    BOOL concurrent;
    CorDebugGCType gcType;
} COR_HEAPINFO;  
```  
  
## <a name="members"></a><span data-ttu-id="a32db-105">成员</span><span class="sxs-lookup"><span data-stu-id="a32db-105">Members</span></span>  
  
|<span data-ttu-id="a32db-106">成员</span><span class="sxs-lookup"><span data-stu-id="a32db-106">Member</span></span>|<span data-ttu-id="a32db-107">说明</span><span class="sxs-lookup"><span data-stu-id="a32db-107">Description</span></span>|  
|------------|-----------------|  
|`areGCStructuresValid`|<span data-ttu-id="a32db-108">`true` 如果垃圾回收结构有效并且可以枚举堆，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="a32db-108">`true` if garbage collection structures are valid and the heap can be enumerated; otherwise, `false`.</span></span>|  
|`pointerSize`|<span data-ttu-id="a32db-109">目标体系结构上指针的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a32db-109">The size, in bytes, of pointers on the target architecture.</span></span>|  
|`numHeaps`|<span data-ttu-id="a32db-110">进程中逻辑垃圾回收堆的数目。</span><span class="sxs-lookup"><span data-stu-id="a32db-110">The number of logical garbage collection heaps in the process.</span></span>|  
|`concurrent`|<span data-ttu-id="a32db-111">`TRUE` 如果启用了并发 (后台) 垃圾回收，则为;否则为 `FALSE` 。</span><span class="sxs-lookup"><span data-stu-id="a32db-111">`TRUE` if concurrent (background) garbage collection is enabled; otherwise, `FALSE`.</span></span>|  
|`gcType`|<span data-ttu-id="a32db-112">[CorDebugGCType](cordebuggctype-enumeration.md)枚举的成员，它指示垃圾回收器是在工作站上运行还是在服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="a32db-112">A member of the [CorDebugGCType](cordebuggctype-enumeration.md) enumeration that indicates whether the garbage collector is running on a workstation or a server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a32db-113">注解</span><span class="sxs-lookup"><span data-stu-id="a32db-113">Remarks</span></span>  

 <span data-ttu-id="a32db-114">使用 `COR_HEAPINFO` [ICorDebugProcess5：： GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) 方法返回结构的实例。</span><span class="sxs-lookup"><span data-stu-id="a32db-114">An instance of the `COR_HEAPINFO` structure is returned by calling the [ICorDebugProcess5::GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) method.</span></span>  
  
 <span data-ttu-id="a32db-115">枚举垃圾回收堆上的对象之前，必须始终检查 `areGCStructuresValid` 字段以确保堆处于可枚举状态。</span><span class="sxs-lookup"><span data-stu-id="a32db-115">Before enumerating objects on the garbage collection heap, you must always check the `areGCStructuresValid` field to ensure that the heap is in an enumerable state.</span></span> <span data-ttu-id="a32db-116">有关详细信息，请参阅 [ICorDebugProcess5：： GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a32db-116">For more information, see the [ICorDebugProcess5::GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a32db-117">要求</span><span class="sxs-lookup"><span data-stu-id="a32db-117">Requirements</span></span>  

 <span data-ttu-id="a32db-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a32db-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a32db-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a32db-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a32db-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a32db-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a32db-121">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a32db-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a32db-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a32db-122">See also</span></span>

- [<span data-ttu-id="a32db-123">调试结构</span><span class="sxs-lookup"><span data-stu-id="a32db-123">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="a32db-124">调试</span><span class="sxs-lookup"><span data-stu-id="a32db-124">Debugging</span></span>](index.md)
