---
title: ModuleBindInfo 结构
ms.date: 03/30/2017
api_name:
- ModuleBindInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ModuleBindInfo
helpviewer_keywords:
- ModuleBindInfo structure [.NET Framework hosting]
ms.assetid: 632d4adc-dbc9-4ce8-9397-abc3285c1c69
topic_type:
- apiref
ms.openlocfilehash: 505015877985492edab4b761b379f33f1e5c6660
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729975"
---
# <a name="modulebindinfo-structure"></a><span data-ttu-id="976a2-102">ModuleBindInfo 结构</span><span class="sxs-lookup"><span data-stu-id="976a2-102">ModuleBindInfo Structure</span></span>

<span data-ttu-id="976a2-103">提供有关被引用模块和包含它的程序集的详细信息。</span><span class="sxs-lookup"><span data-stu-id="976a2-103">Provides detailed information about the referenced module and the assembly that contains it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="976a2-104">语法</span><span class="sxs-lookup"><span data-stu-id="976a2-104">Syntax</span></span>  
  
```cpp  
typedef struct _ModuleBindInfo {  
    DWORD    dwAppDomainId;  
    LPCWSTR  lpAssemblyIdentity;  
    LPCWSTR  lpModuleName  
} ModuleBindInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="976a2-105">成员</span><span class="sxs-lookup"><span data-stu-id="976a2-105">Members</span></span>  
  
|<span data-ttu-id="976a2-106">成员</span><span class="sxs-lookup"><span data-stu-id="976a2-106">Member</span></span>|<span data-ttu-id="976a2-107">说明</span><span class="sxs-lookup"><span data-stu-id="976a2-107">Description</span></span>|  
|------------|-----------------|  
|`dwAppDomainId`|<span data-ttu-id="976a2-108">的唯一标识符，该标识符由要从中 `IStream` 加载所引用的模块的 [IHostAssemblyStore：:P rovidemodule](ihostassemblystore-providemodule-method.md) 方法的调用返回。</span><span class="sxs-lookup"><span data-stu-id="976a2-108">A unique identifier for the `IStream` that is returned by a call to the [IHostAssemblyStore::ProvideModule](ihostassemblystore-providemodule-method.md) method from which the referenced module is to be loaded.</span></span>|  
|`lpAssemblyIdentity`|<span data-ttu-id="976a2-109">包含所引用的模块的程序集的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="976a2-109">A unique identifier for the assembly that contains the referenced module.</span></span>|  
|`lpModuleName`|<span data-ttu-id="976a2-110">引用的模块的名称。</span><span class="sxs-lookup"><span data-stu-id="976a2-110">The name of the referenced module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="976a2-111">注解</span><span class="sxs-lookup"><span data-stu-id="976a2-111">Remarks</span></span>  

 <span data-ttu-id="976a2-112">`ModuleBindInfo` 作为参数传递给 `IHostAssemblyStore::ProvideModule` 。</span><span class="sxs-lookup"><span data-stu-id="976a2-112">`ModuleBindInfo` is passed as a parameter to `IHostAssemblyStore::ProvideModule`.</span></span> <span data-ttu-id="976a2-113">宿主 `dwAppDomainId` (CLR) 向公共语言运行时提供唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="976a2-113">The host supplies the unique identifier `dwAppDomainId` to the common language runtime (CLR).</span></span> <span data-ttu-id="976a2-114">调用 [IHostAssemblyStore：:P rovideassembly](ihostassemblystore-provideassembly-method.md) 方法返回后，运行时将使用标识符来确定是否已映射的内容 `IStream` 。</span><span class="sxs-lookup"><span data-stu-id="976a2-114">After a call to the [IHostAssemblyStore::ProvideAssembly](ihostassemblystore-provideassembly-method.md) method returns, the runtime uses the identifier to determine whether the contents of the `IStream` have been mapped.</span></span> <span data-ttu-id="976a2-115">如果是这样，则运行时加载现有副本，而不是重新映射流。</span><span class="sxs-lookup"><span data-stu-id="976a2-115">If so, the runtime loads the existing copy rather than remapping the stream.</span></span> <span data-ttu-id="976a2-116">运行时还会将此标识符用作从对方法的调用返回的流的查找密钥 `IHostAssemblyStore::ProvideAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="976a2-116">The runtime also uses this identifier as a lookup key for streams that are returned from calls to the `IHostAssemblyStore::ProvideAssembly` method.</span></span> <span data-ttu-id="976a2-117">因此，对于模块请求和程序集请求，标识符必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="976a2-117">Therefore, the identifier must be unique for module requests as well as for assembly requests.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="976a2-118">要求</span><span class="sxs-lookup"><span data-stu-id="976a2-118">Requirements</span></span>  

 <span data-ttu-id="976a2-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="976a2-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="976a2-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="976a2-120">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="976a2-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="976a2-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="976a2-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="976a2-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="976a2-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="976a2-123">See also</span></span>

- [<span data-ttu-id="976a2-124">承载结构</span><span class="sxs-lookup"><span data-stu-id="976a2-124">Hosting Structures</span></span>](hosting-structures.md)
- [<span data-ttu-id="976a2-125">AssemblyBindInfo 结构</span><span class="sxs-lookup"><span data-stu-id="976a2-125">AssemblyBindInfo Structure</span></span>](assemblybindinfo-structure.md)
- [<span data-ttu-id="976a2-126">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="976a2-126">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="976a2-127">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="976a2-127">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="976a2-128">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="976a2-128">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
