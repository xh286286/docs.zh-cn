---
title: ICorDebugAssemblyEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssemblyEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssemblyEnum::Next method
helpviewer_keywords:
- ICorDebugAssemblyEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugAssemblyEnum interface [.NET Framework debugging]
ms.assetid: b3e7d0c2-3baa-4ef8-8e3f-b865cf252940
topic_type:
- apiref
ms.openlocfilehash: dd915a82551f5bed688a28ab77f5d6cf4e38af0f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719242"
---
# <a name="icordebugassemblyenumnext-method"></a><span data-ttu-id="1f648-102">ICorDebugAssemblyEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="1f648-102">ICorDebugAssemblyEnum::Next Method</span></span>

<span data-ttu-id="1f648-103">从当前游标位置开始，从集合中获取指定数目的程序集。</span><span class="sxs-lookup"><span data-stu-id="1f648-103">Gets the specified number of assemblies from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f648-104">语法</span><span class="sxs-lookup"><span data-stu-id="1f648-104">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugAssembly *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1f648-105">参数</span><span class="sxs-lookup"><span data-stu-id="1f648-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="1f648-106">中要检索的程序集的数目。</span><span class="sxs-lookup"><span data-stu-id="1f648-106">[in] The number of assemblies to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="1f648-107">弄指针的数组，其中每个都指向表示程序集的 ICorDebugAssembly 对象。</span><span class="sxs-lookup"><span data-stu-id="1f648-107">[out] An array of pointers, each of which points to an ICorDebugAssembly object that represents an assembly.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="1f648-108">弄一个指针，指向实际返回的程序集的数目。</span><span class="sxs-lookup"><span data-stu-id="1f648-108">[out] A pointer to the number of assemblies actually returned.</span></span> <span data-ttu-id="1f648-109">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="1f648-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1f648-110">要求</span><span class="sxs-lookup"><span data-stu-id="1f648-110">Requirements</span></span>  

 <span data-ttu-id="1f648-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1f648-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1f648-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1f648-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1f648-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1f648-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1f648-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1f648-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
