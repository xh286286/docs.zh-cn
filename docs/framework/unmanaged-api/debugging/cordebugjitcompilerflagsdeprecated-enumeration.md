---
title: CorDebugJITCompilerFlagsDeprecated 枚举
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlagsDeprecated
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlagsDeprecated
helpviewer_keywords:
- CorDebugJITCompilerFlagsDeprecated enumeration [.NET Framework debugging]
ms.assetid: af15e2ca-6be1-472b-bd36-03644a1e3ddd
topic_type:
- apiref
ms.openlocfilehash: 8797f77388bf4992dfb69191ce8a844a9b7fdb8a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696435"
---
# <a name="cordebugjitcompilerflagsdeprecated-enumeration"></a><span data-ttu-id="19d30-102">CorDebugJITCompilerFlagsDeprecated 枚举</span><span class="sxs-lookup"><span data-stu-id="19d30-102">CorDebugJITCompilerFlagsDeprecated Enumeration</span></span>

<span data-ttu-id="19d30-103">此枚举已过时。</span><span class="sxs-lookup"><span data-stu-id="19d30-103">This enumeration is obsolete.</span></span> <span data-ttu-id="19d30-104">改为使用 `CORDEBUG_JIT_DEFAULT` [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的成员。</span><span class="sxs-lookup"><span data-stu-id="19d30-104">Use the `CORDEBUG_JIT_DEFAULT` member of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19d30-105">语法</span><span class="sxs-lookup"><span data-stu-id="19d30-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugJITCompilerFlagsDeprecated {  
    CORDEBUG_JIT_TRACK_DEBUG_INFO  = 0x1  
} CorDebugJITCompilerFlagsDeprecated;  
```  
  
## <a name="members"></a><span data-ttu-id="19d30-106">成员</span><span class="sxs-lookup"><span data-stu-id="19d30-106">Members</span></span>  
  
|<span data-ttu-id="19d30-107">成员</span><span class="sxs-lookup"><span data-stu-id="19d30-107">Member</span></span>|<span data-ttu-id="19d30-108">说明</span><span class="sxs-lookup"><span data-stu-id="19d30-108">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_TRACK_DEBUG_INFO`|<span data-ttu-id="19d30-109">请改用 `CORDEBUG_JIT_DEFAULT`。</span><span class="sxs-lookup"><span data-stu-id="19d30-109">Use `CORDEBUG_JIT_DEFAULT` instead.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="19d30-110">要求</span><span class="sxs-lookup"><span data-stu-id="19d30-110">Requirements</span></span>  

 <span data-ttu-id="19d30-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="19d30-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19d30-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="19d30-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="19d30-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="19d30-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="19d30-114">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="19d30-114">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19d30-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="19d30-115">See also</span></span>

- [<span data-ttu-id="19d30-116">调试枚举</span><span class="sxs-lookup"><span data-stu-id="19d30-116">Debugging Enumerations</span></span>](debugging-enumerations.md)
