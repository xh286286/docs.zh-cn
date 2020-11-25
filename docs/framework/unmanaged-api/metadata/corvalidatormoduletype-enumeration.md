---
title: CorValidatorModuleType 枚举
ms.date: 03/30/2017
api_name:
- CorValidatorModuleType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorValidatorModuleType
helpviewer_keywords:
- CorValidatorModuleType enumeration [.NET Framework metadata]
ms.assetid: 748f1ab2-fbcb-4f55-89ec-8d23d81ebc80
topic_type:
- apiref
ms.openlocfilehash: 2fb7f11677870f7d53439f1867f167fabe70b22a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723839"
---
# <a name="corvalidatormoduletype-enumeration"></a><span data-ttu-id="3122a-102">CorValidatorModuleType 枚举</span><span class="sxs-lookup"><span data-stu-id="3122a-102">CorValidatorModuleType Enumeration</span></span>

<span data-ttu-id="3122a-103">指定模块的类型。</span><span class="sxs-lookup"><span data-stu-id="3122a-103">Specifies the type of a module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3122a-104">语法</span><span class="sxs-lookup"><span data-stu-id="3122a-104">Syntax</span></span>  
  
```cpp  
typedef enum  
{  
    ValidatorModuleTypeInvalid  = 0x0,  
    ValidatorModuleTypeMin      = 0x00000001,  
    ValidatorModuleTypePE       = 0x00000001,  
    ValidatorModuleTypeObj      = 0x00000002,  
    ValidatorModuleTypeEnc      = 0x00000003,  
    ValidatorModuleTypeIncr     = 0x00000004,  
    ValidatorModuleTypeMax      = 0x00000004  
} CorValidatorModuleType;  
```  
  
## <a name="members"></a><span data-ttu-id="3122a-105">成员</span><span class="sxs-lookup"><span data-stu-id="3122a-105">Members</span></span>  
  
|<span data-ttu-id="3122a-106">成员</span><span class="sxs-lookup"><span data-stu-id="3122a-106">Member</span></span>|<span data-ttu-id="3122a-107">说明</span><span class="sxs-lookup"><span data-stu-id="3122a-107">Description</span></span>|  
|------------|-----------------|  
|`ValidatorModuleTypeInvalid`|<span data-ttu-id="3122a-108">模块是无效类型。</span><span class="sxs-lookup"><span data-stu-id="3122a-108">The module is an invalid type.</span></span>|  
|`ValidatorModuleTypeMin`|<span data-ttu-id="3122a-109">枚举的最小值 `CorValidatorModuleType` 。</span><span class="sxs-lookup"><span data-stu-id="3122a-109">The minimum value of the `CorValidatorModuleType` enum.</span></span>|  
|`ValidatorModuleTypePE`|<span data-ttu-id="3122a-110">模块是可移植的可执行文件 (PE) 文件。</span><span class="sxs-lookup"><span data-stu-id="3122a-110">The module is a portable executable (PE) file.</span></span>|  
|`ValidatorModuleTypeObj`|<span data-ttu-id="3122a-111">模块是 .obj 文件。</span><span class="sxs-lookup"><span data-stu-id="3122a-111">The module is a .obj file.</span></span>|  
|`ValidatorModuleTypeEnc`|<span data-ttu-id="3122a-112">模块是 "编辑并继续" 调试器会话。</span><span class="sxs-lookup"><span data-stu-id="3122a-112">The module is an edit-and-continue debugger session.</span></span>|  
|`ValidatorModuleTypeIncr`|<span data-ttu-id="3122a-113">模块是增量生成的模块。</span><span class="sxs-lookup"><span data-stu-id="3122a-113">The module is one that has been incrementally built.</span></span>|  
|`ValidatorModuleTypeMax`|<span data-ttu-id="3122a-114">枚举的最大值 `CorValidatorModuleType` 。</span><span class="sxs-lookup"><span data-stu-id="3122a-114">The maximum value of the `CorValidatorModuleType` enum.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3122a-115">要求</span><span class="sxs-lookup"><span data-stu-id="3122a-115">Requirements</span></span>  

 <span data-ttu-id="3122a-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3122a-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3122a-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3122a-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3122a-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3122a-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3122a-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3122a-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3122a-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3122a-120">See also</span></span>

- [<span data-ttu-id="3122a-121">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="3122a-121">Metadata Enumerations</span></span>](metadata-enumerations.md)
