---
title: IHostIoCompletionManager::CreateIoCompletionPort 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.CreateIoCompletionPort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort
helpviewer_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort method [.NET Framework hosting]
- CreateIoCompletionPort method [.NET Framework hosting]
ms.assetid: 907a2b43-68db-44a7-acac-89e792e7bb3c
topic_type:
- apiref
ms.openlocfilehash: 0c74e073d55ab7dc98620052a0cfd68c294f7a1c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724268"
---
# <a name="ihostiocompletionmanagercreateiocompletionport-method"></a><span data-ttu-id="35aea-102">IHostIoCompletionManager::CreateIoCompletionPort 方法</span><span class="sxs-lookup"><span data-stu-id="35aea-102">IHostIoCompletionManager::CreateIoCompletionPort Method</span></span>

<span data-ttu-id="35aea-103">请求宿主创建新的 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="35aea-103">Requests that the host create a new I/O completion port.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35aea-104">语法</span><span class="sxs-lookup"><span data-stu-id="35aea-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateIoCompletionPort (  
    [out] HANDLE *phPort  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="35aea-105">参数</span><span class="sxs-lookup"><span data-stu-id="35aea-105">Parameters</span></span>  

 `phPort`  
 <span data-ttu-id="35aea-106">弄指向新创建的 i/o 完成端口的句柄的指针; 如果无法创建端口，则为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="35aea-106">[out] A pointer to a handle to the newly created I/O completion port, or 0 (zero), if the port could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="35aea-107">返回值</span><span class="sxs-lookup"><span data-stu-id="35aea-107">Return Value</span></span>  
  
|<span data-ttu-id="35aea-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="35aea-108">HRESULT</span></span>|<span data-ttu-id="35aea-109">说明</span><span class="sxs-lookup"><span data-stu-id="35aea-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="35aea-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="35aea-110">S_OK</span></span>|<span data-ttu-id="35aea-111">`CreateIoCompletionPort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="35aea-111">`CreateIoCompletionPort` returned successfully.</span></span>|  
|<span data-ttu-id="35aea-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="35aea-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="35aea-113"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="35aea-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="35aea-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="35aea-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="35aea-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="35aea-115">The call timed out.</span></span>|  
|<span data-ttu-id="35aea-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="35aea-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="35aea-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="35aea-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="35aea-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="35aea-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="35aea-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="35aea-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="35aea-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="35aea-120">E_FAIL</span></span>|<span data-ttu-id="35aea-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="35aea-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="35aea-122">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="35aea-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="35aea-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="35aea-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="35aea-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="35aea-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="35aea-125">没有足够的内存可用于分配请求的资源。</span><span class="sxs-lookup"><span data-stu-id="35aea-125">Not enough memory was available to allocate the requested resource.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="35aea-126">注解</span><span class="sxs-lookup"><span data-stu-id="35aea-126">Remarks</span></span>  

 <span data-ttu-id="35aea-127">CLR 调用 `CreateIoCompletionPort` 方法来请求宿主创建新的 i/o 完成端口。</span><span class="sxs-lookup"><span data-stu-id="35aea-127">The CLR calls the `CreateIoCompletionPort` method to request that the host create a new I/O completion port.</span></span> <span data-ttu-id="35aea-128">它通过调用 [IHostIoCompletionManager：： Bind](ihostiocompletionmanager-bind-method.md) 方法将 i/o 操作绑定到此端口。</span><span class="sxs-lookup"><span data-stu-id="35aea-128">It binds I/O operations to this port through a call to the [IHostIoCompletionManager::Bind](ihostiocompletionmanager-bind-method.md) method.</span></span> <span data-ttu-id="35aea-129">主机通过调用 [ICLRIoCompletionManager：： OnComplete](iclriocompletionmanager-oncomplete-method.md)将状态报告回 CLR。</span><span class="sxs-lookup"><span data-stu-id="35aea-129">The host reports status back to the CLR by calling [ICLRIoCompletionManager::OnComplete](iclriocompletionmanager-oncomplete-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35aea-130">要求</span><span class="sxs-lookup"><span data-stu-id="35aea-130">Requirements</span></span>  

 <span data-ttu-id="35aea-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="35aea-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35aea-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="35aea-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="35aea-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="35aea-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="35aea-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35aea-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35aea-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35aea-135">See also</span></span>

- [<span data-ttu-id="35aea-136">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="35aea-136">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="35aea-137">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="35aea-137">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
