---
title: ICorDebugRemote::DebugActiveProcessEx 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRemote.DebugActiveProcessEx
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget::DebugActiveProcessEx
helpviewer_keywords:
- ICorDebugRemote::DebugActiveProcessEx method [.NET Framework debugging]
- DebugActiveProcessEx method, ICorDebugRemote interface [.NET Framework debugging]
ms.assetid: b0df5c5d-9a2e-47bf-894c-6f8a9fe24a1f
topic_type:
- apiref
ms.openlocfilehash: c9847fd6122aa32c95aecd5643a62a6775ae38d3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712113"
---
# <a name="icordebugremotedebugactiveprocessex-method"></a><span data-ttu-id="d11b9-102">ICorDebugRemote::DebugActiveProcessEx 方法</span><span class="sxs-lookup"><span data-stu-id="d11b9-102">ICorDebugRemote::DebugActiveProcessEx Method</span></span>

<span data-ttu-id="d11b9-103">在调试器下的远程计算机上启动进程。</span><span class="sxs-lookup"><span data-stu-id="d11b9-103">Launches a process on a remote machine under the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d11b9-104">语法</span><span class="sxs-lookup"><span data-stu-id="d11b9-104">Syntax</span></span>  
  
```cpp  
HRESULT DebugActiveProcessEx (  
    [in]  ICorDebugRemoteTarget *   pRemoteTarget,  
    [in]  DWORD                     dwProcessId,  
    [in]  BOOL                      fWin32Attach,  
    [out] ICorDebugProcess **       ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d11b9-105">参数</span><span class="sxs-lookup"><span data-stu-id="d11b9-105">Parameters</span></span>  

 `pRemoteTarget`  
 <span data-ttu-id="d11b9-106">中指向 [ICorDebugRemoteTarget 接口](icordebugremotetarget-interface.md)的指针。</span><span class="sxs-lookup"><span data-stu-id="d11b9-106">[in] Pointer to an [ICorDebugRemoteTarget Interface](icordebugremotetarget-interface.md).</span></span> <span data-ttu-id="d11b9-107">此参数用于确定正在运行进程的计算机。</span><span class="sxs-lookup"><span data-stu-id="d11b9-107">This parameter is used to determine the machine on which the process is running.</span></span>  
  
 `id`  
 <span data-ttu-id="d11b9-108">中调试器要附加到的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="d11b9-108">[in] The ID of the process to which the debugger is to be attached.</span></span>  
  
 `win32Attach`  
 <span data-ttu-id="d11b9-109">[in] `true` 如果调试器应该表现为进程的 Win32 调试器并调度非托管回调，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="d11b9-109">[in] `true` if the debugger should behave as the Win32 debugger for the process and dispatch the unmanaged callbacks; otherwise, `false`.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="d11b9-110">弄一个指向 "ICorDebugProcess" 对象地址的指针，该对象表示调试器已附加到的进程。</span><span class="sxs-lookup"><span data-stu-id="d11b9-110">[out] A pointer to the address of an "ICorDebugProcess" object that represents the process to which the debugger has been attached.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d11b9-111">返回值</span><span class="sxs-lookup"><span data-stu-id="d11b9-111">Return Value</span></span>  

 <span data-ttu-id="d11b9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d11b9-112">S_OK</span></span>  
 <span data-ttu-id="d11b9-113">已成功附加到远程计算机上的进程。</span><span class="sxs-lookup"><span data-stu-id="d11b9-113">Successfully attached to the process on the remote machine.</span></span>  
  
 <span data-ttu-id="d11b9-114">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="d11b9-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="d11b9-115">无法附加到远程计算机上的进程。</span><span class="sxs-lookup"><span data-stu-id="d11b9-115">Unable to attach to the process on the remote machine.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d11b9-116">注解</span><span class="sxs-lookup"><span data-stu-id="d11b9-116">Remarks</span></span>  

 <span data-ttu-id="d11b9-117">Silverlight 中不支持混合模式调试。</span><span class="sxs-lookup"><span data-stu-id="d11b9-117">Mixed-mode debugging is not supported in Silverlight.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d11b9-118">要求</span><span class="sxs-lookup"><span data-stu-id="d11b9-118">Requirements</span></span>  

 <span data-ttu-id="d11b9-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d11b9-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d11b9-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d11b9-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d11b9-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d11b9-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d11b9-122">**.NET Framework 版本：** 4.5、4、3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="d11b9-122">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d11b9-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d11b9-123">See also</span></span>

- [<span data-ttu-id="d11b9-124">ICorDebugRemote 接口</span><span class="sxs-lookup"><span data-stu-id="d11b9-124">ICorDebugRemote Interface</span></span>](icordebugremote-interface.md)
- [<span data-ttu-id="d11b9-125">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="d11b9-125">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="d11b9-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="d11b9-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
