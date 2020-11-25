---
title: ICorDebugThread::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetProcess
helpviewer_keywords:
- ICorDebugThread::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 163816e7-0739-4566-b3df-cd256be8b8a4
topic_type:
- apiref
ms.openlocfilehash: d3697bd8a3f32c802ab2e335f89c84efaf3e4db0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727986"
---
# <a name="icordebugthreadgetprocess-method"></a><span data-ttu-id="d72e2-102">ICorDebugThread::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="d72e2-102">ICorDebugThread::GetProcess Method</span></span>

<span data-ttu-id="d72e2-103">获取一个接口指针，该指针指向此 ICorDebugThread 构成部件的进程。</span><span class="sxs-lookup"><span data-stu-id="d72e2-103">Gets an interface pointer to the process of which this ICorDebugThread forms a part.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d72e2-104">语法</span><span class="sxs-lookup"><span data-stu-id="d72e2-104">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d72e2-105">参数</span><span class="sxs-lookup"><span data-stu-id="d72e2-105">Parameters</span></span>  

 `ppProcess`  
 <span data-ttu-id="d72e2-106">弄指向表示进程的 ICorDebugProcess 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="d72e2-106">[out] A pointer to the address of an ICorDebugProcess interface object that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d72e2-107">要求</span><span class="sxs-lookup"><span data-stu-id="d72e2-107">Requirements</span></span>  

 <span data-ttu-id="d72e2-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d72e2-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d72e2-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d72e2-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d72e2-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d72e2-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d72e2-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d72e2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
