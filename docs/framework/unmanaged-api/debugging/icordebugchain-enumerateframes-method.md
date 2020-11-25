---
title: ICorDebugChain::EnumerateFrames 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.EnumerateFrames
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::EnumerateFrames method
helpviewer_keywords:
- EnumerateFrames method [.NET Framework debugging]
- ICorDebugChain::EnumerateFrames method [.NET Framework debugging]
ms.assetid: 9fcefa98-750d-4168-8915-8173a43accf2
topic_type:
- apiref
ms.openlocfilehash: ae6d81e6fdab0f8e3346d8a08a3b5ebc329a542a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730144"
---
# <a name="icordebugchainenumerateframes-method"></a><span data-ttu-id="43972-102">ICorDebugChain::EnumerateFrames 方法</span><span class="sxs-lookup"><span data-stu-id="43972-102">ICorDebugChain::EnumerateFrames Method</span></span>

<span data-ttu-id="43972-103">获取一个枚举数，该枚举数包含链中所有托管堆栈帧（从最新帧开始）。</span><span class="sxs-lookup"><span data-stu-id="43972-103">Gets an enumerator that contains all the managed stack frames in the chain, starting with the most recent frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43972-104">语法</span><span class="sxs-lookup"><span data-stu-id="43972-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateFrames (  
    [out] ICorDebugFrameEnum **ppFrames  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="43972-105">参数</span><span class="sxs-lookup"><span data-stu-id="43972-105">Parameters</span></span>  

 `ppFrames`  
 <span data-ttu-id="43972-106">弄指向 ICorDebugFrameEnum 对象地址的指针，该对象是堆栈帧的枚举器。</span><span class="sxs-lookup"><span data-stu-id="43972-106">[out] A pointer to the address of an ICorDebugFrameEnum object that is the enumerator for the stack frames.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="43972-107">注解</span><span class="sxs-lookup"><span data-stu-id="43972-107">Remarks</span></span>  

 <span data-ttu-id="43972-108">链表示线程的物理调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="43972-108">The chain represents the physical call stack for the thread.</span></span>  
  
 <span data-ttu-id="43972-109">`EnumerateFrames`只应为托管链调用方法。</span><span class="sxs-lookup"><span data-stu-id="43972-109">The `EnumerateFrames` method should be called only for managed chains.</span></span> <span data-ttu-id="43972-110">调试 API 不提供用于获取非托管链中包含的帧的方法。</span><span class="sxs-lookup"><span data-stu-id="43972-110">The debugging API does not provide methods for obtaining frames contained in unmanaged chains.</span></span> <span data-ttu-id="43972-111">调试器必须使用其他方法来获取此信息。</span><span class="sxs-lookup"><span data-stu-id="43972-111">The debugger must use other means to obtain this information.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="43972-112">要求</span><span class="sxs-lookup"><span data-stu-id="43972-112">Requirements</span></span>  

 <span data-ttu-id="43972-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="43972-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43972-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="43972-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="43972-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="43972-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="43972-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43972-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
