---
title: ICorDebugILFrame 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame
helpviewer_keywords:
- ICorDebugILFrame interface [.NET Framework debugging]
ms.assetid: d5cf5056-da4d-4629-914d-afe42a5393df
topic_type:
- apiref
ms.openlocfilehash: 4f34fdf9a0eeb47e027cc874afee5bd04f5bd9bc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95712386"
---
# <a name="icordebugilframe-interface"></a><span data-ttu-id="3f61f-102">ICorDebugILFrame 接口</span><span class="sxs-lookup"><span data-stu-id="3f61f-102">ICorDebugILFrame Interface</span></span>

<span data-ttu-id="3f61f-103">表示 Microsoft 中间语言 (MSIL) 代码的堆栈帧。</span><span class="sxs-lookup"><span data-stu-id="3f61f-103">Represents a stack frame of Microsoft intermediate language (MSIL) code.</span></span> <span data-ttu-id="3f61f-104">此接口是 ICorDebugFrame 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="3f61f-104">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3f61f-105">方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-105">Methods</span></span>  
  
|<span data-ttu-id="3f61f-106">方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-106">Method</span></span>|<span data-ttu-id="3f61f-107">说明</span><span class="sxs-lookup"><span data-stu-id="3f61f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3f61f-108">CanSetIP 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-108">CanSetIP Method</span></span>](icordebugilframe-cansetip-method.md)|<span data-ttu-id="3f61f-109">获取一个值，该值指示是否可以安全地将指令指针设置为指定的偏移位置。</span><span class="sxs-lookup"><span data-stu-id="3f61f-109">Gets a value that indicates whether it is safe to set the instruction pointer to the specified offset location.</span></span>|  
|[<span data-ttu-id="3f61f-110">EnumerateArguments 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-110">EnumerateArguments Method</span></span>](icordebugilframe-enumeratearguments-method.md)|<span data-ttu-id="3f61f-111">获取此帧中的参数的枚举数。</span><span class="sxs-lookup"><span data-stu-id="3f61f-111">Gets an enumerator for the arguments in this frame.</span></span>|  
|[<span data-ttu-id="3f61f-112">EnumerateLocalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-112">EnumerateLocalVariables Method</span></span>](icordebugilframe-enumeratelocalvariables-method.md)|<span data-ttu-id="3f61f-113">获取此帧中局部变量的枚举数。</span><span class="sxs-lookup"><span data-stu-id="3f61f-113">Gets an enumerator for the local variables in this frame.</span></span>|  
|[<span data-ttu-id="3f61f-114">GetArgument 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-114">GetArgument Method</span></span>](icordebugilframe-getargument-method.md)|<span data-ttu-id="3f61f-115">获取此 MSIL 堆栈帧中的指定参数的值。</span><span class="sxs-lookup"><span data-stu-id="3f61f-115">Gets the value of the specified argument in this MSIL stack frame.</span></span>|  
|[<span data-ttu-id="3f61f-116">GetIP 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-116">GetIP Method</span></span>](icordebugilframe-getip-method.md)|<span data-ttu-id="3f61f-117">获取指令指针的值和按位组合值，它描述如何获取指令指针的值。</span><span class="sxs-lookup"><span data-stu-id="3f61f-117">Gets the value of the instruction pointer and a bitwise combination value that describes how the value of the instruction pointer was obtained.</span></span>|  
|[<span data-ttu-id="3f61f-118">GetLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-118">GetLocalVariable Method</span></span>](icordebugilframe-getlocalvariable-method.md)|<span data-ttu-id="3f61f-119">获取此 MSIL 堆栈帧中的指定局部变量的值。</span><span class="sxs-lookup"><span data-stu-id="3f61f-119">Gets the value of the specified local variable in this MSIL stack frame.</span></span>|  
|[<span data-ttu-id="3f61f-120">GetStackDepth 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-120">GetStackDepth Method</span></span>](icordebugilframe-getstackdepth-method.md)|<span data-ttu-id="3f61f-121">未实现。</span><span class="sxs-lookup"><span data-stu-id="3f61f-121">Not implemented.</span></span>|  
|[<span data-ttu-id="3f61f-122">GetStackValue 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-122">GetStackValue Method</span></span>](icordebugilframe-getstackvalue-method.md)|<span data-ttu-id="3f61f-123">未实现。</span><span class="sxs-lookup"><span data-stu-id="3f61f-123">Not implemented.</span></span>|  
|[<span data-ttu-id="3f61f-124">SetIP 方法</span><span class="sxs-lookup"><span data-stu-id="3f61f-124">SetIP Method</span></span>](icordebugilframe-setip-method.md)|<span data-ttu-id="3f61f-125">将指令指针设置为指向 MSIL 代码中的指定偏移位置。</span><span class="sxs-lookup"><span data-stu-id="3f61f-125">Sets the instruction pointer to the specified offset location in the MSIL code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3f61f-126">注解</span><span class="sxs-lookup"><span data-stu-id="3f61f-126">Remarks</span></span>  

 <span data-ttu-id="3f61f-127">`ICorDebugILFrame`接口是专用的 ICorDebugFrame 接口。</span><span class="sxs-lookup"><span data-stu-id="3f61f-127">The `ICorDebugILFrame` interface is a specialized ICorDebugFrame interface.</span></span> <span data-ttu-id="3f61f-128">它可用于 MSIL 代码帧或实时 (JIT) 编译的帧。</span><span class="sxs-lookup"><span data-stu-id="3f61f-128">It is used either for MSIL code frames or for just-in-time (JIT) compiled frames.</span></span> <span data-ttu-id="3f61f-129">JIT 编译的帧实现 `ICorDebugILFrame` 接口和 ICorDebugNativeFrame 接口。</span><span class="sxs-lookup"><span data-stu-id="3f61f-129">The JIT-compiled frames implement both the `ICorDebugILFrame` interface and the ICorDebugNativeFrame interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3f61f-130">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3f61f-130">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f61f-131">要求</span><span class="sxs-lookup"><span data-stu-id="3f61f-131">Requirements</span></span>  

 <span data-ttu-id="3f61f-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f61f-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f61f-133">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3f61f-133">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3f61f-134">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3f61f-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3f61f-135">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f61f-135">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f61f-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f61f-136">See also</span></span>

- [<span data-ttu-id="3f61f-137">调试接口</span><span class="sxs-lookup"><span data-stu-id="3f61f-137">Debugging Interfaces</span></span>](debugging-interfaces.md)
