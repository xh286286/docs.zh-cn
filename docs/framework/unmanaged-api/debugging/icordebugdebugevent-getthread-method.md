---
title: ICorDebugDebugEvent::GetThread Method
ms.date: 03/30/2017
ms.assetid: 4f2e9a2c-8369-4a07-a881-ad5422626353
ms.openlocfilehash: ca6aba7897d9e97743d29db49bd058e140f84e6e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713582"
---
# <a name="icordebugdebugeventgetthread-method"></a><span data-ttu-id="8fcde-102">ICorDebugDebugEvent::GetThread Method</span><span class="sxs-lookup"><span data-stu-id="8fcde-102">ICorDebugDebugEvent::GetThread Method</span></span>

<span data-ttu-id="8fcde-103">获取发生事件的线程。</span><span class="sxs-lookup"><span data-stu-id="8fcde-103">Gets the thread on which the event occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fcde-104">语法</span><span class="sxs-lookup"><span data-stu-id="8fcde-104">Syntax</span></span>  
  
```cpp  
HRESULT GetThread(  
        [out]ICorDebugThread **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fcde-105">参数</span><span class="sxs-lookup"><span data-stu-id="8fcde-105">Parameters</span></span>  

 <span data-ttu-id="8fcde-106">ppThread</span><span class="sxs-lookup"><span data-stu-id="8fcde-106">ppThread</span></span>  
 <span data-ttu-id="8fcde-107">[输出] 指针指向代表事件发生线程的 ICorDebugThread 对象的地址。</span><span class="sxs-lookup"><span data-stu-id="8fcde-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread on which the event occurred.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8fcde-108">注解</span><span class="sxs-lookup"><span data-stu-id="8fcde-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8fcde-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="8fcde-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fcde-110">要求</span><span class="sxs-lookup"><span data-stu-id="8fcde-110">Requirements</span></span>  

 <span data-ttu-id="8fcde-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8fcde-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fcde-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8fcde-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8fcde-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8fcde-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8fcde-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8fcde-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fcde-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fcde-115">See also</span></span>

- [<span data-ttu-id="8fcde-116">“ICor调试调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="8fcde-116">ICorDebugDebugEvent Interface</span></span>](icordebugdebugevent-interface.md)
- [<span data-ttu-id="8fcde-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="8fcde-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
