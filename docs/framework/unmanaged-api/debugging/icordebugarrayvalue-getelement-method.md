---
title: ICorDebugArrayValue::GetElement 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElement
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElement
helpviewer_keywords:
- GetElement method [.NET Framework debugging]
- ICorDebugArrayValue::GetElement method [.NET Framework debugging]
ms.assetid: 7ac3cba5-c282-402e-b7ef-b46634f5176b
topic_type:
- apiref
ms.openlocfilehash: 0b6b6f46c7fff8f1d4c2ad555c93423f9ca8ac09
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95698138"
---
# <a name="icordebugarrayvaluegetelement-method"></a><span data-ttu-id="80f75-102">ICorDebugArrayValue::GetElement 方法</span><span class="sxs-lookup"><span data-stu-id="80f75-102">ICorDebugArrayValue::GetElement Method</span></span>

<span data-ttu-id="80f75-103">获取给定数组元素的值。</span><span class="sxs-lookup"><span data-stu-id="80f75-103">Gets the value of the given array element.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80f75-104">语法</span><span class="sxs-lookup"><span data-stu-id="80f75-104">Syntax</span></span>  
  
```cpp  
HRESULT GetElement (  
    [in]  ULONG32          cdim,  
    [in, size_is(cdim), length_is(cdim)]
         ULONG32           indices[],  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="80f75-105">参数</span><span class="sxs-lookup"><span data-stu-id="80f75-105">Parameters</span></span>  

 `cdim`  
 <span data-ttu-id="80f75-106">中此对象的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="80f75-106">[in] The number of dimensions of this `ICorDebugArrayValue` object.</span></span>  
  
 <span data-ttu-id="80f75-107">此值也是数组的大小， `indices` 因为其大小等于对象的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="80f75-107">This value is also the size of the `indices` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `indices`  
 <span data-ttu-id="80f75-108">中索引值的数组，其中每个值指定对象的维度内的位置 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="80f75-108">[in] An array of index values, each of which specifies a position within a dimension of the `ICorDebugArrayValue` object.</span></span>  
  
 <span data-ttu-id="80f75-109">此值不得为 Null。</span><span class="sxs-lookup"><span data-stu-id="80f75-109">This value must not be null.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="80f75-110">弄指向 ICorDebugValue 对象的地址的指针，该对象表示指定元素的值。</span><span class="sxs-lookup"><span data-stu-id="80f75-110">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified element.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="80f75-111">要求</span><span class="sxs-lookup"><span data-stu-id="80f75-111">Requirements</span></span>  

 <span data-ttu-id="80f75-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="80f75-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80f75-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="80f75-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="80f75-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="80f75-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="80f75-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80f75-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
