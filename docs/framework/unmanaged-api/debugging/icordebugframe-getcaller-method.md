---
title: ICorDebugFrame::GetCaller 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCaller
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCaller
helpviewer_keywords:
- GetCaller method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetCaller method [.NET Framework debugging]
ms.assetid: bfdc946b-8238-4eb9-8a85-884049fb0fd4
topic_type:
- apiref
ms.openlocfilehash: b52499e509bf172b03b5e4d2b1e4c677dc800281
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95690468"
---
# <a name="icordebugframegetcaller-method"></a><span data-ttu-id="5a9bc-102">ICorDebugFrame::GetCaller 方法</span><span class="sxs-lookup"><span data-stu-id="5a9bc-102">ICorDebugFrame::GetCaller Method</span></span>

<span data-ttu-id="5a9bc-103">获取一个指针，该指针指向当前链中调用此帧的 ICorDebugFrame 对象。</span><span class="sxs-lookup"><span data-stu-id="5a9bc-103">Gets a pointer to the ICorDebugFrame object in the current chain that called this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a9bc-104">语法</span><span class="sxs-lookup"><span data-stu-id="5a9bc-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCaller (  
    [out] ICorDebugFrame     **ppFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5a9bc-105">参数</span><span class="sxs-lookup"><span data-stu-id="5a9bc-105">Parameters</span></span>  

 `ppFrame`  
 <span data-ttu-id="5a9bc-106">弄指向 `ICorDebugFrame` 表示调用帧的对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="5a9bc-106">[out] A pointer to the address of an `ICorDebugFrame` object that represents the calling frame.</span></span> <span data-ttu-id="5a9bc-107">如果被调用的帧是当前链中最外层的帧，则此值为 null。</span><span class="sxs-lookup"><span data-stu-id="5a9bc-107">This value is null if the called frame is the outermost frame in the current chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5a9bc-108">要求</span><span class="sxs-lookup"><span data-stu-id="5a9bc-108">Requirements</span></span>  

 <span data-ttu-id="5a9bc-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5a9bc-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5a9bc-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5a9bc-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5a9bc-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5a9bc-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5a9bc-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5a9bc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
