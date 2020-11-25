---
title: ICorDebugChain::GetStackRange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetStackRange
helpviewer_keywords:
- ICorDebugChain::GetStackRange method [.NET Framework debugging]
- GetStackRange method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 554284e7-3f6c-4d40-8da5-1c9317fbd484
topic_type:
- apiref
ms.openlocfilehash: 841e3ca608d20a4b8618508e69195de0b1da1341
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724385"
---
# <a name="icordebugchaingetstackrange-method"></a><span data-ttu-id="4a525-102">ICorDebugChain::GetStackRange 方法</span><span class="sxs-lookup"><span data-stu-id="4a525-102">ICorDebugChain::GetStackRange Method</span></span>

<span data-ttu-id="4a525-103">获取此链的堆栈段的地址范围。</span><span class="sxs-lookup"><span data-stu-id="4a525-103">Gets the address range of the stack segment for this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a525-104">语法</span><span class="sxs-lookup"><span data-stu-id="4a525-104">Syntax</span></span>  
  
```cpp  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4a525-105">参数</span><span class="sxs-lookup"><span data-stu-id="4a525-105">Parameters</span></span>  

 `pStart`  
 <span data-ttu-id="4a525-106">弄一个指针，指向作为 `CORDB_ADDRESS` 堆栈段起始地址的值。</span><span class="sxs-lookup"><span data-stu-id="4a525-106">[out] A pointer to a `CORDB_ADDRESS` value that is the starting address of the stack segment.</span></span>  
  
 `pEnd`  
 <span data-ttu-id="4a525-107">弄一个指针，指向作为 `CORDB_ADDRESS` 堆栈段结束地址的值。</span><span class="sxs-lookup"><span data-stu-id="4a525-107">[out] A pointer to a `CORDB_ADDRESS` value that is the ending address of the stack segment.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4a525-108">注解</span><span class="sxs-lookup"><span data-stu-id="4a525-108">Remarks</span></span>  

 <span data-ttu-id="4a525-109">数值范围仅用于比较堆栈帧位置。</span><span class="sxs-lookup"><span data-stu-id="4a525-109">The numeric range is meaningful only for comparison of stack frame locations.</span></span> <span data-ttu-id="4a525-110">您无法对堆栈上实际存储的内容作出任何假设。</span><span class="sxs-lookup"><span data-stu-id="4a525-110">You cannot make any assumptions about what is actually stored on the stack.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a525-111">要求</span><span class="sxs-lookup"><span data-stu-id="4a525-111">Requirements</span></span>  

 <span data-ttu-id="4a525-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a525-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a525-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4a525-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4a525-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a525-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a525-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a525-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
