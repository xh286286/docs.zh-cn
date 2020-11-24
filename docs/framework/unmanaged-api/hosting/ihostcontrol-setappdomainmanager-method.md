---
title: IHostControl::SetAppDomainManager 方法
ms.date: 03/30/2017
api_name:
- IHostControl.SetAppDomainManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl::SetAppDomainManager
helpviewer_keywords:
- IHostControl::SetAppDomainManager method [.NET Framework hosting]
- SetAppDomainManager method [.NET Framework hosting]
ms.assetid: 6562bbe7-0d67-4c50-a958-3a18cf680375
topic_type:
- apiref
ms.openlocfilehash: 2f4c004db39c14e7a71b0caa55a6089e8f69ca3a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680634"
---
# <a name="ihostcontrolsetappdomainmanager-method"></a><span data-ttu-id="bc018-102">IHostControl::SetAppDomainManager 方法</span><span class="sxs-lookup"><span data-stu-id="bc018-102">IHostControl::SetAppDomainManager Method</span></span>

<span data-ttu-id="bc018-103">通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="bc018-103">Notifies the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc018-104">语法</span><span class="sxs-lookup"><span data-stu-id="bc018-104">Syntax</span></span>  
  
```cpp  
HRESULT SetAppDomainManager (  
    [in] DWORD     dwAppDomainID,  
    [in] IUnknown* pUnkAppDomainManager  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bc018-105">参数</span><span class="sxs-lookup"><span data-stu-id="bc018-105">Parameters</span></span>  

 `dwAppDomainID`  
 <span data-ttu-id="bc018-106">中选定的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="bc018-106">[in] The numeric identifier of the selected <xref:System.AppDomain>.</span></span>  
  
 `pUnkAppDomainManager`  
 <span data-ttu-id="bc018-107">中指向 <xref:System.AppDomainManager> 宿主作为实现的对象的指针 `IUnknown` 。</span><span class="sxs-lookup"><span data-stu-id="bc018-107">[in] A pointer to the <xref:System.AppDomainManager> object that the host implements as `IUnknown`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bc018-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bc018-108">Return Value</span></span>  
  
|<span data-ttu-id="bc018-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bc018-109">HRESULT</span></span>|<span data-ttu-id="bc018-110">说明</span><span class="sxs-lookup"><span data-stu-id="bc018-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bc018-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc018-111">S_OK</span></span>|<span data-ttu-id="bc018-112">`SetAppDomainManager` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="bc018-112">`SetAppDomainManager` returned successfully.</span></span>|  
|<span data-ttu-id="bc018-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bc018-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bc018-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="bc018-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bc018-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bc018-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bc018-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="bc018-116">The call timed out.</span></span>|  
|<span data-ttu-id="bc018-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bc018-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bc018-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="bc018-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bc018-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bc018-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bc018-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="bc018-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bc018-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bc018-121">E_FAIL</span></span>|<span data-ttu-id="bc018-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="bc018-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bc018-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="bc018-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bc018-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="bc018-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bc018-125">注解</span><span class="sxs-lookup"><span data-stu-id="bc018-125">Remarks</span></span>  

 <span data-ttu-id="bc018-126">向 <xref:System.AppDomainManager> 宿主提供一种机制，用于启动到托管代码并控制每个代码的创建和设置 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="bc018-126">The <xref:System.AppDomainManager> provides the host with a mechanism to bootstrap into managed code and to control the creation and settings of each <xref:System.AppDomain>.</span></span> <span data-ttu-id="bc018-127"><xref:System.AppDomainManager>创建时，将加载到每个中 <xref:System.AppDomain> <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="bc018-127">The <xref:System.AppDomainManager> is loaded into each <xref:System.AppDomain> when that <xref:System.AppDomain> is created.</span></span> <span data-ttu-id="bc018-128">如果选择此选项，CLR 将通过设置参数的值，通知宿主已创建应用程序域 `pUnkAppDomainManager` 。</span><span class="sxs-lookup"><span data-stu-id="bc018-128">If it chooses, the CLR notifies the host that the application domain has been created by setting the value of the `pUnkAppDomainManager` parameter.</span></span>  
  
 <span data-ttu-id="bc018-129">在其方法的实现中 `SetAppDomainManager` ，宿主可以设置应用程序域管理器的程序集名称和类型。</span><span class="sxs-lookup"><span data-stu-id="bc018-129">In its implementation of the `SetAppDomainManager` method, the host can set the assembly name and type for the application domain manager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc018-130">要求</span><span class="sxs-lookup"><span data-stu-id="bc018-130">Requirements</span></span>  

 <span data-ttu-id="bc018-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bc018-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bc018-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="bc018-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bc018-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bc018-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bc018-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bc018-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc018-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc018-135">See also</span></span>

- <xref:System.AppDomain>
- <xref:System.AppDomainManager>
- [<span data-ttu-id="bc018-136">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="bc018-136">IHostControl Interface</span></span>](ihostcontrol-interface.md)
