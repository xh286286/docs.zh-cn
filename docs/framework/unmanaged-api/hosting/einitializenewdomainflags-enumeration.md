---
title: EInitializeNewDomainFlags 枚举
ms.date: 03/30/2017
api_name:
- EInitializeNewDomainFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EInitializeNewDomainFlags
helpviewer_keywords:
- EInitializeNewDomainFlags enumeration [.NET Framework hosting]
ms.assetid: 3a120ab2-f5ef-4c9b-8595-d3ed7247c342
ms.openlocfilehash: 8350b507609e63c060cda08514200d386c37a6b3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724320"
---
# <a name="einitializenewdomainflags-enumeration"></a><span data-ttu-id="9d4c2-102">EInitializeNewDomainFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="9d4c2-102">EInitializeNewDomainFlags Enumeration</span></span>

<span data-ttu-id="9d4c2-103">使宿主能够向运行时提供有关应用程序域初始化的信息。</span><span class="sxs-lookup"><span data-stu-id="9d4c2-103">Enables the host to provide the runtime with information about the initialization of an application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d4c2-104">语法</span><span class="sxs-lookup"><span data-stu-id="9d4c2-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eInitializeNewDomainFlags_None              = 0x0000,  
    eInitializeNewDomainFlags_NoSecurityChanges = 0x0002  
} EInitializeNewDomainFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="9d4c2-105">成员</span><span class="sxs-lookup"><span data-stu-id="9d4c2-105">Members</span></span>  
  
|<span data-ttu-id="9d4c2-106">成员</span><span class="sxs-lookup"><span data-stu-id="9d4c2-106">Member</span></span>|<span data-ttu-id="9d4c2-107">说明</span><span class="sxs-lookup"><span data-stu-id="9d4c2-107">Description</span></span>|  
|------------|-----------------|  
|`eInitializeNewDomainFlags_None`|<span data-ttu-id="9d4c2-108">无标志。</span><span class="sxs-lookup"><span data-stu-id="9d4c2-108">No flags.</span></span>|  
|`eInitializeNewDomainFlags_NoSecurityChanges`|<span data-ttu-id="9d4c2-109">通知公共语言运行时 (CLR) 宿主不会在方法中更改应用程序域的安全状态 <xref:System.AppDomainManager.InitializeNewDomain%2A> 。</span><span class="sxs-lookup"><span data-stu-id="9d4c2-109">Informs the common language runtime (CLR) that the host will not make changes to the security state of the application domain in the <xref:System.AppDomainManager.InitializeNewDomain%2A> method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9d4c2-110">注解</span><span class="sxs-lookup"><span data-stu-id="9d4c2-110">Remarks</span></span>  

 <span data-ttu-id="9d4c2-111">[ICLRDomainManager：： SetAppDomainManagerType](iclrdomainmanager-setappdomainmanagertype-method.md)方法采用类型的参数 `EInitializeNewDomainFlags` 。</span><span class="sxs-lookup"><span data-stu-id="9d4c2-111">The [ICLRDomainManager::SetAppDomainManagerType](iclrdomainmanager-setappdomainmanagertype-method.md) method takes a parameter of type `EInitializeNewDomainFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d4c2-112">要求</span><span class="sxs-lookup"><span data-stu-id="9d4c2-112">Requirements</span></span>  

 <span data-ttu-id="9d4c2-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9d4c2-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d4c2-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9d4c2-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9d4c2-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9d4c2-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9d4c2-116">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d4c2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d4c2-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9d4c2-117">See also</span></span>

- [<span data-ttu-id="9d4c2-118">承载枚举</span><span class="sxs-lookup"><span data-stu-id="9d4c2-118">Hosting Enumerations</span></span>](hosting-enumerations.md)
- [<span data-ttu-id="9d4c2-119">SetAppDomainManagerType 方法</span><span class="sxs-lookup"><span data-stu-id="9d4c2-119">SetAppDomainManagerType Method</span></span>](iclrdomainmanager-setappdomainmanagertype-method.md)
