---
title: ECustomDumpFlavor 枚举
ms.date: 03/30/2017
api_name:
- ECustomDumpFlavor
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ECustomDumpFlavor
helpviewer_keywords:
- ECustomDumpFlavor enumeration [.NET Framework hosting]
ms.assetid: b39b3320-fac7-41f1-9a03-ab6fb0cd89c7
topic_type:
- apiref
ms.openlocfilehash: 1b8440ed6e878aac3dd08d9f8ed528c93739a724
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95686314"
---
# <a name="ecustomdumpflavor-enumeration"></a><span data-ttu-id="89c66-102">ECustomDumpFlavor 枚举</span><span class="sxs-lookup"><span data-stu-id="89c66-102">ECustomDumpFlavor Enumeration</span></span>

<span data-ttu-id="89c66-103">包含一些值，这些值指示在报告错误时要包含在堆转储的自定义子集中的项。</span><span class="sxs-lookup"><span data-stu-id="89c66-103">Contains values that indicate which items to include in a custom subset of a heap dump when reporting errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89c66-104">语法</span><span class="sxs-lookup"><span data-stu-id="89c66-104">Syntax</span></span>  
  
```cpp  
typedef enum {  
    DUMP_FLAVOR_Mini            = 1,  
    DUMP_FLAVOR_NonHeapCLRState = 2  
} ECustomDumpFlavor;  
```  
  
## <a name="members"></a><span data-ttu-id="89c66-105">成员</span><span class="sxs-lookup"><span data-stu-id="89c66-105">Members</span></span>  
  
|<span data-ttu-id="89c66-106">成员</span><span class="sxs-lookup"><span data-stu-id="89c66-106">Member</span></span>|<span data-ttu-id="89c66-107">说明</span><span class="sxs-lookup"><span data-stu-id="89c66-107">Description</span></span>|  
|------------|-----------------|  
|`DUMP_FLAVOR_Mini`|<span data-ttu-id="89c66-108">指定自定义堆转储应作为小型转储开始，并包含传递给同一方法的任何 [CustomDumpItem](customdumpitem-structure.md) 实例指定的额外数据。</span><span class="sxs-lookup"><span data-stu-id="89c66-108">Specifies that the custom heap dump should start as a minidump and include extra data specified by any [CustomDumpItem](customdumpitem-structure.md) instances passed to the same method.</span></span>|  
|`DUMP_FLAVOR_NonHeapCLRState`|<span data-ttu-id="89c66-109">指定自定义堆转储应收集未动态分配的所有运行时状态数据。</span><span class="sxs-lookup"><span data-stu-id="89c66-109">Specifies that the custom heap dump should gather all run-time state data that was not dynamically allocated.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="89c66-110">注解</span><span class="sxs-lookup"><span data-stu-id="89c66-110">Remarks</span></span>  

 <span data-ttu-id="89c66-111">类型的参数 `ECustomDumpFlavor` 传递给 [ICLRErrorReportingManager：： BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="89c66-111">A parameter of type `ECustomDumpFlavor` is passed to the [ICLRErrorReportingManager::BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="89c66-112">要求</span><span class="sxs-lookup"><span data-stu-id="89c66-112">Requirements</span></span>  

 <span data-ttu-id="89c66-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="89c66-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="89c66-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="89c66-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="89c66-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="89c66-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="89c66-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="89c66-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89c66-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89c66-117">See also</span></span>

- [<span data-ttu-id="89c66-118">ECustomDumpItemKind 枚举</span><span class="sxs-lookup"><span data-stu-id="89c66-118">ECustomDumpItemKind Enumeration</span></span>](ecustomdumpitemkind-enumeration.md)
- [<span data-ttu-id="89c66-119">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="89c66-119">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
- [<span data-ttu-id="89c66-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="89c66-120">Hosting Enumerations</span></span>](hosting-enumerations.md)
