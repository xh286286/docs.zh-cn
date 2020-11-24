---
title: IHostTaskManager 接口
ms.date: 03/30/2017
api_name:
- IHostTaskManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager
helpviewer_keywords:
- IHostTaskManager interface [.NET Framework hosting]
ms.assetid: 4a0b05b9-3ef1-4607-b7c8-bd4dd43647a0
topic_type:
- apiref
ms.openlocfilehash: deb14d291bfd511e8f3534f3c5e32787c259c5e8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95673106"
---
# <a name="ihosttaskmanager-interface"></a><span data-ttu-id="5bfee-102">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="5bfee-102">IHostTaskManager Interface</span></span>

<span data-ttu-id="5bfee-103">提供一些方法，使公共语言运行时 (CLR) 可以通过主机使用任务，而不是使用标准操作系统线程处理或纤程函数。</span><span class="sxs-lookup"><span data-stu-id="5bfee-103">Provides methods that allow the common language runtime (CLR) to work with tasks through the host instead of using the standard operating system threading or fiber functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5bfee-104">方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-104">Methods</span></span>  
  
|<span data-ttu-id="5bfee-105">方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-105">Method</span></span>|<span data-ttu-id="5bfee-106">说明</span><span class="sxs-lookup"><span data-stu-id="5bfee-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5bfee-107">BeginDelayAbort 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-107">BeginDelayAbort Method</span></span>](ihosttaskmanager-begindelayabort-method.md)|<span data-ttu-id="5bfee-108">通知宿主托管代码输入的时间段不得中止当前任务。</span><span class="sxs-lookup"><span data-stu-id="5bfee-108">Notifies the host that managed code is entering a period in which the current task must not be aborted.</span></span>|  
|[<span data-ttu-id="5bfee-109">BeginThreadAffinity 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-109">BeginThreadAffinity Method</span></span>](ihosttaskmanager-beginthreadaffinity-method.md)|<span data-ttu-id="5bfee-110">通知宿主托管代码正在输入一个时间段，在此期间，不能将当前任务移动到另一个操作系统线程。</span><span class="sxs-lookup"><span data-stu-id="5bfee-110">Notifies the host that managed code is entering a period in which the current task must not be moved to another operating system thread.</span></span>|  
|[<span data-ttu-id="5bfee-111">CallNeedsHostHook 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-111">CallNeedsHostHook Method</span></span>](ihosttaskmanager-callneedshosthook-method.md)|<span data-ttu-id="5bfee-112">使宿主能够指定公共语言运行时是否可将指定的调用内联到非托管函数。</span><span class="sxs-lookup"><span data-stu-id="5bfee-112">Enables the host to specify whether the common language runtime can inline the specified call to an unmanaged function.</span></span>|  
|[<span data-ttu-id="5bfee-113">CreateTask 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-113">CreateTask Method</span></span>](ihosttaskmanager-createtask-method.md)|<span data-ttu-id="5bfee-114">请求宿主创建新任务。</span><span class="sxs-lookup"><span data-stu-id="5bfee-114">Requests that the host create a new task.</span></span>|  
|[<span data-ttu-id="5bfee-115">EndDelayAbort 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-115">EndDelayAbort Method</span></span>](ihosttaskmanager-enddelayabort-method.md)|<span data-ttu-id="5bfee-116">向宿主通知托管代码，在之前对的调用之后不得中止当前任务 `BeginDelayAbort` 。</span><span class="sxs-lookup"><span data-stu-id="5bfee-116">Notifies the host that managed code is exiting the period in which the current task must not be aborted, following an earlier call to `BeginDelayAbort`.</span></span>|  
|[<span data-ttu-id="5bfee-117">EndThreadAffinity 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-117">EndThreadAffinity Method</span></span>](ihosttaskmanager-endthreadaffinity-method.md)|<span data-ttu-id="5bfee-118">向宿主通知托管代码，即在之前对的调用之后，不能将当前任务移到另一个操作系统线程 `BeginThreadAffinity` 。</span><span class="sxs-lookup"><span data-stu-id="5bfee-118">Notifies the host that managed code is exiting the period in which the current task must not be moved to another operating system thread, following an earlier call to `BeginThreadAffinity`.</span></span>|  
|[<span data-ttu-id="5bfee-119">EnterRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-119">EnterRuntime Method</span></span>](ihosttaskmanager-enterruntime-method.md)|<span data-ttu-id="5bfee-120">通知宿主对非托管方法的调用（如平台调用方法）正在将执行控制返回到 CLR。</span><span class="sxs-lookup"><span data-stu-id="5bfee-120">Notifies the host that a call to an unmanaged method, such as a platform invoke method, is returning execution control to the CLR.</span></span>|  
|[<span data-ttu-id="5bfee-121">GetCurrentTask 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-121">GetCurrentTask Method</span></span>](ihosttaskmanager-getcurrenttask-method.md)|<span data-ttu-id="5bfee-122">获取一个接口指针，该指针指向正在进行此调用的操作系统线程上当前正在执行的任务。</span><span class="sxs-lookup"><span data-stu-id="5bfee-122">Gets an interface pointer to the task that is currently executing on the operating system thread from which this call is made.</span></span>|  
|[<span data-ttu-id="5bfee-123">GetStackGuarantee 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-123">GetStackGuarantee Method</span></span>](ihosttaskmanager-getstackguarantee-method.md)|<span data-ttu-id="5bfee-124">获取在堆栈操作完成之后但在关闭进程之前保证可用的堆栈空间量。</span><span class="sxs-lookup"><span data-stu-id="5bfee-124">Gets the amount of stack space that is guaranteed to be available after a stack operation completes, but before the closing of a process.</span></span>|  
|[<span data-ttu-id="5bfee-125">LeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-125">LeaveRuntime Method</span></span>](ihosttaskmanager-leaveruntime-method.md)|<span data-ttu-id="5bfee-126">通知宿主托管代码将要对非托管函数进行调用。</span><span class="sxs-lookup"><span data-stu-id="5bfee-126">Notifies the host that managed code is about to make a call to an unmanaged function.</span></span>|  
|[<span data-ttu-id="5bfee-127">ReverseEnterRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-127">ReverseEnterRuntime Method</span></span>](ihosttaskmanager-reverseenterruntime-method.md)|<span data-ttu-id="5bfee-128">通知宿主从非托管代码向公共语言运行时 (CLR) 发出调用。</span><span class="sxs-lookup"><span data-stu-id="5bfee-128">Notifies the host that a call is being made into the common language runtime (CLR) from unmanaged code.</span></span>|  
|[<span data-ttu-id="5bfee-129">ReverseLeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-129">ReverseLeaveRuntime Method</span></span>](ihosttaskmanager-reverseleaveruntime-method.md)|<span data-ttu-id="5bfee-130">通知宿主控件离开 CLR，并进入从托管代码调用的非托管函数。</span><span class="sxs-lookup"><span data-stu-id="5bfee-130">Notifies the host that control is leaving the CLR and entering an unmanaged function that was, in turn, called from managed code.</span></span>|  
|[<span data-ttu-id="5bfee-131">SetCLRTaskManager 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-131">SetCLRTaskManager Method</span></span>](ihosttaskmanager-setclrtaskmanager-method.md)|<span data-ttu-id="5bfee-132">向宿主提供一个接口指针，该指针指向 CLR 实现的 [ICLRTaskManager](iclrtaskmanager-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="5bfee-132">Provides the host with an interface pointer to an [ICLRTaskManager](iclrtaskmanager-interface.md) instance implemented by the CLR.</span></span>|  
|[<span data-ttu-id="5bfee-133">SetLocale 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-133">SetLocale Method</span></span>](ihosttaskmanager-setlocale-method.md)|<span data-ttu-id="5bfee-134">通知宿主 CLR 已更改当前任务的区域设置。</span><span class="sxs-lookup"><span data-stu-id="5bfee-134">Notifies the host that the CLR has changed the locale on the current task.</span></span>|  
|[<span data-ttu-id="5bfee-135">SetStackGuarantee 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-135">SetStackGuarantee Method</span></span>](ihosttaskmanager-setstackguarantee-method.md)|<span data-ttu-id="5bfee-136">保留以仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="5bfee-136">Reserved for internal use only.</span></span>|  
|[<span data-ttu-id="5bfee-137">SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-137">SetUILocale Method</span></span>](ihosttaskmanager-setuilocale-method.md)|<span data-ttu-id="5bfee-138">通知宿主用户界面区域设置在当前任务上已更改。</span><span class="sxs-lookup"><span data-stu-id="5bfee-138">Notifies the host that the user interface locale has been changed on the current task.</span></span>|  
|[<span data-ttu-id="5bfee-139">Sleep 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-139">Sleep Method</span></span>](ihosttaskmanager-sleep-method.md)|<span data-ttu-id="5bfee-140">通知宿主当前任务将要进入睡眠状态。</span><span class="sxs-lookup"><span data-stu-id="5bfee-140">Notifies the host that the current task is going to sleep.</span></span>|  
|[<span data-ttu-id="5bfee-141">SwitchToTask 方法</span><span class="sxs-lookup"><span data-stu-id="5bfee-141">SwitchToTask Method</span></span>](ihosttaskmanager-switchtotask-method.md)|<span data-ttu-id="5bfee-142">通知宿主应切换到当前任务。</span><span class="sxs-lookup"><span data-stu-id="5bfee-142">Notifies the host that it should switch out the current task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5bfee-143">注解</span><span class="sxs-lookup"><span data-stu-id="5bfee-143">Remarks</span></span>  

 <span data-ttu-id="5bfee-144">`IHostTaskManager` 允许 CLR 创建和管理任务，以便在控制从托管到非托管代码的传输时，为宿主提供挂钩，并指定在代码执行期间宿主可以和不能执行的某些操作。</span><span class="sxs-lookup"><span data-stu-id="5bfee-144">`IHostTaskManager` allows the CLR to create and manage tasks, to provide hooks for the host to take action when control transfers from managed to unmanaged code and vice versa, and to specify certain actions the host can and cannot take during code execution.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bfee-145">要求</span><span class="sxs-lookup"><span data-stu-id="5bfee-145">Requirements</span></span>  

 <span data-ttu-id="5bfee-146">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5bfee-146">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bfee-147">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5bfee-147">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5bfee-148">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5bfee-148">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5bfee-149">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bfee-149">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bfee-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5bfee-150">See also</span></span>

- [<span data-ttu-id="5bfee-151">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="5bfee-151">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="5bfee-152">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="5bfee-152">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="5bfee-153">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="5bfee-153">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="5bfee-154">承载接口</span><span class="sxs-lookup"><span data-stu-id="5bfee-154">Hosting Interfaces</span></span>](hosting-interfaces.md)
