---
title: ICorProfilerInfo4::EnumThreads 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.EnumThreads
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::EnumThreads
helpviewer_keywords:
- ICorProfilerInfo4::EnumThreads method [.NET Framework profiling]
- EnumThreads method, ICorProfilerInfo4 interface [.NET Framework profiling]
ms.assetid: bca7a5b4-c207-4894-918c-0733926296dd
topic_type:
- apiref
ms.openlocfilehash: df0e66c8563404d7de4f1e11f41483f2f61f519c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721551"
---
# <a name="icorprofilerinfo4enumthreads-method"></a><span data-ttu-id="d65ff-102">ICorProfilerInfo4::EnumThreads 方法</span><span class="sxs-lookup"><span data-stu-id="d65ff-102">ICorProfilerInfo4::EnumThreads Method</span></span>

<span data-ttu-id="d65ff-103">返回一个枚举器，该枚举器提供按顺序循环访问所分析进程中所有托管线程的集合的方法。</span><span class="sxs-lookup"><span data-stu-id="d65ff-103">Returns an enumerator that provides methods to sequentially iterate through the collection of all managed threads in the profiled process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d65ff-104">语法</span><span class="sxs-lookup"><span data-stu-id="d65ff-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumThreads([out]  
            ICorProfilerThreadEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d65ff-105">参数</span><span class="sxs-lookup"><span data-stu-id="d65ff-105">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="d65ff-106">弄指向 [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="d65ff-106">[out] A pointer to an [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d65ff-107">备注</span><span class="sxs-lookup"><span data-stu-id="d65ff-107">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d65ff-108">要求</span><span class="sxs-lookup"><span data-stu-id="d65ff-108">Requirements</span></span>  

 <span data-ttu-id="d65ff-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d65ff-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d65ff-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d65ff-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d65ff-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d65ff-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d65ff-112">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d65ff-112">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d65ff-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d65ff-113">See also</span></span>

- [<span data-ttu-id="d65ff-114">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d65ff-114">ICorProfilerThreadEnum Interface</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="d65ff-115">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="d65ff-115">ICorProfilerInfo4 Interface</span></span>](icorprofilerinfo4-interface.md)
- [<span data-ttu-id="d65ff-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="d65ff-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="d65ff-117">分析</span><span class="sxs-lookup"><span data-stu-id="d65ff-117">Profiling</span></span>](index.md)
