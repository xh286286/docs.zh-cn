---
title: ICorDebugDataTarget3 接口
ms.date: 03/30/2017
ms.assetid: f477af85-994f-4df0-ae78-404ed252bf49
ms.openlocfilehash: e219c703ce2d8bb42f824a8892991f6803e6ef9d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713725"
---
# <a name="icordebugdatatarget3-interface"></a><span data-ttu-id="e3fbb-102">ICorDebugDataTarget3 接口</span><span class="sxs-lookup"><span data-stu-id="e3fbb-102">ICorDebugDataTarget3 Interface</span></span>

<span data-ttu-id="e3fbb-103">对 [ICorDebugDataTarget](icordebugdatatarget-interface.md) 接口进行逻辑扩展，以提供有关已加载模块的信息。</span><span class="sxs-lookup"><span data-stu-id="e3fbb-103">Logically extends the [ICorDebugDataTarget](icordebugdatatarget-interface.md) interface to provide information about loaded modules.</span></span>  
  
## <a name="method"></a><span data-ttu-id="e3fbb-104">方法</span><span class="sxs-lookup"><span data-stu-id="e3fbb-104">Method</span></span>  
  
|<span data-ttu-id="e3fbb-105">方法</span><span class="sxs-lookup"><span data-stu-id="e3fbb-105">Method</span></span>|<span data-ttu-id="e3fbb-106">说明</span><span class="sxs-lookup"><span data-stu-id="e3fbb-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e3fbb-107">GetLoadedModules 方法</span><span class="sxs-lookup"><span data-stu-id="e3fbb-107">GetLoadedModules Method</span></span>](icordebugdatatarget3-getloadedmodules-method.md)|<span data-ttu-id="e3fbb-108">获取到目前为止已加载的模块的列表。</span><span class="sxs-lookup"><span data-stu-id="e3fbb-108">Gets a list of the modules that have been loaded so far.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e3fbb-109">注解</span><span class="sxs-lookup"><span data-stu-id="e3fbb-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e3fbb-110">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="e3fbb-110">This interface is available with .NET Native only.</span></span> <span data-ttu-id="e3fbb-111">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="e3fbb-111">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3fbb-112">要求</span><span class="sxs-lookup"><span data-stu-id="e3fbb-112">Requirements</span></span>  

 <span data-ttu-id="e3fbb-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e3fbb-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3fbb-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e3fbb-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e3fbb-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e3fbb-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e3fbb-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3fbb-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3fbb-117">See also</span></span>

- [<span data-ttu-id="e3fbb-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="e3fbb-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="e3fbb-119">调试</span><span class="sxs-lookup"><span data-stu-id="e3fbb-119">Debugging</span></span>](index.md)
