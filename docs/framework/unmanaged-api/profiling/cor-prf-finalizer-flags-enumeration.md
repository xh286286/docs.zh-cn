---
title: COR_PRF_FINALIZER_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_FINALIZER_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FINALIZER_FLAGS
helpviewer_keywords:
- COR_PRF_FINALIZER_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 297d7721-3911-4f36-9e34-d9da0c33e22a
topic_type:
- apiref
ms.openlocfilehash: 2b766715d6d87ab17a7cdabf721bbebf67e1ff13
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95718574"
---
# <a name="cor_prf_finalizer_flags-enumeration"></a><span data-ttu-id="838a7-102">COR_PRF_FINALIZER_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="838a7-102">COR_PRF_FINALIZER_FLAGS Enumeration</span></span>

<span data-ttu-id="838a7-103">描述对象的终结器。</span><span class="sxs-lookup"><span data-stu-id="838a7-103">Describes the finalizer for an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="838a7-104">语法</span><span class="sxs-lookup"><span data-stu-id="838a7-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_FINALIZER_CRITICAL = 0x1  
} COR_PRF_FINALIZER_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="838a7-105">成员</span><span class="sxs-lookup"><span data-stu-id="838a7-105">Members</span></span>  
  
|<span data-ttu-id="838a7-106">成员</span><span class="sxs-lookup"><span data-stu-id="838a7-106">Member</span></span>|<span data-ttu-id="838a7-107">说明</span><span class="sxs-lookup"><span data-stu-id="838a7-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FINALIZER_CRITICAL`|<span data-ttu-id="838a7-108">终结器至关重要。</span><span class="sxs-lookup"><span data-stu-id="838a7-108">The finalizer is critical.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="838a7-109">注解</span><span class="sxs-lookup"><span data-stu-id="838a7-109">Remarks</span></span>  

 <span data-ttu-id="838a7-110">`COR_PRF_FINALIZER_FLAGS` [ICorProfilerCallback2：： FinalizeableObjectQueued](icorprofilercallback2-finalizeableobjectqueued-method.md)方法使用枚举来描述对象的终结器。</span><span class="sxs-lookup"><span data-stu-id="838a7-110">The `COR_PRF_FINALIZER_FLAGS` enumeration is used by the [ICorProfilerCallback2::FinalizeableObjectQueued](icorprofilercallback2-finalizeableobjectqueued-method.md) method to describe the finalizer for an object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="838a7-111">要求</span><span class="sxs-lookup"><span data-stu-id="838a7-111">Requirements</span></span>  

 <span data-ttu-id="838a7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="838a7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="838a7-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="838a7-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="838a7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="838a7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="838a7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="838a7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="838a7-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="838a7-116">See also</span></span>

- [<span data-ttu-id="838a7-117">分析枚举</span><span class="sxs-lookup"><span data-stu-id="838a7-117">Profiling Enumerations</span></span>](profiling-enumerations.md)
