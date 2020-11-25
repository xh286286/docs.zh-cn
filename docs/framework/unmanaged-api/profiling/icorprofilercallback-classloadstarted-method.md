---
title: ICorProfilerCallback::ClassLoadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::ClassLoadStarted method [.NET Framework profiling]
- ClassLoadStarted method [.NET Framework profiling]
ms.assetid: 9f728de8-45c2-45a5-ac4a-45660bd36ecf
topic_type:
- apiref
ms.openlocfilehash: fbdc9345c8364f33ac69da452dd91155fd5eede9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700270"
---
# <a name="icorprofilercallbackclassloadstarted-method"></a><span data-ttu-id="7ebb0-102">ICorProfilerCallback::ClassLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="7ebb0-102">ICorProfilerCallback::ClassLoadStarted Method</span></span>

<span data-ttu-id="7ebb0-103">通知探查器正在加载某个类。</span><span class="sxs-lookup"><span data-stu-id="7ebb0-103">Notifies the profiler that a class is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ebb0-104">语法</span><span class="sxs-lookup"><span data-stu-id="7ebb0-104">Syntax</span></span>  
  
```cpp  
HRESULT ClassLoadStarted(  
    [in] ClassID classId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7ebb0-105">参数</span><span class="sxs-lookup"><span data-stu-id="7ebb0-105">Parameters</span></span>

- `classId`

  <span data-ttu-id="7ebb0-106">\[in] 标识正在加载的类。</span><span class="sxs-lookup"><span data-stu-id="7ebb0-106">\[in] Identifies the class that is being loaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ebb0-107">注解</span><span class="sxs-lookup"><span data-stu-id="7ebb0-107">Remarks</span></span>  

 <span data-ttu-id="7ebb0-108">在 `classId` 调用 [ICorProfilerCallback：： ClassLoadFinished](icorprofilercallback-classloadfinished-method.md) 方法之前，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="7ebb0-108">The value of `classId` is not valid for an information request until the [ICorProfilerCallback::ClassLoadFinished](icorprofilercallback-classloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7ebb0-109">要求</span><span class="sxs-lookup"><span data-stu-id="7ebb0-109">Requirements</span></span>  

 <span data-ttu-id="7ebb0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7ebb0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7ebb0-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7ebb0-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7ebb0-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7ebb0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7ebb0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7ebb0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ebb0-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ebb0-114">See also</span></span>

- [<span data-ttu-id="7ebb0-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7ebb0-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
