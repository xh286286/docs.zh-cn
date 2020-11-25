---
title: EClrEvent 枚举
ms.date: 03/30/2017
api_name:
- EClrEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrEvent
helpviewer_keywords:
- EClrEvent enumeration [.NET Framework hosting]
ms.assetid: 7c36a7c2-75a2-4971-bc23-abf54c812154
topic_type:
- apiref
ms.openlocfilehash: 5d6ec42da60a7b294177063b9f8bd5afbf352c62
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726816"
---
# <a name="eclrevent-enumeration"></a><span data-ttu-id="304f2-102">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="304f2-102">EClrEvent Enumeration</span></span>

<span data-ttu-id="304f2-103">介绍了公共语言运行时 (CLR) 事件，主机可以为这些事件注册回调。</span><span class="sxs-lookup"><span data-stu-id="304f2-103">Describes the common language runtime (CLR) events for which the host can register callbacks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="304f2-104">语法</span><span class="sxs-lookup"><span data-stu-id="304f2-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    Event_ClrDisabled,  
    Event_DomainUnload,  
    Event_MDAFired,  
    Event_StackOverflow  
} EClrEvent;  
```  
  
## <a name="members"></a><span data-ttu-id="304f2-105">成员</span><span class="sxs-lookup"><span data-stu-id="304f2-105">Members</span></span>  
  
|<span data-ttu-id="304f2-106">成员</span><span class="sxs-lookup"><span data-stu-id="304f2-106">Member</span></span>|<span data-ttu-id="304f2-107">说明</span><span class="sxs-lookup"><span data-stu-id="304f2-107">Description</span></span>|  
|------------|-----------------|  
|`Event_ClrDisabled`|<span data-ttu-id="304f2-108">指定 CLR 错误的严重错误。</span><span class="sxs-lookup"><span data-stu-id="304f2-108">Specifies a fatal CLR error.</span></span>|  
|`Event_DomainUnload`|<span data-ttu-id="304f2-109">指定卸载特定的 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="304f2-109">Specifies the unloading of a particular <xref:System.AppDomain>.</span></span>|  
|`Event_MDAFired`|<span data-ttu-id="304f2-110">指定已生成 (MDA) 消息的托管调试助手。</span><span class="sxs-lookup"><span data-stu-id="304f2-110">Specifies that a Managed Debugging Assistant (MDA) message has been generated.</span></span>|  
|`Event_StackOverflow`|<span data-ttu-id="304f2-111">指定发生堆栈溢出错误。</span><span class="sxs-lookup"><span data-stu-id="304f2-111">Specifies that a stack overflow error has occurred.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="304f2-112">注解</span><span class="sxs-lookup"><span data-stu-id="304f2-112">Remarks</span></span>  

 <span data-ttu-id="304f2-113">宿主可以 `EClrEvent` 通过调用 [ICLROnEventManager](iclroneventmanager-interface.md) 接口的方法，为描述的任何事件类型注册回调。</span><span class="sxs-lookup"><span data-stu-id="304f2-113">The host can register callbacks for any of the event types described by `EClrEvent` by calling methods of the [ICLROnEventManager](iclroneventmanager-interface.md) interface.</span></span> <span data-ttu-id="304f2-114">宿主通过调用 [ICLRControl：： GetCLRManager](iclrcontrol-getclrmanager-method.md) 方法获取指向此接口的指针。</span><span class="sxs-lookup"><span data-stu-id="304f2-114">The host gets a pointer to this interface by calling the [ICLRControl::GetCLRManager](iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
 <span data-ttu-id="304f2-115">`Event_CLRDisabled`和 `Event_DomainUnload` 事件可以多次引发，并从不同的线程引发，以指示卸载或禁用 CLR。</span><span class="sxs-lookup"><span data-stu-id="304f2-115">The `Event_CLRDisabled` and `Event_DomainUnload` events can be raised more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
 <span data-ttu-id="304f2-116">此 `Event_MDAFired` 事件将引发包含 MDA 消息的详细信息的 [MDAInfo](mdainfo-structure.md) 实例的创建。</span><span class="sxs-lookup"><span data-stu-id="304f2-116">The `Event_MDAFired` event raises the creation of an [MDAInfo](mdainfo-structure.md) instance that contains the details of the MDA message.</span></span> <span data-ttu-id="304f2-117">有关 Mda 的详细信息，请参阅 [诊断托管调试助手的错误](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)。</span><span class="sxs-lookup"><span data-stu-id="304f2-117">For more information about MDAs, see [Diagnosing Errors with Managed Debugging Assistants](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="304f2-118">要求</span><span class="sxs-lookup"><span data-stu-id="304f2-118">Requirements</span></span>  

 <span data-ttu-id="304f2-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="304f2-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="304f2-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="304f2-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="304f2-121">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="304f2-121">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="304f2-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="304f2-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="304f2-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="304f2-123">See also</span></span>

- [<span data-ttu-id="304f2-124">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="304f2-124">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)
- [<span data-ttu-id="304f2-125">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="304f2-125">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="304f2-126">承载枚举</span><span class="sxs-lookup"><span data-stu-id="304f2-126">Hosting Enumerations</span></span>](hosting-enumerations.md)
