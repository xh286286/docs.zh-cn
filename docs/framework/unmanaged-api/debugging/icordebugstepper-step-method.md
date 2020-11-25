---
title: ICorDebugStepper::Step 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.Step
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::Step
helpviewer_keywords:
- Step method, ICorDebugStepper interface [.NET Framework debugging]
- ICorDebugStepper::Step method [.NET Framework debugging]
ms.assetid: 38c1940b-ada1-40ba-8295-4c0833744e1e
topic_type:
- apiref
ms.openlocfilehash: 234705e4495a1a582f3801ad1e645f923cd6f4b2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727687"
---
# <a name="icordebugstepperstep-method"></a><span data-ttu-id="30554-102">ICorDebugStepper::Step 方法</span><span class="sxs-lookup"><span data-stu-id="30554-102">ICorDebugStepper::Step Method</span></span>

<span data-ttu-id="30554-103">使此 ICorDebugStepper 单步执行其包含线程，并根据需要继续单步执行线程中调用的函数。</span><span class="sxs-lookup"><span data-stu-id="30554-103">Causes this ICorDebugStepper to single-step through its containing thread, and optionally, to continue single-stepping through functions that are called within the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30554-104">语法</span><span class="sxs-lookup"><span data-stu-id="30554-104">Syntax</span></span>  
  
```cpp  
HRESULT Step (  
    [in] BOOL   bStepIn  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30554-105">参数</span><span class="sxs-lookup"><span data-stu-id="30554-105">Parameters</span></span>  

 `bStepIn`  
 <span data-ttu-id="30554-106">中设置为 `true` 可单步执行在线程中调用的函数。</span><span class="sxs-lookup"><span data-stu-id="30554-106">[in] Set to `true` to step into a function that is called within the thread.</span></span> <span data-ttu-id="30554-107">设置为 `false` 以逐过程执行函数。</span><span class="sxs-lookup"><span data-stu-id="30554-107">Set to `false` to step over the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="30554-108">注解</span><span class="sxs-lookup"><span data-stu-id="30554-108">Remarks</span></span>  

 <span data-ttu-id="30554-109">当公共语言运行时执行此分档器帧中的下一个托管指令时，此步骤即告完成。</span><span class="sxs-lookup"><span data-stu-id="30554-109">The step completes when the common language runtime performs the next managed instruction in this stepper's frame.</span></span> <span data-ttu-id="30554-110">如果 `Step` 在不在托管代码中的分档器上调用，则在线程执行下一个托管代码指令时，步骤将完成。</span><span class="sxs-lookup"><span data-stu-id="30554-110">If `Step` is called on a stepper, which is not in managed code, the step will complete when the next managed code instruction is executed by the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30554-111">要求</span><span class="sxs-lookup"><span data-stu-id="30554-111">Requirements</span></span>  

 <span data-ttu-id="30554-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="30554-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30554-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="30554-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="30554-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="30554-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="30554-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30554-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
