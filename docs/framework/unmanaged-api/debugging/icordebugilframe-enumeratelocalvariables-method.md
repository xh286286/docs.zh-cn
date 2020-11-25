---
title: ICorDebugILFrame::EnumerateLocalVariables 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.EnumerateLocalVariables
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::EnumerateLocalVariables
helpviewer_keywords:
- EnumerateLocalVariables method [.NET Framework debugging]
- ICorDebugILFrame::EnumerateLocalVariables method [.NET Framework debugging]
ms.assetid: 1a67fa1b-2419-4cd0-aad4-6f46a0719b4b
topic_type:
- apiref
ms.openlocfilehash: 968ceec53aade3d04c500c8247d397ffb71382c1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95703182"
---
# <a name="icordebugilframeenumeratelocalvariables-method"></a><span data-ttu-id="d9ad7-102">ICorDebugILFrame::EnumerateLocalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="d9ad7-102">ICorDebugILFrame::EnumerateLocalVariables Method</span></span>

<span data-ttu-id="d9ad7-103">获取此帧中局部变量的枚举数。</span><span class="sxs-lookup"><span data-stu-id="d9ad7-103">Gets an enumerator for the local variables in this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9ad7-104">语法</span><span class="sxs-lookup"><span data-stu-id="d9ad7-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateLocalVariables(
    [out] ICorDebugValueEnum    **ppValueEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9ad7-105">参数</span><span class="sxs-lookup"><span data-stu-id="d9ad7-105">Parameters</span></span>  

 `ppValueEnum`  
 <span data-ttu-id="d9ad7-106">[out] 一个指向 ICorDebugValueEnum 对象的地址的指针，该对象是此帧中局部变量的枚举器。</span><span class="sxs-lookup"><span data-stu-id="d9ad7-106">[out] A pointer to the address of an ICorDebugValueEnum object that is the enumerator for the local variables in this frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9ad7-107">注解</span><span class="sxs-lookup"><span data-stu-id="d9ad7-107">Remarks</span></span>  

 <span data-ttu-id="d9ad7-108">`EnumerateLocalVariables` 获取一个枚举器，该枚举数可以列出此 ICorDebugILFrame 对象所表示的调用帧中可用的局部变量。</span><span class="sxs-lookup"><span data-stu-id="d9ad7-108">`EnumerateLocalVariables` gets an enumerator that can list the local variables available in the call frame that is represented by this ICorDebugILFrame object.</span></span> <span data-ttu-id="d9ad7-109">此列表可能不包括正在运行的函数中的所有局部变量，因为其中一些局部变量可能不处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="d9ad7-109">The list may not include all of the local variables in the running function, because some of them may not be active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9ad7-110">要求</span><span class="sxs-lookup"><span data-stu-id="d9ad7-110">Requirements</span></span>  

 <span data-ttu-id="d9ad7-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9ad7-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9ad7-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d9ad7-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d9ad7-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d9ad7-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d9ad7-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9ad7-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
