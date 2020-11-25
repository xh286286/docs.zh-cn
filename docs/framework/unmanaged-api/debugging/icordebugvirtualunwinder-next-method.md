---
title: ICorDebugVirtualUnwinder::Next 方法
ms.date: 03/30/2017
ms.assetid: 790e0426-e5cd-49fd-a792-f8c8635d72fe
ms.openlocfilehash: bfc827a1503b0367a442e3f3ca0915bd2aaeb01e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725945"
---
# <a name="icordebugvirtualunwindernext-method"></a><span data-ttu-id="39207-102">ICorDebugVirtualUnwinder::Next 方法</span><span class="sxs-lookup"><span data-stu-id="39207-102">ICorDebugVirtualUnwinder::Next Method</span></span>

<span data-ttu-id="39207-103">前进到调用方的上下文。</span><span class="sxs-lookup"><span data-stu-id="39207-103">Advances to the caller's context.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39207-104">语法</span><span class="sxs-lookup"><span data-stu-id="39207-104">Syntax</span></span>  
  
```cpp  
HRESULT Next();  
```  
  
## <a name="parameters"></a><span data-ttu-id="39207-105">参数</span><span class="sxs-lookup"><span data-stu-id="39207-105">Parameters</span></span>  

 <span data-ttu-id="39207-106">无。</span><span class="sxs-lookup"><span data-stu-id="39207-106">None.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="39207-107">返回值</span><span class="sxs-lookup"><span data-stu-id="39207-107">Return Value</span></span>  

 <span data-ttu-id="39207-108">如果成功展开，则为 `S_OK`如果因帧不够而无法完全展开，则为 `CORDBG_S_AT_END_OF_STACK`。</span><span class="sxs-lookup"><span data-stu-id="39207-108">`S_OK` if the unwind occurred successfully, or `CORDBG_S_AT_END_OF_STACK` if the unwind cannot be completed because there are no more frames.</span></span>  
  
 <span data-ttu-id="39207-109">如果返回失败的 HRESULT，则 ICorDebug API 将返回 `CORDBG_E_DATA_TARGET_ERROR`。</span><span class="sxs-lookup"><span data-stu-id="39207-109">If a failing HRESULT is returned, ICorDebug APIs will return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="39207-110">注解</span><span class="sxs-lookup"><span data-stu-id="39207-110">Remarks</span></span>  

 <span data-ttu-id="39207-111">堆栈查看器应确保向前推进，以便最后 `Next` 的调用将返回失败的 HRESULT 或 `CORDBG_S_AT_END_OF_STACK`。</span><span class="sxs-lookup"><span data-stu-id="39207-111">The stack walker should ensure that it makes forward progress, so that eventually a call to `Next` will return a failing HRESULT or `CORDBG_S_AT_END_OF_STACK`.</span></span> <span data-ttu-id="39207-112">`S_OK`无限期返回可能导致无限循环。</span><span class="sxs-lookup"><span data-stu-id="39207-112">Returning `S_OK` indefinitely may cause an infinite loop.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="39207-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="39207-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39207-114">要求</span><span class="sxs-lookup"><span data-stu-id="39207-114">Requirements</span></span>  

 <span data-ttu-id="39207-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="39207-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39207-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="39207-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="39207-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="39207-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="39207-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39207-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39207-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39207-119">See also</span></span>

- [<span data-ttu-id="39207-120">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="39207-120">ICorDebugMemoryBuffer Interface</span></span>](icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="39207-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="39207-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
