---
title: ICorDebugArrayValue::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetCount
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetCount
helpviewer_keywords:
- ICorDebugArrayValue::GetCount method [.NET Framework debugging]
- GetCount method, ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: 44cd98cf-2127-4d46-8c6a-da4e857bb6b0
topic_type:
- apiref
ms.openlocfilehash: cd45c6d515648819a83d4e9944eb20d5cd20dd86
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95698216"
---
# <a name="icordebugarrayvaluegetcount-method"></a><span data-ttu-id="0298f-102">ICorDebugArrayValue::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="0298f-102">ICorDebugArrayValue::GetCount Method</span></span>

<span data-ttu-id="0298f-103">获取数组中的元素总数。</span><span class="sxs-lookup"><span data-stu-id="0298f-103">Gets the total number of elements in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0298f-104">语法</span><span class="sxs-lookup"><span data-stu-id="0298f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCount (  
    [out] ULONG32 *pnCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0298f-105">参数</span><span class="sxs-lookup"><span data-stu-id="0298f-105">Parameters</span></span>  

 `pnCount`  
 <span data-ttu-id="0298f-106">弄指向数组中元素总数的指针。</span><span class="sxs-lookup"><span data-stu-id="0298f-106">[out] A pointer to the total number of elements in the array.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0298f-107">要求</span><span class="sxs-lookup"><span data-stu-id="0298f-107">Requirements</span></span>  

 <span data-ttu-id="0298f-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0298f-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0298f-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0298f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0298f-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0298f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0298f-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0298f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
