---
title: ICorDebug::GetProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::GetProcess method [.NET Framework debugging]
ms.assetid: 10a40ba0-1b65-4721-bd11-cf12d57b280d
topic_type:
- apiref
ms.openlocfilehash: 46c2b444984c5a0062f1cfbc0cd29dbe409b16fa
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723436"
---
# <a name="icordebuggetprocess-method"></a><span data-ttu-id="95938-102">ICorDebug::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="95938-102">ICorDebug::GetProcess Method</span></span>

<span data-ttu-id="95938-103">获取指向指定进程的 "ICorDebugProcess" 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="95938-103">Gets a pointer to the "ICorDebugProcess" instance for the specified process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95938-104">语法</span><span class="sxs-lookup"><span data-stu-id="95938-104">Syntax</span></span>  
  
```cpp  
HRESULT GetProcess (  
    [in] DWORD               dwProcessId,  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="95938-105">参数</span><span class="sxs-lookup"><span data-stu-id="95938-105">Parameters</span></span>  

 `dwProcessId`  
 <span data-ttu-id="95938-106">中进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="95938-106">[in] The ID of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="95938-107">弄指向指定进程的实例地址的指针 `ICorDebugProcess` 。</span><span class="sxs-lookup"><span data-stu-id="95938-107">[out] A pointer to the address of a `ICorDebugProcess` instance for the specified process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95938-108">要求</span><span class="sxs-lookup"><span data-stu-id="95938-108">Requirements</span></span>  

 <span data-ttu-id="95938-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="95938-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95938-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="95938-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="95938-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="95938-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="95938-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95938-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95938-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95938-113">See also</span></span>

- [<span data-ttu-id="95938-114">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="95938-114">ICorDebug Interface</span></span>](icordebug-interface.md)
