---
title: ICLRHostBindingPolicyManager::ModifyApplicationPolicy 方法
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager.ModifyApplicationPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager::ModifyApplicationPolicy
helpviewer_keywords:
- ICLRHostBindingPolicyManager::ModifyApplicationPolicy method [.NET Framework hosting]
- ModifyApplicationPolicy method [.NET Framework hosting]
ms.assetid: d82d633e-cce6-427c-8b02-8227e34e12ba
topic_type:
- apiref
ms.openlocfilehash: 8da9c9fea5cf5b3a27eeb9d0222f0845c832b7da
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714193"
---
# <a name="iclrhostbindingpolicymanagermodifyapplicationpolicy-method"></a><span data-ttu-id="7f71f-102">ICLRHostBindingPolicyManager::ModifyApplicationPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="7f71f-102">ICLRHostBindingPolicyManager::ModifyApplicationPolicy Method</span></span>

<span data-ttu-id="7f71f-103">修改指定程序集的绑定策略，并创建该策略的新版本。</span><span class="sxs-lookup"><span data-stu-id="7f71f-103">Modifies the binding policy for the specified assembly, and creates a new version of the policy.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f71f-104">语法</span><span class="sxs-lookup"><span data-stu-id="7f71f-104">Syntax</span></span>  
  
