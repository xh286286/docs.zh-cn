---
title: ICorDebugComObjectValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugComObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugComObjectValue
helpviewer_keywords:
- ICorDebugComObjectValue interface [.NET Framework debugging]
ms.assetid: 505a7f6c-d92b-42b4-b539-433f5102ea9b
topic_type:
- apiref
ms.openlocfilehash: 40df1416e68c86efe6d404119cb37277fe21ac56
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677539"
---
# <a name="icordebugcomobjectvalue-interface"></a><span data-ttu-id="e7942-102">ICorDebugComObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="e7942-102">ICorDebugComObjectValue Interface</span></span>

<span data-ttu-id="e7942-103">提供方法以检索与运行时可调用包装关联的信息 (RCW) 。</span><span class="sxs-lookup"><span data-stu-id="e7942-103">Provides methods to retrieve information associated with a runtime callable wrapper (RCW).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e7942-104">方法</span><span class="sxs-lookup"><span data-stu-id="e7942-104">Methods</span></span>  
  
|<span data-ttu-id="e7942-105">方法</span><span class="sxs-lookup"><span data-stu-id="e7942-105">Method</span></span>|<span data-ttu-id="e7942-106">说明</span><span class="sxs-lookup"><span data-stu-id="e7942-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e7942-107">GetCachedInterfacePointers 方法</span><span class="sxs-lookup"><span data-stu-id="e7942-107">GetCachedInterfacePointers Method</span></span>](icordebugcomobjectvalue-getcachedinterfacepointers-method.md)|<span data-ttu-id="e7942-108">获取缓存在当前 RCW 上的原始接口指针。</span><span class="sxs-lookup"><span data-stu-id="e7942-108">Gets the raw interface pointers cached on the current RCW.</span></span>|  
|[<span data-ttu-id="e7942-109">GetCachedInterfaceTypes 方法</span><span class="sxs-lookup"><span data-stu-id="e7942-109">GetCachedInterfaceTypes Method</span></span>](icordebugcomobjectvalue-getcachedinterfacetypes-method.md)|<span data-ttu-id="e7942-110">为当前对象的大小写或用作的接口类型提供枚举器。</span><span class="sxs-lookup"><span data-stu-id="e7942-110">Provides an enumerator for the interface types that the current object has been cased to or used as.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7942-111">注解</span><span class="sxs-lookup"><span data-stu-id="e7942-111">Remarks</span></span>  

 <span data-ttu-id="e7942-112">若要检查 "ICorDebugValue" 接口的实例是否表示 RCW，调试程序 `QueryInterface` 使用 "ICorDebugValue" 调用 `IID_ICorDebugComObjectValue` 。</span><span class="sxs-lookup"><span data-stu-id="e7942-112">To check whether an instance of an "ICorDebugValue" interface represents an RCW, a debugger calls `QueryInterface` on "ICorDebugValue" with `IID_ICorDebugComObjectValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7942-113">要求</span><span class="sxs-lookup"><span data-stu-id="e7942-113">Requirements</span></span>  

 <span data-ttu-id="e7942-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e7942-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7942-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e7942-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e7942-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e7942-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e7942-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7942-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7942-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7942-118">See also</span></span>

- [<span data-ttu-id="e7942-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="e7942-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="e7942-120">调试</span><span class="sxs-lookup"><span data-stu-id="e7942-120">Debugging</span></span>](index.md)
