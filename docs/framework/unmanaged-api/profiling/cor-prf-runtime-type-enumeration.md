---
title: COR_PRF_RUNTIME_TYPE 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_RUNTIME_TYPE Enumeration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_RUNTIME_TYPE
helpviewer_keywords:
- COR_PRF_RUNTIME_TYPE enumeration [.NET Framework profiling]
ms.assetid: 35449514-333f-4918-9c60-7aa198d655d2
topic_type:
- apiref
ms.openlocfilehash: b599a97f414491ff80000f99551a727b86ae13de
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696747"
---
# <a name="cor_prf_runtime_type-enumeration"></a><span data-ttu-id="b474e-102">COR_PRF_RUNTIME_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="b474e-102">COR_PRF_RUNTIME_TYPE Enumeration</span></span>

<span data-ttu-id="b474e-103">包含一些值，这些值指示公共语言运行时的版本 (CLR) ： desktop 或 CoreCLR，用于 Silverlight。</span><span class="sxs-lookup"><span data-stu-id="b474e-103">Contains values that indicate the version of the common language runtime (CLR): desktop or CoreCLR, which is used in Silverlight.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b474e-104">语法</span><span class="sxs-lookup"><span data-stu-id="b474e-104">Syntax</span></span>  
  
```cpp  
typedef enum  
{  
    COR_PRF_DESKTOP_CLR = 0x1,  
    COR_PRF_CORE_CLR    = 0x2,  
} COR_PRF_RUNTIME_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="b474e-105">成员</span><span class="sxs-lookup"><span data-stu-id="b474e-105">Members</span></span>  
  
|<span data-ttu-id="b474e-106">成员</span><span class="sxs-lookup"><span data-stu-id="b474e-106">Member</span></span>|<span data-ttu-id="b474e-107">说明</span><span class="sxs-lookup"><span data-stu-id="b474e-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_DESKTOP_CLR`|<span data-ttu-id="b474e-108">CLR 的桌面版本。</span><span class="sxs-lookup"><span data-stu-id="b474e-108">The desktop version of the CLR.</span></span>|  
|`COR_PRF_CORE_CLR`|<span data-ttu-id="b474e-109">Silverlight 中使用的 CLR 核心版本。</span><span class="sxs-lookup"><span data-stu-id="b474e-109">The core version of the CLR, used in Silverlight.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b474e-110">备注</span><span class="sxs-lookup"><span data-stu-id="b474e-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b474e-111">要求</span><span class="sxs-lookup"><span data-stu-id="b474e-111">Requirements</span></span>  

 <span data-ttu-id="b474e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b474e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b474e-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b474e-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b474e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b474e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b474e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b474e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b474e-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b474e-116">See also</span></span>

- [<span data-ttu-id="b474e-117">分析枚举</span><span class="sxs-lookup"><span data-stu-id="b474e-117">Profiling Enumerations</span></span>](profiling-enumerations.md)
