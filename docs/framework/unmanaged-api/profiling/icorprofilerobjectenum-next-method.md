---
title: ICorProfilerObjectEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Next
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Next
helpviewer_keywords:
- Next method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Next method [.NET Framework profiling]
ms.assetid: b420433c-5ebe-4986-bba1-97902e6db819
topic_type:
- apiref
ms.openlocfilehash: e0c10549ab9075c2e7604a9adb18cae8b9a3b32b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702363"
---
# <a name="icorprofilerobjectenumnext-method"></a><span data-ttu-id="40b9d-102">ICorProfilerObjectEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="40b9d-102">ICorProfilerObjectEnum::Next Method</span></span>

<span data-ttu-id="40b9d-103">从对象的顺序集合中获取指定数目的连续对象，从该序列中的枚举器的当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="40b9d-103">Gets the specified number of contiguous objects from a sequential collection of objects, starting at the enumerator's current position in the sequence.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40b9d-104">语法</span><span class="sxs-lookup"><span data-stu-id="40b9d-104">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG                    celt,  
    [out, size_is(celt), length_is(*pceltFetched)]
        ObjectID                  objects[],  
    [out] ULONG                   *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="40b9d-105">参数</span><span class="sxs-lookup"><span data-stu-id="40b9d-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="40b9d-106">[in] 要检索的对象数。</span><span class="sxs-lookup"><span data-stu-id="40b9d-106">[in] The number of objects to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="40b9d-107">弄值的数组 `ObjectID` ，其中每个值都表示检索到的对象。</span><span class="sxs-lookup"><span data-stu-id="40b9d-107">[out] An array of `ObjectID` values, each of which represents a retrieved object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="40b9d-108">[out] 指向 `objects` 数组中实际返回的元素数目的指针。</span><span class="sxs-lookup"><span data-stu-id="40b9d-108">[out] A pointer to the number of elements actually returned in the `objects` array.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40b9d-109">要求</span><span class="sxs-lookup"><span data-stu-id="40b9d-109">Requirements</span></span>  

 <span data-ttu-id="40b9d-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="40b9d-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40b9d-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="40b9d-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="40b9d-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="40b9d-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="40b9d-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40b9d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40b9d-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="40b9d-114">See also</span></span>

- [<span data-ttu-id="40b9d-115">ICorProfilerObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="40b9d-115">ICorProfilerObjectEnum Interface</span></span>](icorprofilerobjectenum-interface.md)
