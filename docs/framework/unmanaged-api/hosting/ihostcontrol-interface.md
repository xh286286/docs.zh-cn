---
title: IHostControl 接口
ms.date: 03/30/2017
api_name:
- IHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl
helpviewer_keywords:
- IHostControl interface [.NET Framework hosting]
ms.assetid: a4ae0d1f-ade9-4b0a-a122-93ed11a5e6b3
topic_type:
- apiref
ms.openlocfilehash: 1bffef31702aa051d9ca865b18a67ac90c00cd00
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680635"
---
# <a name="ihostcontrol-interface"></a><span data-ttu-id="9713b-102">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="9713b-102">IHostControl Interface</span></span>

<span data-ttu-id="9713b-103">提供用于配置程序集加载和确定宿主支持哪些宿主接口的方法。</span><span class="sxs-lookup"><span data-stu-id="9713b-103">Provides methods for configuring the loading of assemblies, and for determining which hosting interfaces the host supports.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9713b-104">方法</span><span class="sxs-lookup"><span data-stu-id="9713b-104">Methods</span></span>  
  
|<span data-ttu-id="9713b-105">方法</span><span class="sxs-lookup"><span data-stu-id="9713b-105">Method</span></span>|<span data-ttu-id="9713b-106">说明</span><span class="sxs-lookup"><span data-stu-id="9713b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9713b-107">GetHostManager 方法</span><span class="sxs-lookup"><span data-stu-id="9713b-107">GetHostManager Method</span></span>](ihostcontrol-gethostmanager-method.md)|<span data-ttu-id="9713b-108">获取一个接口指针，该指针指向具有指定的接口的主机实现 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="9713b-108">Gets an interface pointer to the host's implementation of the interface with the specified `IID`.</span></span>|  
|[<span data-ttu-id="9713b-109">SetAppDomainManager 方法</span><span class="sxs-lookup"><span data-stu-id="9713b-109">SetAppDomainManager Method</span></span>](ihostcontrol-setappdomainmanager-method.md)|<span data-ttu-id="9713b-110">通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="9713b-110">Notifies the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9713b-111">要求</span><span class="sxs-lookup"><span data-stu-id="9713b-111">Requirements</span></span>  

 <span data-ttu-id="9713b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9713b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9713b-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9713b-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9713b-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9713b-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9713b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9713b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9713b-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9713b-116">See also</span></span>

- <xref:System.AppDomainManager>
- [<span data-ttu-id="9713b-117">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="9713b-117">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
- [<span data-ttu-id="9713b-118">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="9713b-118">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="9713b-119">承载接口</span><span class="sxs-lookup"><span data-stu-id="9713b-119">Hosting Interfaces</span></span>](hosting-interfaces.md)
