---
title: ICorDebugArrayValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue interface
helpviewer_keywords:
- ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: dc437751-7093-44e2-bfdc-191d9ce3c192
topic_type:
- apiref
ms.openlocfilehash: 90688132b98f8316a4b08988c08b2f7cc7ce0fd8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725039"
---
# <a name="icordebugarrayvalue-interface"></a><span data-ttu-id="a610e-102">ICorDebugArrayValue 接口</span><span class="sxs-lookup"><span data-stu-id="a610e-102">ICorDebugArrayValue Interface</span></span>

<span data-ttu-id="a610e-103">表示一维或多维数组的 ICorDebugHeapValue 的子类。</span><span class="sxs-lookup"><span data-stu-id="a610e-103">A subclass of ICorDebugHeapValue that represents a single-dimensional or multi-dimensional array.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a610e-104">方法</span><span class="sxs-lookup"><span data-stu-id="a610e-104">Methods</span></span>  
  
|<span data-ttu-id="a610e-105">方法</span><span class="sxs-lookup"><span data-stu-id="a610e-105">Method</span></span>|<span data-ttu-id="a610e-106">说明</span><span class="sxs-lookup"><span data-stu-id="a610e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a610e-107">GetBaseIndicies 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-107">GetBaseIndicies Method</span></span>](icordebugarrayvalue-getbaseindicies-method.md)|<span data-ttu-id="a610e-108">获取数组中每个维的基索引。</span><span class="sxs-lookup"><span data-stu-id="a610e-108">Gets the base index of each dimension in the array.</span></span>|  
|[<span data-ttu-id="a610e-109">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-109">GetCount Method</span></span>](icordebugarrayvalue-getcount-method.md)|<span data-ttu-id="a610e-110">获取数组中的元素总数。</span><span class="sxs-lookup"><span data-stu-id="a610e-110">Gets the total number of elements in the array.</span></span>|  
|[<span data-ttu-id="a610e-111">GetDimensions 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-111">GetDimensions Method</span></span>](icordebugarrayvalue-getdimensions-method.md)|<span data-ttu-id="a610e-112">获取数组的尺寸。</span><span class="sxs-lookup"><span data-stu-id="a610e-112">Gets the dimensions of the array.</span></span>|  
|[<span data-ttu-id="a610e-113">GetElement 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-113">GetElement Method</span></span>](icordebugarrayvalue-getelement-method.md)|<span data-ttu-id="a610e-114">获取一个值，该值表示数组中的给定元素。</span><span class="sxs-lookup"><span data-stu-id="a610e-114">Gets a value representing the given element in the array.</span></span>|  
|[<span data-ttu-id="a610e-115">GetElementAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-115">GetElementAtPosition Method</span></span>](icordebugarrayvalue-getelementatposition-method.md)|<span data-ttu-id="a610e-116">获取位于给定位置的元素，并将该数组视为从零开始的一维数组。</span><span class="sxs-lookup"><span data-stu-id="a610e-116">Gets the element at the given position, treating the array as a zero-based, single-dimensional array.</span></span>|  
|[<span data-ttu-id="a610e-117">GetElementType 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-117">GetElementType Method</span></span>](icordebugarrayvalue-getelementtype-method.md)|<span data-ttu-id="a610e-118">获取数组中元素的简单类型。</span><span class="sxs-lookup"><span data-stu-id="a610e-118">Gets the simple type of the elements in the array.</span></span>|  
|[<span data-ttu-id="a610e-119">GetRank 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-119">GetRank Method</span></span>](icordebugarrayvalue-getrank-method.md)|<span data-ttu-id="a610e-120">获取数组中的维度数。</span><span class="sxs-lookup"><span data-stu-id="a610e-120">Gets the number of dimensions in the array.</span></span>|  
|[<span data-ttu-id="a610e-121">HasBaseIndicies 方法</span><span class="sxs-lookup"><span data-stu-id="a610e-121">HasBaseIndicies Method</span></span>](icordebugarrayvalue-hasbaseindicies-method.md)|<span data-ttu-id="a610e-122">确定数组是否具有基索引。</span><span class="sxs-lookup"><span data-stu-id="a610e-122">Determines whether the array has base indexes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a610e-123">注解</span><span class="sxs-lookup"><span data-stu-id="a610e-123">Remarks</span></span>  

 <span data-ttu-id="a610e-124">`ICorDebugArrayValue` 支持一维数组和多维数组。</span><span class="sxs-lookup"><span data-stu-id="a610e-124">`ICorDebugArrayValue` supports both single-dimensional and multi-dimensional arrays.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a610e-125">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="a610e-125">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a610e-126">要求</span><span class="sxs-lookup"><span data-stu-id="a610e-126">Requirements</span></span>  

 <span data-ttu-id="a610e-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a610e-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a610e-128">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a610e-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a610e-129">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a610e-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a610e-130">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a610e-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a610e-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a610e-131">See also</span></span>

- [<span data-ttu-id="a610e-132">调试接口</span><span class="sxs-lookup"><span data-stu-id="a610e-132">Debugging Interfaces</span></span>](debugging-interfaces.md)