```cpp  
HRESULT  ModifyApplicationPolicy (  
    [in] LPCWSTR     pwzSourceAssemblyIdentity,
    [in] LPCWSTR     pwzTargetAssemblyIdentity,  
    [in] BYTE       *pbApplicationPolicy,  
    [in] DWORD       cbAppPolicySize,  
    [in] DWORD       dwPolicyModifyFlags,  
    [out, size_is(*pcbNewAppPolicySize)] BYTE *pbNewApplicationPolicy,
    [in, out] DWORD *pcbNewAppPolicySize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f71f-105">参数</span><span class="sxs-lookup"><span data-stu-id="7f71f-105">Parameters</span></span>  

 `pwzSourceAssemblyIdentity`  
 <span data-ttu-id="7f71f-106">中要修改的程序集的标识。</span><span class="sxs-lookup"><span data-stu-id="7f71f-106">[in] The identity of the assembly to modify.</span></span>  
  
 `pwzTargetAssemblyIdentity`  
 <span data-ttu-id="7f71f-107">中已修改的程序集的新标识。</span><span class="sxs-lookup"><span data-stu-id="7f71f-107">[in] The new identity of the modified assembly.</span></span>  
  
 `pbApplicationPolicy`  
 <span data-ttu-id="7f71f-108">中指向包含要修改的程序集的绑定策略数据的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="7f71f-108">[in] A pointer to a buffer that contains the binding policy data for the assembly to modify.</span></span>  
  
 `cbAppPolicySize`  
 <span data-ttu-id="7f71f-109">中要替换的绑定策略的大小。</span><span class="sxs-lookup"><span data-stu-id="7f71f-109">[in] The size of the binding policy to be replaced.</span></span>  
  
 `dwPolicyModifyFlags`  
 <span data-ttu-id="7f71f-110">中 [EHostBindingPolicyModifyFlags](ehostbindingpolicymodifyflags-enumeration.md) 值的逻辑或组合，指示对重定向的控制。</span><span class="sxs-lookup"><span data-stu-id="7f71f-110">[in] A logical OR combination of [EHostBindingPolicyModifyFlags](ehostbindingpolicymodifyflags-enumeration.md) values, indicating control of redirection.</span></span>  
  
 `pbNewApplicationPolicy`  
 <span data-ttu-id="7f71f-111">弄指向包含新绑定策略数据的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="7f71f-111">[out] A pointer to a buffer that contains the new binding policy data.</span></span>  
  
 `pcbNewAppPolicySize`  
 <span data-ttu-id="7f71f-112">[in，out]指向新绑定策略缓冲区的大小的指针。</span><span class="sxs-lookup"><span data-stu-id="7f71f-112">[in, out] A pointer to the size of the new binding policy buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f71f-113">返回值</span><span class="sxs-lookup"><span data-stu-id="7f71f-113">Return Value</span></span>  
  
|<span data-ttu-id="7f71f-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7f71f-114">HRESULT</span></span>|<span data-ttu-id="7f71f-115">说明</span><span class="sxs-lookup"><span data-stu-id="7f71f-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7f71f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f71f-116">S_OK</span></span>|<span data-ttu-id="7f71f-117">已成功修改策略。</span><span class="sxs-lookup"><span data-stu-id="7f71f-117">The policy was modified successfully.</span></span>|  
|<span data-ttu-id="7f71f-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7f71f-118">E_INVALIDARG</span></span>|<span data-ttu-id="7f71f-119">`pwzSourceAssemblyIdentity` 或为 `pwzTargetAssemblyIdentity` 空引用。</span><span class="sxs-lookup"><span data-stu-id="7f71f-119">`pwzSourceAssemblyIdentity` or `pwzTargetAssemblyIdentity` was a null reference.</span></span>|  
|<span data-ttu-id="7f71f-120">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="7f71f-120">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="7f71f-121">`pbNewApplicationPolicy` 太小。</span><span class="sxs-lookup"><span data-stu-id="7f71f-121">`pbNewApplicationPolicy` is too small.</span></span>|  
|<span data-ttu-id="7f71f-122">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7f71f-122">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7f71f-123"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7f71f-123">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7f71f-124">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7f71f-124">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7f71f-125">调用超时。</span><span class="sxs-lookup"><span data-stu-id="7f71f-125">The call timed out.</span></span>|  
|<span data-ttu-id="7f71f-126">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7f71f-126">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7f71f-127">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="7f71f-127">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7f71f-128">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7f71f-128">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7f71f-129">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="7f71f-129">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7f71f-130">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7f71f-130">E_FAIL</span></span>|<span data-ttu-id="7f71f-131">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7f71f-131">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7f71f-132">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7f71f-132">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7f71f-133">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7f71f-133">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7f71f-134">注解</span><span class="sxs-lookup"><span data-stu-id="7f71f-134">Remarks</span></span>  

 <span data-ttu-id="7f71f-135">`ModifyApplicationPolicy`可以调用方法两次。</span><span class="sxs-lookup"><span data-stu-id="7f71f-135">The `ModifyApplicationPolicy` method can be called twice.</span></span> <span data-ttu-id="7f71f-136">第一次调用应为参数提供 null 值 `pbNewApplicationPolicy` 。</span><span class="sxs-lookup"><span data-stu-id="7f71f-136">The first call should supply a null value for the `pbNewApplicationPolicy` parameter.</span></span> <span data-ttu-id="7f71f-137">此调用将返回，并具有的必需值 `pcbNewAppPolicySize` 。</span><span class="sxs-lookup"><span data-stu-id="7f71f-137">This call will return with the necessary value for `pcbNewAppPolicySize`.</span></span> <span data-ttu-id="7f71f-138">第二次调用应为提供此值 `pcbNewAppPolicySize` ，并指向该大小的缓冲区 `pbNewApplicationPolicy` 。</span><span class="sxs-lookup"><span data-stu-id="7f71f-138">The second call should supply this value for `pcbNewAppPolicySize`, and point to a buffer of that size for `pbNewApplicationPolicy`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f71f-139">要求</span><span class="sxs-lookup"><span data-stu-id="7f71f-139">Requirements</span></span>  

 <span data-ttu-id="7f71f-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f71f-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f71f-141">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7f71f-141">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7f71f-142">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f71f-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7f71f-143">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f71f-143">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f71f-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7f71f-144">See also</span></span>

- [<span data-ttu-id="7f71f-145">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="7f71f-145">ICLRHostBindingPolicyManager Interface</span></span>](iclrhostbindingpolicymanager-interface.md)
