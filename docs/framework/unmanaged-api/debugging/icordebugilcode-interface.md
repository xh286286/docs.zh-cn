---
title: ICorDebugILCode 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILCode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 51c4de0c-3813-4142-be25-a85bb84efb90
topic_type:
- apiref
ms.openlocfilehash: 980e97dd8ec4792e35bb8c7fbbc2091e9ced719a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728649"
---
# <a name="icordebugilcode-interface"></a><span data-ttu-id="49444-102">ICorDebugILCode 接口</span><span class="sxs-lookup"><span data-stu-id="49444-102">ICorDebugILCode Interface</span></span>

<span data-ttu-id="49444-103">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="49444-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="49444-104">表示中间语言 (IL) 代码段。</span><span class="sxs-lookup"><span data-stu-id="49444-104">Represents a segment of intermediate language (IL) code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="49444-105">方法</span><span class="sxs-lookup"><span data-stu-id="49444-105">Methods</span></span>  
  
|<span data-ttu-id="49444-106">方法</span><span class="sxs-lookup"><span data-stu-id="49444-106">Method</span></span>|<span data-ttu-id="49444-107">说明</span><span class="sxs-lookup"><span data-stu-id="49444-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="49444-108">GetEHClauses 方法</span><span class="sxs-lookup"><span data-stu-id="49444-108">GetEHClauses Method</span></span>](icordebugilcode-getehclauses-method.md)|<span data-ttu-id="49444-109">返回指向为此 IL 定义的异常处理 (EH) 子句列表的指针。</span><span class="sxs-lookup"><span data-stu-id="49444-109">Returns a pointer to a list of exception handling (EH) clauses that are defined for this IL.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="49444-110">要求</span><span class="sxs-lookup"><span data-stu-id="49444-110">Requirements</span></span>  

 <span data-ttu-id="49444-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49444-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49444-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="49444-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="49444-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="49444-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="49444-114">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49444-114">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49444-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49444-115">See also</span></span>

- [<span data-ttu-id="49444-116">调试接口</span><span class="sxs-lookup"><span data-stu-id="49444-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="49444-117">调试</span><span class="sxs-lookup"><span data-stu-id="49444-117">Debugging</span></span>](index.md)
