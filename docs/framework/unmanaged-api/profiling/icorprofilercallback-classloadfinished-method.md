---
title: ICorProfilerCallback::ClassLoadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassLoadFinished
helpviewer_keywords:
- ClassLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ClassLoadFinished method [.NET Framework profiling]
ms.assetid: 3dd80fbe-d62d-4d4d-acf8-5b7d0efe607e
topic_type:
- apiref
ms.openlocfilehash: 3be00d278a92398ad282a071f3e313e5de0e65a6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700283"
---
# <a name="icorprofilercallbackclassloadfinished-method"></a><span data-ttu-id="d419a-102">ICorProfilerCallback::ClassLoadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="d419a-102">ICorProfilerCallback::ClassLoadFinished Method</span></span>

<span data-ttu-id="d419a-103">通知探查器类已经完成加载。</span><span class="sxs-lookup"><span data-stu-id="d419a-103">Notifies the profiler that a class has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d419a-104">语法</span><span class="sxs-lookup"><span data-stu-id="d419a-104">Syntax</span></span>  
  
```cpp  
HRESULT ClassLoadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d419a-105">参数</span><span class="sxs-lookup"><span data-stu-id="d419a-105">Parameters</span></span>

- `classId`

  <span data-ttu-id="d419a-106">\[in] 标识已加载的类。</span><span class="sxs-lookup"><span data-stu-id="d419a-106">\[in] Identifies the class that was loaded.</span></span>

- `hrStatus`

  <span data-ttu-id="d419a-107">\[在] 中指示是否已成功加载类的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d419a-107">\[in] An HRESULT that indicates whether the class loaded successfully.</span></span>

## <a name="remarks"></a><span data-ttu-id="d419a-108">注解</span><span class="sxs-lookup"><span data-stu-id="d419a-108">Remarks</span></span>  

 <span data-ttu-id="d419a-109">在 `classId` 调用方法之前，的值对信息请求无效 `ClassLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="d419a-109">The value of `classId` is not valid for an information request until the `ClassLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="d419a-110">在回调后，某些加载类的部分可能会继续 `ClassLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="d419a-110">Some parts of loading the class might continue after the `ClassLoadFinished` callback.</span></span> <span data-ttu-id="d419a-111">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="d419a-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="d419a-112">但是，中的成功 HRESULT `hrStatus` 仅指示加载类的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="d419a-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the class has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d419a-113">要求</span><span class="sxs-lookup"><span data-stu-id="d419a-113">Requirements</span></span>  

 <span data-ttu-id="d419a-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d419a-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d419a-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d419a-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d419a-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d419a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d419a-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d419a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d419a-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d419a-118">See also</span></span>

- [<span data-ttu-id="d419a-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d419a-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="d419a-120">ClassLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="d419a-120">ClassLoadStarted Method</span></span>](icorprofilercallback-classloadstarted-method.md)
