---
title: ICorDebugProcess2::ClearUnmanagedBreakpoint 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.ClearUnmanagedBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::ClearUnmanagedBreakpoint
helpviewer_keywords:
- ClearUnmanagedBreakpoint method [.NET Framework debugging]
- ICorDebugProcess2::ClearUnmanagedBreakpoint method [.NET Framework debugging]
ms.assetid: 12ed0fff-7f0e-4d7a-bb70-b3376371f36c
topic_type:
- apiref
ms.openlocfilehash: a713fd006f1e9ad8fe7109651c2cda5025da3566
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95673938"
---
# <a name="icordebugprocess2clearunmanagedbreakpoint-method"></a><span data-ttu-id="fac9a-102">ICorDebugProcess2::ClearUnmanagedBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="fac9a-102">ICorDebugProcess2::ClearUnmanagedBreakpoint Method</span></span>

<span data-ttu-id="fac9a-103">删除给定地址上先前设置的断点。</span><span class="sxs-lookup"><span data-stu-id="fac9a-103">Removes a previously set breakpoint at the given address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fac9a-104">语法</span><span class="sxs-lookup"><span data-stu-id="fac9a-104">Syntax</span></span>  
  
```cpp  
HRESULT ClearUnmanagedBreakpoint (  
    [in] CORDB_ADDRESS   address  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fac9a-105">参数</span><span class="sxs-lookup"><span data-stu-id="fac9a-105">Parameters</span></span>  

 `address`  
 <span data-ttu-id="fac9a-106">中一个 `CORDB_ADDRESS` 值，该值指定设置断点的地址。</span><span class="sxs-lookup"><span data-stu-id="fac9a-106">[in] A `CORDB_ADDRESS` value that specifies the address at which the breakpoint was set.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fac9a-107">注解</span><span class="sxs-lookup"><span data-stu-id="fac9a-107">Remarks</span></span>  

 <span data-ttu-id="fac9a-108">之前调用 [ICorDebugProcess2：： SetUnmanagedBreakpoint](icordebugprocess2-setunmanagedbreakpoint-method.md)之前已设置了指定的断点。</span><span class="sxs-lookup"><span data-stu-id="fac9a-108">The specified breakpoint would have been previously set by an earlier call to [ICorDebugProcess2::SetUnmanagedBreakpoint](icordebugprocess2-setunmanagedbreakpoint-method.md).</span></span>  
  
 <span data-ttu-id="fac9a-109">`ClearUnmanagedBreakpoint`当正在调试的进程正在运行时，可以调用方法。</span><span class="sxs-lookup"><span data-stu-id="fac9a-109">The `ClearUnmanagedBreakpoint` method can be called while the process being debugged is running.</span></span>  
  
 <span data-ttu-id="fac9a-110">`ClearUnmanagedBreakpoint`如果在仅限托管模式下附加调试器，则方法将返回失败代码; 如果指定地址处不存在任何断点，则返回。</span><span class="sxs-lookup"><span data-stu-id="fac9a-110">The `ClearUnmanagedBreakpoint` method returns a failure code if the debugger is attached in managed-only mode or if no breakpoint exists at the specified address.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fac9a-111">要求</span><span class="sxs-lookup"><span data-stu-id="fac9a-111">Requirements</span></span>  

 <span data-ttu-id="fac9a-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fac9a-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fac9a-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fac9a-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fac9a-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fac9a-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fac9a-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fac9a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
