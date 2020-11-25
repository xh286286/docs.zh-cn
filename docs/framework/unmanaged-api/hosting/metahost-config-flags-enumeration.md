---
title: METAHOST_CONFIG_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- METAHOST_CONFIG_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- METAHOST_CONFIG_FLAGS
helpviewer_keywords:
- METAHOST_CONFIG_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 6f1e389f-ed99-4d6a-a0ba-72d7d869a01d
topic_type:
- apiref
ms.openlocfilehash: 01e55659bf2a348ec763f51112cbdcd706f27c84
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730001"
---
# <a name="metahost_config_flags-enumeration"></a><span data-ttu-id="a7b96-102">METAHOST_CONFIG_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="a7b96-102">METAHOST_CONFIG_FLAGS Enumeration</span></span>

<span data-ttu-id="a7b96-103">描述在 `pdwConfigFlags` [ICLRMetaHostPolicy：： GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md)方法的参数中返回的可能的标志，指示 `useLegacyV2RuntimeActivationPolicy` 配置文件的[ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)中的特性的状态和设置。</span><span class="sxs-lookup"><span data-stu-id="a7b96-103">Describes the possible flags returned in the `pdwConfigFlags` parameter of the [ICLRMetaHostPolicy::GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md) method, indicating the presence and setting of the `useLegacyV2RuntimeActivationPolicy` attribute in the [\<startup> element](../../configure-apps/file-schema/startup/startup-element.md) of the configuration file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7b96-104">语法</span><span class="sxs-lookup"><span data-stu-id="a7b96-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET  = 0x00,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE   = 0x01,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE  = 0x02,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK   = 0x03  
} METAHOST_CONFIG_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="a7b96-105">成员</span><span class="sxs-lookup"><span data-stu-id="a7b96-105">Members</span></span>  
  
|<span data-ttu-id="a7b96-106">成员</span><span class="sxs-lookup"><span data-stu-id="a7b96-106">Member</span></span>|<span data-ttu-id="a7b96-107">说明</span><span class="sxs-lookup"><span data-stu-id="a7b96-107">Description</span></span>|  
|------------|-----------------|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET`|<span data-ttu-id="a7b96-108">`useLegacyV2RuntimeActivationPolicy` [ \<startup> 元素](../../configure-apps/file-schema/startup/startup-element.md)中不存在该特性。</span><span class="sxs-lookup"><span data-stu-id="a7b96-108">The `useLegacyV2RuntimeActivationPolicy` attribute was not present in the [\<startup> Element](../../configure-apps/file-schema/startup/startup-element.md).</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE`|<span data-ttu-id="a7b96-109">`useLegacyV2RuntimeActivationPolicy`特性存在并设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="a7b96-109">The `useLegacyV2RuntimeActivationPolicy` attribute was present and set to `true`.</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE`|<span data-ttu-id="a7b96-110">`useLegacyV2RuntimeActivationPolicy`特性存在并设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="a7b96-110">The `useLegacyV2RuntimeActivationPolicy` attribute was present and set to `false`.</span></span>|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK`|<span data-ttu-id="a7b96-111">将此掩码应用于在中返回的值，以 `pdwConfigFlags` 获取与相关的值 `useLegacyV2RuntimeActivationPolicy` 。</span><span class="sxs-lookup"><span data-stu-id="a7b96-111">Apply this mask to the value returned in `pdwConfigFlags` to get the values relevant to `useLegacyV2RuntimeActivationPolicy`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a7b96-112">备注</span><span class="sxs-lookup"><span data-stu-id="a7b96-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7b96-113">要求</span><span class="sxs-lookup"><span data-stu-id="a7b96-113">Requirements</span></span>  

 <span data-ttu-id="a7b96-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a7b96-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7b96-115">**标头：** Metahost</span><span class="sxs-lookup"><span data-stu-id="a7b96-115">**Header:** Metahost.h</span></span>  
  
 <span data-ttu-id="a7b96-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a7b96-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a7b96-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7b96-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7b96-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a7b96-118">See also</span></span>

- [<span data-ttu-id="a7b96-119">承载枚举</span><span class="sxs-lookup"><span data-stu-id="a7b96-119">Hosting Enumerations</span></span>](hosting-enumerations.md)
- [<span data-ttu-id="a7b96-120">GetRequestedRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="a7b96-120">GetRequestedRuntime Method</span></span>](iclrmetahostpolicy-getrequestedruntime-method.md)
- [<span data-ttu-id="a7b96-121">\<startup> 元素</span><span class="sxs-lookup"><span data-stu-id="a7b96-121">\<startup> Element</span></span>](../../configure-apps/file-schema/startup/startup-element.md)
