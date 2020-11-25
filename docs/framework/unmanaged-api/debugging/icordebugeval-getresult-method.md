---
title: ICorDebugEval::GetResult 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetResult
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetResult
helpviewer_keywords:
- ICorDebugEval::GetResult method [.NET Framework debugging]
- GetResult method [.NET Framework debugging]
ms.assetid: 50dbb9af-58a1-41f4-b56d-3da20011884f
topic_type:
- apiref
ms.openlocfilehash: 86c017f581c7b980b8b0cb8bd7bdc1b0aa439afe
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705813"
---
# <a name="icordebugevalgetresult-method"></a><span data-ttu-id="a52e9-102">ICorDebugEval::GetResult 方法</span><span class="sxs-lookup"><span data-stu-id="a52e9-102">ICorDebugEval::GetResult Method</span></span>

<span data-ttu-id="a52e9-103">获取此计算的结果。</span><span class="sxs-lookup"><span data-stu-id="a52e9-103">Gets the results of this evaluation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a52e9-104">语法</span><span class="sxs-lookup"><span data-stu-id="a52e9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetResult (  
    [out] ICorDebugValue    **ppResult  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a52e9-105">参数</span><span class="sxs-lookup"><span data-stu-id="a52e9-105">Parameters</span></span>  

 `ppResult`  
 <span data-ttu-id="a52e9-106">弄一个指针，指向表示此计算结果的 ICorDebugValue 对象的地址（如果计算正常完成）。</span><span class="sxs-lookup"><span data-stu-id="a52e9-106">[out] Pointer to the address of an ICorDebugValue object that represents the results of this evaluation, if the evaluation completes normally.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a52e9-107">注解</span><span class="sxs-lookup"><span data-stu-id="a52e9-107">Remarks</span></span>  

 <span data-ttu-id="a52e9-108">此 `GetResult` 方法仅在计算完成后有效。</span><span class="sxs-lookup"><span data-stu-id="a52e9-108">The `GetResult` method is valid only after the evaluation is completed.</span></span>  
  
 <span data-ttu-id="a52e9-109">如果计算正常完成，则 `ppResult` 指定结果。</span><span class="sxs-lookup"><span data-stu-id="a52e9-109">If the evaluation completes normally, `ppResult` specifies the results.</span></span> <span data-ttu-id="a52e9-110">如果终止时出现异常，则结果为引发的异常。</span><span class="sxs-lookup"><span data-stu-id="a52e9-110">If it terminates with an exception, the result is the exception thrown.</span></span> <span data-ttu-id="a52e9-111">如果计算为新的对象，则结果是对新的对象的引用。</span><span class="sxs-lookup"><span data-stu-id="a52e9-111">If the evaluation was for a new object, the result is the reference to the new object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a52e9-112">要求</span><span class="sxs-lookup"><span data-stu-id="a52e9-112">Requirements</span></span>  

 <span data-ttu-id="a52e9-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a52e9-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a52e9-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a52e9-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a52e9-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a52e9-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a52e9-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a52e9-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
