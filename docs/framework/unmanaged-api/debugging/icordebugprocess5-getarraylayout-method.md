---
title: ICorDebugProcess5::GetArrayLayout 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetArrayLayout
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetArrayLayout
helpviewer_keywords:
- ICorDebugProcess5::GetArrayLayout method [.NET Framework debugging]
- GetArrayLayout method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 9a7393b9-9735-43c6-8616-afb103c432fd
topic_type:
- apiref
ms.openlocfilehash: 8b7fab5fc5a02f8e43dc5f6fe8fc98087859ee3d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671104"
---
# <a name="icordebugprocess5getarraylayout-method"></a><span data-ttu-id="d4e4a-102">ICorDebugProcess5::GetArrayLayout 方法</span><span class="sxs-lookup"><span data-stu-id="d4e4a-102">ICorDebugProcess5::GetArrayLayout Method</span></span>

<span data-ttu-id="d4e4a-103">提供有关数组类型布局的信息。</span><span class="sxs-lookup"><span data-stu-id="d4e4a-103">Provides information about the layout of array types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4e4a-104">语法</span><span class="sxs-lookup"><span data-stu-id="d4e4a-104">Syntax</span></span>  
  
```cpp  
HRESULT GetArrayLayout(    [in] COR_TYPEID id,     [out] COR_ARRAY_LAYOUT *pLayout);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d4e4a-105">参数</span><span class="sxs-lookup"><span data-stu-id="d4e4a-105">Parameters</span></span>  

 `id`  
 <span data-ttu-id="d4e4a-106">中一个 [COR_TYPEID](cor-typeid-structure.md) 标记，它指定需要其布局的数组。</span><span class="sxs-lookup"><span data-stu-id="d4e4a-106">[in] A [COR_TYPEID](cor-typeid-structure.md) token that specifies the array whose layout is desired.</span></span>  
  
 `pLayout`  
 <span data-ttu-id="d4e4a-107">弄指向 [COR_ARRAY_LAYOUT](cor-array-layout-structure.md) 结构的指针，该结构包含有关内存中数组的布局的信息。</span><span class="sxs-lookup"><span data-stu-id="d4e4a-107">[out] A pointer to a [COR_ARRAY_LAYOUT](cor-array-layout-structure.md) structure that contains information about the layout of the array in memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d4e4a-108">备注</span><span class="sxs-lookup"><span data-stu-id="d4e4a-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4e4a-109">要求</span><span class="sxs-lookup"><span data-stu-id="d4e4a-109">Requirements</span></span>  

 <span data-ttu-id="d4e4a-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d4e4a-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4e4a-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d4e4a-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d4e4a-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d4e4a-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d4e4a-113">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4e4a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4e4a-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d4e4a-114">See also</span></span>

- [<span data-ttu-id="d4e4a-115">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="d4e4a-115">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="d4e4a-116">调试接口</span><span class="sxs-lookup"><span data-stu-id="d4e4a-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
