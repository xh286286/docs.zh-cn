---
title: CLSID_RESOLUTION_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- CLSID_RESOLUTION_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLSID_RESOLUTION_FLAGS
helpviewer_keywords:
- CLSID_RESOLUTION_FLAGS enumeration [.NET Framework hosting]
ms.assetid: cd8b9879-962a-4811-aa46-2e2b6bae0d84
topic_type:
- apiref
ms.openlocfilehash: 19731f34d259757e6de62dd4b4f0d4735d1c2e61
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706159"
---
# <a name="clsid_resolution_flags-enumeration"></a><span data-ttu-id="01c87-102">CLSID_RESOLUTION_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="01c87-102">CLSID_RESOLUTION_FLAGS Enumeration</span></span>

<span data-ttu-id="01c87-103">包含指示公共语言运行时 (CLR) 应如何解析的值 `CLSID` 。</span><span class="sxs-lookup"><span data-stu-id="01c87-103">Contains values that indicate how the common language runtime (CLR) should resolve a `CLSID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01c87-104">语法</span><span class="sxs-lookup"><span data-stu-id="01c87-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    CLSID_RESOLUTION_DEFAULT      = 0x0,  
    CLSID_RESOLUTION_REGISTERED   = 0x1  
} CLSID_RESOLUTION_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="01c87-105">成员</span><span class="sxs-lookup"><span data-stu-id="01c87-105">Members</span></span>  
  
|<span data-ttu-id="01c87-106">成员</span><span class="sxs-lookup"><span data-stu-id="01c87-106">Member</span></span>|<span data-ttu-id="01c87-107">说明</span><span class="sxs-lookup"><span data-stu-id="01c87-107">Description</span></span>|  
|------------|-----------------|  
|`CLSID_RESOLUTION_DEFAULT`|<span data-ttu-id="01c87-108">指示默认行为。</span><span class="sxs-lookup"><span data-stu-id="01c87-108">Indicates the default behavior.</span></span>|  
|`CLSID_RESOLUTION_REGISTERED`|<span data-ttu-id="01c87-109">指示运行时搜索注册表并应用填充码策略。</span><span class="sxs-lookup"><span data-stu-id="01c87-109">Indicates that the runtime searches the registry and applies shim policy.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="01c87-110">要求</span><span class="sxs-lookup"><span data-stu-id="01c87-110">Requirements</span></span>  

 <span data-ttu-id="01c87-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="01c87-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01c87-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="01c87-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="01c87-113">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01c87-113">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01c87-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01c87-114">See also</span></span>

- [<span data-ttu-id="01c87-115">承载枚举</span><span class="sxs-lookup"><span data-stu-id="01c87-115">Hosting Enumerations</span></span>](hosting-enumerations.md)
