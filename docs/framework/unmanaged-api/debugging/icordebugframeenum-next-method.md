---
title: ICorDebugFrameEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrameEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrameEnum::Next
helpviewer_keywords:
- ICorDebugFrameEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugFrameEnum interface [.NET Framework debugging]
ms.assetid: 0bc96acb-6179-4328-a447-cda562ce9e98
topic_type:
- apiref
ms.openlocfilehash: 76b96dfd9d22c7e770671dcc01cb421430df729f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728181"
---
# <a name="icordebugframeenumnext-method"></a><span data-ttu-id="e93d0-102">ICorDebugFrameEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="e93d0-102">ICorDebugFrameEnum::Next Method</span></span>

<span data-ttu-id="e93d0-103">从当前位置开始，获取指定数量的 ICorDebugFrame 实例。</span><span class="sxs-lookup"><span data-stu-id="e93d0-103">Gets the specified number of ICorDebugFrame instances, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e93d0-104">语法</span><span class="sxs-lookup"><span data-stu-id="e93d0-104">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugFrame *frames[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e93d0-105">参数</span><span class="sxs-lookup"><span data-stu-id="e93d0-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="e93d0-106">中 `ICorDebugFrame` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="e93d0-106">[in] The number of `ICorDebugFrame` instances to be retrieved.</span></span>  
  
 `frames`  
 <span data-ttu-id="e93d0-107">弄指针的数组，其中每个都指向一个 `ICorDebugFrame` 对象。</span><span class="sxs-lookup"><span data-stu-id="e93d0-107">[out] An array of pointers, each of which points to an `ICorDebugFrame` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="e93d0-108">弄一个指针，指向 `ICorDebugFrame` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="e93d0-108">[out] A pointer to the number of `ICorDebugFrame` instances actually returned.</span></span> <span data-ttu-id="e93d0-109">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="e93d0-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e93d0-110">要求</span><span class="sxs-lookup"><span data-stu-id="e93d0-110">Requirements</span></span>  

 <span data-ttu-id="e93d0-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e93d0-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e93d0-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e93d0-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e93d0-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e93d0-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e93d0-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e93d0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
