---
title: ICorDebugFunction::GetNativeCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetNativeCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetNativeCode
helpviewer_keywords:
- GetNativeCode method [.NET Framework debugging]
- ICorDebugFunction::GetNativeCode method [.NET Framework debugging]
ms.assetid: c8a34916-0eef-4987-8d29-c8bcb4be9cf6
topic_type:
- apiref
ms.openlocfilehash: e34dff2ebdb6e1ea56c2682b351c3e17a44416f3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726309"
---
# <a name="icordebugfunctiongetnativecode-method"></a><span data-ttu-id="c027d-102">ICorDebugFunction::GetNativeCode 方法</span><span class="sxs-lookup"><span data-stu-id="c027d-102">ICorDebugFunction::GetNativeCode Method</span></span>

<span data-ttu-id="c027d-103">获取此 ICorDebugFunction 实例所表示的函数的本机代码。</span><span class="sxs-lookup"><span data-stu-id="c027d-103">Gets the native code for the function that is represented by this ICorDebugFunction instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c027d-104">语法</span><span class="sxs-lookup"><span data-stu-id="c027d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNativeCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c027d-105">参数</span><span class="sxs-lookup"><span data-stu-id="c027d-105">Parameters</span></span>  

 `ppCode`  
 <span data-ttu-id="c027d-106">弄一个指针，指向表示此函数的本机代码的 ICorDebugCode 实例，如果此函数为 Microsoft 中间语言，则为 null; 如果此函数为 Microsoft 中间 (语言，则为) 代码，该代码不是实时 (JIT) 编译的。</span><span class="sxs-lookup"><span data-stu-id="c027d-106">[out] A pointer to the ICorDebugCode instance that represents the native code for this function, or null, if this function is Microsoft intermediate language (MSIL) code that has not been just-in-time (JIT) compiled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c027d-107">注解</span><span class="sxs-lookup"><span data-stu-id="c027d-107">Remarks</span></span>  

 <span data-ttu-id="c027d-108">如果此实例表示的函数已多次 `ICorDebugFunction` JIT 编译（如泛型类型），则 `GetNativeCode` 返回随机的本机代码对象。</span><span class="sxs-lookup"><span data-stu-id="c027d-108">If the function that is represented by this `ICorDebugFunction` instance has been JIT-compiled more than once, as in the case of generic types, `GetNativeCode` returns a random native code object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c027d-109">要求</span><span class="sxs-lookup"><span data-stu-id="c027d-109">Requirements</span></span>  

 <span data-ttu-id="c027d-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c027d-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c027d-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c027d-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c027d-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c027d-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c027d-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c027d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
