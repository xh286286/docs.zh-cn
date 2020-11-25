---
title: IAppDomainBinding::OnAppDomain 方法
ms.date: 03/30/2017
api_name:
- IAppDomainBinding.OnAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- OnAppDomain
helpviewer_keywords:
- IAppDomainBinding::OnAppDomain method [.NET Framework hosting]
- OnAppDomain method [.NET Framework hosting]
ms.assetid: b419dcc9-e8aa-484b-af0d-0f40358edb99
topic_type:
- apiref
ms.openlocfilehash: 65f6be8c12ce057422ad178c759affed170e44ba
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721707"
---
# <a name="iappdomainbindingonappdomain-method"></a><span data-ttu-id="61a7c-102">IAppDomainBinding::OnAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="61a7c-102">IAppDomainBinding::OnAppDomain Method</span></span>

<span data-ttu-id="61a7c-103">由公共语言运行时 (CLR) 调用，以通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="61a7c-103">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61a7c-104">语法</span><span class="sxs-lookup"><span data-stu-id="61a7c-104">Syntax</span></span>  
  
```cpp  
HRESULT OnAppDomain (  
    [in] IUnknown* pAppdomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61a7c-105">参数</span><span class="sxs-lookup"><span data-stu-id="61a7c-105">Parameters</span></span>  

 `pAppdomain`  
 <span data-ttu-id="61a7c-106">中指向 [IUnknown](/cpp/atl/iunknown) 接口对象的指针，该对象表示新的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="61a7c-106">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) interface object that represents the new application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61a7c-107">要求</span><span class="sxs-lookup"><span data-stu-id="61a7c-107">Requirements</span></span>  

 <span data-ttu-id="61a7c-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="61a7c-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61a7c-109">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="61a7c-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="61a7c-110">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="61a7c-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="61a7c-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61a7c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61a7c-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61a7c-112">See also</span></span>

- [<span data-ttu-id="61a7c-113">IAppDomainBinding 接口</span><span class="sxs-lookup"><span data-stu-id="61a7c-113">IAppDomainBinding Interface</span></span>](iappdomainbinding-interface.md)
