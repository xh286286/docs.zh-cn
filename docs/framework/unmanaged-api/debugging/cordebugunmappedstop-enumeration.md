---
title: CorDebugUnmappedStop 枚举
ms.date: 03/30/2017
api_name:
- CorDebugUnmappedStop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugUnmappedStop
helpviewer_keywords:
- CorDebugUnmappedStop enumeration [.NET Framework debugging]
ms.assetid: a684f7d7-d0c2-4690-b721-639e613f11f8
topic_type:
- apiref
ms.openlocfilehash: e251bf67adcaf2bbd6565eda068d487eb0d70efd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725763"
---
# <a name="cordebugunmappedstop-enumeration"></a><span data-ttu-id="2f573-102">CorDebugUnmappedStop 枚举</span><span class="sxs-lookup"><span data-stu-id="2f573-102">CorDebugUnmappedStop Enumeration</span></span>

<span data-ttu-id="2f573-103">指定未映射代码的类型，这些代码可以中断分档器代码执行。</span><span class="sxs-lookup"><span data-stu-id="2f573-103">Specifies the type of unmapped code that can trigger a halt in code execution by the stepper.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f573-104">语法</span><span class="sxs-lookup"><span data-stu-id="2f573-104">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugUnmappedStop {  
    STOP_NONE               = 0x0,  
    STOP_PROLOG             = 0x01,  
    STOP_EPILOG             = 0x02,  
    STOP_NO_MAPPING_INFO    = 0x04,  
    STOP_OTHER_UNMAPPED     = 0x08,  
    STOP_UNMANAGED          = 0x10,  
    STOP_ALL                = 0xffff,  
} CorDebugUnmappedStop;  
```  
  
## <a name="members"></a><span data-ttu-id="2f573-105">成员</span><span class="sxs-lookup"><span data-stu-id="2f573-105">Members</span></span>  
  
|<span data-ttu-id="2f573-106">成员</span><span class="sxs-lookup"><span data-stu-id="2f573-106">Member</span></span>|<span data-ttu-id="2f573-107">说明</span><span class="sxs-lookup"><span data-stu-id="2f573-107">Description</span></span>|  
|------------|-----------------|  
|`STOP_NONE`|<span data-ttu-id="2f573-108">请勿在任何类型的未映射代码中停止。</span><span class="sxs-lookup"><span data-stu-id="2f573-108">Do not stop in any type of unmapped code.</span></span>|  
|`STOP_PROLOG`|<span data-ttu-id="2f573-109">在 prolog 代码中停止。</span><span class="sxs-lookup"><span data-stu-id="2f573-109">Stop in prolog code.</span></span>|  
|`STOP_EPILOG`|<span data-ttu-id="2f573-110">在 epilog 代码中停止。</span><span class="sxs-lookup"><span data-stu-id="2f573-110">Stop in epilog code.</span></span>|  
|`STOP_NO_MAPPING_INFO`|<span data-ttu-id="2f573-111">在没有映射信息的代码中停止。</span><span class="sxs-lookup"><span data-stu-id="2f573-111">Stop in code that has no mapping information.</span></span>|  
|`STOP_OTHER_UNMAPPED`|<span data-ttu-id="2f573-112">在未映射的代码中停止，不适合 prolog、epilog、无映射-信息或非托管类别。</span><span class="sxs-lookup"><span data-stu-id="2f573-112">Stop in unmapped code that does not fit into the prolog, epilog, no-mapping-information, or unmanaged category.</span></span>|  
|`STOP_UNMANAGED`|<span data-ttu-id="2f573-113">在非托管代码中停止。</span><span class="sxs-lookup"><span data-stu-id="2f573-113">Stop in unmanaged code.</span></span> <span data-ttu-id="2f573-114">此值仅适用于互操作调试。</span><span class="sxs-lookup"><span data-stu-id="2f573-114">This value is valid only with interop debugging.</span></span>|  
|`STOP_ALL`|<span data-ttu-id="2f573-115">在所有类型的未映射代码中停止。</span><span class="sxs-lookup"><span data-stu-id="2f573-115">Stop in all types of unmapped code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2f573-116">注解</span><span class="sxs-lookup"><span data-stu-id="2f573-116">Remarks</span></span>  

 <span data-ttu-id="2f573-117">使用 [ICorDebugStepper：： SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) 方法设置标志，这些标志指定分档器将停止的未映射代码。</span><span class="sxs-lookup"><span data-stu-id="2f573-117">Use the [ICorDebugStepper::SetUnmappedStopMask](icordebugstepper-setunmappedstopmask-method.md) method to set the flags that specify the unmapped code in which the stepper will stop.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f573-118">要求</span><span class="sxs-lookup"><span data-stu-id="2f573-118">Requirements</span></span>  

 <span data-ttu-id="2f573-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2f573-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f573-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2f573-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2f573-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2f573-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2f573-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2f573-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f573-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f573-123">See also</span></span>

- [<span data-ttu-id="2f573-124">调试枚举</span><span class="sxs-lookup"><span data-stu-id="2f573-124">Debugging Enumerations</span></span>](debugging-enumerations.md)
