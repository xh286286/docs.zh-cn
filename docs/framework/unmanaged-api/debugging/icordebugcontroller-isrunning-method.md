---
title: ICorDebugController::IsRunning 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.IsRunning
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::IsRunning
helpviewer_keywords:
- IsRunning method [.NET Framework debugging]
- ICorDebugController::IsRunning method [.NET Framework debugging]
ms.assetid: b33ff059-40c4-4dfe-9cb2-21bfed2de0b0
topic_type:
- apiref
ms.openlocfilehash: 73ed86ee12b02d292dc6dfc1d652459a679f81ca
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679931"
---
# <a name="icordebugcontrollerisrunning-method"></a><span data-ttu-id="77b53-102">ICorDebugController::IsRunning 方法</span><span class="sxs-lookup"><span data-stu-id="77b53-102">ICorDebugController::IsRunning Method</span></span>

<span data-ttu-id="77b53-103">获取一个值，该值指示进程中的线程当前是否可以自由运行。</span><span class="sxs-lookup"><span data-stu-id="77b53-103">Gets a value that indicates whether the threads in the process are currently running freely.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77b53-104">语法</span><span class="sxs-lookup"><span data-stu-id="77b53-104">Syntax</span></span>  
  
```cpp  
HRESULT IsRunning (  
    [out] BOOL *pbRunning  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77b53-105">参数</span><span class="sxs-lookup"><span data-stu-id="77b53-105">Parameters</span></span>  

 `pbRunning`  
 <span data-ttu-id="77b53-106">弄一个指向值的指针， `true` 如果进程中的线程自由运行，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="77b53-106">[out] A pointer to a value that is `true` if the threads in the process are running freely; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77b53-107">要求</span><span class="sxs-lookup"><span data-stu-id="77b53-107">Requirements</span></span>  

 <span data-ttu-id="77b53-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77b53-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77b53-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="77b53-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="77b53-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="77b53-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="77b53-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77b53-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77b53-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77b53-112">See also</span></span>
