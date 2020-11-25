---
title: COR_PRF_FUNCTION_ARGUMENT_RANGE 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
helpviewer_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE structure [.NET Framework profiling'
ms.assetid: 9f469eac-ac66-419b-8668-fe705bc1a51f
topic_type:
- apiref
ms.openlocfilehash: 028395b1c8677d07d4a6481740ecdc7ebb48c180
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95718509"
---
# <a name="cor_prf_function_argument_range-structure"></a><span data-ttu-id="0b9d5-102">COR_PRF_FUNCTION_ARGUMENT_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="0b9d5-102">COR_PRF_FUNCTION_ARGUMENT_RANGE Structure</span></span>

<span data-ttu-id="0b9d5-103">表示内存中按从左向右的顺序连续存储的函数自变量块。</span><span class="sxs-lookup"><span data-stu-id="0b9d5-103">Represents a block of function arguments stored contiguously in left-to-right order in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b9d5-104">语法</span><span class="sxs-lookup"><span data-stu-id="0b9d5-104">Syntax</span></span>  
  
```cpp  
typedef struct _COR_PRF_FUNCTION_ARGUMENT_RANGE {  
    UINT_PTR startAddress;  
    ULONG length;  
} COR_PRF_FUNCTION_ARGUMENT_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="0b9d5-105">成员</span><span class="sxs-lookup"><span data-stu-id="0b9d5-105">Members</span></span>  
  
|<span data-ttu-id="0b9d5-106">成员</span><span class="sxs-lookup"><span data-stu-id="0b9d5-106">Members</span></span>|<span data-ttu-id="0b9d5-107">说明</span><span class="sxs-lookup"><span data-stu-id="0b9d5-107">Description</span></span>|  
|-------------|-----------------|  
|`startAddress`|<span data-ttu-id="0b9d5-108">块的起始地址。</span><span class="sxs-lookup"><span data-stu-id="0b9d5-108">The starting address of the block.</span></span>|  
|`length`|<span data-ttu-id="0b9d5-109">连续块的长度。</span><span class="sxs-lookup"><span data-stu-id="0b9d5-109">The length of the contiguous block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0b9d5-110">要求</span><span class="sxs-lookup"><span data-stu-id="0b9d5-110">Requirements</span></span>  

 <span data-ttu-id="0b9d5-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0b9d5-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b9d5-112">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="0b9d5-112">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="0b9d5-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0b9d5-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0b9d5-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b9d5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b9d5-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b9d5-115">See also</span></span>

- [<span data-ttu-id="0b9d5-116">分析结构</span><span class="sxs-lookup"><span data-stu-id="0b9d5-116">Profiling Structures</span></span>](profiling-structures.md)
