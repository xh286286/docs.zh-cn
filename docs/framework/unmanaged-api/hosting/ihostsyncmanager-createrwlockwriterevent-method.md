---
title: IHostSyncManager::CreateRWLockWriterEvent 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateRWLockWriterEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateRWLockWriterEvent
helpviewer_keywords:
- CreateRWLockWriterEvent method [.NET Framework hosting]
- IHostSyncManager::CreateRWLockWriterEvent method [.NET Framework hosting]
ms.assetid: 70e488c2-cf53-4dc0-ba52-74372d215c41
topic_type:
- apiref
ms.openlocfilehash: 5b5faf14337f78d9b176787528ae8947f5810ba6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95704365"
---
# <a name="ihostsyncmanagercreaterwlockwriterevent-method"></a><span data-ttu-id="2c12f-102">IHostSyncManager::CreateRWLockWriterEvent 方法</span><span class="sxs-lookup"><span data-stu-id="2c12f-102">IHostSyncManager::CreateRWLockWriterEvent Method</span></span>

<span data-ttu-id="2c12f-103">创建自动重置事件对象，以便实现编写器锁。</span><span class="sxs-lookup"><span data-stu-id="2c12f-103">Creates an auto-reset event object for the implementation of a writer lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c12f-104">语法</span><span class="sxs-lookup"><span data-stu-id="2c12f-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateRWLockWriterEvent (  
    [in]  SIZE_T cookie,  
    [out] IHostAutoEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2c12f-105">参数</span><span class="sxs-lookup"><span data-stu-id="2c12f-105">Parameters</span></span>  

 `cookie`  
 <span data-ttu-id="2c12f-106">中与自动重置事件关联的 cookie。</span><span class="sxs-lookup"><span data-stu-id="2c12f-106">[in] A cookie to associate with the auto-reset event.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="2c12f-107">弄指向 [IHostAutoEvent](ihostautoevent-interface.md) 实例的地址的指针; 如果无法创建事件对象，则为 null。</span><span class="sxs-lookup"><span data-stu-id="2c12f-107">[out] A pointer to the address of an [IHostAutoEvent](ihostautoevent-interface.md) instance, or null if the event object could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2c12f-108">返回值</span><span class="sxs-lookup"><span data-stu-id="2c12f-108">Return Value</span></span>  
  
|<span data-ttu-id="2c12f-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2c12f-109">HRESULT</span></span>|<span data-ttu-id="2c12f-110">说明</span><span class="sxs-lookup"><span data-stu-id="2c12f-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2c12f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c12f-111">S_OK</span></span>|<span data-ttu-id="2c12f-112">`CreateRWLockWriterEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="2c12f-112">`CreateRWLockWriterEvent` returned successfully.</span></span>|  
|<span data-ttu-id="2c12f-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2c12f-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2c12f-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="2c12f-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2c12f-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2c12f-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2c12f-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="2c12f-116">The call timed out.</span></span>|  
|<span data-ttu-id="2c12f-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2c12f-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2c12f-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="2c12f-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2c12f-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2c12f-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2c12f-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="2c12f-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2c12f-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2c12f-121">E_FAIL</span></span>|<span data-ttu-id="2c12f-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="2c12f-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2c12f-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="2c12f-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2c12f-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="2c12f-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="2c12f-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="2c12f-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="2c12f-126">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="2c12f-126">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2c12f-127">注解</span><span class="sxs-lookup"><span data-stu-id="2c12f-127">Remarks</span></span>  

 <span data-ttu-id="2c12f-128">CLR 调用 `CreateRWLockWriterEvent` 方法来获取对实例的引用 `IHostAutoEvent` ，以便在它的编写器锁实现中使用。</span><span class="sxs-lookup"><span data-stu-id="2c12f-128">The CLR calls the `CreateRWLockWriterEvent` method to get a reference to an `IHostAutoEvent` instance to use in its implementation of a writer lock.</span></span> <span data-ttu-id="2c12f-129">主机可以通过调用 [ICLRSyncManager](iclrsyncmanager-interface.md) 接口的迭代方法，使用指定的 cookie 来确定哪些任务正在等待锁定。</span><span class="sxs-lookup"><span data-stu-id="2c12f-129">The host can use the specified cookie to determine which tasks are waiting on the lock by calling the iteration methods of the [ICLRSyncManager](iclrsyncmanager-interface.md) interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c12f-130">要求</span><span class="sxs-lookup"><span data-stu-id="2c12f-130">Requirements</span></span>  

 <span data-ttu-id="2c12f-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2c12f-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2c12f-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2c12f-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2c12f-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2c12f-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2c12f-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c12f-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c12f-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c12f-135">See also</span></span>

- [<span data-ttu-id="2c12f-136">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="2c12f-136">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="2c12f-137">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="2c12f-137">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="2c12f-138">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="2c12f-138">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="2c12f-139">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="2c12f-139">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
