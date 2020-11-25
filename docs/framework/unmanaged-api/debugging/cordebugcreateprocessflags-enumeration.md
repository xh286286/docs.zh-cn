---
title: CorDebugCreateProcessFlags 枚举
ms.date: 03/30/2017
api_name:
- CorDebugCreateProcessFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugCreateProcessFlags
helpviewer_keywords:
- CorDebugCreateProcessFlags enumeration [.NET Framework debugging]
ms.assetid: e709acce-6a17-4346-b38a-467dba567358
topic_type:
- apiref
ms.openlocfilehash: f6f589656a3063fc89bd276b32d0ed751fd8d2d3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733394"
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="80fd6-102">CorDebugCreateProcessFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="80fd6-102">CorDebugCreateProcessFlags Enumeration</span></span>

<span data-ttu-id="80fd6-103">提供可在对 [ICorDebug：： CreateProcess](icordebug-createprocess-method.md) 方法的调用中使用的其他调试选项。</span><span class="sxs-lookup"><span data-stu-id="80fd6-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80fd6-104">语法</span><span class="sxs-lookup"><span data-stu-id="80fd6-104">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="80fd6-105">成员</span><span class="sxs-lookup"><span data-stu-id="80fd6-105">Members</span></span>  
  
|<span data-ttu-id="80fd6-106">成员</span><span class="sxs-lookup"><span data-stu-id="80fd6-106">Member</span></span>|<span data-ttu-id="80fd6-107">说明</span><span class="sxs-lookup"><span data-stu-id="80fd6-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="80fd6-108">未设置任何特殊选项。</span><span class="sxs-lookup"><span data-stu-id="80fd6-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="80fd6-109">要求</span><span class="sxs-lookup"><span data-stu-id="80fd6-109">Requirements</span></span>  

 <span data-ttu-id="80fd6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="80fd6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80fd6-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="80fd6-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="80fd6-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="80fd6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="80fd6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80fd6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80fd6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80fd6-114">See also</span></span>

- [<span data-ttu-id="80fd6-115">调试枚举</span><span class="sxs-lookup"><span data-stu-id="80fd6-115">Debugging Enumerations</span></span>](debugging-enumerations.md)
