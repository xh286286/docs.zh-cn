---
title: ICorDebugThread::GetActiveChain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetActiveChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetActiveChain
helpviewer_keywords:
- ICorDebugThread::GetActiveChain method [.NET Framework debugging]
- GetActiveChain method [.NET Framework debugging]
ms.assetid: f50de1f7-40ef-4949-b542-1d9a61f7bfef
topic_type:
- apiref
ms.openlocfilehash: e6b1d78b2bd95ea27f4b19a045cd2680342e8a80
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728090"
---
# <a name="icordebugthreadgetactivechain-method"></a><span data-ttu-id="b28d2-102">ICorDebugThread::GetActiveChain 方法</span><span class="sxs-lookup"><span data-stu-id="b28d2-102">ICorDebugThread::GetActiveChain Method</span></span>

<span data-ttu-id="b28d2-103">获取一个接口指针，该指针指向此 ICorDebugThread 对象上的活动 (最新) 堆栈链。</span><span class="sxs-lookup"><span data-stu-id="b28d2-103">Gets an interface pointer to the active (most recent) stack chain on this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b28d2-104">语法</span><span class="sxs-lookup"><span data-stu-id="b28d2-104">Syntax</span></span>  
  
```cpp  
HRESULT GetActiveChain (  
    [out] ICorDebugChain **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b28d2-105">参数</span><span class="sxs-lookup"><span data-stu-id="b28d2-105">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="b28d2-106">弄指向表示堆栈链的 ICorDebugChain 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="b28d2-106">[out] A pointer to the address of an ICorDebugChain object that represents the stack chain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b28d2-107">注解</span><span class="sxs-lookup"><span data-stu-id="b28d2-107">Remarks</span></span>  

 <span data-ttu-id="b28d2-108">`ppChain`如果当前没有堆栈链处于活动状态，则参数为 null。</span><span class="sxs-lookup"><span data-stu-id="b28d2-108">The `ppChain` parameter is null if no stack chain is currently active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b28d2-109">要求</span><span class="sxs-lookup"><span data-stu-id="b28d2-109">Requirements</span></span>  

 <span data-ttu-id="b28d2-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b28d2-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b28d2-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b28d2-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b28d2-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b28d2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b28d2-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b28d2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
