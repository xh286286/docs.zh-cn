---
title: CustomDumpItem 结构
ms.date: 03/30/2017
api_name:
- CustomDumpItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CustomDumpItem
helpviewer_keywords:
- CustomDumpItem structure [.NET Framework hosting]
ms.assetid: fd9085ff-7beb-4c38-97f0-037cd8ba4f65
topic_type:
- apiref
ms.openlocfilehash: c77e93686c7d121e9fe2a92f03970404ab823dc0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95673236"
---
# <a name="customdumpitem-structure"></a><span data-ttu-id="ae71d-102">CustomDumpItem 结构</span><span class="sxs-lookup"><span data-stu-id="ae71d-102">CustomDumpItem Structure</span></span>

<span data-ttu-id="ae71d-103">描述要添加到错误报告中的自定义转储的项。</span><span class="sxs-lookup"><span data-stu-id="ae71d-103">Describes an item to be added to a custom dump in error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae71d-104">语法</span><span class="sxs-lookup"><span data-stu-id="ae71d-104">Syntax</span></span>  
  
```cpp  
struct {  
    ECustomDumpItemKind itemKind;
    union {  
        UINT_PTR pReserved;  
    }  
} CustomDumpItem;  
```  
  
## <a name="members"></a><span data-ttu-id="ae71d-105">成员</span><span class="sxs-lookup"><span data-stu-id="ae71d-105">Members</span></span>  
  
|<span data-ttu-id="ae71d-106">成员</span><span class="sxs-lookup"><span data-stu-id="ae71d-106">Member</span></span>|<span data-ttu-id="ae71d-107">说明</span><span class="sxs-lookup"><span data-stu-id="ae71d-107">Description</span></span>|  
|------------|-----------------|  
|`itemKind`|<span data-ttu-id="ae71d-108">一个 [ECustomDumpItemKind](ecustomdumpitemkind-enumeration.md) 值，指示要添加的项的类型。</span><span class="sxs-lookup"><span data-stu-id="ae71d-108">An [ECustomDumpItemKind](ecustomdumpitemkind-enumeration.md) value that indicates the kind of item to be added.</span></span>|  
|`pReserved`|<span data-ttu-id="ae71d-109">当前未使用。</span><span class="sxs-lookup"><span data-stu-id="ae71d-109">Not currently used.</span></span> <span data-ttu-id="ae71d-110">添加到联合的任何项都必须不大于指针大小。</span><span class="sxs-lookup"><span data-stu-id="ae71d-110">Any items added to the union must be no larger than pointer size.</span></span> <span data-ttu-id="ae71d-111">如果 `struct` 需要，您必须单独分配并指向它。</span><span class="sxs-lookup"><span data-stu-id="ae71d-111">If a `struct` is required, you must allocate it separately and point to it.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae71d-112">注解</span><span class="sxs-lookup"><span data-stu-id="ae71d-112">Remarks</span></span>  

 <span data-ttu-id="ae71d-113">[ICLRErrorReportingManager：： BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) 采用类型为的参数 `CustomDumpItem` 。</span><span class="sxs-lookup"><span data-stu-id="ae71d-113">[ICLRErrorReportingManager::BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) takes a parameter of type `CustomDumpItem`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae71d-114">要求</span><span class="sxs-lookup"><span data-stu-id="ae71d-114">Requirements</span></span>  

 <span data-ttu-id="ae71d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae71d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae71d-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ae71d-116">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="ae71d-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ae71d-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ae71d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae71d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae71d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae71d-119">See also</span></span>

- [<span data-ttu-id="ae71d-120">承载结构</span><span class="sxs-lookup"><span data-stu-id="ae71d-120">Hosting Structures</span></span>](hosting-structures.md)
