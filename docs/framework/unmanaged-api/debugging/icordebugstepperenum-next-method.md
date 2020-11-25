---
title: ICorDebugStepperEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type:
- apiref
ms.openlocfilehash: b8156b858bde550bb66a8f4ac254f850058ea1a2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697189"
---
# <a name="icordebugstepperenumnext-method"></a><span data-ttu-id="6df61-102">ICorDebugStepperEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="6df61-102">ICorDebugStepperEnum::Next Method</span></span>

<span data-ttu-id="6df61-103">从当前位置开始，从枚举中获取指定数量的 ICorDebugStepper 实例。</span><span class="sxs-lookup"><span data-stu-id="6df61-103">Gets the specified number of ICorDebugStepper instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6df61-104">语法</span><span class="sxs-lookup"><span data-stu-id="6df61-104">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6df61-105">参数</span><span class="sxs-lookup"><span data-stu-id="6df61-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="6df61-106">中 `ICorDebugStepper` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="6df61-106">[in] The number of `ICorDebugStepper` instances to be retrieved.</span></span>  
  
 `steppers`  
 <span data-ttu-id="6df61-107">弄指针的数组，其中每个都指向一个 `ICorDebugStepper` 对象。</span><span class="sxs-lookup"><span data-stu-id="6df61-107">[out] An array of pointers, each of which points to an `ICorDebugStepper` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="6df61-108">弄一个指针，指向 `ICorDebugStepper` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="6df61-108">[out] Pointer to the number of `ICorDebugStepper` instances actually returned.</span></span> <span data-ttu-id="6df61-109">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="6df61-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6df61-110">要求</span><span class="sxs-lookup"><span data-stu-id="6df61-110">Requirements</span></span>  

 <span data-ttu-id="6df61-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6df61-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6df61-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6df61-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6df61-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6df61-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6df61-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6df61-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
