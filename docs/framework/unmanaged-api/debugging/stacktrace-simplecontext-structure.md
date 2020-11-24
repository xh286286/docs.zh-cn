---
title: StackTrace_SimpleContext 结构
ms.date: 03/30/2017
api_name:
- StackTrace_SimpleContext
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SimpleContext
helpviewer_keywords:
- SimpleContext structure [.NET Framework debugging]
- StackTrace_SimpleContext structure [.NET Framework debugging]
ms.assetid: d4cef11f-a8ca-49bc-a1b8-6631f9e28f3e
topic_type:
- apiref
ms.openlocfilehash: 30775b4a6f904d06b9c77e6b2b64aec693c446d7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671793"
---
# <a name="stacktrace_simplecontext-structure"></a><span data-ttu-id="97491-102">StackTrace_SimpleContext 结构</span><span class="sxs-lookup"><span data-stu-id="97491-102">StackTrace_SimpleContext Structure</span></span>

<span data-ttu-id="97491-103">提供可用于代替完整的 `CONTEXT` 结构的简单上下文。</span><span class="sxs-lookup"><span data-stu-id="97491-103">Provides a simple context that can be used in place of a full `CONTEXT` structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97491-104">语法</span><span class="sxs-lookup"><span data-stu-id="97491-104">Syntax</span></span>  
  
```cpp  
struct StackTrace_SimpleContext  
{  
    ULONG64 StackOffset;       // ESP on x86  
    ULONG64 FrameOffset;       // EBP on x86  
    ULONG64 InstructionOffset; // EIP on x86  
};  
```  
  
## <a name="members"></a><span data-ttu-id="97491-105">成员</span><span class="sxs-lookup"><span data-stu-id="97491-105">Members</span></span>  
  
|<span data-ttu-id="97491-106">成员</span><span class="sxs-lookup"><span data-stu-id="97491-106">Member</span></span>|<span data-ttu-id="97491-107">说明</span><span class="sxs-lookup"><span data-stu-id="97491-107">Description</span></span>|  
|------------|-----------------|  
|`StackOffset`|<span data-ttu-id="97491-108">堆栈指针或输入堆栈指针 (ESP) 在 x86 平台上。</span><span class="sxs-lookup"><span data-stu-id="97491-108">The stack pointer, or the enter stack pointer (ESP) on x86 platforms.</span></span>|  
|`FrameOffset`|<span data-ttu-id="97491-109">X86 平台上的帧偏移量或 EBP 寄存器。</span><span class="sxs-lookup"><span data-stu-id="97491-109">The frame offset, or the EBP register on x86 platforms.</span></span>|  
|`InstructionOffset`|<span data-ttu-id="97491-110">在 x86 平台上，指令指针或输入指令指针 (EIP) 。</span><span class="sxs-lookup"><span data-stu-id="97491-110">The instruction pointer, or the enter instruction pointer (EIP) on x86 platforms.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="97491-111">注解</span><span class="sxs-lookup"><span data-stu-id="97491-111">Remarks</span></span>  

 <span data-ttu-id="97491-112">因为堆栈跟踪函数通常只需要返回地址、帧偏移量和堆栈地址，所以，您可以选择使用 `SimpleContext` 结构而不是大 `CONTEXT` 结构。</span><span class="sxs-lookup"><span data-stu-id="97491-112">Because stack trace functions typically need to return only the address, frame offset, and stack address, you can optionally use the `SimpleContext` structure instead of a large `CONTEXT` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97491-113">要求</span><span class="sxs-lookup"><span data-stu-id="97491-113">Requirements</span></span>  

 <span data-ttu-id="97491-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="97491-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97491-115">**标头：** SOS_Stacktrace。h</span><span class="sxs-lookup"><span data-stu-id="97491-115">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="97491-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97491-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97491-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="97491-117">See also</span></span>

- [<span data-ttu-id="97491-118">调试结构</span><span class="sxs-lookup"><span data-stu-id="97491-118">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="97491-119">调试</span><span class="sxs-lookup"><span data-stu-id="97491-119">Debugging</span></span>](index.md)
