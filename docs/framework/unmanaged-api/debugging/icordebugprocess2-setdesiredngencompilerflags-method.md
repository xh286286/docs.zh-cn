---
title: ICorDebugProcess2::SetDesiredNGENCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.SetDesiredNGENCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::SetDesiredNGENCompilerFlags
helpviewer_keywords:
- ICorDebugProcess2::SetDesiredNGENCompilerFlags method [.NET Framework debugging]
- SetDesiredNGENCompilerFlags method [.NET Framework debugging]
ms.assetid: 98320175-7c5e-4dbb-8683-86fa82e2641f
topic_type:
- apiref
ms.openlocfilehash: 40b944f6a1204bfe506ed64408be30f68adf3170
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675251"
---
# <a name="icordebugprocess2setdesiredngencompilerflags-method"></a><span data-ttu-id="e6f56-102">ICorDebugProcess2::SetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="e6f56-102">ICorDebugProcess2::SetDesiredNGENCompilerFlags Method</span></span>

<span data-ttu-id="e6f56-103">设置必须嵌入到预编译的映像中的标志，使运行时能够将该图像加载到当前进程。</span><span class="sxs-lookup"><span data-stu-id="e6f56-103">Sets the flags that must be embedded in a precompiled image in order for the runtime to load that image into the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6f56-104">语法</span><span class="sxs-lookup"><span data-stu-id="e6f56-104">Syntax</span></span>  
  
```cpp  
HRESULT SetDesiredNGENCompilerFlags (  
    [in] DWORD    pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6f56-105">参数</span><span class="sxs-lookup"><span data-stu-id="e6f56-105">Parameters</span></span>  

 `pdwFlags`  
 <span data-ttu-id="e6f56-106">中 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的一个值，该值指定用于选择正确预编译图像的编译器标志。</span><span class="sxs-lookup"><span data-stu-id="e6f56-106">[in] A value of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration that specifies the compiler flags used to select the correct pre-compiled image.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6f56-107">注解</span><span class="sxs-lookup"><span data-stu-id="e6f56-107">Remarks</span></span>  

 <span data-ttu-id="e6f56-108">`SetDesiredNGENCompilerFlags`方法指定必须嵌入到预编译的映像中的标志，以使运行时将该图像加载到此进程中。</span><span class="sxs-lookup"><span data-stu-id="e6f56-108">The `SetDesiredNGENCompilerFlags` method specifies the flags that must be embedded in a precompiled image so that the runtime will load that image into this process.</span></span> <span data-ttu-id="e6f56-109">此方法设置的标志仅用于选择正确的预编译映像。</span><span class="sxs-lookup"><span data-stu-id="e6f56-109">The flags set by this method are used only to select the correct precompiled image.</span></span> <span data-ttu-id="e6f56-110">如果不存在这样的图像，则运行时将 (MSIL) 映像和实时 (JIT) 编译器加载 Microsoft 中间语言。</span><span class="sxs-lookup"><span data-stu-id="e6f56-110">If no such image exists, the runtime will load the Microsoft intermediate language (MSIL) image and the just-in-time (JIT) compiler instead.</span></span> <span data-ttu-id="e6f56-111">在这种情况下，调试器仍必须使用 [ICorDebugModule2：： SetJITCompilerFlags](icordebugmodule2-setjitcompilerflags-method.md) 方法根据需要为 JIT 编译设置标志。</span><span class="sxs-lookup"><span data-stu-id="e6f56-111">In that case, the debugger must still use the [ICorDebugModule2::SetJITCompilerFlags](icordebugmodule2-setjitcompilerflags-method.md) method to set the flags as desired for the JIT compilation.</span></span>  
  
 <span data-ttu-id="e6f56-112">如果加载了某个映像，但对于该映像必须进行一些 JIT 编译 (这种情况下，如果映像包含泛型) ，则该方法指定的编译器标志 `SetDesiredNGENCompilerFlags` 将应用于额外的 JIT 编译。</span><span class="sxs-lookup"><span data-stu-id="e6f56-112">If an image is loaded, but some JIT compiling must take place for that image (which will be the case if the image contains generics), the compiler flags specified by the `SetDesiredNGENCompilerFlags` method will apply to the extra JIT compilation.</span></span>  
  
 <span data-ttu-id="e6f56-113">`SetDesiredNGENCompilerFlags`必须在[ICorDebugManagedCallback：： CreateProcess](icordebugmanagedcallback-createprocess-method.md)回调过程中调用方法。</span><span class="sxs-lookup"><span data-stu-id="e6f56-113">The `SetDesiredNGENCompilerFlags` method must be called during the [ICorDebugManagedCallback::CreateProcess](icordebugmanagedcallback-createprocess-method.md) callback.</span></span> <span data-ttu-id="e6f56-114">此后尝试调用 `SetDesiredNGENCompilerFlags` 方法将失败。</span><span class="sxs-lookup"><span data-stu-id="e6f56-114">Attempts to call the `SetDesiredNGENCompilerFlags` method afterwards will fail.</span></span> <span data-ttu-id="e6f56-115">另外，尝试设置未在枚举中定义的 `CorDebugJITCompilerFlags` 或对给定进程不合法的标志的尝试将失败。</span><span class="sxs-lookup"><span data-stu-id="e6f56-115">Also, attempts to set flags that are either not defined in the `CorDebugJITCompilerFlags` enumeration or are not legal for the given process will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6f56-116">要求</span><span class="sxs-lookup"><span data-stu-id="e6f56-116">Requirements</span></span>  

 <span data-ttu-id="e6f56-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e6f56-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6f56-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e6f56-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e6f56-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6f56-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e6f56-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6f56-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6f56-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6f56-121">See also</span></span>

- [<span data-ttu-id="e6f56-122">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="e6f56-122">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="e6f56-123">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="e6f56-123">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
