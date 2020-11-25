---
title: IEnumReferenceIdentity 接口
ms.date: 03/30/2017
api_name:
- IEnumReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumReferenceIdentity
helpviewer_keywords:
- IEnumReferenceIdentity interface [.NET Framework fusion]
ms.assetid: a17b3155-7216-4e16-8c9f-abce21f549e7
topic_type:
- apiref
ms.openlocfilehash: bea357fe9a154ffb8f69228c7332c026dc2759e9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728962"
---
# <a name="ienumreferenceidentity-interface"></a><span data-ttu-id="3f9c1-102">IEnumReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="3f9c1-102">IEnumReferenceIdentity Interface</span></span>

<span data-ttu-id="3f9c1-103">用作对象集合的枚举器 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="3f9c1-103">Serves as an enumerator for a collection of `IReferenceIdentity` objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3f9c1-104">方法</span><span class="sxs-lookup"><span data-stu-id="3f9c1-104">Methods</span></span>  
  
|<span data-ttu-id="3f9c1-105">方法</span><span class="sxs-lookup"><span data-stu-id="3f9c1-105">Method</span></span>|<span data-ttu-id="3f9c1-106">说明</span><span class="sxs-lookup"><span data-stu-id="3f9c1-106">Description</span></span>|  
|------------|-----------------|  
|`IEnumReferenceIdentity::Clone`|<span data-ttu-id="3f9c1-107">获取一个接口指针，该指针指向 `IEnumReferenceIdentity` 包含与此相同的成员的新 `IEnumReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="3f9c1-107">Gets an interface pointer to a new `IEnumReferenceIdentity` that contains the same members as this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Next`|<span data-ttu-id="3f9c1-108">`IReferenceIdentity`从当前位置开始，获取指定数目的对象。</span><span class="sxs-lookup"><span data-stu-id="3f9c1-108">Gets the specified number of `IReferenceIdentity` objects, starting at the current position.</span></span>|  
|`IEnumReferenceIdentity::Reset`|<span data-ttu-id="3f9c1-109">将指令指针移到此的开头 `IEnumReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="3f9c1-109">Moves the instruction pointer to the beginning of this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Skip`|<span data-ttu-id="3f9c1-110">从当前位置开始，将指令指针向前移动指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="3f9c1-110">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3f9c1-111">要求</span><span class="sxs-lookup"><span data-stu-id="3f9c1-111">Requirements</span></span>  

 <span data-ttu-id="3f9c1-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9c1-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f9c1-113">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="3f9c1-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="3f9c1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f9c1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f9c1-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f9c1-115">See also</span></span>

- [<span data-ttu-id="3f9c1-116">合成接口</span><span class="sxs-lookup"><span data-stu-id="3f9c1-116">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="3f9c1-117">IReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="3f9c1-117">IReferenceIdentity Interface</span></span>](ireferenceidentity-interface.md)
