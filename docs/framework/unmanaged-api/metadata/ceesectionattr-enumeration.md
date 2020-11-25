---
title: CeeSectionAttr 枚举
ms.date: 03/30/2017
api_name:
- CeeSectionAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CeeSectionAttr
helpviewer_keywords:
- CeeSectionAttr enumeration [.NET Framework metadata]
ms.assetid: 0db51881-b869-4677-a715-1726a9216489
topic_type:
- apiref
ms.openlocfilehash: 4b2fb80298f6eef331b5b7ae4a46222ce97ede6f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732731"
---
# <a name="ceesectionattr-enumeration"></a><span data-ttu-id="24ecd-102">CeeSectionAttr 枚举</span><span class="sxs-lookup"><span data-stu-id="24ecd-102">CeeSectionAttr Enumeration</span></span>

<span data-ttu-id="24ecd-103">提供指定节的属性的值，供 [ICeeGen](iceegen-interface.md) 接口使用。</span><span class="sxs-lookup"><span data-stu-id="24ecd-103">Provides values that specify attributes of a section for use by the [ICeeGen](iceegen-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24ecd-104">语法</span><span class="sxs-lookup"><span data-stu-id="24ecd-104">Syntax</span></span>  
  
```cpp  
typedef enum  {  
    sdNone      = 0,  
    sdReadOnly  = IMAGE_SCN_CNT_INITIALIZED_DATA |  
                  IMAGE_SCN_MEM_READ,  
    sdReadWrite = sdReadOnly | IMAGE_SCN_MEM_WRITE,  
    sdExecute   = IMAGE_SCN_MEM_READ | IMAGE_SCN_CNT_CODE |  
                  IMAGE_SCN_MEM_EXECUTE  
} CeeSectionAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="24ecd-105">成员</span><span class="sxs-lookup"><span data-stu-id="24ecd-105">Members</span></span>  
  
|<span data-ttu-id="24ecd-106">成员</span><span class="sxs-lookup"><span data-stu-id="24ecd-106">Member</span></span>|<span data-ttu-id="24ecd-107">说明</span><span class="sxs-lookup"><span data-stu-id="24ecd-107">Description</span></span>|  
|------------|-----------------|  
|`sdNone`|<span data-ttu-id="24ecd-108">节没有特性。</span><span class="sxs-lookup"><span data-stu-id="24ecd-108">Section has no attributes.</span></span>|  
|`sdReadOnly`|<span data-ttu-id="24ecd-109">部分包含初始化的数据，该数据只能读取，而不是更新。</span><span class="sxs-lookup"><span data-stu-id="24ecd-109">Section contains initialized data that can be only read, not updated.</span></span>|  
|`sdReadWrite`|<span data-ttu-id="24ecd-110">节包含可读取或更新的初始化数据。</span><span class="sxs-lookup"><span data-stu-id="24ecd-110">Section contains initialized data that can be read or updated.</span></span>|  
|`sdExecute`|<span data-ttu-id="24ecd-111">部分包含允许读取和执行的可执行代码。</span><span class="sxs-lookup"><span data-stu-id="24ecd-111">Section contains executable code that is allowed to be read and executed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="24ecd-112">要求</span><span class="sxs-lookup"><span data-stu-id="24ecd-112">Requirements</span></span>  

 <span data-ttu-id="24ecd-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24ecd-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24ecd-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="24ecd-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="24ecd-115">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="24ecd-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="24ecd-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24ecd-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24ecd-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24ecd-117">See also</span></span>

- [<span data-ttu-id="24ecd-118">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="24ecd-118">Metadata Enumerations</span></span>](metadata-enumerations.md)
