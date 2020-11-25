---
title: IActionOnCLREvent::OnEvent 方法
ms.date: 03/30/2017
api_name:
- IActionOnCLREvent.OnEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IActionOnCLREvent::OnEvent
helpviewer_keywords:
- OnEvent method [.NET Framework hosting]
- IActionOnCLREvent::OnEvent method [.NET Framework hosting]
ms.assetid: 0970f10c-4304-4c12-91c0-83e51455afb4
topic_type:
- apiref
ms.openlocfilehash: 3bfcb01e30b4cb33ec9276f1d3c6ac2f3bde4b58
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721759"
---
# <a name="iactiononclreventonevent-method"></a><span data-ttu-id="05360-102">IActionOnCLREvent::OnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="05360-102">IActionOnCLREvent::OnEvent Method</span></span>

<span data-ttu-id="05360-103">对已使用 [ICLROnEventManager：： RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) 方法的调用注册的事件执行回调。</span><span class="sxs-lookup"><span data-stu-id="05360-103">Performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05360-104">语法</span><span class="sxs-lookup"><span data-stu-id="05360-104">Syntax</span></span>  
  
```cpp  
HRESULT OnEvent (  
    [in] EClrEvent event,  
    [in] PVOID     data  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05360-105">参数</span><span class="sxs-lookup"><span data-stu-id="05360-105">Parameters</span></span>  

 `event`  
 <span data-ttu-id="05360-106">中 [EClrEvent](eclrevent-enumeration.md) 值之一，指示事件的类型。</span><span class="sxs-lookup"><span data-stu-id="05360-106">[in] One of the [EClrEvent](eclrevent-enumeration.md) values, which indicates the type of event.</span></span>  
  
 `data`  
 <span data-ttu-id="05360-107">中指向对象的指针，该对象包含有关的详细信息 `event` 。</span><span class="sxs-lookup"><span data-stu-id="05360-107">[in] A pointer to an object that contains details about `event`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="05360-108">返回值</span><span class="sxs-lookup"><span data-stu-id="05360-108">Return Value</span></span>  
  
|<span data-ttu-id="05360-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="05360-109">HRESULT</span></span>|<span data-ttu-id="05360-110">说明</span><span class="sxs-lookup"><span data-stu-id="05360-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="05360-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="05360-111">S_OK</span></span>|<span data-ttu-id="05360-112">`OnEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="05360-112">`OnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="05360-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="05360-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="05360-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="05360-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="05360-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="05360-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="05360-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="05360-116">The call timed out.</span></span>|  
|<span data-ttu-id="05360-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="05360-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="05360-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="05360-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="05360-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="05360-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="05360-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="05360-120">An event was cancelled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="05360-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="05360-121">E_FAIL</span></span>|<span data-ttu-id="05360-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="05360-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="05360-123">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="05360-123">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="05360-124">对任何宿主方法的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="05360-124">Subsequent calls to any hosting method return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="05360-125">注解</span><span class="sxs-lookup"><span data-stu-id="05360-125">Remarks</span></span>  

 <span data-ttu-id="05360-126">`data`参数是指向未指定类型的对象的指针。</span><span class="sxs-lookup"><span data-stu-id="05360-126">The `data` parameter is a pointer to an object of unspecified type.</span></span> <span data-ttu-id="05360-127">如果 `event` 参数为 `Event_DomainUnload` ， `data` 则是已卸载的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="05360-127">If the `event` parameter is `Event_DomainUnload`, `data` is the numeric identifier for the <xref:System.AppDomain> that was unloaded.</span></span> <span data-ttu-id="05360-128">主机可以使用此标识符作为键来执行适当的操作。</span><span class="sxs-lookup"><span data-stu-id="05360-128">The host can take appropriate action using this identifier as a key.</span></span>  
  
 <span data-ttu-id="05360-129">如果 `event` 为 `Event_MDAFired` ， `data` 则为指向 [MDAInfo](mdainfo-structure.md) 实例的指针，该实例包含从托管调试助手 (MDA) 的消息输出。</span><span class="sxs-lookup"><span data-stu-id="05360-129">If `event` is `Event_MDAFired`, `data` is a pointer to an [MDAInfo](mdainfo-structure.md) instance that contains the message output from a Managed Debugging Assistant (MDA).</span></span> <span data-ttu-id="05360-130">Mda 是 CLR 的一项功能，可帮助开发人员进行调试，方法是生成有关其他难以捕获的事件的 XML 消息。</span><span class="sxs-lookup"><span data-stu-id="05360-130">MDAs are a feature of the CLR that help developers with debugging, by generating XML messages about events that are otherwise difficult to trap.</span></span> <span data-ttu-id="05360-131">在调试托管代码和非托管代码之间的转换时，此类消息特别有用。</span><span class="sxs-lookup"><span data-stu-id="05360-131">Such messages can be especially useful in debugging transitions between managed and unmanaged code.</span></span> <span data-ttu-id="05360-132">有关详细信息，请参阅 [诊断托管调试助手的错误](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)。</span><span class="sxs-lookup"><span data-stu-id="05360-132">For more information, see [Diagnosing Errors with Managed Debugging Assistants](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05360-133">要求</span><span class="sxs-lookup"><span data-stu-id="05360-133">Requirements</span></span>  

 <span data-ttu-id="05360-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="05360-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05360-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="05360-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="05360-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="05360-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="05360-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05360-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05360-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05360-138">See also</span></span>

- [<span data-ttu-id="05360-139">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="05360-139">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="05360-140">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="05360-140">EClrEvent Enumeration</span></span>](eclrevent-enumeration.md)
- [<span data-ttu-id="05360-141">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="05360-141">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)
- [<span data-ttu-id="05360-142">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="05360-142">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="05360-143">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="05360-143">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)
- [<span data-ttu-id="05360-144">MDAInfo 结构</span><span class="sxs-lookup"><span data-stu-id="05360-144">MDAInfo Structure</span></span>](mdainfo-structure.md)
