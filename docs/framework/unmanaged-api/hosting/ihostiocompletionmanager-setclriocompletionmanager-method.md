---
title: IHostIoCompletionManager::SetCLRIoCompletionManager 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.SetCLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::SetCLRIoCompletionManager
helpviewer_keywords:
- IHostIoCompletionManager::SetCLRIoCompletionManager method [.NET Framework hosting]
- SetCLRIoCompletionManager method [.NET Framework hosting]
ms.assetid: 4254bb01-3a14-4f34-a3be-60ff1f5072b5
topic_type:
- apiref
ms.openlocfilehash: d370cc81942269bd79e06e0fa57fe5d79832b3c2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724840"
---
# <a name="ihostiocompletionmanagersetclriocompletionmanager-method"></a><span data-ttu-id="ac919-102">IHostIoCompletionManager::SetCLRIoCompletionManager 方法</span><span class="sxs-lookup"><span data-stu-id="ac919-102">IHostIoCompletionManager::SetCLRIoCompletionManager Method</span></span>

<span data-ttu-id="ac919-103">向宿主提供一个接口指针，该指针指向由公共语言运行时 (CLR) 实现的 [ICLRIoCompletionManager](iclriocompletionmanager-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="ac919-103">Provides the host with an interface pointer to the [ICLRIoCompletionManager](iclriocompletionmanager-interface.md) instance implemented by the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac919-104">语法</span><span class="sxs-lookup"><span data-stu-id="ac919-104">Syntax</span></span>  
  
```cpp  
HRESULT SetCLRIoCompletionManager (  
    [in] ICLRIoCompletionManager *pManager  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac919-105">参数</span><span class="sxs-lookup"><span data-stu-id="ac919-105">Parameters</span></span>  

 `pManager`  
 <span data-ttu-id="ac919-106">中CLR 提供的实例的接口指针 `ICLRIoCompletionManager` 。</span><span class="sxs-lookup"><span data-stu-id="ac919-106">[in] An interface pointer to an `ICLRIoCompletionManager` instance provided by the CLR.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ac919-107">返回值</span><span class="sxs-lookup"><span data-stu-id="ac919-107">Return Value</span></span>  
  
|<span data-ttu-id="ac919-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ac919-108">HRESULT</span></span>|<span data-ttu-id="ac919-109">说明</span><span class="sxs-lookup"><span data-stu-id="ac919-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ac919-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac919-110">S_OK</span></span>|<span data-ttu-id="ac919-111">`SetCLRIoCompletionManager` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ac919-111">`SetCLRIoCompletionManager` returned successfully.</span></span>|  
|<span data-ttu-id="ac919-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ac919-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ac919-113">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ac919-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ac919-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ac919-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ac919-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ac919-115">The call timed out.</span></span>|  
|<span data-ttu-id="ac919-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ac919-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ac919-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ac919-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ac919-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ac919-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ac919-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ac919-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ac919-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ac919-120">E_FAIL</span></span>|<span data-ttu-id="ac919-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ac919-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ac919-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ac919-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ac919-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ac919-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac919-124">注解</span><span class="sxs-lookup"><span data-stu-id="ac919-124">Remarks</span></span>  

 <span data-ttu-id="ac919-125">在 CLR 调用后 `SetCLRIoCompletionManager` ，主机必须调用 [ICLRIoCompletionManager：： OnComplete](iclriocompletionmanager-oncomplete-method.md) 以在 i/o 请求完成时通知 CLR。</span><span class="sxs-lookup"><span data-stu-id="ac919-125">After the CLR has called `SetCLRIoCompletionManager`, the host must call [ICLRIoCompletionManager::OnComplete](iclriocompletionmanager-oncomplete-method.md) to notify the CLR when an I/O request has been completed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac919-126">要求</span><span class="sxs-lookup"><span data-stu-id="ac919-126">Requirements</span></span>  

 <span data-ttu-id="ac919-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ac919-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac919-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ac919-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ac919-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ac919-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ac919-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac919-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac919-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ac919-131">See also</span></span>

- [<span data-ttu-id="ac919-132">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="ac919-132">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="ac919-133">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="ac919-133">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
