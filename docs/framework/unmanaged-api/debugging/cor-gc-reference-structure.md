---
title: COR_GC_REFERENCE 结构
ms.date: 03/30/2017
api_name:
- COR_GC_REFERENCE
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_GC_REFERENCE
helpviewer_keywords:
- COR_GC_REFERENCE structure [.NET Framework debugging]
ms.assetid: 162e8179-0cd4-4110-8f06-5f387698bd62
topic_type:
- apiref
ms.openlocfilehash: bb4a8f7ff3ee54474804e3e5620dcce7c9f79fb5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726608"
---
# <a name="cor_gc_reference-structure"></a><span data-ttu-id="6e11b-102">COR_GC_REFERENCE 结构</span><span class="sxs-lookup"><span data-stu-id="6e11b-102">COR_GC_REFERENCE Structure</span></span>

<span data-ttu-id="6e11b-103">包含有关要进行垃圾回收的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="6e11b-103">Contains information about an object that is to be garbage-collected.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e11b-104">语法</span><span class="sxs-lookup"><span data-stu-id="6e11b-104">Syntax</span></span>  
  
```cpp  
typedef struct _COR_GC_REFERENCE {  
    ICorDebugAppDomain *domain;
    ICorDebugValue *location;  
    CorGCReferenceType type;  
    UINT64 extraData;  
} COR_GC_REFERENCE;  
```  
  
## <a name="members"></a><span data-ttu-id="6e11b-105">成员</span><span class="sxs-lookup"><span data-stu-id="6e11b-105">Members</span></span>  
  
|<span data-ttu-id="6e11b-106">成员</span><span class="sxs-lookup"><span data-stu-id="6e11b-106">Member</span></span>|<span data-ttu-id="6e11b-107">说明</span><span class="sxs-lookup"><span data-stu-id="6e11b-107">Description</span></span>|  
|------------|-----------------|  
|`domain`|<span data-ttu-id="6e11b-108">指向句柄或对象所属的应用程序域的指针。</span><span class="sxs-lookup"><span data-stu-id="6e11b-108">A pointer to the application domain to which the handle or object belongs.</span></span> <span data-ttu-id="6e11b-109">其值可以是 `null` 。</span><span class="sxs-lookup"><span data-stu-id="6e11b-109">Its value may be `null`.</span></span>|  
|`location`|<span data-ttu-id="6e11b-110">与要进行垃圾回收的对象相对应的 ICorDebugValue 或 ICorDebugReferenceValue 接口。</span><span class="sxs-lookup"><span data-stu-id="6e11b-110">Either an ICorDebugValue or an ICorDebugReferenceValue interface that corresponds to the object to be garbage-collected.</span></span>|  
|`type`|<span data-ttu-id="6e11b-111">一个 [CorGCReferenceType](corgcreferencetype-enumeration.md) 枚举值，该值指示根的来源。</span><span class="sxs-lookup"><span data-stu-id="6e11b-111">A [CorGCReferenceType](corgcreferencetype-enumeration.md) enumeration value that indicates where the root came from.</span></span> <span data-ttu-id="6e11b-112">有关详细信息，请参阅“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="6e11b-112">For more information, see the Remarks section.</span></span>|  
|`extraData`|<span data-ttu-id="6e11b-113">有关要进行垃圾回收的对象的其他数据。</span><span class="sxs-lookup"><span data-stu-id="6e11b-113">Additional data about the object to be garbage-collected.</span></span> <span data-ttu-id="6e11b-114">此信息取决于对象的源，如字段所示 `type` 。</span><span class="sxs-lookup"><span data-stu-id="6e11b-114">This information depends on the source of the object, as indicated by the `type` field.</span></span> <span data-ttu-id="6e11b-115">有关详细信息，请参阅“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="6e11b-115">For more information, see the Remarks section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e11b-116">注解</span><span class="sxs-lookup"><span data-stu-id="6e11b-116">Remarks</span></span>  

 <span data-ttu-id="6e11b-117">该 `type` 字段是一个 [CorGCReferenceType](corgcreferencetype-enumeration.md) 枚举值，该值指示引用来自何处。</span><span class="sxs-lookup"><span data-stu-id="6e11b-117">The `type` field is a [CorGCReferenceType](corgcreferencetype-enumeration.md) enumeration value that indicates where the reference came from.</span></span> <span data-ttu-id="6e11b-118">特定 `COR_GC_REFERENCE` 值可以反映以下任意一种类型的托管对象：</span><span class="sxs-lookup"><span data-stu-id="6e11b-118">A particular `COR_GC_REFERENCE` value can reflect any of the following kinds of managed objects:</span></span>  
  
