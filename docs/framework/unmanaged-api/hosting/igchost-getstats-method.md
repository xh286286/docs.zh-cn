---
title: IGCHost::GetStats 方法
ms.date: 03/30/2017
api_name:
- IGCHost.GetStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetStats
helpviewer_keywords:
- GetStats method, IGCHost interface [.NET Framework hosting]
- IGCHost::GetStats method [.NET Framework hosting]
ms.assetid: c4ae022c-46ac-4f19-9ddd-09b955f19412
topic_type:
- apiref
ms.openlocfilehash: 7e664d88bf9f67e936e693b663f27ca490da13ed
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95670103"
---
# <a name="igchostgetstats-method"></a><span data-ttu-id="f137f-102">IGCHost::GetStats 方法</span><span class="sxs-lookup"><span data-stu-id="f137f-102">IGCHost::GetStats Method</span></span>

<span data-ttu-id="f137f-103">获取垃圾收集系统的当前状态的统计信息。</span><span class="sxs-lookup"><span data-stu-id="f137f-103">Gets the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f137f-104">语法</span><span class="sxs-lookup"><span data-stu-id="f137f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f137f-105">参数</span><span class="sxs-lookup"><span data-stu-id="f137f-105">Parameters</span></span>  

 `pStats`  
 <span data-ttu-id="f137f-106">[in，out]指向 [COR_GC_STATS](cor-gc-stats-structure.md) 结构的指针，该结构包含垃圾收集系统的当前状态的统计信息。</span><span class="sxs-lookup"><span data-stu-id="f137f-106">[in, out] A pointer to a [COR_GC_STATS](cor-gc-stats-structure.md) structure that contains the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f137f-107">注解</span><span class="sxs-lookup"><span data-stu-id="f137f-107">Remarks</span></span>  

 <span data-ttu-id="f137f-108">智能分配系统可以使用统计信息来帮助垃圾回收系统操作。</span><span class="sxs-lookup"><span data-stu-id="f137f-108">The statistics can be used by a smart allocation system to help the garbage collection system operate.</span></span> <span data-ttu-id="f137f-109">例如，在查看统计信息后，分配系统可能会确定它是否需要添加更多内存或强制集合。</span><span class="sxs-lookup"><span data-stu-id="f137f-109">For example, the allocation system may determine, after reviewing the statistics, that it needs to add more memory or force a collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f137f-110">要求</span><span class="sxs-lookup"><span data-stu-id="f137f-110">Requirements</span></span>  

 <span data-ttu-id="f137f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f137f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f137f-112">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="f137f-112">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="f137f-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f137f-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f137f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f137f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f137f-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f137f-115">See also</span></span>

- [<span data-ttu-id="f137f-116">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="f137f-116">IGCHost Interface</span></span>](igchost-interface.md)
