---
title: IHostSyncManager 接口
ms.date: 03/30/2017
api_name:
- IHostSyncManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager
helpviewer_keywords:
- IHostSyncManager interface [.NET Framework hosting]
ms.assetid: 2e081a37-6a28-4c93-b7ab-1c96a464637c
topic_type:
- apiref
ms.openlocfilehash: 8a5fc42191634a2e5a441baecc4b78212ffad687
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720485"
---
# <a name="ihostsyncmanager-interface"></a><span data-ttu-id="320d5-102">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="320d5-102">IHostSyncManager Interface</span></span>

<span data-ttu-id="320d5-103">提供一些方法，使公共语言运行时 (CLR) 通过调用主机而不是使用 Win32 同步函数来创建同步基元。</span><span class="sxs-lookup"><span data-stu-id="320d5-103">Provides methods that allow the common language runtime (CLR) to create synchronization primitives by calling the host instead of using the Win32 synchronization functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="320d5-104">方法</span><span class="sxs-lookup"><span data-stu-id="320d5-104">Methods</span></span>  
  
|<span data-ttu-id="320d5-105">方法</span><span class="sxs-lookup"><span data-stu-id="320d5-105">Method</span></span>|<span data-ttu-id="320d5-106">说明</span><span class="sxs-lookup"><span data-stu-id="320d5-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="320d5-107">CreateAutoEvent 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-107">CreateAutoEvent Method</span></span>](ihostsyncmanager-createautoevent-method.md)|<span data-ttu-id="320d5-108">创建自动重置事件对象。</span><span class="sxs-lookup"><span data-stu-id="320d5-108">Creates an auto-reset event object.</span></span>|  
|[<span data-ttu-id="320d5-109">CreateCrst 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-109">CreateCrst Method</span></span>](ihostsyncmanager-createcrst-method.md)|<span data-ttu-id="320d5-110">创建用于同步的临界区对象。</span><span class="sxs-lookup"><span data-stu-id="320d5-110">Creates a critical section object for synchronization.</span></span>|  
|[<span data-ttu-id="320d5-111">CreateCrstWithSpinCount 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-111">CreateCrstWithSpinCount Method</span></span>](ihostsyncmanager-createcrstwithspincount-method.md)|<span data-ttu-id="320d5-112">使用自旋计数为同步创建一个临界区对象。</span><span class="sxs-lookup"><span data-stu-id="320d5-112">Creates a critical section object with spin count for synchronization.</span></span>|  
|[<span data-ttu-id="320d5-113">CreateManualEvent 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-113">CreateManualEvent Method</span></span>](ihostsyncmanager-createmanualevent-method.md)|<span data-ttu-id="320d5-114">创建手动重置的事件对象。</span><span class="sxs-lookup"><span data-stu-id="320d5-114">Creates a manual-reset event object.</span></span>|  
|[<span data-ttu-id="320d5-115">CreateMonitorEvent 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-115">CreateMonitorEvent Method</span></span>](ihostsyncmanager-createmonitorevent-method.md)|<span data-ttu-id="320d5-116">创建监视的自动重置事件对象。</span><span class="sxs-lookup"><span data-stu-id="320d5-116">Creates a monitored auto-reset event object.</span></span>|  
|[<span data-ttu-id="320d5-117">CreateRWLockReaderEvent 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-117">CreateRWLockReaderEvent Method</span></span>](ihostsyncmanager-createrwlockreaderevent-method.md)|<span data-ttu-id="320d5-118">创建手动重置的事件对象，以便实现读取器锁。</span><span class="sxs-lookup"><span data-stu-id="320d5-118">Creates a manual-reset event object for the implementation of a reader lock.</span></span>|  
|[<span data-ttu-id="320d5-119">CreateRWLockWriterEvent 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-119">CreateRWLockWriterEvent Method</span></span>](ihostsyncmanager-createrwlockwriterevent-method.md)|<span data-ttu-id="320d5-120">创建自动重置事件对象，以便实现编写器锁。</span><span class="sxs-lookup"><span data-stu-id="320d5-120">Creates an auto-reset event object for the implementation of a writer lock.</span></span>|  
|[<span data-ttu-id="320d5-121">CreateSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-121">CreateSemaphore Method</span></span>](ihostsyncmanager-createsemaphore-method.md)|<span data-ttu-id="320d5-122">为 CLR 创建一个 [IHostSemaphore](ihostsemaphore-interface.md) 对象，以用作等待事件的信号量。</span><span class="sxs-lookup"><span data-stu-id="320d5-122">Creates an [IHostSemaphore](ihostsemaphore-interface.md) object for the CLR to use as a semaphore for wait events.</span></span>|  
|[<span data-ttu-id="320d5-123">SetCLRSyncManager 方法</span><span class="sxs-lookup"><span data-stu-id="320d5-123">SetCLRSyncManager Method</span></span>](ihostsyncmanager-setclrsyncmanager-method.md)|<span data-ttu-id="320d5-124">设置要与当前实例关联的 [ICLRSyncManager](iclrsyncmanager-interface.md) 实例 `IHostSyncManager` 。</span><span class="sxs-lookup"><span data-stu-id="320d5-124">Sets the [ICLRSyncManager](iclrsyncmanager-interface.md) instance to associate with the current `IHostSyncManager` instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="320d5-125">注解</span><span class="sxs-lookup"><span data-stu-id="320d5-125">Remarks</span></span>  

 <span data-ttu-id="320d5-126">CLR `IHostSyncManager` 通过使用 IID_IHostSyncManager 的调用 [IHostControl：： GetHostManager](ihostcontrol-gethostmanager-method.md) 方法来发现主机的实现 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="320d5-126">The CLR discovers the host's implementation of `IHostSyncManager` by calling the [IHostControl::GetHostManager](ihostcontrol-gethostmanager-method.md) method with an `IID` of IID_IHostSyncManager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="320d5-127">要求</span><span class="sxs-lookup"><span data-stu-id="320d5-127">Requirements</span></span>  

 <span data-ttu-id="320d5-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="320d5-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="320d5-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="320d5-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="320d5-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="320d5-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="320d5-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="320d5-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="320d5-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="320d5-132">See also</span></span>

- [<span data-ttu-id="320d5-133">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="320d5-133">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="320d5-134">承载接口</span><span class="sxs-lookup"><span data-stu-id="320d5-134">Hosting Interfaces</span></span>](hosting-interfaces.md)
