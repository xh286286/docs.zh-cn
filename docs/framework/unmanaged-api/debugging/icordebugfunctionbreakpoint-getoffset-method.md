---
title: ICorDebugFunctionBreakpoint::GetOffset 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint.GetOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint::GetOffset
helpviewer_keywords:
- ICorDebugFunctionBreakpoint::GetOffset method [.NET Framework debugging]
- GetOffset method, ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: e619eae4-3ac3-4c37-bba4-55e59989b9cb
topic_type:
- apiref
ms.openlocfilehash: 8b9e483e24068656ddda0a3ecfee5934a2df962d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95695889"
---
# <a name="icordebugfunctionbreakpointgetoffset-method"></a><span data-ttu-id="b671c-102">ICorDebugFunctionBreakpoint::GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="b671c-102">ICorDebugFunctionBreakpoint::GetOffset Method</span></span>

<span data-ttu-id="b671c-103">获取函数内断点的偏移量。</span><span class="sxs-lookup"><span data-stu-id="b671c-103">Gets the offset of the breakpoint within the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b671c-104">语法</span><span class="sxs-lookup"><span data-stu-id="b671c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetOffset (  
    [out] ULONG32  *pnOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b671c-105">参数</span><span class="sxs-lookup"><span data-stu-id="b671c-105">Parameters</span></span>  

 `pnOffset`  
 <span data-ttu-id="b671c-106">弄指向断点偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="b671c-106">[out] A pointer to the offset of the breakpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b671c-107">要求</span><span class="sxs-lookup"><span data-stu-id="b671c-107">Requirements</span></span>  

 <span data-ttu-id="b671c-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b671c-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b671c-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b671c-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b671c-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b671c-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b671c-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b671c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
