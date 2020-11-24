---
title: ICorDebugValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue
helpviewer_keywords:
- ICorDebugValue interface [.NET Framework debugging]
ms.assetid: b2f7007f-c446-4b18-aed1-a25cff8aee31
topic_type:
- apiref
ms.openlocfilehash: 7d3c35ed6cda637e3b885afe089ddfa590d51076
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683597"
---
# <a name="icordebugvalue-interface"></a><span data-ttu-id="06e20-102">ICorDebugValue 接口</span><span class="sxs-lookup"><span data-stu-id="06e20-102">ICorDebugValue Interface</span></span>

<span data-ttu-id="06e20-103">表示正在调试的进程中的值。</span><span class="sxs-lookup"><span data-stu-id="06e20-103">Represents a value in the process being debugged.</span></span> <span data-ttu-id="06e20-104">该值可以是读取或写入值。</span><span class="sxs-lookup"><span data-stu-id="06e20-104">The value can be a read or a write value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="06e20-105">方法</span><span class="sxs-lookup"><span data-stu-id="06e20-105">Methods</span></span>  
  
|<span data-ttu-id="06e20-106">方法</span><span class="sxs-lookup"><span data-stu-id="06e20-106">Method</span></span>|<span data-ttu-id="06e20-107">说明</span><span class="sxs-lookup"><span data-stu-id="06e20-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="06e20-108">CreateBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="06e20-108">CreateBreakpoint Method</span></span>](icordebugvalue-createbreakpoint-method.md)|<span data-ttu-id="06e20-109">目前未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="06e20-109">This method is not currently implemented.</span></span>|  
|[<span data-ttu-id="06e20-110">GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="06e20-110">GetAddress Method</span></span>](icordebugvalue-getaddress-method.md)|<span data-ttu-id="06e20-111">获取此对象的地址，该地址正在进行 `ICorDebugValue` 调试。</span><span class="sxs-lookup"><span data-stu-id="06e20-111">Gets the address of this `ICorDebugValue` object, which is in the process of being debugged.</span></span>|  
|[<span data-ttu-id="06e20-112">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="06e20-112">GetSize Method</span></span>](icordebugvalue-getsize-method.md)|<span data-ttu-id="06e20-113">获取此对象的大小（以字节为单位） `ICorDebugValue` 。</span><span class="sxs-lookup"><span data-stu-id="06e20-113">Gets the size, in bytes, of this `ICorDebugValue` object.</span></span>|  
|[<span data-ttu-id="06e20-114">GetType 方法</span><span class="sxs-lookup"><span data-stu-id="06e20-114">GetType Method</span></span>](icordebugvalue-gettype-method.md)|<span data-ttu-id="06e20-115">获取此对象的基元类型 `ICorDebugValue` 。</span><span class="sxs-lookup"><span data-stu-id="06e20-115">Gets the primitive type of this `ICorDebugValue` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06e20-116">注解</span><span class="sxs-lookup"><span data-stu-id="06e20-116">Remarks</span></span>  

 <span data-ttu-id="06e20-117">通常，值对象的所有权在返回时传递。</span><span class="sxs-lookup"><span data-stu-id="06e20-117">In general, ownership of a value object is passed when it is returned.</span></span> <span data-ttu-id="06e20-118">当对象使用完对象后，接收方负责从对象中删除引用。</span><span class="sxs-lookup"><span data-stu-id="06e20-118">The recipient is responsible for removing a reference from the object when it is finished with the object.</span></span>  
  
 <span data-ttu-id="06e20-119">根据从何处检索值，在恢复进程后，值可能不会保持有效。</span><span class="sxs-lookup"><span data-stu-id="06e20-119">Depending on where the value was retrieved from, the value may not remain valid after the process is resumed.</span></span> <span data-ttu-id="06e20-120">因此，通常情况下，不应在对 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 方法的调用中保存值。</span><span class="sxs-lookup"><span data-stu-id="06e20-120">So, in general, the value shouldn't be held across a call of the [ICorDebugController::Continue](icordebugcontroller-continue-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="06e20-121">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="06e20-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06e20-122">要求</span><span class="sxs-lookup"><span data-stu-id="06e20-122">Requirements</span></span>  

 <span data-ttu-id="06e20-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06e20-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06e20-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="06e20-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="06e20-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="06e20-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="06e20-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06e20-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06e20-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06e20-127">See also</span></span>

- [<span data-ttu-id="06e20-128">ICorDebugValue3 接口</span><span class="sxs-lookup"><span data-stu-id="06e20-128">ICorDebugValue3 Interface</span></span>](icordebugvalue3-interface.md)
- [<span data-ttu-id="06e20-129">调试接口</span><span class="sxs-lookup"><span data-stu-id="06e20-129">Debugging Interfaces</span></span>](debugging-interfaces.md)
