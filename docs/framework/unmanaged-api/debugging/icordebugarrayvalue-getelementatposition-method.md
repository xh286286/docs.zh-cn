---
title: ICorDebugArrayValue::GetElementAtPosition 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElementAtPosition
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElementAtPosition
helpviewer_keywords:
- GetElementAtPosition method [.NET Framework debugging]
- ICorDebugArrayValue::GetElementAtPosition method [.NET Framework debugging]
ms.assetid: 6fd5eaa4-1997-4910-82f5-3887480db764
topic_type:
- apiref
ms.openlocfilehash: a6e5ecee9a89da98a73dfb20935c5ec594d5958f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732926"
---
# <a name="icordebugarrayvaluegetelementatposition-method"></a><span data-ttu-id="28b78-102">ICorDebugArrayValue::GetElementAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="28b78-102">ICorDebugArrayValue::GetElementAtPosition Method</span></span>

<span data-ttu-id="28b78-103">获取位于给定位置的元素，并将该数组视为从零开始的一维数组。</span><span class="sxs-lookup"><span data-stu-id="28b78-103">Gets the element at the given position, treating the array as a zero-based, single-dimensional array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28b78-104">语法</span><span class="sxs-lookup"><span data-stu-id="28b78-104">Syntax</span></span>  
  
```cpp  
HRESULT GetElementAtPosition (  
    [in]  ULONG32          nPosition,  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="28b78-105">参数</span><span class="sxs-lookup"><span data-stu-id="28b78-105">Parameters</span></span>  

 `nPosition`  
 <span data-ttu-id="28b78-106">中要检索的元素的位置。</span><span class="sxs-lookup"><span data-stu-id="28b78-106">[in] The position of the element to be retrieved.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="28b78-107">弄指向表示元素值的 ICorDebugValue 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="28b78-107">[out] A pointer to the address of an ICorDebugValue object that represents the value of the element.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="28b78-108">注解</span><span class="sxs-lookup"><span data-stu-id="28b78-108">Remarks</span></span>  

 <span data-ttu-id="28b78-109">多维数组的布局遵循数组布局的 c + + 样式。</span><span class="sxs-lookup"><span data-stu-id="28b78-109">The layout of a multi-dimension array follows the C++ style of array layout.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28b78-110">要求</span><span class="sxs-lookup"><span data-stu-id="28b78-110">Requirements</span></span>  

 <span data-ttu-id="28b78-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28b78-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28b78-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="28b78-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="28b78-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="28b78-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="28b78-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28b78-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
