---
title: CorNotificationForTokenMovement 枚举
ms.date: 03/30/2017
api_name:
- CorNotificationForTokenMovement
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNotificationForTokenMovement
helpviewer_keywords:
- CorNotificationForTokenMovement enumeration [.NET Framework metadata]
ms.assetid: 1edd1670-976a-4fc8-bef7-7c41e60ad989
topic_type:
- apiref
ms.openlocfilehash: 0f9cb8db35a1669cead6f9f26c9a89e063628dd8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687666"
---
# <a name="cornotificationfortokenmovement-enumeration"></a><span data-ttu-id="4a2fc-102">CorNotificationForTokenMovement 枚举</span><span class="sxs-lookup"><span data-stu-id="4a2fc-102">CorNotificationForTokenMovement Enumeration</span></span>

<span data-ttu-id="4a2fc-103">指定在进行标记重新映射时将发送到元数据 API 客户端的通知。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-103">Specifies the notifications that will be sent to the metadata API client when a token remap occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a2fc-104">语法</span><span class="sxs-lookup"><span data-stu-id="4a2fc-104">Syntax</span></span>  
  
```cpp  
typedef enum CorNotificationForTokenMovement {  
  
    MDNotifyDefault             = 0x0000000f,  
    MDNotifyAll                 = 0xffffffff,  
    MDNotifyNone                = 0x00000000,  
    MDNotifyMethodDef           = 0x00000001,  
    MDNotifyMemberRef           = 0x00000002,  
    MDNotifyFieldDef            = 0x00000004,  
    MDNotifyTypeRef             = 0x00000008,  
  
    MDNotifyTypeDef             = 0x00000010,  
    MDNotifyParamDef            = 0x00000020,  
    MDNotifyInterfaceImpl       = 0x00000040,  
    MDNotifyProperty            = 0x00000080,  
    MDNotifyEvent               = 0x00000100,  
    MDNotifySignature           = 0x00000200,  
    MDNotifyTypeSpec            = 0x00000400,  
    MDNotifyCustomAttribute     = 0x00000800,  
    MDNotifySecurityValue       = 0x00001000,  
    MDNotifyPermission          = 0x00002000,  
    MDNotifyModuleRef           = 0x00004000,  
  
    MDNotifyNameSpace           = 0x00008000,  
  
    MDNotifyAssemblyRef         = 0x01000000,  
    MDNotifyFile                = 0x02000000,  
    MDNotifyExportedType        = 0x04000000,  
    MDNotifyResource            = 0x08000000  
  
} CorNotificationForTokenMovement;  
```  
  
## <a name="members"></a><span data-ttu-id="4a2fc-105">成员</span><span class="sxs-lookup"><span data-stu-id="4a2fc-105">Members</span></span>  
  
