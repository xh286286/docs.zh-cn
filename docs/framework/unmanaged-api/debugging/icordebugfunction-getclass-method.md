---
title: ICorDebugFunction::GetClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetClass
helpviewer_keywords:
- GetClass method, ICorDebugFunction interface [.NET Framework debugging]
- ICorDebugFunction::GetClass method [.NET Framework debugging]
ms.assetid: 27967230-144f-40d3-9e23-961d0241abd9
topic_type:
- apiref
ms.openlocfilehash: 40cb59a2ad0539764702369b13d632eddbab8174
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728155"
---
# <a name="icordebugfunctiongetclass-method"></a><span data-ttu-id="52ef4-102">ICorDebugFunction::GetClass 方法</span><span class="sxs-lookup"><span data-stu-id="52ef4-102">ICorDebugFunction::GetClass Method</span></span>

<span data-ttu-id="52ef4-103">获取一个 ICorDebugClass 对象，该对象表示此函数所属的类。</span><span class="sxs-lookup"><span data-stu-id="52ef4-103">Gets an ICorDebugClass object that represents the class this function is a member of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52ef4-104">语法</span><span class="sxs-lookup"><span data-stu-id="52ef4-104">Syntax</span></span>  
  
```cpp  
HRESULT GetClass (  
    [out] ICorDebugClass **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="52ef4-105">参数</span><span class="sxs-lookup"><span data-stu-id="52ef4-105">Parameters</span></span>  

 `ppClass`  
 <span data-ttu-id="52ef4-106">弄指向表示类的对象的地址的指针 `ICorDebugClass` ; 如果此函数不是类的成员，则为 null。</span><span class="sxs-lookup"><span data-stu-id="52ef4-106">[out] A pointer to the address of the `ICorDebugClass` object that represents the class, or null, if this function is not a member of a class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52ef4-107">要求</span><span class="sxs-lookup"><span data-stu-id="52ef4-107">Requirements</span></span>  

 <span data-ttu-id="52ef4-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="52ef4-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="52ef4-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="52ef4-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="52ef4-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="52ef4-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="52ef4-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="52ef4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
