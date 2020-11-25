---
title: CorDebugNGenPolicy 枚举
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugNGenPolicy
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugNGenPolicy
helpviewer_keywords:
- CorDebugNgenPolicy enumeration [.NET Framework debugging]
ms.assetid: edb4e4d2-3166-44d4-8b17-bf302f7ea093
topic_type:
- apiref
ms.openlocfilehash: b64de0fa2ecbddd2decf69a4099d9897ec42a563
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696422"
---
# <a name="cordebugngenpolicy-enumeration"></a><span data-ttu-id="83fc2-102">CorDebugNGenPolicy 枚举</span><span class="sxs-lookup"><span data-stu-id="83fc2-102">CorDebugNGenPolicy Enumeration</span></span>

<span data-ttu-id="83fc2-103">提供用于确定调试器是否从本机映像缓存中加载本机 (NGen) 映像的值。</span><span class="sxs-lookup"><span data-stu-id="83fc2-103">Provides a value that determines whether a debugger loads native (NGen) images from the native image cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83fc2-104">语法</span><span class="sxs-lookup"><span data-stu-id="83fc2-104">Syntax</span></span>  
  
```cpp
enum CorDebugNGENPolicy {  
    DISABLE_LOCAL_NIC = 1  
} CorDebugNGENPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="83fc2-105">成员</span><span class="sxs-lookup"><span data-stu-id="83fc2-105">Members</span></span>  
  
|<span data-ttu-id="83fc2-106">成员名称</span><span class="sxs-lookup"><span data-stu-id="83fc2-106">Member name</span></span>|<span data-ttu-id="83fc2-107">说明</span><span class="sxs-lookup"><span data-stu-id="83fc2-107">Description</span></span>|  
|-----------------|-----------------|  
|`DISABLE_LOCAL_NIC`|<span data-ttu-id="83fc2-108">在 Windows 8.x 应用商店应用中，禁用了本地本机映像缓存中的映像。</span><span class="sxs-lookup"><span data-stu-id="83fc2-108">In a Windows 8.x Store app, the use of images from the local native image cache is disabled.</span></span> <span data-ttu-id="83fc2-109">在桌面应用中，此设置不起作用。</span><span class="sxs-lookup"><span data-stu-id="83fc2-109">In a desktop app, this setting has no effect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83fc2-110">注解</span><span class="sxs-lookup"><span data-stu-id="83fc2-110">Remarks</span></span>  

 <span data-ttu-id="83fc2-111">`CorDebugNGENPolicy`枚举由[ICorDebugProcess5：： EnableNGENPolicy](icordebugprocess5-enablengenpolicy-method.md)方法使用。</span><span class="sxs-lookup"><span data-stu-id="83fc2-111">The `CorDebugNGENPolicy` enumeration is used by the [ICorDebugProcess5::EnableNGENPolicy](icordebugprocess5-enablengenpolicy-method.md) method.</span></span> <span data-ttu-id="83fc2-112">禁用本地本机映像缓存中的映像可提供一致的调试体验，方法是确保调试器加载可调试 JIT 编译的映像，而不是优化的本机映像。</span><span class="sxs-lookup"><span data-stu-id="83fc2-112">Disabling the use of images from the local native image cache provides for a consistent debugging experience by ensuring that the debugger loads debuggable JIT-compiled images instead of optimized native images.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83fc2-113">要求</span><span class="sxs-lookup"><span data-stu-id="83fc2-113">Requirements</span></span>  

 <span data-ttu-id="83fc2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="83fc2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83fc2-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="83fc2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="83fc2-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="83fc2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="83fc2-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83fc2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83fc2-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83fc2-118">See also</span></span>

- [<span data-ttu-id="83fc2-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="83fc2-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
