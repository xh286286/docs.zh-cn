---
title: ICorRuntimeHost::GetDefaultDomain 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetDefaultDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetDefaultDomain
helpviewer_keywords:
- ICorRuntimeHost::GetDefaultDomain method [.NET Framework hosting]
- GetDefaultDomain method [.NET Framework hosting]
ms.assetid: 5e17a6fc-f335-4aae-9bb0-c3e1271a9426
topic_type:
- apiref
ms.openlocfilehash: 673c32c86c808c36db6454b8a9f0d8e68f9b1258
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720628"
---
# <a name="icorruntimehostgetdefaultdomain-method"></a><span data-ttu-id="669f0-102">ICorRuntimeHost::GetDefaultDomain 方法</span><span class="sxs-lookup"><span data-stu-id="669f0-102">ICorRuntimeHost::GetDefaultDomain Method</span></span>

<span data-ttu-id="669f0-103">获取类型的接口指针 <xref:System._AppDomain?displayProperty=nameWithType> ，该指针表示当前进程的默认域。</span><span class="sxs-lookup"><span data-stu-id="669f0-103">Gets an interface pointer of type <xref:System._AppDomain?displayProperty=nameWithType> that represents the default domain for the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="669f0-104">语法</span><span class="sxs-lookup"><span data-stu-id="669f0-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDefaultDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="669f0-105">参数</span><span class="sxs-lookup"><span data-stu-id="669f0-105">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="669f0-106">弄类型为的接口指针， <xref:System._AppDomain?displayProperty=nameWithType> 用于 <xref:System.AppDomain> 表示进程的默认应用程序域的实例。</span><span class="sxs-lookup"><span data-stu-id="669f0-106">[out] An interface pointer of type <xref:System._AppDomain?displayProperty=nameWithType> to the <xref:System.AppDomain> instance that represents the default application domain for the process.</span></span>  
  
 <span data-ttu-id="669f0-107">此指针已类型化 `IUnknown` ，因此调用方通常应调用 `QueryInterface` 以获取类型的接口指针 <xref:System._AppDomain?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="669f0-107">This pointer is typed `IUnknown`, so callers should generally call `QueryInterface` to obtain an interface pointer of type <xref:System._AppDomain?displayProperty=nameWithType>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="669f0-108">返回值</span><span class="sxs-lookup"><span data-stu-id="669f0-108">Return Value</span></span>  
  
|<span data-ttu-id="669f0-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="669f0-109">HRESULT</span></span>|<span data-ttu-id="669f0-110">说明</span><span class="sxs-lookup"><span data-stu-id="669f0-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="669f0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="669f0-111">S_OK</span></span>|<span data-ttu-id="669f0-112">操作成功。</span><span class="sxs-lookup"><span data-stu-id="669f0-112">The operation was successful.</span></span>|  
|<span data-ttu-id="669f0-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="669f0-113">S_FALSE</span></span>|<span data-ttu-id="669f0-114">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="669f0-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="669f0-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="669f0-115">E_FAIL</span></span>|<span data-ttu-id="669f0-116">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="669f0-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="669f0-117">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="669f0-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="669f0-118">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="669f0-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="669f0-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="669f0-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="669f0-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="669f0-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="669f0-121">要求</span><span class="sxs-lookup"><span data-stu-id="669f0-121">Requirements</span></span>  

 <span data-ttu-id="669f0-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="669f0-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="669f0-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="669f0-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="669f0-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="669f0-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="669f0-125">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="669f0-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="669f0-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="669f0-126">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="669f0-127">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="669f0-127">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
