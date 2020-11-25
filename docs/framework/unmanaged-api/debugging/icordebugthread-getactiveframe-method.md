---
title: ICorDebugThread::GetActiveFrame 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetActiveFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetActiveFrame
helpviewer_keywords:
- ICorDebugThread::GetActiveFrame method [.NET Framework debugging]
- GetActiveFrame method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 8d6d3a1a-fef6-4f2f-a22c-3bdd30d70e07
topic_type:
- apiref
ms.openlocfilehash: 6ca4c1ad5ef575db075a5066146bacb6d1e59ea2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728077"
---
# <a name="icordebugthreadgetactiveframe-method"></a><span data-ttu-id="7f529-102">ICorDebugThread::GetActiveFrame 方法</span><span class="sxs-lookup"><span data-stu-id="7f529-102">ICorDebugThread::GetActiveFrame Method</span></span>

<span data-ttu-id="7f529-103">获取一个接口指针，该指针指向此 ICorDebugThread 对象上的活动 (最新) 帧。</span><span class="sxs-lookup"><span data-stu-id="7f529-103">Gets an interface pointer to the active (most recent) frame on this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f529-104">语法</span><span class="sxs-lookup"><span data-stu-id="7f529-104">Syntax</span></span>  
  
```cpp  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f529-105">参数</span><span class="sxs-lookup"><span data-stu-id="7f529-105">Parameters</span></span>  

 `ppFrame`  
 <span data-ttu-id="7f529-106">弄指向表示帧的 ICorDebugFrame 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="7f529-106">[out] A pointer to the address of an ICorDebugFrame interface object that represents a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7f529-107">注解</span><span class="sxs-lookup"><span data-stu-id="7f529-107">Remarks</span></span>  

 <span data-ttu-id="7f529-108">`ppFrame`如果当前没有活动帧，则参数为 null。</span><span class="sxs-lookup"><span data-stu-id="7f529-108">The `ppFrame` parameter is null if no frame is currently active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f529-109">要求</span><span class="sxs-lookup"><span data-stu-id="7f529-109">Requirements</span></span>  

 <span data-ttu-id="7f529-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f529-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f529-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7f529-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7f529-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7f529-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7f529-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f529-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
