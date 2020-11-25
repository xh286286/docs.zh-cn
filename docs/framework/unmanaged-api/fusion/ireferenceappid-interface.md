---
title: IReferenceAppId 接口
ms.date: 03/30/2017
api_name:
- IReferenceAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceAppId
helpviewer_keywords:
- IReferenceAppId interface [.NET Framework fusion]
ms.assetid: 8eb9e565-f358-43ce-900e-a8f8a5aa6cfb
topic_type:
- apiref
ms.openlocfilehash: 9aa7173d81d84d9080d90b0890769ffeaee6a738
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728610"
---
# <a name="ireferenceappid-interface"></a><span data-ttu-id="60842-102">IReferenceAppId 接口</span><span class="sxs-lookup"><span data-stu-id="60842-102">IReferenceAppId Interface</span></span>

<span data-ttu-id="60842-103">表示对当前范围内的应用程序的唯一标识符的引用。</span><span class="sxs-lookup"><span data-stu-id="60842-103">Represents a reference to the unique identifier for the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="60842-104">方法</span><span class="sxs-lookup"><span data-stu-id="60842-104">Methods</span></span>  
  
|<span data-ttu-id="60842-105">方法</span><span class="sxs-lookup"><span data-stu-id="60842-105">Method</span></span>|<span data-ttu-id="60842-106">说明</span><span class="sxs-lookup"><span data-stu-id="60842-106">Description</span></span>|  
|------------|-----------------|  
|`IReferenceAppId::get_CodeBase`|<span data-ttu-id="60842-107">获取一个指针，该指针指向由此引用的应用程序的代码标识符的字符串表示形式 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="60842-107">Gets a pointer to a string representation of the code identifier for the application referenced by this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::put_CodeBase`|<span data-ttu-id="60842-108">设置由此引用的应用程序的代码标识符 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="60842-108">Sets the code identifier for the application referenced by this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::EnumAppPath`|<span data-ttu-id="60842-109">获取一个接口指针，该指针指向一个 `IEnumReferenceIdentity` 实例，该实例包含 `IReferenceIdentity` 表示此的成员的实例 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="60842-109">Gets an interface pointer to an `IEnumReferenceIdentity` instance containing the `IReferenceIdentity` instances that represent members of this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::get_SubscriptionId`|<span data-ttu-id="60842-110">获取一个指针，该指针指向此的订阅的标记标识符的字符串表示形式 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="60842-110">Gets a pointer to a string representation of the token identifier for a subscription to this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::put_SubscriptionId`|<span data-ttu-id="60842-111">将此订阅的标记标识符设置为 `IReferenceAppId` 指定的字符串值。</span><span class="sxs-lookup"><span data-stu-id="60842-111">Sets the token identifier for a subscription to this `IReferenceAppId` to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="60842-112">要求</span><span class="sxs-lookup"><span data-stu-id="60842-112">Requirements</span></span>  

 <span data-ttu-id="60842-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="60842-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60842-114">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="60842-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="60842-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60842-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60842-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="60842-116">See also</span></span>

- [<span data-ttu-id="60842-117">合成接口</span><span class="sxs-lookup"><span data-stu-id="60842-117">Fusion Interfaces</span></span>](fusion-interfaces.md)
- [<span data-ttu-id="60842-118">IEnumReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="60842-118">IEnumReferenceIdentity Interface</span></span>](ienumreferenceidentity-interface.md)
- [<span data-ttu-id="60842-119">IReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="60842-119">IReferenceIdentity Interface</span></span>](ireferenceidentity-interface.md)
