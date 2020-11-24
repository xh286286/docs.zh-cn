---
title: ICorDebugType::GetClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetClass
helpviewer_keywords:
- ICorDebugType::GetClass method [.NET Framework debugging]
- GetClass method, ICorDebugType interface [.NET Framework debugging]
ms.assetid: 2644f48b-db3c-429f-ae62-76f1c98a1af5
topic_type:
- apiref
ms.openlocfilehash: 1cb9729f175a2e82e88386b0694467c6fe05636a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684455"
---
# <a name="icordebugtypegetclass-method"></a><span data-ttu-id="c92db-102">ICorDebugType::GetClass 方法</span><span class="sxs-lookup"><span data-stu-id="c92db-102">ICorDebugType::GetClass Method</span></span>

<span data-ttu-id="c92db-103">获取一个接口指针，该指针指向表示未实例化的泛型类型的 ICorDebugClass。</span><span class="sxs-lookup"><span data-stu-id="c92db-103">Gets an interface pointer to an ICorDebugClass that represents the uninstantiated generic type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c92db-104">语法</span><span class="sxs-lookup"><span data-stu-id="c92db-104">Syntax</span></span>  
  
```cpp  
HRESULT GetClass (  
    [out] ICorDebugClass   **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c92db-105">参数</span><span class="sxs-lookup"><span data-stu-id="c92db-105">Parameters</span></span>  

 `ppClass`  
 <span data-ttu-id="c92db-106">弄一个指针，指向 `ICorDebugClass` 表示未实例化的泛型类型的接口的地址。</span><span class="sxs-lookup"><span data-stu-id="c92db-106">[out] A pointer to the address of an `ICorDebugClass` interface that represents the uninstantiated generic type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c92db-107">注解</span><span class="sxs-lookup"><span data-stu-id="c92db-107">Remarks</span></span>  

 <span data-ttu-id="c92db-108">`GetClass` 只能在某些条件下调用。</span><span class="sxs-lookup"><span data-stu-id="c92db-108">`GetClass` can be called only under certain conditions.</span></span> <span data-ttu-id="c92db-109">调用 [ICorDebugType：： GetType](icordebugtype-gettype-method.md) ，然后调用 `GetClass` 。</span><span class="sxs-lookup"><span data-stu-id="c92db-109">Call [ICorDebugType::GetType](icordebugtype-gettype-method.md) before calling `GetClass`.</span></span> <span data-ttu-id="c92db-110">如果 `ICorDebugType::GetType` 返回 ELEMENT_TYPE_CLASS 或 ELEMENT_TYPE_VALUETYPE 的 CorElementType 值，则 `GetClass` 可以调用来获取泛型类型的实例化类型。</span><span class="sxs-lookup"><span data-stu-id="c92db-110">If `ICorDebugType::GetType` returns a CorElementType value that is ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE, `GetClass` can be called to get the uninstantiated type for a generic type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c92db-111">要求</span><span class="sxs-lookup"><span data-stu-id="c92db-111">Requirements</span></span>  

 <span data-ttu-id="c92db-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c92db-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c92db-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c92db-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c92db-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c92db-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c92db-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c92db-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
