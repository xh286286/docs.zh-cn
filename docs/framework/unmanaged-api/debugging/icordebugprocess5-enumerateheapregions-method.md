---
title: ICorDebugProcess5::EnumerateHeapRegions 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.EnumerateHeapRegions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnumerateHeapRegions
helpviewer_keywords:
- EnumerateHeapRegions method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::EnumerateHeapRegions method [.NET Framework debugging]
ms.assetid: b1edba68-9c36-4f69-be9f-678ce0b33480
topic_type:
- apiref
ms.openlocfilehash: 5a51670200f8fc8a98ff7b80334253b37c7d89ed
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671117"
---
# <a name="icordebugprocess5enumerateheapregions-method"></a><span data-ttu-id="1530d-102">ICorDebugProcess5::EnumerateHeapRegions 方法</span><span class="sxs-lookup"><span data-stu-id="1530d-102">ICorDebugProcess5::EnumerateHeapRegions Method</span></span>

<span data-ttu-id="1530d-103">获取托管堆的内存范围的枚举器。</span><span class="sxs-lookup"><span data-stu-id="1530d-103">Gets an enumerator for the memory ranges of the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1530d-104">语法</span><span class="sxs-lookup"><span data-stu-id="1530d-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateHeapRegions(  
   [out] ICorDebugHeapSegmentEnum **ppRegions  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1530d-105">参数</span><span class="sxs-lookup"><span data-stu-id="1530d-105">Parameters</span></span>  

 `ppRegions`  
 <span data-ttu-id="1530d-106">弄指向 [ICorDebugHeapSegmentEnum](icordebugheapsegmentenum-interface.md) 接口对象地址的指针，该对象是对象驻留在托管堆中的内存范围的枚举器。</span><span class="sxs-lookup"><span data-stu-id="1530d-106">[out] A pointer to the address of an [ICorDebugHeapSegmentEnum](icordebugheapsegmentenum-interface.md) interface object that is an enumerator for the ranges of memory in which objects reside in the managed heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1530d-107">注解</span><span class="sxs-lookup"><span data-stu-id="1530d-107">Remarks</span></span>  

 <span data-ttu-id="1530d-108">在调用 `ICorDebugProcess5::EnumerateHeapRegions` 方法之前，应调用 [ICorDebugProcess5：： GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) 方法，并检查 `areGCStructuresValid` 返回 [COR_HEAPINFO](cor-heapinfo-structure.md) 对象的字段值，以确保其当前状态的垃圾回收堆可枚举。</span><span class="sxs-lookup"><span data-stu-id="1530d-108">Before calling the `ICorDebugProcess5::EnumerateHeapRegions` method, you should call the [ICorDebugProcess5::GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) method and examine the value of the `areGCStructuresValid` field of the returned [COR_HEAPINFO](cor-heapinfo-structure.md) object to ensure that the garbage collection heap in its current state is enumerable.</span></span> <span data-ttu-id="1530d-109">此外，如果在 `ICorDebugProcess5::EnumerateHeapRegions` 进程的 `E_FAIL` 生存期内附加过早，则在创建内存区域之前，此方法返回。</span><span class="sxs-lookup"><span data-stu-id="1530d-109">In addition, the `ICorDebugProcess5::EnumerateHeapRegions` method returns `E_FAIL` if you attach too early in the lifetime of the process, before memory regions are created.</span></span>  
  
 <span data-ttu-id="1530d-110">此方法保证可以枚举可能包含托管对象的所有内存区域，但不保证托管对象实际驻留在这些区域中。</span><span class="sxs-lookup"><span data-stu-id="1530d-110">This method is guaranteed to enumerate all memory regions that may contain managed objects, but it does not guarantee that managed objects actually reside in those regions.</span></span> <span data-ttu-id="1530d-111">[ICorDebugHeapSegmentEnum](icordebugheapsegmentenum-interface.md)集合对象可能包含空的或保留的内存区域。</span><span class="sxs-lookup"><span data-stu-id="1530d-111">The [ICorDebugHeapSegmentEnum](icordebugheapsegmentenum-interface.md) collection object may include empty or reserved memory regions.</span></span>  
  
 <span data-ttu-id="1530d-112">[ICorDebugHeapSegmentEnum](icordebugheapsegmentenum-interface.md)接口对象是从 ICorDebugEnum 接口派生的标准枚举器，该枚举器可用于枚举[COR_SEGMENT](cor-segment-structure.md)的对象。</span><span class="sxs-lookup"><span data-stu-id="1530d-112">The [ICorDebugHeapSegmentEnum](icordebugheapsegmentenum-interface.md) interface object is a standard enumerator derived from the ICorDebugEnum interface that allows you to enumerate [COR_SEGMENT](cor-segment-structure.md) objects.</span></span> <span data-ttu-id="1530d-113">每个 [COR_SEGMENT](cor-segment-structure.md) 对象均提供有关特定段的内存范围以及该段中的对象的生成信息。</span><span class="sxs-lookup"><span data-stu-id="1530d-113">Each [COR_SEGMENT](cor-segment-structure.md) object provides information about the memory range of a particular segment, along with the generation of the objects in that segment.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1530d-114">要求</span><span class="sxs-lookup"><span data-stu-id="1530d-114">Requirements</span></span>  

 <span data-ttu-id="1530d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1530d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1530d-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1530d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1530d-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1530d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1530d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1530d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1530d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1530d-119">See also</span></span>

- [<span data-ttu-id="1530d-120">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="1530d-120">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="1530d-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="1530d-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
