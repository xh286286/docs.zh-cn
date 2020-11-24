---
title: COR_PRF_GC_ROOT_KIND 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_ROOT_KIND
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_ROOT_KIND
helpviewer_keywords:
- COR_PRF_GC_ROOT_KIND enumeration [.NET Framework profiling]
ms.assetid: b9fb1c03-417f-41d4-aed4-02cb4ade8def
topic_type:
- apiref
ms.openlocfilehash: e86074031b8fc2c82636e7aef2177eaf04a9db14
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95682358"
---
# <a name="cor_prf_gc_root_kind-enumeration"></a><span data-ttu-id="e86e1-102">COR_PRF_GC_ROOT_KIND 枚举</span><span class="sxs-lookup"><span data-stu-id="e86e1-102">COR_PRF_GC_ROOT_KIND Enumeration</span></span>

<span data-ttu-id="e86e1-103">指示由 [ICorProfilerCallback2：： RootReferences2](icorprofilercallback2-rootreferences2-method.md) 回调公开的垃圾回收根的类型。</span><span class="sxs-lookup"><span data-stu-id="e86e1-103">Indicates the kind of garbage collection root that is exposed by the [ICorProfilerCallback2::RootReferences2](icorprofilercallback2-rootreferences2-method.md) callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e86e1-104">语法</span><span class="sxs-lookup"><span data-stu-id="e86e1-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_GC_ROOT_STACK = 1,  
    COR_PRF_GC_ROOT_FINALIZER = 2,  
    COR_PRF_GC_ROOT_HANDLE = 3,  
    COR_PRF_GC_ROOT_OTHER = 0  
} COR_PRF_GC_ROOT_KIND;  
```  
  
## <a name="members"></a><span data-ttu-id="e86e1-105">成员</span><span class="sxs-lookup"><span data-stu-id="e86e1-105">Members</span></span>  
  
|<span data-ttu-id="e86e1-106">成员</span><span class="sxs-lookup"><span data-stu-id="e86e1-106">Member</span></span>|<span data-ttu-id="e86e1-107">说明</span><span class="sxs-lookup"><span data-stu-id="e86e1-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_ROOT_STACK`|<span data-ttu-id="e86e1-108">根是堆栈上的变量。</span><span class="sxs-lookup"><span data-stu-id="e86e1-108">The root is a variable on the stack.</span></span>|  
|`COR_PRF_GC_ROOT_FINALIZER`|<span data-ttu-id="e86e1-109">根是终结器队列中的条目。</span><span class="sxs-lookup"><span data-stu-id="e86e1-109">The root is an entry in the finalizer queue.</span></span>|  
|`COR_PRF_GC_ROOT_HANDLE`|<span data-ttu-id="e86e1-110">根为垃圾回收句柄。</span><span class="sxs-lookup"><span data-stu-id="e86e1-110">The root is a garbage collection handle.</span></span>|  
|`COR_PRF_GC_ROOT_OTHER`|<span data-ttu-id="e86e1-111">根的类型未指定。</span><span class="sxs-lookup"><span data-stu-id="e86e1-111">The kind of root is unspecified.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e86e1-112">要求</span><span class="sxs-lookup"><span data-stu-id="e86e1-112">Requirements</span></span>  

 <span data-ttu-id="e86e1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e86e1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e86e1-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e86e1-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e86e1-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e86e1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e86e1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e86e1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e86e1-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e86e1-117">See also</span></span>

- [<span data-ttu-id="e86e1-118">分析枚举</span><span class="sxs-lookup"><span data-stu-id="e86e1-118">Profiling Enumerations</span></span>](profiling-enumerations.md)
