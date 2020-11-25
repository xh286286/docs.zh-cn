---
title: CeeSectionRelocExtra 联合
ms.date: 03/30/2017
api_name:
- CeeSectionRelocExtra Union
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CeeSectionRelocExtra
helpviewer_keywords:
- CeeSectionRelocExtra union [.NET Framework metadata]
ms.assetid: d9568cf6-7f98-4cd6-ab36-0a2bd509afcc
topic_type:
- apiref
ms.openlocfilehash: d5f61aa9b4a65a5f33e64aa4441370c3f7ca5b03
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732718"
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="f55e0-102">CeeSectionRelocExtra 联合</span><span class="sxs-lookup"><span data-stu-id="f55e0-102">CeeSectionRelocExtra Union</span></span>

<span data-ttu-id="f55e0-103">表示 [ICeeGen](iceegen-interface.md) 接口用于重定位节的地址偏移量。</span><span class="sxs-lookup"><span data-stu-id="f55e0-103">Represents an address offset that is used by the [ICeeGen](iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f55e0-104">语法</span><span class="sxs-lookup"><span data-stu-id="f55e0-104">Syntax</span></span>  
  
```cpp  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="f55e0-105">成员</span><span class="sxs-lookup"><span data-stu-id="f55e0-105">Members</span></span>  
  
|<span data-ttu-id="f55e0-106">成员</span><span class="sxs-lookup"><span data-stu-id="f55e0-106">Member</span></span>|<span data-ttu-id="f55e0-107">说明</span><span class="sxs-lookup"><span data-stu-id="f55e0-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="f55e0-108">部分的大小上限。</span><span class="sxs-lookup"><span data-stu-id="f55e0-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f55e0-109">要求</span><span class="sxs-lookup"><span data-stu-id="f55e0-109">Requirements</span></span>  

 <span data-ttu-id="f55e0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f55e0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f55e0-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f55e0-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f55e0-112">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f55e0-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f55e0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f55e0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f55e0-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f55e0-114">See also</span></span>

- [<span data-ttu-id="f55e0-115">元数据联合</span><span class="sxs-lookup"><span data-stu-id="f55e0-115">Metadata Unions</span></span>](metadata-unions.md)
