---
title: ICorDebugThread::GetUserState 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetUserState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetUserState
helpviewer_keywords:
- GetUserState method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetUserState method [.NET Framework debugging]
ms.assetid: ae0cfd73-8ead-4d36-9310-dccaac9db0bd
topic_type:
- apiref
ms.openlocfilehash: dd3936656ce1c9482b7f07a5780fcf651356b4be
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727960"
---
# <a name="icordebugthreadgetuserstate-method"></a><span data-ttu-id="126d9-102">ICorDebugThread::GetUserState 方法</span><span class="sxs-lookup"><span data-stu-id="126d9-102">ICorDebugThread::GetUserState Method</span></span>

<span data-ttu-id="126d9-103">获取此 ICorDebugThread 的当前用户状态。</span><span class="sxs-lookup"><span data-stu-id="126d9-103">Gets the current user state of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="126d9-104">语法</span><span class="sxs-lookup"><span data-stu-id="126d9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetUserState (  
    [out] CorDebugUserState   *pState  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="126d9-105">参数</span><span class="sxs-lookup"><span data-stu-id="126d9-105">Parameters</span></span>  

 `pState`  
 <span data-ttu-id="126d9-106">弄一个指针，指向用于描述此线程当前用户状态的 CorDebugUserState 枚举值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="126d9-106">[out] A pointer to a bitwise combination of CorDebugUserState enumeration values that describe the current user state of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="126d9-107">注解</span><span class="sxs-lookup"><span data-stu-id="126d9-107">Remarks</span></span>  

 <span data-ttu-id="126d9-108">线程的用户状态是由正在调试的程序检查的线程的状态。</span><span class="sxs-lookup"><span data-stu-id="126d9-108">The user state of the thread is the state of the thread when it is examined by the program that is being debugged.</span></span> <span data-ttu-id="126d9-109">线程可能会设置多个状态位。</span><span class="sxs-lookup"><span data-stu-id="126d9-109">A thread may have multiple state bits set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="126d9-110">要求</span><span class="sxs-lookup"><span data-stu-id="126d9-110">Requirements</span></span>  

 <span data-ttu-id="126d9-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="126d9-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="126d9-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="126d9-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="126d9-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="126d9-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="126d9-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="126d9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
