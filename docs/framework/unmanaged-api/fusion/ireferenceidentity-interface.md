---
title: IReferenceIdentity 接口
ms.date: 03/30/2017
api_name:
- IReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceIdentity
helpviewer_keywords:
- IReferenceIdentity interface [.NET Framework fusion]
ms.assetid: 9180ac5a-7019-4716-9f83-8a91d157239a
topic_type:
- apiref
ms.openlocfilehash: 867c09caa3bd3aed50de21c2ef91a02782830be2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95704547"
---
# <a name="ireferenceidentity-interface"></a><span data-ttu-id="5300c-102">IReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="5300c-102">IReferenceIdentity Interface</span></span>

<span data-ttu-id="5300c-103">表示对代码对象的唯一签名的引用。</span><span class="sxs-lookup"><span data-stu-id="5300c-103">Represents a reference to the unique signature of a code object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5300c-104">方法</span><span class="sxs-lookup"><span data-stu-id="5300c-104">Methods</span></span>  
  
|<span data-ttu-id="5300c-105">方法</span><span class="sxs-lookup"><span data-stu-id="5300c-105">Method</span></span>|<span data-ttu-id="5300c-106">说明</span><span class="sxs-lookup"><span data-stu-id="5300c-106">Description</span></span>|  
|------------|-----------------|  
|`IReferenceIdentity::Clone`|<span data-ttu-id="5300c-107">获取一个指向与 `IReferenceIdentity` 此相同的新实例的接口指针 `IReferenceIdentity` ，指定的特性更改除外。</span><span class="sxs-lookup"><span data-stu-id="5300c-107">Gets an interface pointer to a new `IReferenceIdentity` instance that is identical to this `IReferenceIdentity`, except for the specified attribute changes.</span></span>|  
|`IReferenceIdentity::EnumAttributes`|<span data-ttu-id="5300c-108">获取一个接口指针，该指针指向 `IEnumIDENTITY_ATTRIBUTE` 包含与此关联的特性的实例 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="5300c-108">Gets an interface pointer to an `IEnumIDENTITY_ATTRIBUTE` instance that contains the attributes associated with this `IReferenceIdentity`.</span></span>|  
|`IReferenceIdentity::GetAttribute`|<span data-ttu-id="5300c-109">获取指定命名空间中具有指定名称的特性的值。</span><span class="sxs-lookup"><span data-stu-id="5300c-109">Gets the value of the attribute in the specified namespace, with the specified name.</span></span>|  
|`IReferenceIdentity::SetAttribute`|<span data-ttu-id="5300c-110">将具有指定命名空间和指定名称的特性设置为指定值。</span><span class="sxs-lookup"><span data-stu-id="5300c-110">Sets the attribute that has the specified namespace and the specified name to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5300c-111">要求</span><span class="sxs-lookup"><span data-stu-id="5300c-111">Requirements</span></span>  

 <span data-ttu-id="5300c-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5300c-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5300c-113">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="5300c-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="5300c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5300c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5300c-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5300c-115">See also</span></span>

- [<span data-ttu-id="5300c-116">合成接口</span><span class="sxs-lookup"><span data-stu-id="5300c-116">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="5300c-117">IEnumIDENTITY_ATTRIBUTE 接口</span><span class="sxs-lookup"><span data-stu-id="5300c-117">IEnumIDENTITY_ATTRIBUTE Interface</span></span>](ienumidentity-attribute-interface.md)
