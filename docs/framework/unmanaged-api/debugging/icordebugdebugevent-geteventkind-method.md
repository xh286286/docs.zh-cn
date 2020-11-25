---
title: ICorDebugDebugEvent::GetEventKind 方法
ms.date: 03/30/2017
ms.assetid: c37aaceb-c948-46bd-a943-08be4cbb76f4
ms.openlocfilehash: 7876dc6ec5ecee52b64e54e1c42533f8348e4dc4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713673"
---
# <a name="icordebugdebugeventgeteventkind-method"></a><span data-ttu-id="3c116-102">ICorDebugDebugEvent::GetEventKind 方法</span><span class="sxs-lookup"><span data-stu-id="3c116-102">ICorDebugDebugEvent::GetEventKind Method</span></span>

<span data-ttu-id="3c116-103">指出该 `ICorDebugDebugEvent` 对象代表的事件类型。</span><span class="sxs-lookup"><span data-stu-id="3c116-103">Indicates what kind of event this `ICorDebugDebugEvent` object represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c116-104">语法</span><span class="sxs-lookup"><span data-stu-id="3c116-104">Syntax</span></span>  
  
```cpp  
HRESULT GetEventKind(  
    [out]CorDebugDebugEventKind *pDebugEventKind  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3c116-105">参数</span><span class="sxs-lookup"><span data-stu-id="3c116-105">Parameters</span></span>  

 <span data-ttu-id="3c116-106">p调试事件类型</span><span class="sxs-lookup"><span data-stu-id="3c116-106">pDebugEventKind</span></span>  
 <span data-ttu-id="3c116-107">指向指示事件类型的 [CorDebugDebugEventKind](cordebugdebugeventkind-enumeration.md) 枚举成员的指针。</span><span class="sxs-lookup"><span data-stu-id="3c116-107">A pointer to a [CorDebugDebugEventKind](cordebugdebugeventkind-enumeration.md) enumeration member that indicates the type of event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3c116-108">注解</span><span class="sxs-lookup"><span data-stu-id="3c116-108">Remarks</span></span>  

 <span data-ttu-id="3c116-109">基于 `pDebugEventKind` 值，可调用 `QueryInterface` 以获取包含其他数据的精确度更高的调试事件接口。</span><span class="sxs-lookup"><span data-stu-id="3c116-109">Based on the value of `pDebugEventKind`, you can call `QueryInterface` to get a more precise debug event interface that has additional data.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3c116-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="3c116-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c116-111">要求</span><span class="sxs-lookup"><span data-stu-id="3c116-111">Requirements</span></span>  

 <span data-ttu-id="3c116-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c116-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c116-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3c116-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3c116-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c116-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c116-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c116-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c116-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c116-116">See also</span></span>

- [<span data-ttu-id="3c116-117">“ICor调试调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="3c116-117">ICorDebugDebugEvent Interface</span></span>](icordebugdebugevent-interface.md)
- [<span data-ttu-id="3c116-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="3c116-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
