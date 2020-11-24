---
title: CorCheckDuplicatesFor 枚举
ms.date: 03/30/2017
api_name:
- CorCheckDuplicatesFor
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCheckDuplicatesFor
helpviewer_keywords:
- CorCheckDuplicatesFor enumeration [.NET Framework metadata]
ms.assetid: d8ec8d3c-70f7-4cc6-9957-68068fd8f49c
topic_type:
- apiref
ms.openlocfilehash: 4acdfd6df410f229a002fa191ef24766748a1262
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95672352"
---
# <a name="corcheckduplicatesfor-enumeration"></a><span data-ttu-id="c0d3f-102">CorCheckDuplicatesFor 枚举</span><span class="sxs-lookup"><span data-stu-id="c0d3f-102">CorCheckDuplicatesFor Enumeration</span></span>

<span data-ttu-id="c0d3f-103">指定将检查重复项的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-103">Specifies the metadata tokens that will be checked for duplicates.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0d3f-104">语法</span><span class="sxs-lookup"><span data-stu-id="c0d3f-104">Syntax</span></span>  
  
```cpp  
typedef enum CorCheckDuplicatesFor {  
  
    MDDupAll                    = 0xffffffff,  
    MDDupENC                    = MDDupAll,  
    MDNoDupChecks               = 0x00000000,  
    MDDupTypeDef                = 0x00000001,  
    MDDupInterfaceImpl          = 0x00000002,  
    MDDupMethodDef              = 0x00000004,  
    MDDupTypeRef                = 0x00000008,  
    MDDupMemberRef              = 0x00000010,  
    MDDupCustomAttribute        = 0x00000020,  
    MDDupParamDef               = 0x00000040,  
    MDDupPermission             = 0x00000080,  
    MDDupProperty               = 0x00000100,  
    MDDupEvent                  = 0x00000200,  
    MDDupFieldDef               = 0x00000400,  
    MDDupSignature              = 0x00000800,  
    MDDupModuleRef              = 0x00001000,  
    MDDupTypeSpec               = 0x00002000,  
    MDDupImplMap                = 0x00004000,  
    MDDupAssemblyRef            = 0x00008000,  
    MDDupFile                   = 0x00010000,  
    MDDupExportedType           = 0x00020000,  
    MDDupManifestResource       = 0x00040000,  
    MDDupGenericParam           = 0x00080000,  
    MDDupMethodSpec             = 0x00100000,  
    MDDupGenericParamConstraint = 0x00200000,  
  
    MDDupAssembly               = 0x10000000,  
  
    MDDupDefault =
        MDNoDupChecks | MDDupTypeRef | MDDupMemberRef |
        MDDupSignature | MDDupTypeSpec | MDDupMethodSpec  
  
} CorCheckDuplicatesFor;  
```  
  
## <a name="members"></a><span data-ttu-id="c0d3f-105">成员</span><span class="sxs-lookup"><span data-stu-id="c0d3f-105">Members</span></span>  
  
