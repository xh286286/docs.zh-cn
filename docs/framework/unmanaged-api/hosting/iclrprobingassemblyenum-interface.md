---
title: ICLRProbingAssemblyEnum 接口
ms.date: 03/30/2017
api_name:
- ICLRProbingAssemblyEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRProbingAssemblyEnum
helpviewer_keywords:
- ICLRProbingAssemblyEnum interface [.NET Framework hosting]
ms.assetid: e7d3ccab-b0f0-4872-8935-0ed72920171b
topic_type:
- apiref
ms.openlocfilehash: 6df08889af30542af5a128cbffc38a57ce640fde
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728922"
---
# <a name="iclrprobingassemblyenum-interface"></a><span data-ttu-id="e6c3b-102">ICLRProbingAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e6c3b-102">ICLRProbingAssemblyEnum Interface</span></span>

<span data-ttu-id="e6c3b-103">提供一些方法，这些方法使宿主可以通过使用公共语言运行时 (CLR) 内部的程序集的标识信息来获取程序集的探测标识，无需创建或了解该标识。</span><span class="sxs-lookup"><span data-stu-id="e6c3b-103">Provides methods that enable the host to get the probing identities of an assembly by using the assembly's identity information that is internal to the common language runtime (CLR), without needing to create or understand that identity.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e6c3b-104">方法</span><span class="sxs-lookup"><span data-stu-id="e6c3b-104">Methods</span></span>  
  
|<span data-ttu-id="e6c3b-105">方法</span><span class="sxs-lookup"><span data-stu-id="e6c3b-105">Method</span></span>|<span data-ttu-id="e6c3b-106">说明</span><span class="sxs-lookup"><span data-stu-id="e6c3b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e6c3b-107">Get 方法</span><span class="sxs-lookup"><span data-stu-id="e6c3b-107">Get Method</span></span>](iclrprobingassemblyenum-get-method.md)|<span data-ttu-id="e6c3b-108">获取指定索引处的程序集标识。</span><span class="sxs-lookup"><span data-stu-id="e6c3b-108">Gets the assembly identity at the specified index.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e6c3b-109">注解</span><span class="sxs-lookup"><span data-stu-id="e6c3b-109">Remarks</span></span>  

 <span data-ttu-id="e6c3b-110">方法（如 [ICLRAssemblyIdentityManager：： GetProbingAssembliesFromReference](iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md) ）返回 `ICLRProbingAssemblyEnum` 实例。</span><span class="sxs-lookup"><span data-stu-id="e6c3b-110">Methods such as [ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference](iclrassemblyidentitymanager-getprobingassembliesfromreference-method.md) return an `ICLRProbingAssemblyEnum` instance.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6c3b-111">要求</span><span class="sxs-lookup"><span data-stu-id="e6c3b-111">Requirements</span></span>  

 <span data-ttu-id="e6c3b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e6c3b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6c3b-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e6c3b-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e6c3b-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e6c3b-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e6c3b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6c3b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6c3b-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6c3b-116">See also</span></span>

- [<span data-ttu-id="e6c3b-117">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="e6c3b-117">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="e6c3b-118">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="e6c3b-118">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="e6c3b-119">承载接口</span><span class="sxs-lookup"><span data-stu-id="e6c3b-119">Hosting Interfaces</span></span>](hosting-interfaces.md)
