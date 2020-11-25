---
title: IAppDomainBinding 接口
ms.date: 03/30/2017
api_name:
- IAppDomainBinding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainBinding
helpviewer_keywords:
- IAppDomainBinding interface [.NET Framework hosting]
ms.assetid: 368881ab-c4ea-4731-bf22-c596aac7c66c
topic_type:
- apiref
ms.openlocfilehash: 652739ad51e0a177f7b0fc6c0c9a11508c820bb3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721716"
---
# <a name="iappdomainbinding-interface"></a><span data-ttu-id="ebc2e-102">IAppDomainBinding 接口</span><span class="sxs-lookup"><span data-stu-id="ebc2e-102">IAppDomainBinding Interface</span></span>

<span data-ttu-id="ebc2e-103">提供一个方法，该方法由公共语言运行时 (CLR) ，用于通知宿主应用程序已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="ebc2e-103">Provides a method that is called by the common language runtime (CLR) to notify the host application that an application domain has been created.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ebc2e-104">方法</span><span class="sxs-lookup"><span data-stu-id="ebc2e-104">Methods</span></span>  
  
|<span data-ttu-id="ebc2e-105">方法</span><span class="sxs-lookup"><span data-stu-id="ebc2e-105">Method</span></span>|<span data-ttu-id="ebc2e-106">说明</span><span class="sxs-lookup"><span data-stu-id="ebc2e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ebc2e-107">OnAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="ebc2e-107">OnAppDomain Method</span></span>](iappdomainbinding-onappdomain-method.md)|<span data-ttu-id="ebc2e-108">由公共语言运行时 (CLR) 调用，以通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="ebc2e-108">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ebc2e-109">要求</span><span class="sxs-lookup"><span data-stu-id="ebc2e-109">Requirements</span></span>  

 <span data-ttu-id="ebc2e-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ebc2e-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebc2e-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ebc2e-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ebc2e-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ebc2e-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ebc2e-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ebc2e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebc2e-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ebc2e-114">See also</span></span>

- [<span data-ttu-id="ebc2e-115">承载接口</span><span class="sxs-lookup"><span data-stu-id="ebc2e-115">Hosting Interfaces</span></span>](hosting-interfaces.md)
