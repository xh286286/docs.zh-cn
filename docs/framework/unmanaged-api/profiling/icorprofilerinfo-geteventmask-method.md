---
title: ICorProfilerInfo::GetEventMask 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetEventMask
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetEventMask
helpviewer_keywords:
- GetEventMask method [.NET Framework profiling]
- ICorProfilerInfo::GetEventMask method [.NET Framework profiling]
ms.assetid: ec34cc13-45a3-4695-abc3-b3347d4e6fc2
topic_type:
- apiref
ms.openlocfilehash: 16bd8b09d5118171e669e9c428fb444384b5867d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722558"
---
# <a name="icorprofilerinfogeteventmask-method"></a><span data-ttu-id="20d94-102">ICorProfilerInfo::GetEventMask 方法</span><span class="sxs-lookup"><span data-stu-id="20d94-102">ICorProfilerInfo::GetEventMask Method</span></span>

<span data-ttu-id="20d94-103">获取探查器要从公共语言运行时 (CLR) 中接收其事件通知的当前事件类别。</span><span class="sxs-lookup"><span data-stu-id="20d94-103">Gets the current event categories for which the profiler wants to receive event notifications from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20d94-104">语法</span><span class="sxs-lookup"><span data-stu-id="20d94-104">Syntax</span></span>  
  
```cpp  
HRESULT GetEventMask(  
    [out] DWORD *pdwEvents);  
```  
  
## <a name="parameters"></a><span data-ttu-id="20d94-105">参数</span><span class="sxs-lookup"><span data-stu-id="20d94-105">Parameters</span></span>  

 `pdwEvents`  
 <span data-ttu-id="20d94-106">[out] 一个指向指定事件类别的 4 字节值的指针。</span><span class="sxs-lookup"><span data-stu-id="20d94-106">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="20d94-107">每个位都可控制不同的功能、行为或事件类型。</span><span class="sxs-lookup"><span data-stu-id="20d94-107">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="20d94-108">[COR_PRF_MONITOR](cor-prf-monitor-enumeration.md)枚举中描述了这些位。</span><span class="sxs-lookup"><span data-stu-id="20d94-108">The bits are described in the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="20d94-109">注解</span><span class="sxs-lookup"><span data-stu-id="20d94-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="20d94-110">应调用 [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) 方法，而不是此方法。</span><span class="sxs-lookup"><span data-stu-id="20d94-110">You should call the [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) method instead of this method.</span></span> <span data-ttu-id="20d94-111">尽管此 `SetEventMask` 方法继续受支持，但 [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) 提供其他功能。</span><span class="sxs-lookup"><span data-stu-id="20d94-111">Although the `SetEventMask` method continues to be supported, [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) provides additional functionality.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20d94-112">要求</span><span class="sxs-lookup"><span data-stu-id="20d94-112">Requirements</span></span>  

 <span data-ttu-id="20d94-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20d94-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20d94-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="20d94-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="20d94-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="20d94-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="20d94-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20d94-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20d94-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="20d94-117">See also</span></span>

- [<span data-ttu-id="20d94-118">GetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="20d94-118">GetEventMask2 Method</span></span>](icorprofilerinfo5-geteventmask2-method.md)
- [<span data-ttu-id="20d94-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="20d94-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
