---
title: ICorPublishEnum 接口
ms.date: 03/30/2017
api_name:
- ICorPublishEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum
helpviewer_keywords:
- ICorPublishEnum interface [.NET Framework debugging]
ms.assetid: 76a136b5-e444-417a-8ade-f1596d597dc7
topic_type:
- apiref
ms.openlocfilehash: 492d4b727ce507340fec47d30a791aa49d0cecb6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95693341"
---
# <a name="icorpublishenum-interface"></a><span data-ttu-id="7a9c2-102">ICorPublishEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7a9c2-102">ICorPublishEnum Interface</span></span>

<span data-ttu-id="7a9c2-103">用作枚举器的抽象基接口，这些枚举器用于发布有关进程和应用程序域的信息。</span><span class="sxs-lookup"><span data-stu-id="7a9c2-103">Serves as the abstract base interface for the enumerators that are used in the publishing of information about processes and application domains.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7a9c2-104">方法</span><span class="sxs-lookup"><span data-stu-id="7a9c2-104">Methods</span></span>  
  
|<span data-ttu-id="7a9c2-105">方法</span><span class="sxs-lookup"><span data-stu-id="7a9c2-105">Method</span></span>|<span data-ttu-id="7a9c2-106">说明</span><span class="sxs-lookup"><span data-stu-id="7a9c2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7a9c2-107">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="7a9c2-107">Clone Method</span></span>](icorpublishenum-clone-method.md)|<span data-ttu-id="7a9c2-108">创建此 `ICorPublishEnum` 对象的一个副本。</span><span class="sxs-lookup"><span data-stu-id="7a9c2-108">Creates a copy of this `ICorPublishEnum` object.</span></span>|  
|[<span data-ttu-id="7a9c2-109">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="7a9c2-109">GetCount Method</span></span>](icorpublishenum-getcount-method.md)|<span data-ttu-id="7a9c2-110">获取枚举中的项数。</span><span class="sxs-lookup"><span data-stu-id="7a9c2-110">Gets the number of items in the enumeration.</span></span>|  
|[<span data-ttu-id="7a9c2-111">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="7a9c2-111">Reset Method</span></span>](icorpublishenum-reset-method.md)|<span data-ttu-id="7a9c2-112">将光标移到枚举的开头。</span><span class="sxs-lookup"><span data-stu-id="7a9c2-112">Moves the cursor of to the beginning of the enumeration.</span></span>|  
|[<span data-ttu-id="7a9c2-113">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="7a9c2-113">Skip Method</span></span>](icorpublishenum-skip-method.md)|<span data-ttu-id="7a9c2-114">按指定的项数在枚举中向前移动光标。</span><span class="sxs-lookup"><span data-stu-id="7a9c2-114">Moves the cursor forward in the enumeration by the specified number of items.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a9c2-115">注解</span><span class="sxs-lookup"><span data-stu-id="7a9c2-115">Remarks</span></span>  

 <span data-ttu-id="7a9c2-116">以下枚举器派生自 `ICorPublishEnum` ：</span><span class="sxs-lookup"><span data-stu-id="7a9c2-116">The following enumerators derive from `ICorPublishEnum`:</span></span>  
  
- [<span data-ttu-id="7a9c2-117">ICorPublishAppDomainEnum</span><span class="sxs-lookup"><span data-stu-id="7a9c2-117">ICorPublishAppDomainEnum</span></span>](icorpublishappdomainenum-interface.md)  
  
- [<span data-ttu-id="7a9c2-118">ICorPublishProcessEnum</span><span class="sxs-lookup"><span data-stu-id="7a9c2-118">ICorPublishProcessEnum</span></span>](icorpublishprocessenum-interface.md)  
  
## <a name="requirements"></a><span data-ttu-id="7a9c2-119">要求</span><span class="sxs-lookup"><span data-stu-id="7a9c2-119">Requirements</span></span>  

 <span data-ttu-id="7a9c2-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a9c2-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a9c2-121">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="7a9c2-121">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="7a9c2-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a9c2-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a9c2-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a9c2-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a9c2-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a9c2-124">See also</span></span>

- [<span data-ttu-id="7a9c2-125">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="7a9c2-125">CorpubPublish Coclass</span></span>](corpubpublish-coclass.md)
- [<span data-ttu-id="7a9c2-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="7a9c2-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
