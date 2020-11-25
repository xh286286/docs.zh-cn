---
title: ICLRRuntimeHost::ExecuteInAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteInAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteInAppDomain
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteInAppDomain method [.NET Framework hosting]
- ExecuteInAppDomain method [.NET Framework hosting]
ms.assetid: e2b0e2db-3fae-4b56-844e-d30a125a660c
topic_type:
- apiref
ms.openlocfilehash: 4c28c4a5cc64b20c9ac9c57e1aef5e7b90a20e01
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728883"
---
# <a name="iclrruntimehostexecuteinappdomain-method"></a><span data-ttu-id="b3531-102">ICLRRuntimeHost::ExecuteInAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="b3531-102">ICLRRuntimeHost::ExecuteInAppDomain Method</span></span>

<span data-ttu-id="b3531-103">指定 <xref:System.AppDomain> 要在其中执行指定的托管代码的。</span><span class="sxs-lookup"><span data-stu-id="b3531-103">Specifies the <xref:System.AppDomain> in which to execute the specified managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3531-104">语法</span><span class="sxs-lookup"><span data-stu-id="b3531-104">Syntax</span></span>  
  
```cpp  
HRESULT ExecuteInAppDomain(  
    [in] DWORD AppDomainId,
    [in] FExecuteInDomainCallback pCallback,
    [in] void* cookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b3531-105">参数</span><span class="sxs-lookup"><span data-stu-id="b3531-105">Parameters</span></span>  

 `AppDomainId`  
 <span data-ttu-id="b3531-106">中 <xref:System.AppDomain> 要在其中执行指定方法的的数值 ID。</span><span class="sxs-lookup"><span data-stu-id="b3531-106">[in] The numeric ID of the <xref:System.AppDomain> in which to execute the specified method.</span></span>  
  
 `pCallback`  
 <span data-ttu-id="b3531-107">中指向函数的指针，该函数在指定的中执行 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="b3531-107">[in] A pointer to the function to execute within the specified <xref:System.AppDomain>.</span></span>  
  
 `cookie`  
 <span data-ttu-id="b3531-108">中指向不透明调用方分配的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="b3531-108">[in] A pointer to opaque caller-allocated memory.</span></span> <span data-ttu-id="b3531-109">此参数由公共语言运行时 (CLR) 传递到域回调。</span><span class="sxs-lookup"><span data-stu-id="b3531-109">This parameter is passed by the common language runtime (CLR) to the domain callback.</span></span> <span data-ttu-id="b3531-110">它不是运行时托管堆内存;此内存的分配和生存期均由调用方控制。</span><span class="sxs-lookup"><span data-stu-id="b3531-110">It is not runtime-managed heap memory; both the allocation and lifetime of this memory are controlled by the caller.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b3531-111">返回值</span><span class="sxs-lookup"><span data-stu-id="b3531-111">Return Value</span></span>  
  
|<span data-ttu-id="b3531-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b3531-112">HRESULT</span></span>|<span data-ttu-id="b3531-113">说明</span><span class="sxs-lookup"><span data-stu-id="b3531-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b3531-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3531-114">S_OK</span></span>|<span data-ttu-id="b3531-115">`ExecuteInAppDomain` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b3531-115">`ExecuteInAppDomain` returned successfully.</span></span>|  
|<span data-ttu-id="b3531-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b3531-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b3531-117">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b3531-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b3531-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b3531-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b3531-119">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b3531-119">The call timed out.</span></span>|  
|<span data-ttu-id="b3531-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3531-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b3531-121">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b3531-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b3531-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b3531-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b3531-123">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b3531-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b3531-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b3531-124">E_FAIL</span></span>|<span data-ttu-id="b3531-125">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b3531-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b3531-126">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b3531-126">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b3531-127">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b3531-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3531-128">注解</span><span class="sxs-lookup"><span data-stu-id="b3531-128">Remarks</span></span>  

 <span data-ttu-id="b3531-129">`ExecuteInAppDomain` 允许主机控制 <xref:System.AppDomain> 应在其上执行指定托管方法的管理。</span><span class="sxs-lookup"><span data-stu-id="b3531-129">`ExecuteInAppDomain` allows the host to exercise control over which managed <xref:System.AppDomain> the specified managed method should be executed in.</span></span> <span data-ttu-id="b3531-130">可以 <xref:System.AppDomain.Id%2A> 通过调用 [GetCurrentAppDomainId 方法](iclrruntimehost-getcurrentappdomainid-method.md)，获取与属性的值相对应的应用程序域标识符的值。</span><span class="sxs-lookup"><span data-stu-id="b3531-130">You can get the value of an application domain's identifier, which corresponds to the value of the <xref:System.AppDomain.Id%2A> property, by calling [GetCurrentAppDomainId Method](iclrruntimehost-getcurrentappdomainid-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3531-131">要求</span><span class="sxs-lookup"><span data-stu-id="b3531-131">Requirements</span></span>  

 <span data-ttu-id="b3531-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b3531-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3531-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b3531-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b3531-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b3531-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b3531-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3531-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3531-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b3531-136">See also</span></span>

- [<span data-ttu-id="b3531-137">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="b3531-137">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
