---
title: COR_PRF_TRANSITION_REASON 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_TRANSITION_REASON
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_TRANSITION_REASON
helpviewer_keywords:
- COR_PRF_TRANSITION_REASON enumeration [.NET Framework profiling]
ms.assetid: da941118-01b7-4197-ae5b-9f2f8adcd623
topic_type:
- apiref
ms.openlocfilehash: 747313f217092652d5a9404fbf81383fa0828ee9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696656"
---
# <a name="cor_prf_transition_reason-enumeration"></a><span data-ttu-id="58d9c-102">COR_PRF_TRANSITION_REASON 枚举</span><span class="sxs-lookup"><span data-stu-id="58d9c-102">COR_PRF_TRANSITION_REASON Enumeration</span></span>

<span data-ttu-id="58d9c-103">指示从托管代码向非托管代码转换或从非托管代码向托管代码转换的原因。</span><span class="sxs-lookup"><span data-stu-id="58d9c-103">Indicates the reason for a transition from managed to unmanaged code, or vice versa.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58d9c-104">语法</span><span class="sxs-lookup"><span data-stu-id="58d9c-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_TRANSITION_CALL,  
    COR_PRF_TRANSITION_RETURN  
} COR_PRF_TRANSITION_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="58d9c-105">成员</span><span class="sxs-lookup"><span data-stu-id="58d9c-105">Members</span></span>  
  
|<span data-ttu-id="58d9c-106">成员</span><span class="sxs-lookup"><span data-stu-id="58d9c-106">Member</span></span>|<span data-ttu-id="58d9c-107">说明</span><span class="sxs-lookup"><span data-stu-id="58d9c-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_TRANSITION_CALL`|<span data-ttu-id="58d9c-108">由于调用了函数，因此转换。</span><span class="sxs-lookup"><span data-stu-id="58d9c-108">The transition is due to a call into a function.</span></span>|  
|`COR_PRF_TRANSITION_RETURN`|<span data-ttu-id="58d9c-109">由于从函数返回，因此转换。</span><span class="sxs-lookup"><span data-stu-id="58d9c-109">The transition is due to a return from a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="58d9c-110">注解</span><span class="sxs-lookup"><span data-stu-id="58d9c-110">Remarks</span></span>  

 <span data-ttu-id="58d9c-111">发生转换时，探查器会接收 [ICorProfilerCallback：： ManagedToUnmanagedTransition](icorprofilercallback-managedtounmanagedtransition-method.md) 或 [ICorProfilerCallback：： UnmanagedToManagedTransition](icorprofilercallback-unmanagedtomanagedtransition-method.md) 回调，其中任何一个都提供枚举的值， `COR_PRF_TRANSITION_REASON` 以指示转换的原因。</span><span class="sxs-lookup"><span data-stu-id="58d9c-111">When a transition occurs, the profiler receives an [ICorProfilerCallback::ManagedToUnmanagedTransition](icorprofilercallback-managedtounmanagedtransition-method.md) or [ICorProfilerCallback::UnmanagedToManagedTransition](icorprofilercallback-unmanagedtomanagedtransition-method.md) callback, either of which provides a value of the `COR_PRF_TRANSITION_REASON` enumeration to indicate the reason for the transition.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58d9c-112">要求</span><span class="sxs-lookup"><span data-stu-id="58d9c-112">Requirements</span></span>  

 <span data-ttu-id="58d9c-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58d9c-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58d9c-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="58d9c-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="58d9c-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58d9c-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58d9c-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58d9c-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
