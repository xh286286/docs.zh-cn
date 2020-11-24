---
title: ICorDebugType::GetBase 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetBase
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetBase
helpviewer_keywords:
- ICorDebugType::GetBase method [.NET Framework debugging]
- GetBase method [.NET Framework debugging]
ms.assetid: f24e1af9-c220-4f79-ae62-4153ec17ea81
topic_type:
- apiref
ms.openlocfilehash: 967f8f25e240f484ae86852c740be12cd3a6409e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95681816"
---
# <a name="icordebugtypegetbase-method"></a><span data-ttu-id="c459b-102">ICorDebugType::GetBase 方法</span><span class="sxs-lookup"><span data-stu-id="c459b-102">ICorDebugType::GetBase Method</span></span>

<span data-ttu-id="c459b-103">获取一个接口指针，该指针指向表示此所表示的类型的基类型（如果存在）的 ICorDebugType `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="c459b-103">Gets an interface pointer to an ICorDebugType that represents the base type, if one exists, of the type represented by this `ICorDebugType`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c459b-104">语法</span><span class="sxs-lookup"><span data-stu-id="c459b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetBase (  
    [out] ICorDebugType   **pBase  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c459b-105">参数</span><span class="sxs-lookup"><span data-stu-id="c459b-105">Parameters</span></span>  

 `pBase`  
 <span data-ttu-id="c459b-106">弄指向 `ICorDebugType` 表示基类型的对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="c459b-106">[out] A pointer to the address of an `ICorDebugType` object that represents the base type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c459b-107">注解</span><span class="sxs-lookup"><span data-stu-id="c459b-107">Remarks</span></span>  

 <span data-ttu-id="c459b-108">查找类型的基类型对于实现常见调试器功能非常有用，例如打印对象或其父类的所有字段。</span><span class="sxs-lookup"><span data-stu-id="c459b-108">Looking up the base type for a type is useful to implement common debugger functionality, such as printing out all the fields of an object or its parent classes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c459b-109">要求</span><span class="sxs-lookup"><span data-stu-id="c459b-109">Requirements</span></span>  

 <span data-ttu-id="c459b-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c459b-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c459b-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c459b-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c459b-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c459b-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c459b-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c459b-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
