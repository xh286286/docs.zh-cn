---
title: ICLRReferenceAssemblyEnum 接口
ms.date: 03/30/2017
api_name:
- ICLRReferenceAssemblyEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRReferenceAssemblyEnum
helpviewer_keywords:
- ICLRReferenceAssemblyEnum interface [.NET Framework hosting]
ms.assetid: 8adbf092-c3ba-4bee-b25b-0de6e43a4ce5
topic_type:
- apiref
ms.openlocfilehash: 189fbb1943d049dc4f52ea6cb626c02e9e25b3c7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95686132"
---
# <a name="iclrreferenceassemblyenum-interface"></a><span data-ttu-id="ddeb4-102">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="ddeb4-102">ICLRReferenceAssemblyEnum Interface</span></span>

<span data-ttu-id="ddeb4-103">提供一些方法，这些方法允许主机使用公共语言运行时 (CLR) 内部的程序集标识数据来操作由文件或流引用的程序集，而无需创建或了解这些标识。</span><span class="sxs-lookup"><span data-stu-id="ddeb4-103">Provides methods that allow the host to manipulate the set of assemblies referenced by a file or stream using assembly identity data that is internal to the common language runtime (CLR), without needing to create or understand those identities.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ddeb4-104">方法</span><span class="sxs-lookup"><span data-stu-id="ddeb4-104">Methods</span></span>  
  
|<span data-ttu-id="ddeb4-105">方法</span><span class="sxs-lookup"><span data-stu-id="ddeb4-105">Method</span></span>|<span data-ttu-id="ddeb4-106">说明</span><span class="sxs-lookup"><span data-stu-id="ddeb4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ddeb4-107">Get 方法</span><span class="sxs-lookup"><span data-stu-id="ddeb4-107">Get Method</span></span>](iclrreferenceassemblyenum-get-method.md)|<span data-ttu-id="ddeb4-108">获取所提供索引处的程序集标识。</span><span class="sxs-lookup"><span data-stu-id="ddeb4-108">Gets the assembly identity at the supplied index.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ddeb4-109">要求</span><span class="sxs-lookup"><span data-stu-id="ddeb4-109">Requirements</span></span>  

 <span data-ttu-id="ddeb4-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ddeb4-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ddeb4-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ddeb4-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ddeb4-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ddeb4-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ddeb4-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ddeb4-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddeb4-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ddeb4-114">See also</span></span>

- [<span data-ttu-id="ddeb4-115">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="ddeb4-115">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="ddeb4-116">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="ddeb4-116">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="ddeb4-117">承载接口</span><span class="sxs-lookup"><span data-stu-id="ddeb4-117">Hosting Interfaces</span></span>](hosting-interfaces.md)
