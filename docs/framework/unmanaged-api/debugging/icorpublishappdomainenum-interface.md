---
title: ICorPublishAppDomainEnum 接口
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum
helpviewer_keywords:
- ICorPublishAppDomainEnum interface [.NET Framework debugging]
ms.assetid: bb798c56-042e-475d-a245-b6fac36d0c07
topic_type:
- apiref
ms.openlocfilehash: 5b5a901bef779948467cfcc3d71a1fcd057c1aeb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95693705"
---
# <a name="icorpublishappdomainenum-interface"></a><span data-ttu-id="26f92-102">ICorPublishAppDomainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="26f92-102">ICorPublishAppDomainEnum Interface</span></span>

<span data-ttu-id="26f92-103">[ICorPublishEnum](icorpublishenum-interface.md)接口的子类，它提供了用于遍历进程中当前存在的[ICorPublishAppDomain](icorpublishappdomain-interface.md)对象的集合的方法。</span><span class="sxs-lookup"><span data-stu-id="26f92-103">A subclass of the [ICorPublishEnum](icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishAppDomain](icorpublishappdomain-interface.md) objects that currently exist within a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="26f92-104">方法</span><span class="sxs-lookup"><span data-stu-id="26f92-104">Methods</span></span>  
  
|<span data-ttu-id="26f92-105">方法</span><span class="sxs-lookup"><span data-stu-id="26f92-105">Method</span></span>|<span data-ttu-id="26f92-106">说明</span><span class="sxs-lookup"><span data-stu-id="26f92-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="26f92-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="26f92-107">Next Method</span></span>](icorpublishappdomainenum-next-method.md)|<span data-ttu-id="26f92-108">`ICorPublishAppDomain`从当前位置开始，获取集合中指定数量的实例。</span><span class="sxs-lookup"><span data-stu-id="26f92-108">Gets the specified number of `ICorPublishAppDomain` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="26f92-109">注解</span><span class="sxs-lookup"><span data-stu-id="26f92-109">Remarks</span></span>  

 <span data-ttu-id="26f92-110">`ICorPublishAppDomainEnum`接口实现抽象接口的方法[ICorPublishEnum](icorpublishenum-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="26f92-110">The `ICorPublishAppDomainEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](icorpublishenum-interface.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26f92-111">要求</span><span class="sxs-lookup"><span data-stu-id="26f92-111">Requirements</span></span>  

 <span data-ttu-id="26f92-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26f92-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26f92-113">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="26f92-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="26f92-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26f92-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26f92-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26f92-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26f92-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26f92-116">See also</span></span>

- [<span data-ttu-id="26f92-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="26f92-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="26f92-118">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="26f92-118">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
