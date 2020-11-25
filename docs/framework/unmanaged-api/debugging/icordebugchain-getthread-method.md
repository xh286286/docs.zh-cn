---
title: ICorDebugChain::GetThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugChain interface [.NET Framework debugging]
- ICorDebugChain::GetThread method [.NET Framework debugging]
ms.assetid: b3390319-6366-418c-ba80-b552ac4dfc1e
topic_type:
- apiref
ms.openlocfilehash: ad220289b45078130a0a41e67373fd3384ae9682
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724411"
---
# <a name="icordebugchaingetthread-method"></a><span data-ttu-id="e0649-102">ICorDebugChain::GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="e0649-102">ICorDebugChain::GetThread Method</span></span>

<span data-ttu-id="e0649-103">获取此调用链所属的物理线程。</span><span class="sxs-lookup"><span data-stu-id="e0649-103">Gets the physical thread this call chain is part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0649-104">语法</span><span class="sxs-lookup"><span data-stu-id="e0649-104">Syntax</span></span>  
  
```cpp  
HRESULT GetThread (  
    [out] ICorDebugThread    **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e0649-105">参数</span><span class="sxs-lookup"><span data-stu-id="e0649-105">Parameters</span></span>  

 `ppThread`  
 <span data-ttu-id="e0649-106">弄指向 ICorDebugThread 对象的指针，该对象表示此调用链所属的物理线程。</span><span class="sxs-lookup"><span data-stu-id="e0649-106">[out] A pointer to an ICorDebugThread object that represents the physical thread this call chain is part of.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e0649-107">要求</span><span class="sxs-lookup"><span data-stu-id="e0649-107">Requirements</span></span>  

 <span data-ttu-id="e0649-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e0649-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0649-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e0649-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e0649-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e0649-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e0649-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e0649-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
