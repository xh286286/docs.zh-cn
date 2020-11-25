---
title: ICorProfilerInfo4::EnumJITedFunctions2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.EnumJITedFunctions2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::EnumJITedFunctions2
helpviewer_keywords:
- EnumJITedFunctions2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::EnumJITedFunctions2 method [.NET Framework profiling]
ms.assetid: 40e9a1be-9bd2-4fad-9921-34a84b61c1e3
topic_type:
- apiref
ms.openlocfilehash: 2a6ddaef7b64427f8349abedbbd85b4d82a0b88c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697787"
---
# <a name="icorprofilerinfo4enumjitedfunctions2-method"></a><span data-ttu-id="93940-102">ICorProfilerInfo4::EnumJITedFunctions2 方法</span><span class="sxs-lookup"><span data-stu-id="93940-102">ICorProfilerInfo4::EnumJITedFunctions2 Method</span></span>

<span data-ttu-id="93940-103">返回之前 JIT 编译和 JIT 重新编译的所有函数的枚举器。</span><span class="sxs-lookup"><span data-stu-id="93940-103">Returns an enumerator for all functions that were previously JIT-compiled and JIT-recompiled.</span></span> <span data-ttu-id="93940-104">此方法将替换 [ICorProfilerInfo3：： EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) 方法，该方法不枚举 JIT 重新编译的 id。</span><span class="sxs-lookup"><span data-stu-id="93940-104">This method replaces the [ICorProfilerInfo3::EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) method, which does not enumerate JIT-recompiled IDs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93940-105">语法</span><span class="sxs-lookup"><span data-stu-id="93940-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumJITedFunctions([out] ICorProfilerFunctionEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="93940-106">参数</span><span class="sxs-lookup"><span data-stu-id="93940-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="93940-107">弄指向 [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) 枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="93940-107">[out] A pointer to the [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) enumerator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="93940-108">注解</span><span class="sxs-lookup"><span data-stu-id="93940-108">Remarks</span></span>  

 <span data-ttu-id="93940-109">此方法可能与 `JITCompilation` 回调（如 [ICorProfilerCallback：： JITCompilationStarted](icorprofilercallback-jitcompilationstarted-method.md) 方法）重叠。</span><span class="sxs-lookup"><span data-stu-id="93940-109">This method may overlap with `JITCompilation` callbacks such as the [ICorProfilerCallback::JITCompilationStarted](icorprofilercallback-jitcompilationstarted-method.md) method.</span></span> <span data-ttu-id="93940-110">返回的枚举包含字段的值 `COR_PRF_FUNCTION::reJitId` 。</span><span class="sxs-lookup"><span data-stu-id="93940-110">The returned enumeration includes values for the `COR_PRF_FUNCTION::reJitId` field.</span></span> <span data-ttu-id="93940-111">此方法替换的 [ICorProfilerInfo3：： EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) 方法不枚举 JIT 重新编译的 id，因为 `COR_PRF_FUNCTION::reJitId` 字段始终设置为0。</span><span class="sxs-lookup"><span data-stu-id="93940-111">The [ICorProfilerInfo3::EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) method, which this method replaces, does not enumerate JIT-recompiled IDs, because the `COR_PRF_FUNCTION::reJitId` field is always set to 0.</span></span> <span data-ttu-id="93940-112">`ICorProfilerInfo4::EnumJITedFunctions`方法会枚举 JIT 重新编译的 id，因为 `COR_PRF_FUNCTION::reJitId` 字段设置正确。</span><span class="sxs-lookup"><span data-stu-id="93940-112">The `ICorProfilerInfo4::EnumJITedFunctions` method does enumerate JIT-recompiled IDs, because the `COR_PRF_FUNCTION::reJitId` field is set properly.</span></span> <span data-ttu-id="93940-113">请注意， [ICorProfilerInfo4：： EnumJITedFunctions2](icorprofilerinfo4-enumjitedfunctions2-method.md) 方法可以触发垃圾回收，而 [ICorProfilerInfo3：： EnumJITedFunctions 方法](icorprofilerinfo3-enumjitedfunctions-method.md) 将不会触发垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="93940-113">Note that the [ICorProfilerInfo4::EnumJITedFunctions2](icorprofilerinfo4-enumjitedfunctions2-method.md) method can trigger a garbage collection, whereas [ICorProfilerInfo3::EnumJITedFunctions method](icorprofilerinfo3-enumjitedfunctions-method.md) will not.</span></span>  <span data-ttu-id="93940-114">有关详细信息，请参阅 [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](corprof-e-unsupported-call-sequence-hresult.md)。</span><span class="sxs-lookup"><span data-stu-id="93940-114">For more information, see [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](corprof-e-unsupported-call-sequence-hresult.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93940-115">要求</span><span class="sxs-lookup"><span data-stu-id="93940-115">Requirements</span></span>  

 <span data-ttu-id="93940-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="93940-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93940-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="93940-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="93940-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93940-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93940-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93940-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93940-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="93940-120">See also</span></span>

- [<span data-ttu-id="93940-121">EnumJITedFunctions 方法</span><span class="sxs-lookup"><span data-stu-id="93940-121">EnumJITedFunctions Method</span></span>](icorprofilerinfo3-enumjitedfunctions-method.md)
- [<span data-ttu-id="93940-122">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="93940-122">ICorProfilerInfo4 Interface</span></span>](icorprofilerinfo4-interface.md)
- [<span data-ttu-id="93940-123">分析接口</span><span class="sxs-lookup"><span data-stu-id="93940-123">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="93940-124">分析</span><span class="sxs-lookup"><span data-stu-id="93940-124">Profiling</span></span>](index.md)
