---
title: ICorDebugDataTarget::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget.GetThreadContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget::GetThreadContext
helpviewer_keywords:
- ICorDebugDataTarget::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: c8954268-1821-4b23-b665-dbb55f2af31b
topic_type:
- apiref
ms.openlocfilehash: faacea6a2f04ef20025fd33adb4ce76eaf54f32c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95679736"
---
# <a name="icordebugdatatargetgetthreadcontext-method"></a><span data-ttu-id="1dc72-102">ICorDebugDataTarget::GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="1dc72-102">ICorDebugDataTarget::GetThreadContext Method</span></span>

<span data-ttu-id="1dc72-103">返回指定线程的当前线程上下文。</span><span class="sxs-lookup"><span data-stu-id="1dc72-103">Returns the current thread context for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1dc72-104">语法</span><span class="sxs-lookup"><span data-stu-id="1dc72-104">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadContext(  
       [in] DWORD dwThreadID,  
       [in] ULONG32 contextFlags,  
       [in] ULONG32 contextSize,  
       [out, size_is(contextSize)] BYTE * pContext);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1dc72-105">参数</span><span class="sxs-lookup"><span data-stu-id="1dc72-105">Parameters</span></span>  

 `dwThreadID`  
 <span data-ttu-id="1dc72-106">中要检索其上下文的线程的标识符。</span><span class="sxs-lookup"><span data-stu-id="1dc72-106">[in] The identifier of the thread whose context is to be retrieved.</span></span> <span data-ttu-id="1dc72-107">标识符由操作系统定义。</span><span class="sxs-lookup"><span data-stu-id="1dc72-107">The identifier is defined by the operating system.</span></span>  
  
 `contextFlags`  
 <span data-ttu-id="1dc72-108">中平台相关标志的按位组合，用于指示应读取上下文的哪些部分。</span><span class="sxs-lookup"><span data-stu-id="1dc72-108">[in] A bitwise combination of platform-dependent flags that indicate which portions of the context should be read.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="1dc72-109">[输入] `pContext` 的大小。</span><span class="sxs-lookup"><span data-stu-id="1dc72-109">[in] The size of `pContext`.</span></span>  
  
 `pContext`  
 <span data-ttu-id="1dc72-110">弄将存储线程上下文的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="1dc72-110">[out] The buffer where the thread context will be stored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1dc72-111">注解</span><span class="sxs-lookup"><span data-stu-id="1dc72-111">Remarks</span></span>  

 <span data-ttu-id="1dc72-112">在 Windows 平台上， `pContext` 必须是 `CONTEXT`) 在 [ICorDebugDataTarget：： GetPlatform](icordebugdatatarget-getplatform-method.md) 方法指定的计算机类型中定义的结构 (。</span><span class="sxs-lookup"><span data-stu-id="1dc72-112">On Windows platforms, `pContext` must be a `CONTEXT` structure (defined in WinNT.h) that is appropriate for the machine type specified by the [ICorDebugDataTarget::GetPlatform](icordebugdatatarget-getplatform-method.md) method.</span></span> <span data-ttu-id="1dc72-113">`contextFlags` 必须与结构的字段具有相同的值 `ContextFlags` `CONTEXT` 。</span><span class="sxs-lookup"><span data-stu-id="1dc72-113">`contextFlags` must have the same values as the `ContextFlags` field of the `CONTEXT` structure.</span></span> <span data-ttu-id="1dc72-114">`CONTEXT`结构特定于处理器; 有关详细信息，请参阅 WinNT .h 文件。</span><span class="sxs-lookup"><span data-stu-id="1dc72-114">The `CONTEXT` structure is processor-specific; refer to the WinNT.h file for details.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1dc72-115">要求</span><span class="sxs-lookup"><span data-stu-id="1dc72-115">Requirements</span></span>  

 <span data-ttu-id="1dc72-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1dc72-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1dc72-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1dc72-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1dc72-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1dc72-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1dc72-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1dc72-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1dc72-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1dc72-120">See also</span></span>

- [<span data-ttu-id="1dc72-121">ICorDebugDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="1dc72-121">ICorDebugDataTarget Interface</span></span>](icordebugdatatarget-interface.md)
- [<span data-ttu-id="1dc72-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="1dc72-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="1dc72-123">调试</span><span class="sxs-lookup"><span data-stu-id="1dc72-123">Debugging</span></span>](index.md)
