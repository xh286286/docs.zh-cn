---
title: ICorDebugProcess8 接口
ms.date: 03/30/2017
ms.assetid: 7ab1a70f-ec11-46ff-8869-cd8ca679cc51
ms.openlocfilehash: 00c432374eeb82692492b8e6b10472f13bc44d6e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732510"
---
# <a name="icordebugprocess8-interface"></a><span data-ttu-id="a6c31-102">ICorDebugProcess8 接口</span><span class="sxs-lookup"><span data-stu-id="a6c31-102">ICorDebugProcess8 Interface</span></span>

<span data-ttu-id="a6c31-103">[.NET Framework 4.6 及更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="a6c31-103">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="a6c31-104">对 ICorDebugProcess 接口进行逻辑扩展，以启用或禁用某些类型的 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 异常回调。</span><span class="sxs-lookup"><span data-stu-id="a6c31-104">Logically extends the ICorDebugProcess interface to enable or disable certain types of [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) exception callbacks.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a6c31-105">方法</span><span class="sxs-lookup"><span data-stu-id="a6c31-105">Methods</span></span>  
  
|<span data-ttu-id="a6c31-106">方法</span><span class="sxs-lookup"><span data-stu-id="a6c31-106">Method</span></span>|<span data-ttu-id="a6c31-107">说明</span><span class="sxs-lookup"><span data-stu-id="a6c31-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a6c31-108">EnableExceptionCallbacksOutsideOfMyCode 方法</span><span class="sxs-lookup"><span data-stu-id="a6c31-108">EnableExceptionCallbacksOutsideOfMyCode Method</span></span>](icordebugprocess8-enableexceptioncallbacksoutsideofmycode-method.md)|<span data-ttu-id="a6c31-109">启用或禁用某些类型的 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 异常回调。</span><span class="sxs-lookup"><span data-stu-id="a6c31-109">Enables or disables certain types of [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) exception callbacks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6c31-110">备注</span><span class="sxs-lookup"><span data-stu-id="a6c31-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6c31-111">要求</span><span class="sxs-lookup"><span data-stu-id="a6c31-111">Requirements</span></span>  

 <span data-ttu-id="a6c31-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c31-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6c31-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a6c31-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a6c31-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a6c31-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a6c31-115">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6c31-115">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6c31-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6c31-116">See also</span></span>

- [<span data-ttu-id="a6c31-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="a6c31-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="a6c31-118">调试</span><span class="sxs-lookup"><span data-stu-id="a6c31-118">Debugging</span></span>](index.md)
