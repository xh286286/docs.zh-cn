---
title: ICLRRuntimeInfo::BindAsLegacyV2Runtime 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.BindAsLegacyV2Runtime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime
helpviewer_keywords:
- ICLRRuntimeInfo::BindAsLegacyV2Runtime method [.NET Framework hosting]
- BindAsLegacyV2Runtime method [.NET Framework hosting]
ms.assetid: 65fd55ac-4a24-4479-9384-a2e8013bfb2b
topic_type:
- apiref
ms.openlocfilehash: f0a03ecce49bbc3c1c03d037c9be31a8e994259d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732083"
---
# <a name="iclrruntimeinfobindaslegacyv2runtime-method"></a><span data-ttu-id="97c79-102">ICLRRuntimeInfo::BindAsLegacyV2Runtime 方法</span><span class="sxs-lookup"><span data-stu-id="97c79-102">ICLRRuntimeInfo::BindAsLegacyV2Runtime Method</span></span>

<span data-ttu-id="97c79-103">将所有旧公共语言运行时的当前运行时绑定 (CLR) 版本2激活策略决策。</span><span class="sxs-lookup"><span data-stu-id="97c79-103">Binds the current runtime for all legacy common language runtime (CLR) version 2 activation policy decisions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97c79-104">语法</span><span class="sxs-lookup"><span data-stu-id="97c79-104">Syntax</span></span>  
  
```cpp  
HRESULT BindAsLegacyV2Runtime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="97c79-105">返回值</span><span class="sxs-lookup"><span data-stu-id="97c79-105">Return Value</span></span>  

 <span data-ttu-id="97c79-106">此方法返回以下特定 Hresult：</span><span class="sxs-lookup"><span data-stu-id="97c79-106">This method returns the following specific HRESULTs:</span></span>  
  
|<span data-ttu-id="97c79-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="97c79-107">HRESULT</span></span>|<span data-ttu-id="97c79-108">说明</span><span class="sxs-lookup"><span data-stu-id="97c79-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="97c79-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="97c79-109">S_OK</span></span>|<span data-ttu-id="97c79-110">绑定成功，或已将此运行时绑定为旧版 CLR 版本2激活策略运行时。</span><span class="sxs-lookup"><span data-stu-id="97c79-110">Either binding succeeded, or this runtime was already bound as the legacy CLR version 2 activation policy runtime.</span></span>|  
|<span data-ttu-id="97c79-111">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="97c79-111">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="97c79-112">已将其他运行时绑定到旧版 CLR 版本2激活策略。</span><span class="sxs-lookup"><span data-stu-id="97c79-112">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="97c79-113">注解</span><span class="sxs-lookup"><span data-stu-id="97c79-113">Remarks</span></span>  

 <span data-ttu-id="97c79-114">如果当前运行时已绑定到所有旧版 CLR 版本2激活策略决策 (例如，通过使用 `useLegacyV2RuntimeActivationPolicy` 配置文件) 中[ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)上的属性，则此方法不会返回错误结果，而是 S_OK 结果，就像在方法成功绑定了旧激活策略时一样。</span><span class="sxs-lookup"><span data-stu-id="97c79-114">If the current runtime is already bound for all legacy CLR version 2 activation policy decisions (for example, by using the `useLegacyV2RuntimeActivationPolicy` attribute on the [\<startup> element](../../configure-apps/file-schema/startup/startup-element.md) in the configuration file), this method does not return an error result; instead, the result is S_OK, just as it would be if the method had successfully bound legacy activation policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97c79-115">要求</span><span class="sxs-lookup"><span data-stu-id="97c79-115">Requirements</span></span>  

 <span data-ttu-id="97c79-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="97c79-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97c79-117">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="97c79-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="97c79-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="97c79-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="97c79-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97c79-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97c79-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97c79-120">See also</span></span>

- [<span data-ttu-id="97c79-121">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="97c79-121">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="97c79-122">承载接口</span><span class="sxs-lookup"><span data-stu-id="97c79-122">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="97c79-123">承载</span><span class="sxs-lookup"><span data-stu-id="97c79-123">Hosting</span></span>](index.md)
- [<span data-ttu-id="97c79-124">\<startup> 元素</span><span class="sxs-lookup"><span data-stu-id="97c79-124">\<startup> Element</span></span>](../../configure-apps/file-schema/startup/startup-element.md)
