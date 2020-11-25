---
title: “Cor调试调试事件类型”枚举
ms.date: 03/30/2017
api_name:
- CorDebugDebugEventKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6075a6cd-97e6-4472-a090-0dd14860d1f3
topic_type:
- apiref
ms.openlocfilehash: e348e0070a5ce619f95dad9ebe4085d17f7ade6d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733368"
---
# <a name="cordebugdebugeventkind-enumeration"></a><span data-ttu-id="15249-102">“Cor调试调试事件类型”枚举</span><span class="sxs-lookup"><span data-stu-id="15249-102">CorDebugDebugEventKind Enumeration</span></span>

<span data-ttu-id="15249-103">指示 [DecodeEvent](icordebugprocess6-decodeevent-method.md) 方法对其信息进行解码的事件类型。</span><span class="sxs-lookup"><span data-stu-id="15249-103">Indicates the type of event whose information is decoded by the [DecodeEvent](icordebugprocess6-decodeevent-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15249-104">语法</span><span class="sxs-lookup"><span data-stu-id="15249-104">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugDebugEventKind {  
    DEBUG_EVENT_KIND_MODULE_LOADED                          = 1,  
    DEBUG_EVENT_KIND_MODULE_UNLOADED                        = 2,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE         = 3,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE    = 4,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND  = 5,  
    DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED            = 6  
} CorDebugRecordFormat;  
```  
  
## <a name="members"></a><span data-ttu-id="15249-105">成员</span><span class="sxs-lookup"><span data-stu-id="15249-105">Members</span></span>  
  
|<span data-ttu-id="15249-106">成员</span><span class="sxs-lookup"><span data-stu-id="15249-106">Member</span></span>|<span data-ttu-id="15249-107">说明</span><span class="sxs-lookup"><span data-stu-id="15249-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EVENT_KIND_MODULE_LOADED`|<span data-ttu-id="15249-108">模块加载事件。</span><span class="sxs-lookup"><span data-stu-id="15249-108">A module load event.</span></span>|  
|`DEBUG_EVENT_KIND_MODULE_UNLOADED`|<span data-ttu-id="15249-109">模块卸载事件。</span><span class="sxs-lookup"><span data-stu-id="15249-109">A module unload event.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_FIRST_CHANCE`|<span data-ttu-id="15249-110">最可能的异常。</span><span class="sxs-lookup"><span data-stu-id="15249-110">A first-chance exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_USER_FIRST_CHANCE`|<span data-ttu-id="15249-111">最可能的用户异常。</span><span class="sxs-lookup"><span data-stu-id="15249-111">A first-chance user exception.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_CATCH_HANDLER_FOUND`|<span data-ttu-id="15249-112">`catch` 处理程序存在的异常。</span><span class="sxs-lookup"><span data-stu-id="15249-112">An exception for which a `catch` handler exists.</span></span>|  
|`DEBUG_EVENT_KIND_MANAGED_EXCEPTION_UNHANDLED`|<span data-ttu-id="15249-113">未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="15249-113">An unhandled exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15249-114">注解</span><span class="sxs-lookup"><span data-stu-id="15249-114">Remarks</span></span>  

 <span data-ttu-id="15249-115">枚举的成员 `CorDebugDebugEventKind` 是通过调用 [ICorDebugDebugEvent：： GetEventKind](icordebugdebugevent-geteventkind-method.md) 方法返回的。</span><span class="sxs-lookup"><span data-stu-id="15249-115">A member of the `CorDebugDebugEventKind` enumeration is returned by calling the [ICorDebugDebugEvent::GetEventKind](icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="15249-116">此枚举仅用于 .NET Native 调试方案。</span><span class="sxs-lookup"><span data-stu-id="15249-116">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15249-117">要求</span><span class="sxs-lookup"><span data-stu-id="15249-117">Requirements</span></span>  

 <span data-ttu-id="15249-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="15249-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15249-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="15249-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="15249-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="15249-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="15249-121">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15249-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15249-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15249-122">See also</span></span>

- [<span data-ttu-id="15249-123">调试枚举</span><span class="sxs-lookup"><span data-stu-id="15249-123">Debugging Enumerations</span></span>](debugging-enumerations.md)