|<span data-ttu-id="c0d3f-106">成员</span><span class="sxs-lookup"><span data-stu-id="c0d3f-106">Member</span></span>|<span data-ttu-id="c0d3f-107">说明</span><span class="sxs-lookup"><span data-stu-id="c0d3f-107">Description</span></span>|  
|------------|-----------------|  
|`MDDupAll`|<span data-ttu-id="c0d3f-108">检查所有元数据标记的重复项。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-108">Check all metadata tokens for duplicates.</span></span>|  
|`MDDupENC`|<span data-ttu-id="c0d3f-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-109">Not used.</span></span>|  
|`MDNoDupChecks`|<span data-ttu-id="c0d3f-110">请勿检查重复项的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-110">Do not check metadata tokens for duplicates.</span></span>|  
|`MDDupTypeDef`|<span data-ttu-id="c0d3f-111">检查标记的重复项 `mdTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-111">Check for duplicates of `mdTypeDef` tokens.</span></span>|  
|`MDDupInterfaceImpl`|<span data-ttu-id="c0d3f-112">检查标记的重复项 `mdInterfaceImpl` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-112">Check for duplicates of `mdInterfaceImpl` tokens.</span></span>|  
|`MDDupMethodDef`|<span data-ttu-id="c0d3f-113">检查标记的重复项 `mdMethodDef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-113">Check for duplicates of `mdMethodDef` tokens.</span></span>|  
|`MDDupTypeRef`|<span data-ttu-id="c0d3f-114">检查标记的重复项 `mdTypeRef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-114">Check for duplicates of `mdTypeRef` tokens.</span></span>|  
|`MDDupMemberRef`|<span data-ttu-id="c0d3f-115">检查标记的重复项 `mdMemberRef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-115">Check for duplicates of `mdMemberRef` tokens.</span></span>|  
|`MDDupCustomAttribute`|<span data-ttu-id="c0d3f-116">检查标记的重复项 `mdCustomAttribute` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-116">Check for duplicates of `mdCustomAttribute` tokens.</span></span>|  
|`MDDupParamDef`|<span data-ttu-id="c0d3f-117">检查标记的重复项 `mdParamDef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-117">Check for duplicates of `mdParamDef` tokens.</span></span>|  
|`MDDupPermission`|<span data-ttu-id="c0d3f-118">检查标记的重复项 `mdPermission` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-118">Check for duplicates of `mdPermission` tokens.</span></span>|  
|`MDDupProperty`|<span data-ttu-id="c0d3f-119">检查标记的重复项 `mdProperty` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-119">Check for duplicates of `mdProperty` tokens.</span></span>|  
|`MDDupEvent`|<span data-ttu-id="c0d3f-120">检查标记的重复项 `mdEvent` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-120">Check for duplicates of `mdEvent` tokens.</span></span>|  
|`MDDupFieldDef`|<span data-ttu-id="c0d3f-121">检查标记的重复项 `mdFieldDef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-121">Check for duplicates of `mdFieldDef` tokens.</span></span>|  
|`MDDupSignature`|<span data-ttu-id="c0d3f-122">检查标记的重复项 `mdSignature` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-122">Check for duplicates of `mdSignature` tokens.</span></span>|  
|`MDDupModuleRef`|<span data-ttu-id="c0d3f-123">检查标记的重复项 `mdModuleRef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-123">Check for duplicates of `mdModuleRef` tokens.</span></span>|  
|`MDDupTypeSpec`|<span data-ttu-id="c0d3f-124">检查标记的重复项 `mdTypeSpec` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-124">Check for duplicates of `mdTypeSpec` tokens.</span></span>|  
|`MDDupImplMap`|<span data-ttu-id="c0d3f-125">检查标记的重复项 `mdImplMap` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-125">Check for duplicates of `mdImplMap` tokens.</span></span>|  
|`MDDupAssemblyRef`|<span data-ttu-id="c0d3f-126">检查标记的重复项 `mdAssemblyRef` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-126">Check for duplicates of `mdAssemblyRef` tokens.</span></span>|  
|`MDDupFile`|<span data-ttu-id="c0d3f-127">检查标记的重复项 `mdFile` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-127">Check for duplicates of `mdFile` tokens.</span></span>|  
|`MDDupExportedType`|<span data-ttu-id="c0d3f-128">检查标记的重复项 `mdExportedType` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-128">Check for duplicates of `mdExportedType` tokens.</span></span>|  
|`MDDupManifestResource`|<span data-ttu-id="c0d3f-129">检查标记的重复项 `mdManifestResource` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-129">Check for duplicates of `mdManifestResource` tokens.</span></span>|  
|`MDDupGenericParam`|<span data-ttu-id="c0d3f-130">检查标记的重复项 `mdGenericParam` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-130">Check for duplicates of `mdGenericParam` tokens.</span></span>|  
|`MDDupMethodSpec`|<span data-ttu-id="c0d3f-131">检查标记的重复项 `mdMethodSpec` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-131">Check for duplicates of `mdMethodSpec` tokens.</span></span>|  
|`MDDupGenericParamConstraint`|<span data-ttu-id="c0d3f-132">检查标记的重复项 `mdGenericParamConstraint` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-132">Check for duplicates of `mdGenericParamConstraint` tokens.</span></span>|  
|`MDDupAssembly`|<span data-ttu-id="c0d3f-133">检查标记的重复项 `mdAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-133">Check for duplicates of `mdAssembly` tokens.</span></span>|  
|`MDDupDefault`|<span data-ttu-id="c0d3f-134">检查、、、 `mdMemberRef` `mdTypeRef` `mdSignature` `mdTypeSpec` 和标记的重复项 `mdMethodSpec` 。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-134">Check for duplicates of `mdMemberRef`, `mdTypeRef`, `mdSignature`, `mdTypeSpec`, and `mdMethodSpec` tokens.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c0d3f-135">要求</span><span class="sxs-lookup"><span data-stu-id="c0d3f-135">Requirements</span></span>  

 <span data-ttu-id="c0d3f-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c0d3f-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0d3f-137">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="c0d3f-137">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="c0d3f-138">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0d3f-138">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0d3f-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0d3f-139">See also</span></span>

- [<span data-ttu-id="c0d3f-140">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="c0d3f-140">Metadata Enumerations</span></span>](metadata-enumerations.md)
