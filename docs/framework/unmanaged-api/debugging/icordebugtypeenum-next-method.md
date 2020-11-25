---
title: ICorDebugTypeEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugTypeEnum::Next
helpviewer_keywords:
- ICorDebugTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugTypeEnum interface [.NET Framework debugging]
ms.assetid: d0fdeba3-c195-4ece-8caf-79b1f40025d2
topic_type:
- apiref
ms.openlocfilehash: 78ea76033b0b83c84446e16fb330bd3ba34c6e21
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725698"
---
# <a name="icordebugtypeenumnext-method"></a><span data-ttu-id="dc00c-102">ICorDebugTypeEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="dc00c-102">ICorDebugTypeEnum::Next Method</span></span>

<span data-ttu-id="dc00c-103">从当前位置开始，获取由枚举指定的 "ICorDebugType" 实例的数目 `celt` 。</span><span class="sxs-lookup"><span data-stu-id="dc00c-103">Gets the number of "ICorDebugType" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc00c-104">语法</span><span class="sxs-lookup"><span data-stu-id="dc00c-104">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugType *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc00c-105">参数</span><span class="sxs-lookup"><span data-stu-id="dc00c-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="dc00c-106">中 `ICorDebugType` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="dc00c-106">[in] The number of `ICorDebugType` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="dc00c-107">弄指针的数组，其中每个都指向一个 `ICorDebugType` 对象。</span><span class="sxs-lookup"><span data-stu-id="dc00c-107">[out] An array of pointers, each of which points to an `ICorDebugType` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="dc00c-108">弄一个指针，指向 `ICorDebugType` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="dc00c-108">[out] Pointer to the number of `ICorDebugType` instances actually returned.</span></span> <span data-ttu-id="dc00c-109">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="dc00c-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc00c-110">要求</span><span class="sxs-lookup"><span data-stu-id="dc00c-110">Requirements</span></span>  

 <span data-ttu-id="dc00c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dc00c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc00c-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dc00c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dc00c-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dc00c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dc00c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc00c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc00c-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc00c-115">See also</span></span>
