---
title: ICorDebugExceptionObjectValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectValue
helpviewer_keywords:
- ICorDebugExceptionObjectValue interface [.NET Framework debugging]
ms.assetid: 43416dd5-8892-4106-9f59-f9143b19ddb4
topic_type:
- apiref
ms.openlocfilehash: 6a0c33799b2b2aaa48e3b18b7b4bb37643508bd4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95678878"
---
# <a name="icordebugexceptionobjectvalue-interface"></a><span data-ttu-id="bb977-102">ICorDebugExceptionObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="bb977-102">ICorDebugExceptionObjectValue Interface</span></span>

<span data-ttu-id="bb977-103">扩展 "ICorDebugObjectValue" 接口，以提供来自托管异常对象的堆栈跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="bb977-103">Extends the "ICorDebugObjectValue" interface to provide stack trace information from a managed exception object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bb977-104">方法</span><span class="sxs-lookup"><span data-stu-id="bb977-104">Methods</span></span>  
  
|<span data-ttu-id="bb977-105">方法</span><span class="sxs-lookup"><span data-stu-id="bb977-105">Method</span></span>|<span data-ttu-id="bb977-106">说明</span><span class="sxs-lookup"><span data-stu-id="bb977-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bb977-107">EnumerateExceptionCallStack 方法</span><span class="sxs-lookup"><span data-stu-id="bb977-107">EnumerateExceptionCallStack Method</span></span>](icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md)|<span data-ttu-id="bb977-108">获取一个枚举器，该枚举器指向嵌入到异常对象中的调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="bb977-108">Gets an enumerator to the call stack embedded in an exception object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bb977-109">注解</span><span class="sxs-lookup"><span data-stu-id="bb977-109">Remarks</span></span>  

 <span data-ttu-id="bb977-110">`QueryInterface`对于派生自的托管对象，对的调用将成功 <xref:System.Exception?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="bb977-110">The call to `QueryInterface` will succeed for managed objects that derive from <xref:System.Exception?displayProperty=nameWithType>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb977-111">要求</span><span class="sxs-lookup"><span data-stu-id="bb977-111">Requirements</span></span>  

 <span data-ttu-id="bb977-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb977-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb977-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bb977-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bb977-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb977-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bb977-115">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb977-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb977-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb977-116">See also</span></span>

- [<span data-ttu-id="bb977-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="bb977-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="bb977-118">调试</span><span class="sxs-lookup"><span data-stu-id="bb977-118">Debugging</span></span>](index.md)
