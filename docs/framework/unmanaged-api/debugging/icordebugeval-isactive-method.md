---
title: ICorDebugEval::IsActive 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::IsActive
helpviewer_keywords:
- IsActive method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::IsActive method [.NET Framework debugging]
ms.assetid: bf2bba24-d278-43bd-b1c5-35680e748d3e
topic_type:
- apiref
ms.openlocfilehash: 5ac221b0b5837175b8073ab29f94c1f28078d3e4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729767"
---
# <a name="icordebugevalisactive-method"></a><span data-ttu-id="97bc0-102">ICorDebugEval::IsActive 方法</span><span class="sxs-lookup"><span data-stu-id="97bc0-102">ICorDebugEval::IsActive Method</span></span>

<span data-ttu-id="97bc0-103">获取一个值，该值指示此 ICorDebugEval 对象当前是否正在执行。</span><span class="sxs-lookup"><span data-stu-id="97bc0-103">Gets a value that indicates whether this ICorDebugEval object is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97bc0-104">语法</span><span class="sxs-lookup"><span data-stu-id="97bc0-104">Syntax</span></span>  
  
```cpp  
HRESULT IsActive (  
    [out] BOOL              *pbActive  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="97bc0-105">参数</span><span class="sxs-lookup"><span data-stu-id="97bc0-105">Parameters</span></span>  

 `pbActive`  
 <span data-ttu-id="97bc0-106">弄指向一个值的指针，该值指示此计算是否处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="97bc0-106">[out] Pointer to a value that indicates whether this evaluation is active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97bc0-107">要求</span><span class="sxs-lookup"><span data-stu-id="97bc0-107">Requirements</span></span>  

 <span data-ttu-id="97bc0-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="97bc0-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97bc0-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="97bc0-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="97bc0-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="97bc0-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="97bc0-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97bc0-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
