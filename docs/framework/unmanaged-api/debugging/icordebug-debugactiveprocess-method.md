---
title: ICorDebug::DebugActiveProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.DebugActiveProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::DebugActiveProcess
helpviewer_keywords:
- DebugActiveProcess method [.NET Framework debugging]
- ICorDebug::DebugActiveProcess method [.NET Framework debugging]
ms.assetid: fdab0ade-7f56-4fa2-b3ef-f7a1d2852bba
topic_type:
- apiref
ms.openlocfilehash: 1713623fa575bea6df649106b37212f7aeaee6db
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723462"
---
# <a name="icordebugdebugactiveprocess-method"></a><span data-ttu-id="746db-102">ICorDebug::DebugActiveProcess 方法</span><span class="sxs-lookup"><span data-stu-id="746db-102">ICorDebug::DebugActiveProcess Method</span></span>

<span data-ttu-id="746db-103">将调试器附加到现有进程。</span><span class="sxs-lookup"><span data-stu-id="746db-103">Attaches the debugger to an existing process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="746db-104">语法</span><span class="sxs-lookup"><span data-stu-id="746db-104">Syntax</span></span>  
  
```cpp  
HRESULT DebugActiveProcess (  
    [in]  DWORD               id,  
    [in]  BOOL                win32Attach,  
    [out] ICorDebugProcess    **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="746db-105">参数</span><span class="sxs-lookup"><span data-stu-id="746db-105">Parameters</span></span>  

 `id`  
 <span data-ttu-id="746db-106">中调试器要附加到的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="746db-106">[in] The ID of the process to which the debugger is to be attached.</span></span>  
  
 `win32Attach`  
 <span data-ttu-id="746db-107">中 `true` 如果调试器应该表现为进程的 Win32 调试器并调度非托管回调，则设置为的布尔值; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="746db-107">[in] Boolean value that is set to `true` if the debugger should behave as the Win32 debugger for the process and dispatch the unmanaged callbacks; otherwise, `false`.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="746db-108">弄一个指向 "ICorDebugProcess" 对象地址的指针，该对象表示调试器已附加到的进程。</span><span class="sxs-lookup"><span data-stu-id="746db-108">[out] A pointer to the address of an "ICorDebugProcess" object that represents the process to which the debugger has been attached.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="746db-109">注解</span><span class="sxs-lookup"><span data-stu-id="746db-109">Remarks</span></span>  

 <span data-ttu-id="746db-110">Win9x 和非 x86 平台都不支持互操作调试，如基于 IA-64 和基于 AMD64 的平台。</span><span class="sxs-lookup"><span data-stu-id="746db-110">Interop debugging is not supported on Win9x and non-x86 platforms, such as IA-64-based and AMD64-based platforms.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="746db-111">要求</span><span class="sxs-lookup"><span data-stu-id="746db-111">Requirements</span></span>  

 <span data-ttu-id="746db-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="746db-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="746db-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="746db-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="746db-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="746db-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="746db-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="746db-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="746db-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="746db-116">See also</span></span>

- [<span data-ttu-id="746db-117">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="746db-117">ICorDebug Interface</span></span>](icordebug-interface.md)
