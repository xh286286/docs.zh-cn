---
title: ICLRControl 接口
ms.date: 03/30/2017
api_name:
- ICLRControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl
helpviewer_keywords:
- ICLRControl interface [.NET Framework hosting]
ms.assetid: a24fd905-1fa6-45a0-ad65-e9e2ee58861e
topic_type:
- apiref
ms.openlocfilehash: acf449014f5bf5683d5488f8ed2ead963676fe6b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728324"
---
# <a name="iclrcontrol-interface"></a><span data-ttu-id="1094e-102">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-102">ICLRControl Interface</span></span>

<span data-ttu-id="1094e-103">提供一些方法，这些方法允许宿主获取公共语言运行时 (CLR) 的引用并配置这些方面。</span><span class="sxs-lookup"><span data-stu-id="1094e-103">Provides methods that allow a host to get references to, and configure aspects of, the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1094e-104">方法</span><span class="sxs-lookup"><span data-stu-id="1094e-104">Methods</span></span>  
  
|<span data-ttu-id="1094e-105">方法</span><span class="sxs-lookup"><span data-stu-id="1094e-105">Method</span></span>|<span data-ttu-id="1094e-106">说明</span><span class="sxs-lookup"><span data-stu-id="1094e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1094e-107">GetCLRManager 方法</span><span class="sxs-lookup"><span data-stu-id="1094e-107">GetCLRManager Method</span></span>](iclrcontrol-getclrmanager-method.md)|<span data-ttu-id="1094e-108">获取一个接口指针，该指针指向主机可用于配置 CLR 的任何管理器类型的实例。</span><span class="sxs-lookup"><span data-stu-id="1094e-108">Gets an interface pointer to an instance of any of the manager types the host can use to configure the CLR.</span></span>|  
|[<span data-ttu-id="1094e-109">SetAppDomainManagerType 方法</span><span class="sxs-lookup"><span data-stu-id="1094e-109">SetAppDomainManagerType Method</span></span>](iclrcontrol-setappdomainmanagertype-method.md)|<span data-ttu-id="1094e-110">将派生自的类型设置 <xref:System.AppDomainManager> 为应用程序域管理器的类型。</span><span class="sxs-lookup"><span data-stu-id="1094e-110">Sets a type derived from <xref:System.AppDomainManager> as the type for application domain managers.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1094e-111">要求</span><span class="sxs-lookup"><span data-stu-id="1094e-111">Requirements</span></span>  

 <span data-ttu-id="1094e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1094e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1094e-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1094e-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1094e-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1094e-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1094e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1094e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1094e-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1094e-116">See also</span></span>

- [<span data-ttu-id="1094e-117">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-117">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="1094e-118">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-118">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)
- [<span data-ttu-id="1094e-119">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-119">ICLRGCManager Interface</span></span>](iclrgcmanager-interface.md)
- [<span data-ttu-id="1094e-120">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-120">ICLRHostBindingPolicyManager Interface</span></span>](iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="1094e-121">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-121">ICLRHostProtectionManager Interface</span></span>](iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="1094e-122">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-122">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)
- [<span data-ttu-id="1094e-123">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-123">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="1094e-124">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="1094e-124">IHostControl Interface</span></span>](ihostcontrol-interface.md)
- [<span data-ttu-id="1094e-125">承载接口</span><span class="sxs-lookup"><span data-stu-id="1094e-125">Hosting Interfaces</span></span>](hosting-interfaces.md)
