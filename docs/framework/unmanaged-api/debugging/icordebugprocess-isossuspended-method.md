---
title: ICorDebugProcess::IsOSSuspended 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.IsOSSuspended
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::IsOSSuspended
helpviewer_keywords:
- IsOSSuspended method [.NET Framework debugging]
- ICorDebugProcess::IsOSSuspended method [.NET Framework debugging]
ms.assetid: 83406cb2-5797-4402-872d-89c9516aefec
topic_type:
- apiref
ms.openlocfilehash: fffa61d8e406162251b0934a9846e5a813422798
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724580"
---
# <a name="icordebugprocessisossuspended-method"></a><span data-ttu-id="6a3d0-102">ICorDebugProcess::IsOSSuspended 方法</span><span class="sxs-lookup"><span data-stu-id="6a3d0-102">ICorDebugProcess::IsOSSuspended Method</span></span>

<span data-ttu-id="6a3d0-103">获取一个值，该值指示是否由于调试器停止此进程而挂起了指定线程。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-103">Gets a value that indicates whether the specified thread has been suspended as a result of the debugger stopping this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a3d0-104">语法</span><span class="sxs-lookup"><span data-stu-id="6a3d0-104">Syntax</span></span>  
  
```cpp  
HRESULT IsOSSuspended(  
    [in]  DWORD threadID,  
    [out] BOOL  *pbSuspended);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6a3d0-105">参数</span><span class="sxs-lookup"><span data-stu-id="6a3d0-105">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="6a3d0-106">中相关线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-106">[in] The ID of thread in question.</span></span>  
  
 `pbSuspended`  
 <span data-ttu-id="6a3d0-107">弄指向布尔值的指针， `true` 如果指定线程已挂起，则为; 否则 `pbSuspended` 为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-107">[out] A pointer to a Boolean value that is `true` if the specified thread has been suspended; otherwise \*`pbSuspended` is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6a3d0-108">注解</span><span class="sxs-lookup"><span data-stu-id="6a3d0-108">Remarks</span></span>  

 <span data-ttu-id="6a3d0-109">当由于调试器停止此进程而暂停指定的线程时，指定线程的 Win32 挂起计数将递增1。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-109">When the specified thread has been suspended as a result of the debugger stopping this process, the specified thread's Win32 suspend count is incremented by one.</span></span> <span data-ttu-id="6a3d0-110">如果调试器用户界面向用户显示操作系统 (OS) 挂起线程计数，则 (UI) 可能需要考虑此信息。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-110">The debugger user interface (UI) may want to take this information into account if it displays the operating system (OS) suspend count of the thread to the user.</span></span>  
  
 <span data-ttu-id="6a3d0-111">此 `IsOSSuspended` 方法仅在非托管调试的上下文中有意义。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-111">The `IsOSSuspended` method makes sense only in the context of unmanaged debugging.</span></span> <span data-ttu-id="6a3d0-112">在托管调试期间，线程会以协作方式暂停，而不是由 OS 挂起。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-112">During managed debugging, threads are cooperatively suspended rather than OS-suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a3d0-113">要求</span><span class="sxs-lookup"><span data-stu-id="6a3d0-113">Requirements</span></span>  

 <span data-ttu-id="6a3d0-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6a3d0-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a3d0-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6a3d0-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6a3d0-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a3d0-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a3d0-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a3d0-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
