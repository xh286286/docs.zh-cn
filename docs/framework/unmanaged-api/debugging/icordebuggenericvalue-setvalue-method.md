---
title: ICorDebugGenericValue::SetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue.SetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue::SetValue
helpviewer_keywords:
- ICorDebugGenericValue::SetValue method [.NET Framework debugging]
- SetValue method, ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: ed4c6458-0435-44fc-8e78-8ba00be362f2
topic_type:
- apiref
ms.openlocfilehash: 493793c45e7d13511e4c36fe76e472a856b50d72
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705730"
---
# <a name="icordebuggenericvaluesetvalue-method"></a><span data-ttu-id="0c2ce-102">ICorDebugGenericValue::SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="0c2ce-102">ICorDebugGenericValue::SetValue Method</span></span>

<span data-ttu-id="0c2ce-103">从指定的缓冲区复制新值。</span><span class="sxs-lookup"><span data-stu-id="0c2ce-103">Copies a new value from the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c2ce-104">语法</span><span class="sxs-lookup"><span data-stu-id="0c2ce-104">Syntax</span></span>  
  
```cpp  
HRESULT SetValue (  
    [in] void      *pFrom  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c2ce-105">参数</span><span class="sxs-lookup"><span data-stu-id="0c2ce-105">Parameters</span></span>  

 `pFrom`  
 <span data-ttu-id="0c2ce-106">中指向要从中复制值的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="0c2ce-106">[in] A pointer to the buffer from which to copy the value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0c2ce-107">注解</span><span class="sxs-lookup"><span data-stu-id="0c2ce-107">Remarks</span></span>  

 <span data-ttu-id="0c2ce-108">对于引用类型，该值是引用，而不是内容。</span><span class="sxs-lookup"><span data-stu-id="0c2ce-108">For reference types, the value is the reference, not the content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c2ce-109">要求</span><span class="sxs-lookup"><span data-stu-id="0c2ce-109">Requirements</span></span>  

 <span data-ttu-id="0c2ce-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0c2ce-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c2ce-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0c2ce-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0c2ce-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0c2ce-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0c2ce-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c2ce-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
