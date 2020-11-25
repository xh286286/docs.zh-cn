---
title: IHostPolicyManager 接口
ms.date: 03/30/2017
api_name:
- IHostPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostPolicyManager
helpviewer_keywords:
- IHostPolicyManager interface [.NET Framework hosting]
ms.assetid: 8c4aa124-5e00-46d9-b1e8-57ba6574bb0d
topic_type:
- apiref
ms.openlocfilehash: 3c85bcbe8aee453b19217ebd1f48feea113e3bb1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731212"
---
# <a name="ihostpolicymanager-interface"></a><span data-ttu-id="f4ab2-102">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="f4ab2-102">IHostPolicyManager Interface</span></span>

<span data-ttu-id="f4ab2-103">提供一些方法，这些方法可通知宿主公共语言运行时 (CLR) 在发生中止、超时或失败时执行的操作。</span><span class="sxs-lookup"><span data-stu-id="f4ab2-103">Provides methods that notify the host of the actions the common language runtime (CLR) performs in case of aborts, timeouts, or failures.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f4ab2-104">方法</span><span class="sxs-lookup"><span data-stu-id="f4ab2-104">Methods</span></span>  
  
|<span data-ttu-id="f4ab2-105">方法</span><span class="sxs-lookup"><span data-stu-id="f4ab2-105">Method</span></span>|<span data-ttu-id="f4ab2-106">说明</span><span class="sxs-lookup"><span data-stu-id="f4ab2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f4ab2-107">OnDefaultAction 方法</span><span class="sxs-lookup"><span data-stu-id="f4ab2-107">OnDefaultAction Method</span></span>](ihostpolicymanager-ondefaultaction-method.md)|<span data-ttu-id="f4ab2-108">向宿主通知 CLR 将使用对 [ICLRPolicyManager：： SetDefaultAction](iclrpolicymanager-setdefaultaction-method.md) 的调用指定的默认操作来响应线程中止或 <xref:System.AppDomain> 卸载。</span><span class="sxs-lookup"><span data-stu-id="f4ab2-108">Notifies the host that the CLR is about to take the default action specified by a call to [ICLRPolicyManager::SetDefaultAction](iclrpolicymanager-setdefaultaction-method.md) in response to a thread abort or <xref:System.AppDomain> unload.</span></span>|  
|[<span data-ttu-id="f4ab2-109">OnFailure 方法</span><span class="sxs-lookup"><span data-stu-id="f4ab2-109">OnFailure Method</span></span>](ihostpolicymanager-onfailure-method.md)|<span data-ttu-id="f4ab2-110">向宿主通知 CLR 即将获取调用 [ICLRPolicyManager：： SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) 所指定的操作，以响应资源分配或回收失败。</span><span class="sxs-lookup"><span data-stu-id="f4ab2-110">Notifies the host that the CLR is about to take the action specified by a call to [ICLRPolicyManager::SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) in response to a resource allocation or reclamation failure.</span></span>|  
|[<span data-ttu-id="f4ab2-111">OnTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="f4ab2-111">OnTimeout Method</span></span>](ihostpolicymanager-ontimeout-method.md)|<span data-ttu-id="f4ab2-112">向宿主通知 CLR 即将使用对 [ICLRPolicyManager：： SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) 的调用指定的操作来响应超时。</span><span class="sxs-lookup"><span data-stu-id="f4ab2-112">Notifies the host that the CLR is about to take the action specified by a call to [ICLRPolicyManager::SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) in response to a timeout.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f4ab2-113">要求</span><span class="sxs-lookup"><span data-stu-id="f4ab2-113">Requirements</span></span>  

 <span data-ttu-id="f4ab2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f4ab2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4ab2-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f4ab2-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f4ab2-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f4ab2-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f4ab2-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4ab2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4ab2-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4ab2-118">See also</span></span>

- [<span data-ttu-id="f4ab2-119">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="f4ab2-119">EClrFailure Enumeration</span></span>](eclrfailure-enumeration.md)
- [<span data-ttu-id="f4ab2-120">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="f4ab2-120">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="f4ab2-121">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="f4ab2-121">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="f4ab2-122">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="f4ab2-122">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="f4ab2-123">承载接口</span><span class="sxs-lookup"><span data-stu-id="f4ab2-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
