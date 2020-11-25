---
title: ICorDebugVariableHome：： GetSlotIndex 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetSlotIndex
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetSlotIndex
helpviewer_keywords:
- ICorDebugVariableHome::GetSlotIndex method [.NET Framework debugging]
- GetSlotIndex method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 966da50d-5665-4fff-bf7b-1c72bbadd9a4
topic_type:
- apiref
ms.openlocfilehash: 4b071bd8e9d96084848c1553385eec5f8beca624
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95711723"
---
# <a name="icordebugvariablehomegetslotindex-method"></a><span data-ttu-id="9692f-102">ICorDebugVariableHome：： GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="9692f-102">ICorDebugVariableHome::GetSlotIndex Method</span></span>

<span data-ttu-id="9692f-103">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="9692f-103">Gets the managed slot-index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9692f-104">语法</span><span class="sxs-lookup"><span data-stu-id="9692f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSlotIndex(  
    [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9692f-105">参数</span><span class="sxs-lookup"><span data-stu-id="9692f-105">Parameters</span></span>  

 `pSlotIndex`  
 <span data-ttu-id="9692f-106">弄指向局部变量的槽索引的指针。</span><span class="sxs-lookup"><span data-stu-id="9692f-106">[out] A pointer to the slot-index of a local variable.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9692f-107">返回值</span><span class="sxs-lookup"><span data-stu-id="9692f-107">Return Value</span></span>  

 <span data-ttu-id="9692f-108">方法返回以下值。</span><span class="sxs-lookup"><span data-stu-id="9692f-108">The method returns the following values.</span></span>  
  
|<span data-ttu-id="9692f-109">Value</span><span class="sxs-lookup"><span data-stu-id="9692f-109">Value</span></span>|<span data-ttu-id="9692f-110">说明</span><span class="sxs-lookup"><span data-stu-id="9692f-110">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="9692f-111">方法调用返回中的槽索引值 `pSlotIndex` 。</span><span class="sxs-lookup"><span data-stu-id="9692f-111">The method call returned a slot-index value in `pSlotIndex`.</span></span>|  
|`E_FAIL`|<span data-ttu-id="9692f-112">当前 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 实例表示函数参数。</span><span class="sxs-lookup"><span data-stu-id="9692f-112">The current [ICorDebugVariableHome](icordebugvariablehome-interface.md) instance represents a function argument.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9692f-113">注解</span><span class="sxs-lookup"><span data-stu-id="9692f-113">Remarks</span></span>  

 <span data-ttu-id="9692f-114">槽索引可用于检索此局部变量的元数据。</span><span class="sxs-lookup"><span data-stu-id="9692f-114">The slot-index can be used to retrieve the metadata for this local variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9692f-115">要求</span><span class="sxs-lookup"><span data-stu-id="9692f-115">Requirements</span></span>  

 <span data-ttu-id="9692f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9692f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9692f-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9692f-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9692f-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9692f-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9692f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9692f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9692f-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9692f-120">See also</span></span>

- [<span data-ttu-id="9692f-121">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="9692f-121">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
