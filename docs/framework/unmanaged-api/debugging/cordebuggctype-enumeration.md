---
title: CorDebugGCType 枚举
ms.date: 03/30/2017
api_name:
- CorDebugGCType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGCType
helpviewer_keywords:
- CorDebugGCType enumeration [.NET Framework debugging]
ms.assetid: 880ca92a-42d4-42a5-9b9c-c2848eb39c6a
topic_type:
- apiref
ms.openlocfilehash: 6b3075613af0403527ecf67d574c0f5733a5cd8b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712607"
---
# <a name="cordebuggctype-enumeration"></a><span data-ttu-id="04e24-102">CorDebugGCType 枚举</span><span class="sxs-lookup"><span data-stu-id="04e24-102">CorDebugGCType Enumeration</span></span>

<span data-ttu-id="04e24-103">指示垃圾回收器是在工作站还是服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="04e24-103">Indicates whether the garbage collector is running on a workstation or a server.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04e24-104">语法</span><span class="sxs-lookup"><span data-stu-id="04e24-104">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugGCType {  
    CorDebugWorkstationGC  = 0,  
    CorDebugServerGC       = ( CorDebugWorkstationGC + 1 )  
} CorDebugGCType;  
```  
  
## <a name="parameters"></a><span data-ttu-id="04e24-105">参数</span><span class="sxs-lookup"><span data-stu-id="04e24-105">Parameters</span></span>  
  
## <a name="members"></a><span data-ttu-id="04e24-106">成员</span><span class="sxs-lookup"><span data-stu-id="04e24-106">Members</span></span>  
  
|<span data-ttu-id="04e24-107">成员名称</span><span class="sxs-lookup"><span data-stu-id="04e24-107">Member name</span></span>|<span data-ttu-id="04e24-108">说明</span><span class="sxs-lookup"><span data-stu-id="04e24-108">Description</span></span>|  
|-----------------|-----------------|  
|`CorDebugWorkstationGC`|<span data-ttu-id="04e24-109">垃圾回收器正在工作站上运行。</span><span class="sxs-lookup"><span data-stu-id="04e24-109">The garbage collector is running on a workstation.</span></span>|  
|`CorDebugServerGC`|<span data-ttu-id="04e24-110">垃圾回收器正在服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="04e24-110">The garbage collector is running on a server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="04e24-111">备注</span><span class="sxs-lookup"><span data-stu-id="04e24-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04e24-112">要求</span><span class="sxs-lookup"><span data-stu-id="04e24-112">Requirements</span></span>  

 <span data-ttu-id="04e24-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="04e24-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04e24-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="04e24-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="04e24-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="04e24-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="04e24-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04e24-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04e24-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04e24-117">See also</span></span>

- [<span data-ttu-id="04e24-118">调试枚举</span><span class="sxs-lookup"><span data-stu-id="04e24-118">Debugging Enumerations</span></span>](debugging-enumerations.md)
