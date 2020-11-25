---
title: CorSaveSize 枚举
ms.date: 03/30/2017
api_name:
- CorSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSaveSize
helpviewer_keywords:
- CorSaveSize enumeration [.NET Framework metadata]
ms.assetid: eb95ce39-5688-43c1-a34d-578794b32faa
topic_type:
- apiref
ms.openlocfilehash: 81d47a3e4d72f991dc15924e7ff1ecc8df2e7322
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706045"
---
# <a name="corsavesize-enumeration"></a><span data-ttu-id="d5bfa-102">CorSaveSize 枚举</span><span class="sxs-lookup"><span data-stu-id="d5bfa-102">CorSaveSize Enumeration</span></span>

<span data-ttu-id="d5bfa-103">包含一些值，用于指示查询保存操作的大小时所需的精度级别。</span><span class="sxs-lookup"><span data-stu-id="d5bfa-103">Contains values indicating the level of precision required when querying for the size of a save operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5bfa-104">语法</span><span class="sxs-lookup"><span data-stu-id="d5bfa-104">Syntax</span></span>  
  
```cpp  
typedef enum CorSaveSize {  
    cssAccurate                = 0x0000,
    cssQuick                   = 0x0001,
    cssDiscardTransientCAs     = 0x0002  
} CorSaveSize;  
```  
  
## <a name="members"></a><span data-ttu-id="d5bfa-105">成员</span><span class="sxs-lookup"><span data-stu-id="d5bfa-105">Members</span></span>  
  
|<span data-ttu-id="d5bfa-106">成员</span><span class="sxs-lookup"><span data-stu-id="d5bfa-106">Member</span></span>|<span data-ttu-id="d5bfa-107">说明</span><span class="sxs-lookup"><span data-stu-id="d5bfa-107">Description</span></span>|  
|------------|-----------------|  
|`cssAccurate`|<span data-ttu-id="d5bfa-108">指定返回值应是精确的。</span><span class="sxs-lookup"><span data-stu-id="d5bfa-108">Specifies that the return value should be exact.</span></span>|  
|`cssQuick`|<span data-ttu-id="d5bfa-109">指定应估算返回值。</span><span class="sxs-lookup"><span data-stu-id="d5bfa-109">Specifies that the return value should be estimated.</span></span>|  
|`cssDiscardTransientCAs`|<span data-ttu-id="d5bfa-110">指定应删除可放弃类型。</span><span class="sxs-lookup"><span data-stu-id="d5bfa-110">Specifies that discardable types should be removed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d5bfa-111">要求</span><span class="sxs-lookup"><span data-stu-id="d5bfa-111">Requirements</span></span>  

 <span data-ttu-id="d5bfa-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d5bfa-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5bfa-113">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="d5bfa-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d5bfa-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d5bfa-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d5bfa-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5bfa-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5bfa-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5bfa-116">See also</span></span>

- [<span data-ttu-id="d5bfa-117">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="d5bfa-117">Metadata Enumerations</span></span>](metadata-enumerations.md)
