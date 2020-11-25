---
title: ICLRMemoryNotificationCallback::OnMemoryNotification 方法
ms.date: 03/30/2017
api_name:
- ICLRMemoryNotificationCallback.OnMemoryNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMemoryNotificationCallback::OnMemoryNotification
helpviewer_keywords:
- ICLRMemoryNotificationCallback::OnMemoryNotification method [.NET Framework hosting]
- OnMemoryNotification method [.NET Framework hosting]
ms.assetid: 5612a44d-56cc-4f34-af31-8c9809ba9431
topic_type:
- apiref
ms.openlocfilehash: f9b2715801ebcaff3d97962540a4b1b103bbd53b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730461"
---
# <a name="iclrmemorynotificationcallbackonmemorynotification-method"></a><span data-ttu-id="83965-102">ICLRMemoryNotificationCallback::OnMemoryNotification 方法</span><span class="sxs-lookup"><span data-stu-id="83965-102">ICLRMemoryNotificationCallback::OnMemoryNotification Method</span></span>

<span data-ttu-id="83965-103"> (CLR) 计算机上的内存负载通知公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="83965-103">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83965-104">语法</span><span class="sxs-lookup"><span data-stu-id="83965-104">Syntax</span></span>  
  
```cpp  
HRESULT OnMemoryNotification (  
    [in] EMemoryAvailable eMemoryAvailable  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="83965-105">参数</span><span class="sxs-lookup"><span data-stu-id="83965-105">Parameters</span></span>  

 `eMemoryAvailable`  
 <span data-ttu-id="83965-106">中 [EMemoryAvailable](ememoryavailable-enumeration.md) 值之一，指示计算机当前遇到的内存压力。</span><span class="sxs-lookup"><span data-stu-id="83965-106">[in] One of the [EMemoryAvailable](ememoryavailable-enumeration.md) values, indicating the memory pressure the computer is currently experiencing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="83965-107">返回值</span><span class="sxs-lookup"><span data-stu-id="83965-107">Return Value</span></span>  
  
|<span data-ttu-id="83965-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="83965-108">HRESULT</span></span>|<span data-ttu-id="83965-109">说明</span><span class="sxs-lookup"><span data-stu-id="83965-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="83965-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="83965-110">S_OK</span></span>|<span data-ttu-id="83965-111">`OnMemoryNotification` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="83965-111">`OnMemoryNotification` returned successfully.</span></span>|  
|<span data-ttu-id="83965-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="83965-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="83965-113">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="83965-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="83965-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="83965-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="83965-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="83965-115">The call timed out.</span></span>|  
|<span data-ttu-id="83965-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="83965-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="83965-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="83965-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="83965-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="83965-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="83965-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="83965-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="83965-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="83965-120">E_FAIL</span></span>|<span data-ttu-id="83965-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="83965-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="83965-122">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="83965-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="83965-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="83965-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83965-124">注解</span><span class="sxs-lookup"><span data-stu-id="83965-124">Remarks</span></span>  

 <span data-ttu-id="83965-125">CLR `OnMemoryNotification` 使用对 [IHostMemoryManager：： RegisterMemoryNotificationCallback](ihostmemorymanager-registermemorynotificationcallback-method.md) 方法的调用向注册回调。</span><span class="sxs-lookup"><span data-stu-id="83965-125">The CLR registers a callback to `OnMemoryNotification` by using a call to the [IHostMemoryManager::RegisterMemoryNotificationCallback](ihostmemorymanager-registermemorynotificationcallback-method.md) method.</span></span> <span data-ttu-id="83965-126">当主机报告内存资源不足时，运行时将使用在回调中返回的信息来释放额外内存。</span><span class="sxs-lookup"><span data-stu-id="83965-126">The runtime uses the information returned in the callback to free additional memory when the host reports that memory resources are running low.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="83965-127">对 `OnMemoryNotification` 从不阻止的的调用。</span><span class="sxs-lookup"><span data-stu-id="83965-127">Calls to `OnMemoryNotification` never block.</span></span> <span data-ttu-id="83965-128">它们始终立即返回。</span><span class="sxs-lookup"><span data-stu-id="83965-128">They always return immediately.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83965-129">要求</span><span class="sxs-lookup"><span data-stu-id="83965-129">Requirements</span></span>  

 <span data-ttu-id="83965-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="83965-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83965-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="83965-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="83965-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="83965-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="83965-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83965-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83965-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83965-134">See also</span></span>

- [<span data-ttu-id="83965-135">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="83965-135">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="83965-136">RegisterMemoryNotificationCallback 方法</span><span class="sxs-lookup"><span data-stu-id="83965-136">RegisterMemoryNotificationCallback Method</span></span>](ihostmemorymanager-registermemorynotificationcallback-method.md)
- [<span data-ttu-id="83965-137">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="83965-137">ICLRMemoryNotificationCallback Interface</span></span>](iclrmemorynotificationcallback-interface.md)
