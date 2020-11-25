---
title: ICorDebugFunction::CreateBreakpoint 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.CreateBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::CreateBreakpoint
helpviewer_keywords:
- ICorDebugFunction::CreateBreakpoint method [.NET Framework debugging]
- CreateBreakpoint method, ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: ffd0f708-0d21-4fae-a395-63b6c45828fa
topic_type:
- apiref
ms.openlocfilehash: 2d1846acae51f416471404389dd1dbcfb2383760
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728168"
---
# <a name="icordebugfunctioncreatebreakpoint-method"></a><span data-ttu-id="a2121-102">ICorDebugFunction::CreateBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="a2121-102">ICorDebugFunction::CreateBreakpoint Method</span></span>

<span data-ttu-id="a2121-103">在此函数的开头创建一个断点。</span><span class="sxs-lookup"><span data-stu-id="a2121-103">Creates a breakpoint at the beginning of this function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2121-104">语法</span><span class="sxs-lookup"><span data-stu-id="a2121-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateBreakpoint (  
    [out] ICorDebugFunctionBreakpoint **ppBreakpoint  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a2121-105">参数</span><span class="sxs-lookup"><span data-stu-id="a2121-105">Parameters</span></span>  

 `ppBreakpoint`  
 <span data-ttu-id="a2121-106">弄指向 ICorDebugFunctionBreakpoint 对象的地址的指针，该对象表示函数的新断点。</span><span class="sxs-lookup"><span data-stu-id="a2121-106">[out] A pointer to the address of an ICorDebugFunctionBreakpoint object that represents the new breakpoint for the function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2121-107">要求</span><span class="sxs-lookup"><span data-stu-id="a2121-107">Requirements</span></span>  

 <span data-ttu-id="a2121-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a2121-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2121-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a2121-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a2121-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a2121-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a2121-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2121-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
