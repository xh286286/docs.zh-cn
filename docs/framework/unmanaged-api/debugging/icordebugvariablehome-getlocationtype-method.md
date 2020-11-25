---
title: ICorDebugVariableHome：： GetLocationType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetLocationType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetLocationType
helpviewer_keywords:
- ICorDebugVariableHome::GetLocationType method [.NET Framework debugging]
- GetLocationType method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 88027c55-8ec6-4f1e-a55b-7eefdbbc3515
topic_type:
- apiref
ms.openlocfilehash: 3979ed19f8a61ac1fc045b83c52e23d7255ac364
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95711866"
---
# <a name="icordebugvariablehomegetlocationtype-method"></a><span data-ttu-id="74a9c-102">ICorDebugVariableHome：： GetLocationType 方法</span><span class="sxs-lookup"><span data-stu-id="74a9c-102">ICorDebugVariableHome::GetLocationType Method</span></span>

<span data-ttu-id="74a9c-103">获取变量的本机位置的类型。</span><span class="sxs-lookup"><span data-stu-id="74a9c-103">Gets the type of the variable's native location.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74a9c-104">语法</span><span class="sxs-lookup"><span data-stu-id="74a9c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetLocationType(  
    [out] VariableLocationType *pLocationType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="74a9c-105">参数</span><span class="sxs-lookup"><span data-stu-id="74a9c-105">Parameters</span></span>  

 `pLocationType`  
 <span data-ttu-id="74a9c-106">弄指向变量的本机位置的类型的指针。</span><span class="sxs-lookup"><span data-stu-id="74a9c-106">[out] A pointer to the type of the variable's native location.</span></span>  <span data-ttu-id="74a9c-107">有关详细信息，请参阅 [VariableLocationType](variablelocationtype-enumeration.md) 枚举。</span><span class="sxs-lookup"><span data-stu-id="74a9c-107">See the [VariableLocationType](variablelocationtype-enumeration.md) enumeration for more information.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74a9c-108">要求</span><span class="sxs-lookup"><span data-stu-id="74a9c-108">Requirements</span></span>  

 <span data-ttu-id="74a9c-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="74a9c-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74a9c-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="74a9c-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="74a9c-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="74a9c-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="74a9c-112">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="74a9c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74a9c-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="74a9c-113">See also</span></span>

- [<span data-ttu-id="74a9c-114">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="74a9c-114">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
- [<span data-ttu-id="74a9c-115">VariableLocationType 枚举</span><span class="sxs-lookup"><span data-stu-id="74a9c-115">VariableLocationType Enumeration</span></span>](variablelocationtype-enumeration.md)
