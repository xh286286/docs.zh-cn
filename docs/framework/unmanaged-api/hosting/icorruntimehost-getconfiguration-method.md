---
title: ICorRuntimeHost::GetConfiguration 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetConfiguration
helpviewer_keywords:
- ICorRuntimeHost::GetConfiguration method [.NET Framework hosting]
- GetConfiguration method [.NET Framework hosting]
ms.assetid: c431617a-b055-44a0-8730-48b7a86d9610
topic_type:
- apiref
ms.openlocfilehash: 2a50814a67be5a01a7413050683a915355665f3c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720641"
---
# <a name="icorruntimehostgetconfiguration-method"></a><span data-ttu-id="9a1c6-102">ICorRuntimeHost::GetConfiguration 方法</span><span class="sxs-lookup"><span data-stu-id="9a1c6-102">ICorRuntimeHost::GetConfiguration Method</span></span>

<span data-ttu-id="9a1c6-103">获取一个对象，该对象允许主机指定 (CLR) 的公共语言运行时的回调配置。</span><span class="sxs-lookup"><span data-stu-id="9a1c6-103">Gets an object that allows the host to specify the callback configuration of the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a1c6-104">语法</span><span class="sxs-lookup"><span data-stu-id="9a1c6-104">Syntax</span></span>  
  
```cpp  
HRESULT GetConfiguration(  
    [out] ICorConfiguration** pConfiguration  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a1c6-105">参数</span><span class="sxs-lookup"><span data-stu-id="9a1c6-105">Parameters</span></span>  

 `pConfiguration`  
 <span data-ttu-id="9a1c6-106">弄指向可用于配置 CLR 的 [ICorConfiguration](icorconfiguration-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="9a1c6-106">[out] A pointer to the address of an [ICorConfiguration](icorconfiguration-interface.md) object that can be used to configure the CLR.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9a1c6-107">注解</span><span class="sxs-lookup"><span data-stu-id="9a1c6-107">Remarks</span></span>  

 <span data-ttu-id="9a1c6-108">必须在初始化之前配置 CLR;否则，该 `GetConfiguration` 方法将返回一个 HRESULT，指示错误。</span><span class="sxs-lookup"><span data-stu-id="9a1c6-108">The CLR must be configured prior to its initialization; otherwise, the `GetConfiguration` method returns an HRESULT indicating an error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a1c6-109">要求</span><span class="sxs-lookup"><span data-stu-id="9a1c6-109">Requirements</span></span>  

 <span data-ttu-id="9a1c6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9a1c6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a1c6-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9a1c6-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9a1c6-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9a1c6-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9a1c6-113">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="9a1c6-113">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a1c6-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a1c6-114">See also</span></span>

- [<span data-ttu-id="9a1c6-115">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="9a1c6-115">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