|<span data-ttu-id="4a2fc-106">成员</span><span class="sxs-lookup"><span data-stu-id="4a2fc-106">Member</span></span>|<span data-ttu-id="4a2fc-107">说明</span><span class="sxs-lookup"><span data-stu-id="4a2fc-107">Description</span></span>|  
|------------|-----------------|  
|`MDNotifyDefault`|<span data-ttu-id="4a2fc-108">当 `mdTypeRef` 、、 `mdMethodDef` `mdMemberRef` 或 `mdFieldDef` 标记移动时通知。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-108">Notify when `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, or `mdFieldDef` tokens move.</span></span>|  
|`MDNotifyAll`|<span data-ttu-id="4a2fc-109">任何标记移动时发出通知。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-109">Notify when any token moves.</span></span>|  
|`MDNotifyNone`|<span data-ttu-id="4a2fc-110">标记移动时不发出通知。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-110">Do not notify when tokens move.</span></span>|  
|`MDNotifyMethodDef`|<span data-ttu-id="4a2fc-111">移动令牌时发出通知 `mdMethodDef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-111">Notify when an `mdMethodDef` token moves.</span></span>|  
|`MDNotifyMemberRef`|<span data-ttu-id="4a2fc-112">移动令牌时发出通知 `mdMemberRef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-112">Notify when an `mdMemberRef` token moves.</span></span>|  
|`MDNotifyFieldDef`|<span data-ttu-id="4a2fc-113">移动令牌时发出通知 `mdFieldDef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-113">Notify when an `mdFieldDef` token moves.</span></span>|  
|`MDNotifyTypeRef`|<span data-ttu-id="4a2fc-114">移动令牌时发出通知 `mdTypeRef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-114">Notify when an `mdTypeRef` token moves.</span></span>|  
|`MDNotifyTypeDef`|<span data-ttu-id="4a2fc-115">移动令牌时发出通知 `mdTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-115">Notify when an `mdTypeDef` token moves.</span></span>|  
|`MDNotifyParamDef`|<span data-ttu-id="4a2fc-116">移动令牌时发出通知 `mdParamDef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-116">Notify when an `mdParamDef` token moves.</span></span>|  
|`MDNotifyInterfaceImpl`|<span data-ttu-id="4a2fc-117">移动令牌时发出通知 `mdInterfaceImpl` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-117">Notify when an `mdInterfaceImpl` token moves.</span></span>|  
|`MDNotifyProperty`|<span data-ttu-id="4a2fc-118">移动令牌时发出通知 `mdProperty` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-118">Notify when an `mdProperty` token moves.</span></span>|  
|`MDNotifyEvent`|<span data-ttu-id="4a2fc-119">移动令牌时发出通知 `mdEvent` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-119">Notify when an `mdEvent` token moves.</span></span>|  
|`MDNotifySignature`|<span data-ttu-id="4a2fc-120">移动令牌时发出通知 `mdSignature` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-120">Notify when an `mdSignature` token moves.</span></span>|  
|`MDNotifyTypeSpec`|<span data-ttu-id="4a2fc-121">移动令牌时发出通知 `mdTypeSpec` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-121">Notify when an `mdTypeSpec` token moves.</span></span>|  
|`MDNotifyCustomAttribute`|<span data-ttu-id="4a2fc-122">移动令牌时发出通知 `mdCustomAttribute` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-122">Notify when an `mdCustomAttribute` token moves.</span></span>|  
|`MDNotifySecurityValue`|<span data-ttu-id="4a2fc-123">移动令牌时发出通知 `mdSecurityValue` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-123">Notify when an `mdSecurityValue` token moves.</span></span>|  
|`MDNotifyPermission`|<span data-ttu-id="4a2fc-124">移动令牌时发出通知 `mdPermission` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-124">Notify when an `mdPermission` token moves.</span></span>|  
|`MDNotifyModuleRef`|<span data-ttu-id="4a2fc-125">移动令牌时发出通知 `mdModuleRef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-125">Notify when an `mdModuleRef` token moves.</span></span>|  
|`MDNotifyNameSpace`|<span data-ttu-id="4a2fc-126">移动令牌时发出通知 `mdNameSpace` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-126">Notify when an `mdNameSpace` token moves.</span></span>|  
|`MDNotifyAssemblyRef`|<span data-ttu-id="4a2fc-127">移动令牌时发出通知 `mdAssemblyRef` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-127">Notify when an `mdAssemblyRef` token moves.</span></span>|  
|`MDNotifyFile`|<span data-ttu-id="4a2fc-128">移动令牌时发出通知 `mdFile` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-128">Notify when an `mdFile` token moves.</span></span>|  
|`MDNotifyExportedType`|<span data-ttu-id="4a2fc-129">移动令牌时发出通知 `mdExportedType` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-129">Notify when an `mdExportedType` token moves.</span></span>|  
|`MDNotifyResource`|<span data-ttu-id="4a2fc-130">移动令牌时发出通知 `mdManifestResource` 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-130">Notify when an `mdManifestResource` token moves.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4a2fc-131">注解</span><span class="sxs-lookup"><span data-stu-id="4a2fc-131">Remarks</span></span>  

 <span data-ttu-id="4a2fc-132">标记可以重新映射 (即，在元数据合并期间移动) 。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-132">A token may be re-mapped (that is, moved) during a metadata merge.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a2fc-133">要求</span><span class="sxs-lookup"><span data-stu-id="4a2fc-133">Requirements</span></span>  

 <span data-ttu-id="4a2fc-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2fc-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a2fc-135">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="4a2fc-135">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="4a2fc-136">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a2fc-136">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a2fc-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a2fc-137">See also</span></span>

- [<span data-ttu-id="4a2fc-138">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="4a2fc-138">Metadata Enumerations</span></span>](metadata-enumerations.md)
