---
title: ICorDebugChain::GetCallee 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetCallee
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetCallee method
helpviewer_keywords:
- ICorDebugChain::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 19560c79-abdc-4bdf-a5fe-eb362a59edc0
topic_type:
- apiref
ms.openlocfilehash: a28da34cd3080826f346b8957aa6ba38258b924f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730118"
---
# <a name="icordebugchaingetcallee-method"></a><span data-ttu-id="d3ab9-102">ICorDebugChain::GetCallee 方法</span><span class="sxs-lookup"><span data-stu-id="d3ab9-102">ICorDebugChain::GetCallee Method</span></span>

<span data-ttu-id="d3ab9-103">获取此链调用的链。</span><span class="sxs-lookup"><span data-stu-id="d3ab9-103">Gets the chain that was called by this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3ab9-104">语法</span><span class="sxs-lookup"><span data-stu-id="d3ab9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCallee (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d3ab9-105">参数</span><span class="sxs-lookup"><span data-stu-id="d3ab9-105">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="d3ab9-106">弄指向 ICorDebugChain 对象的地址的指针，该对象表示调用的链。</span><span class="sxs-lookup"><span data-stu-id="d3ab9-106">[out] A pointer to the address of an ICorDebugChain object that represents the called chain.</span></span> <span data-ttu-id="d3ab9-107">如果此链当前正在执行 (即，如果此链未等待调用的链返回) ， `ppChain` 则将为 null。</span><span class="sxs-lookup"><span data-stu-id="d3ab9-107">If this chain is currently executing (that is, if this chain is not waiting for a called chain to return), `ppChain` will be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d3ab9-108">注解</span><span class="sxs-lookup"><span data-stu-id="d3ab9-108">Remarks</span></span>  

 <span data-ttu-id="d3ab9-109">此链将等待调用的链返回，然后再继续执行。</span><span class="sxs-lookup"><span data-stu-id="d3ab9-109">This chain will wait for the called chain to return before it resumes execution.</span></span> <span data-ttu-id="d3ab9-110">对于跨线程封送调用，被调用的链可以在另一个线程上。</span><span class="sxs-lookup"><span data-stu-id="d3ab9-110">The called chain may be on another thread in the case of cross-thread marshaled calls.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3ab9-111">要求</span><span class="sxs-lookup"><span data-stu-id="d3ab9-111">Requirements</span></span>  

 <span data-ttu-id="d3ab9-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d3ab9-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3ab9-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d3ab9-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d3ab9-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d3ab9-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d3ab9-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3ab9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
