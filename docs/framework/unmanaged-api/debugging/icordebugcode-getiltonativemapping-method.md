---
title: ICorDebugCode::GetILToNativeMapping 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetILToNativeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetILToNativeMapping
helpviewer_keywords:
- GetILToNativeMapping method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetILToNativeMapping method [.NET Framework debugging]
ms.assetid: a8ecd8c8-9627-4356-9c6f-bd05e24637c0
topic_type:
- apiref
ms.openlocfilehash: 0adb9e58ca2c6b5b430a0413fa11ba59d79a0539
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688102"
---
# <a name="icordebugcodegetiltonativemapping-method"></a><span data-ttu-id="d7c6b-102">ICorDebugCode::GetILToNativeMapping 方法</span><span class="sxs-lookup"><span data-stu-id="d7c6b-102">ICorDebugCode::GetILToNativeMapping Method</span></span>

<span data-ttu-id="d7c6b-103">获取 "COR_DEBUG_IL_TO_NATIVE_MAP" 实例的数组，这些实例表示从 Microsoft 中间语言 (MSIL 到本机偏移量) 偏移量的映射。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-103">Gets an array of "COR_DEBUG_IL_TO_NATIVE_MAP" instances that represent mappings from Microsoft intermediate language (MSIL) offsets to native offsets.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7c6b-104">语法</span><span class="sxs-lookup"><span data-stu-id="d7c6b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetILToNativeMapping (  
    [in]  ULONG32    cMap,  
    [out] ULONG32    *pcMap,  
    [out, size_is(cMap), length_is(*pcMap)]  
        COR_DEBUG_IL_TO_NATIVE_MAP map[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d7c6b-105">参数</span><span class="sxs-lookup"><span data-stu-id="d7c6b-105">Parameters</span></span>  

 `cMap`  
 <span data-ttu-id="d7c6b-106">[in] `map` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-106">[in] The size of the `map` array.</span></span>  
  
 `pcMap`  
 <span data-ttu-id="d7c6b-107">弄一个指针，它指向数组中返回的元素的实际数目 `map` 。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-107">[out] A pointer to the actual number of elements returned in the `map` array.</span></span>  
  
 `map`  
 <span data-ttu-id="d7c6b-108">弄结构的数组 `COR_DEBUG_IL_TO_NATIVE_MAP` ，其中每个结构都表示从 MSIL 偏移量到本机偏移量的映射。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-108">[out] An array of `COR_DEBUG_IL_TO_NATIVE_MAP` structures, each of which represents a mapping from an MSIL offset to a native offset.</span></span>  
  
 <span data-ttu-id="d7c6b-109">返回的元素数组没有排序。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-109">There is no ordering to the array of elements returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d7c6b-110">注解</span><span class="sxs-lookup"><span data-stu-id="d7c6b-110">Remarks</span></span>  

 <span data-ttu-id="d7c6b-111">`GetILToNativeMapping`仅当此 "ICorDebugCode" 实例表示实时 (JIT) 从 MSIL 代码编译的本机代码时，此方法才会返回有意义的结果。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-111">The `GetILToNativeMapping` method returns meaningful results only if this "ICorDebugCode" instance represents native code that was just-in-time (JIT) compiled from MSIL code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7c6b-112">要求</span><span class="sxs-lookup"><span data-stu-id="d7c6b-112">Requirements</span></span>  

 <span data-ttu-id="d7c6b-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d7c6b-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7c6b-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d7c6b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d7c6b-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d7c6b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d7c6b-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7c6b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7c6b-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7c6b-117">See also</span></span>

- [<span data-ttu-id="d7c6b-118">ICorDebugCode 接口</span><span class="sxs-lookup"><span data-stu-id="d7c6b-118">ICorDebugCode Interface</span></span>](icordebugcode-interface1.md)
