---
title: ICorDebugGuidToTypeEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum
helpviewer_keywords:
- ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: aa32b12b-05fc-4ea8-a904-adae25034269
topic_type:
- apiref
ms.openlocfilehash: 149c5b09639c8809e736ade09566e7b1b530e3eb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705704"
---
# <a name="icordebugguidtotypeenum-interface"></a><span data-ttu-id="f85c4-102">ICorDebugGuidToTypeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="f85c4-102">ICorDebugGuidToTypeEnum Interface</span></span>

<span data-ttu-id="f85c4-103">提供一个枚举器，该枚举器定义一组 Guid 与它们对应的类型之间的映射（由 ICorDebugType 实例表示）。</span><span class="sxs-lookup"><span data-stu-id="f85c4-103">Provides an enumerator that defines the mapping between a set of GUIDs and their corresponding types, which are represented by ICorDebugType instances.</span></span> <span data-ttu-id="f85c4-104">此接口继承 ICorDebugEnum 接口中的方法。</span><span class="sxs-lookup"><span data-stu-id="f85c4-104">This interface inherits the methods from the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f85c4-105">方法</span><span class="sxs-lookup"><span data-stu-id="f85c4-105">Methods</span></span>  
  
|<span data-ttu-id="f85c4-106">方法</span><span class="sxs-lookup"><span data-stu-id="f85c4-106">Method</span></span>|<span data-ttu-id="f85c4-107">说明</span><span class="sxs-lookup"><span data-stu-id="f85c4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f85c4-108">ICorDebugGuidToTypeEnum：： Next</span><span class="sxs-lookup"><span data-stu-id="f85c4-108">ICorDebugGuidToTypeEnum::Next</span></span>](icordebugguidtotypeenum-next-method.md)|<span data-ttu-id="f85c4-109">获取指定数量的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 实例，这些实例将 guid 映射到类型信息。</span><span class="sxs-lookup"><span data-stu-id="f85c4-109">Gets the specified number of [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) instances that map GUIDs to type information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f85c4-110">注解</span><span class="sxs-lookup"><span data-stu-id="f85c4-110">Remarks</span></span>  

 <span data-ttu-id="f85c4-111">`ICorDebugGuidToTypeEnum`可以通过调用[ICorDebugAppDomain3：： GetCachedWinRTTypes](icordebugappdomain3-getcachedwinrttypes-method.md)方法来检索 interface 对象。</span><span class="sxs-lookup"><span data-stu-id="f85c4-111">An `ICorDebugGuidToTypeEnum` interface object can be retrieved by calling the [ICorDebugAppDomain3::GetCachedWinRTTypes](icordebugappdomain3-getcachedwinrttypes-method.md) method.</span></span> <span data-ttu-id="f85c4-112">调试器可以调用此接口的 [下一](icordebugguidtotypeenum-next-method.md) 方法来检索 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 对象，这些对象表示在用于调用 [ICorDebugAppDomain3：： GetCachedWinRTTypes](icordebugappdomain3-getcachedwinrttypes-method.md) 方法的应用程序域中加载的 Windows 运行时类型的托管表示形式的映射。</span><span class="sxs-lookup"><span data-stu-id="f85c4-112">A debugger can call this interface's [Next](icordebugguidtotypeenum-next-method.md) method to retrieve [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) objects that represent mappings of managed representations of Windows Runtime types loaded in the application domain used for the call to the [ICorDebugAppDomain3::GetCachedWinRTTypes](icordebugappdomain3-getcachedwinrttypes-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f85c4-113">要求</span><span class="sxs-lookup"><span data-stu-id="f85c4-113">Requirements</span></span>  

 <span data-ttu-id="f85c4-114">**平台：** Windows 运行时</span><span class="sxs-lookup"><span data-stu-id="f85c4-114">**Platforms:** Windows Runtime</span></span>  
  
 <span data-ttu-id="f85c4-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f85c4-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f85c4-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f85c4-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f85c4-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f85c4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f85c4-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f85c4-118">See also</span></span>

- [<span data-ttu-id="f85c4-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="f85c4-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
