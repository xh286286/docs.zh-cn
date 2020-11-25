---
title: ICorDebugArrayValue::GetDimensions 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetDimensions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetDimensions
helpviewer_keywords:
- ICorDebugArrayValue::GetDimensions method [.NET Framework debugging]
- GetDimensions method [.NET Framework debugging]
ms.assetid: 6c116592-134b-4ef2-a319-680e92d013aa
topic_type:
- apiref
ms.openlocfilehash: bf498a14af3dccc7278155ecfc74132c2b519ed3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95698190"
---
# <a name="icordebugarrayvaluegetdimensions-method"></a><span data-ttu-id="ec10f-102">ICorDebugArrayValue::GetDimensions 方法</span><span class="sxs-lookup"><span data-stu-id="ec10f-102">ICorDebugArrayValue::GetDimensions Method</span></span>

<span data-ttu-id="ec10f-103">获取此数组的每个维度中的元素数。</span><span class="sxs-lookup"><span data-stu-id="ec10f-103">Gets the number of elements in each dimension of this array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec10f-104">语法</span><span class="sxs-lookup"><span data-stu-id="ec10f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDimensions (  
    [in] ULONG32         cdim,  
    [out, size_is(cdim), length_is(cdim)]
        ULONG32          dims[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec10f-105">参数</span><span class="sxs-lookup"><span data-stu-id="ec10f-105">Parameters</span></span>  

 `cdim`  
 <span data-ttu-id="ec10f-106">中此 ICorDebugArrayValue 对象的维度数。</span><span class="sxs-lookup"><span data-stu-id="ec10f-106">[in] The number of dimensions of this ICorDebugArrayValue object.</span></span>  
  
 <span data-ttu-id="ec10f-107">此值也是数组的大小， `dims` 因为其大小等于对象的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="ec10f-107">This value is also the size of the `dims` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `dims`  
 <span data-ttu-id="ec10f-108">弄一个整数数组，其中每个整数指定了此对象的维度中的元素数目 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="ec10f-108">[out] An array of integers, each of which specifies the number of elements in a dimension in this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec10f-109">要求</span><span class="sxs-lookup"><span data-stu-id="ec10f-109">Requirements</span></span>  

 <span data-ttu-id="ec10f-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ec10f-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec10f-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ec10f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ec10f-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ec10f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ec10f-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec10f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
