---
title: ICLRPolicyManager::SetUnhandledExceptionPolicy 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetUnhandledExceptionPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetUnhandledExceptionPolicy
helpviewer_keywords:
- ICLRPolicyManager::SetUnhandledExceptionPolicy method [.NET Framework hosting]
- SetUnhandledExceptionPolicy method [.NET Framework hosting]
ms.assetid: 5268480e-280a-4931-b7a3-dc3ffdf7f78f
topic_type:
- apiref
ms.openlocfilehash: 1088374c9df18ded38b44384be44de245f0bd403
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728948"
---
# <a name="iclrpolicymanagersetunhandledexceptionpolicy-method"></a><span data-ttu-id="da9ca-102">ICLRPolicyManager::SetUnhandledExceptionPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="da9ca-102">ICLRPolicyManager::SetUnhandledExceptionPolicy Method</span></span>

<span data-ttu-id="da9ca-103">指定在发生未经处理的异常时公共语言运行时 (CLR) 的行为。</span><span class="sxs-lookup"><span data-stu-id="da9ca-103">Specifies the behavior of the common language runtime (CLR) when an unhandled exception occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da9ca-104">语法</span><span class="sxs-lookup"><span data-stu-id="da9ca-104">Syntax</span></span>  
  
```cpp  
HRESULT SetUnhandledExceptionPolicy (  
    [in] EClrUnhandledExceptionPolicy policy  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="da9ca-105">参数</span><span class="sxs-lookup"><span data-stu-id="da9ca-105">Parameters</span></span>  

 `policy`  
 <span data-ttu-id="da9ca-106">中 [EClrUnhandledException](eclrunhandledexception-enumeration.md) 值之一，指示行为是由 CLR 还是宿主设置。</span><span class="sxs-lookup"><span data-stu-id="da9ca-106">[in] One of the [EClrUnhandledException](eclrunhandledexception-enumeration.md) values, indicating whether the behavior is set by the CLR or the host.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="da9ca-107">返回值</span><span class="sxs-lookup"><span data-stu-id="da9ca-107">Return Value</span></span>  
  
|<span data-ttu-id="da9ca-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="da9ca-108">HRESULT</span></span>|<span data-ttu-id="da9ca-109">说明</span><span class="sxs-lookup"><span data-stu-id="da9ca-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="da9ca-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="da9ca-110">S_OK</span></span>|<span data-ttu-id="da9ca-111">`SetUnhandledExceptionPolicy` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="da9ca-111">`SetUnhandledExceptionPolicy` returned successfully.</span></span>|  
|<span data-ttu-id="da9ca-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="da9ca-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="da9ca-113">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="da9ca-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="da9ca-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="da9ca-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="da9ca-115">调用超时。</span><span class="sxs-lookup"><span data-stu-id="da9ca-115">The call timed out.</span></span>|  
|<span data-ttu-id="da9ca-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="da9ca-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="da9ca-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="da9ca-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="da9ca-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="da9ca-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="da9ca-119">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="da9ca-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="da9ca-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="da9ca-120">E_FAIL</span></span>|<span data-ttu-id="da9ca-121">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="da9ca-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="da9ca-122">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="da9ca-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="da9ca-123">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="da9ca-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="da9ca-124">注解</span><span class="sxs-lookup"><span data-stu-id="da9ca-124">Remarks</span></span>  

 <span data-ttu-id="da9ca-125">默认情况下，CLR 是所有未经处理的异常的最终处理程序，其默认行为是销毁进程。</span><span class="sxs-lookup"><span data-stu-id="da9ca-125">By default, the CLR is the final handler for all unhandled exceptions, and its default behavior is to tear down the process.</span></span> <span data-ttu-id="da9ca-126">宿主可以通过将值设置为 eHostDeterminedPolicy 来更改此行为 `policy` 。</span><span class="sxs-lookup"><span data-stu-id="da9ca-126">The host can change this behavior by setting the `policy` value to eHostDeterminedPolicy.</span></span> <span data-ttu-id="da9ca-127">与早期版本的 CLR 一样，此值允许主机实现其自己的默认行为。</span><span class="sxs-lookup"><span data-stu-id="da9ca-127">This value allows the host to implement its own default behavior, as with earlier versions of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da9ca-128">要求</span><span class="sxs-lookup"><span data-stu-id="da9ca-128">Requirements</span></span>  

 <span data-ttu-id="da9ca-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="da9ca-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da9ca-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="da9ca-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="da9ca-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="da9ca-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="da9ca-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da9ca-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da9ca-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da9ca-133">See also</span></span>

- [<span data-ttu-id="da9ca-134">EClrUnhandledException 枚举</span><span class="sxs-lookup"><span data-stu-id="da9ca-134">EClrUnhandledException Enumeration</span></span>](eclrunhandledexception-enumeration.md)
- [<span data-ttu-id="da9ca-135">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="da9ca-135">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="da9ca-136">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="da9ca-136">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="da9ca-137">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="da9ca-137">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