- <span data-ttu-id="6e11b-119">所有托管堆栈中的对象 (`CorGCReferenceType.CorReferenceStack`) 。</span><span class="sxs-lookup"><span data-stu-id="6e11b-119">Objects from all managed stacks (`CorGCReferenceType.CorReferenceStack`).</span></span> <span data-ttu-id="6e11b-120">这包括托管代码中的实时引用以及由公共语言运行时创建的对象。</span><span class="sxs-lookup"><span data-stu-id="6e11b-120">This includes live references in managed code, as well as objects created by the common language runtime.</span></span>  
  
- <span data-ttu-id="6e11b-121">句柄表中的对象 (`CorGCReferenceType.CorHandle*`) 。</span><span class="sxs-lookup"><span data-stu-id="6e11b-121">Objects from the handle table (`CorGCReferenceType.CorHandle*`).</span></span> <span data-ttu-id="6e11b-122">这包括 `HNDTYPE_STRONG` 模块中 (和 `HNDTYPE_REFCOUNT`) 和静态变量的强引用。</span><span class="sxs-lookup"><span data-stu-id="6e11b-122">This includes strong references (`HNDTYPE_STRONG` and `HNDTYPE_REFCOUNT`) and static variables in a module.</span></span>  
  
- <span data-ttu-id="6e11b-123">终结器队列中的对象 (`CorGCReferenceType.CorReferenceFinalizer`) 。</span><span class="sxs-lookup"><span data-stu-id="6e11b-123">Objects from the finalizer queue (`CorGCReferenceType.CorReferenceFinalizer`).</span></span> <span data-ttu-id="6e11b-124">终结器队列根对象，直到终结器运行。</span><span class="sxs-lookup"><span data-stu-id="6e11b-124">The finalizer queue roots objects until the finalizer has run.</span></span>  
  
 <span data-ttu-id="6e11b-125">该 `extraData` 字段包含其他数据，具体取决于引用 (或类型) 的源。</span><span class="sxs-lookup"><span data-stu-id="6e11b-125">The `extraData` field contains extra data depending on the source (or type) of the reference.</span></span> <span data-ttu-id="6e11b-126">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="6e11b-126">Possible values are:</span></span>  
  
- <span data-ttu-id="6e11b-127">`DependentSource`.</span><span class="sxs-lookup"><span data-stu-id="6e11b-127">`DependentSource`.</span></span> <span data-ttu-id="6e11b-128">如果 `type` 为 `CorGCREferenceType.CorHandleStrongDependent` ，则此字段为对象，如果为，则此字段为要在其上进行垃圾回收的对象的根 `COR_GC_REFERENCE.Location` 。</span><span class="sxs-lookup"><span data-stu-id="6e11b-128">If the `type` is `CorGCREferenceType.CorHandleStrongDependent`, this field is the object that, if alive, roots the object to be garbage-collected at `COR_GC_REFERENCE.Location`.</span></span>  
  
- <span data-ttu-id="6e11b-129">`RefCount`.</span><span class="sxs-lookup"><span data-stu-id="6e11b-129">`RefCount`.</span></span> <span data-ttu-id="6e11b-130">如果 `type` 为 `CorGCREferenceType.CorHandleStrongRefCount` ，则此字段是句柄的引用计数。</span><span class="sxs-lookup"><span data-stu-id="6e11b-130">If the `type` is `CorGCREferenceType.CorHandleStrongRefCount`, this field is the reference count of the handle.</span></span>  
  
- <span data-ttu-id="6e11b-131">`Size`.</span><span class="sxs-lookup"><span data-stu-id="6e11b-131">`Size`.</span></span> <span data-ttu-id="6e11b-132">如果 `type` 为 `CorGCREferenceType.CorHandleStrongSizedByref` ，则此字段是垃圾回收器为其计算对象根的对象树的最后一个大小。</span><span class="sxs-lookup"><span data-stu-id="6e11b-132">If the `type` is `CorGCREferenceType.CorHandleStrongSizedByref`, this field is the last size of the object tree for which the garbage collector calculated the object roots.</span></span> <span data-ttu-id="6e11b-133">请注意，此计算不一定是最新的。</span><span class="sxs-lookup"><span data-stu-id="6e11b-133">Note that this calculation is not necessarily up to date.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e11b-134">要求</span><span class="sxs-lookup"><span data-stu-id="6e11b-134">Requirements</span></span>  

 <span data-ttu-id="6e11b-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e11b-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e11b-136">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6e11b-136">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6e11b-137">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6e11b-137">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6e11b-138">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e11b-138">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e11b-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6e11b-139">See also</span></span>

- [<span data-ttu-id="6e11b-140">调试结构</span><span class="sxs-lookup"><span data-stu-id="6e11b-140">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="6e11b-141">调试</span><span class="sxs-lookup"><span data-stu-id="6e11b-141">Debugging</span></span>](index.md)
