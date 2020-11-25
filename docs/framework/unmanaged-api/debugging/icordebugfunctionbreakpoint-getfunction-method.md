---
title: ICorDebugFunctionBreakpoint::GetFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint::GetFunction
helpviewer_keywords:
- ICorDebugFunctionBreakpoint::GetFunction method [.NET Framework debugging]
- GetFunction method, ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: 2a62dae5-dd8a-4696-b817-0e1e586c24a0
topic_type:
- apiref
ms.openlocfilehash: 4ef5728e4b13d6d3d73aef06f9f7f50ab22609ad
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726257"
---
# <a name="icordebugfunctionbreakpointgetfunction-method"></a><span data-ttu-id="00078-102">ICorDebugFunctionBreakpoint::GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="00078-102">ICorDebugFunctionBreakpoint::GetFunction Method</span></span>

<span data-ttu-id="00078-103">获取一个指向 ICorDebugFunction 的接口指针，该指针引用在其中设置断点的函数。</span><span class="sxs-lookup"><span data-stu-id="00078-103">Gets an interface pointer to an ICorDebugFunction that references the function in which the breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00078-104">语法</span><span class="sxs-lookup"><span data-stu-id="00078-104">Syntax</span></span>  
  
```cpp  
HRESULT GetFunction (  
    [out] ICorDebugFunction  **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00078-105">参数</span><span class="sxs-lookup"><span data-stu-id="00078-105">Parameters</span></span>  

 `ppFunction`  
 <span data-ttu-id="00078-106">弄一个指针，指向设置断点的函数的地址。</span><span class="sxs-lookup"><span data-stu-id="00078-106">[out] A pointer to the address of the function in which the breakpoint is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00078-107">要求</span><span class="sxs-lookup"><span data-stu-id="00078-107">Requirements</span></span>  

 <span data-ttu-id="00078-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="00078-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00078-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="00078-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="00078-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="00078-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="00078-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00078-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
