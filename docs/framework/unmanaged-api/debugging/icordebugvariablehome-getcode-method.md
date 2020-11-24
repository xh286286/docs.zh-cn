---
title: ICorDebugVariableHome：： GetCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetCode
helpviewer_keywords:
- ICorDebugVariableHome::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: ef002890-4a7b-4a5d-abbf-16c60083f794
topic_type:
- apiref
ms.openlocfilehash: 6f5d99e6dc4290ef69c0a0748fe15ae538e83558
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684221"
---
# <a name="icordebugvariablehomegetcode-method"></a><span data-ttu-id="ebdd4-102">ICorDebugVariableHome：： GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="ebdd4-102">ICorDebugVariableHome::GetCode Method</span></span>

<span data-ttu-id="ebdd4-103">获取包含此 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 对象的 "ICorDebugCode" 实例。</span><span class="sxs-lookup"><span data-stu-id="ebdd4-103">Gets the "ICorDebugCode" instance that contains this [ICorDebugVariableHome](icordebugvariablehome-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebdd4-104">语法</span><span class="sxs-lookup"><span data-stu-id="ebdd4-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCode(  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ebdd4-105">参数</span><span class="sxs-lookup"><span data-stu-id="ebdd4-105">Parameters</span></span>  

 `ppCode`  
 <span data-ttu-id="ebdd4-106">弄一个指针，指向包含此 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 对象的 "ICorDebugCode" 实例的地址。</span><span class="sxs-lookup"><span data-stu-id="ebdd4-106">[out] A pointer to the address of the "ICorDebugCode" instance that contains this [ICorDebugVariableHome](icordebugvariablehome-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ebdd4-107">要求</span><span class="sxs-lookup"><span data-stu-id="ebdd4-107">Requirements</span></span>  

 <span data-ttu-id="ebdd4-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ebdd4-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebdd4-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ebdd4-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ebdd4-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ebdd4-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ebdd4-111">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ebdd4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebdd4-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ebdd4-112">See also</span></span>

- [<span data-ttu-id="ebdd4-113">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="ebdd4-113">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
