---
title: CorNativeLinkType 枚举
ms.date: 03/30/2017
api_name:
- CorNativeLinkType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNativeLinkType
helpviewer_keywords:
- CorNativeLinkType enumeration [.NET Framework metadata]
ms.assetid: 4f86ff37-2dab-4e64-819a-76b3bfe828ff
topic_type:
- apiref
ms.openlocfilehash: c155373f7da47e904c94a44efa2fba42309d4218
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671351"
---
# <a name="cornativelinktype-enumeration"></a><span data-ttu-id="23239-102">CorNativeLinkType 枚举</span><span class="sxs-lookup"><span data-stu-id="23239-102">CorNativeLinkType Enumeration</span></span>

<span data-ttu-id="23239-103">提供一些值，用于指示本机代码中链接的类型。</span><span class="sxs-lookup"><span data-stu-id="23239-103">Provides values that indicate the type linked in native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23239-104">语法</span><span class="sxs-lookup"><span data-stu-id="23239-104">Syntax</span></span>  
  
```cpp  
typedef enum
{  
    nltNone       = 1,  
    nltAnsi       = 2,  
    nltUnicode    = 3,  
    nltAuto       = 4,  
    nltOle        = 5,  
    nltMaxValue   = 7  
} CorNativeLinkType;  
```  
  
## <a name="members"></a><span data-ttu-id="23239-105">成员</span><span class="sxs-lookup"><span data-stu-id="23239-105">Members</span></span>  
  
|<span data-ttu-id="23239-106">成员</span><span class="sxs-lookup"><span data-stu-id="23239-106">Member</span></span>|<span data-ttu-id="23239-107">说明</span><span class="sxs-lookup"><span data-stu-id="23239-107">Description</span></span>|  
|------------|-----------------|  
|`nltNone`|<span data-ttu-id="23239-108">指示未指定任何关键字。</span><span class="sxs-lookup"><span data-stu-id="23239-108">Indicates that none of the keywords are specified.</span></span>|  
|`nltAnsi`|<span data-ttu-id="23239-109">指示指定了 ANSI 关键字。</span><span class="sxs-lookup"><span data-stu-id="23239-109">Indicates that an ANSI keyword is specified.</span></span>|  
|`nltUnicode`|<span data-ttu-id="23239-110">指示指定了 Unicode 关键字</span><span class="sxs-lookup"><span data-stu-id="23239-110">Indicates that a Unicode keyword is specified</span></span>|  
|`nltAuto`|<span data-ttu-id="23239-111">指示指定了 auto 关键字。</span><span class="sxs-lookup"><span data-stu-id="23239-111">Indicates that an auto keyword is specified.</span></span>|  
|`nltOle`|<span data-ttu-id="23239-112">指示指定了 OLE 关键字。</span><span class="sxs-lookup"><span data-stu-id="23239-112">Indicates that an OLE keyword is specified.</span></span>|  
|`nltMaxValue`|<span data-ttu-id="23239-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="23239-113">Not used.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="23239-114">要求</span><span class="sxs-lookup"><span data-stu-id="23239-114">Requirements</span></span>  

 <span data-ttu-id="23239-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="23239-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="23239-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="23239-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="23239-117">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="23239-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="23239-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="23239-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23239-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23239-119">See also</span></span>

- [<span data-ttu-id="23239-120">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="23239-120">Metadata Enumerations</span></span>](metadata-enumerations.md)
