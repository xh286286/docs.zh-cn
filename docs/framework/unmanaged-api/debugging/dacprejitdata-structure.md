---
title: DacpReJitData 结构
ms.date: 02/01/2019
api.name:
- DacpReJitData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpReJitData Structure
helpviewer.keywords:
- DacpReJitData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 46708acc77dad00727ee35e7d06e4228eacbd502
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723033"
---
# <a name="dacprejitdata-structure"></a><span data-ttu-id="7cdbe-102">DacpReJitData 结构</span><span class="sxs-lookup"><span data-stu-id="7cdbe-102">DacpReJitData Structure</span></span>

<span data-ttu-id="7cdbe-103">定义有关给定探查器检测到的方法的基本信息。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-103">Defines the basic information about a given profiler-instrumented method.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="7cdbe-104">语法</span><span class="sxs-lookup"><span data-stu-id="7cdbe-104">Syntax</span></span>

```cpp
struct MSLAYOUT DacpReJitData
{
    enum Flags
    {
        kUnknown,
        kRequested,
        kActive,
        kReverted,
    };

    CLRDATA_ADDRESS                 rejitID;
    Flags                           flags;
    CLRDATA_ADDRESS                 NativeCodeAddr;
};
```

## <a name="members"></a><span data-ttu-id="7cdbe-105">成员</span><span class="sxs-lookup"><span data-stu-id="7cdbe-105">Members</span></span>

| <span data-ttu-id="7cdbe-106">成员</span><span class="sxs-lookup"><span data-stu-id="7cdbe-106">Member</span></span>           | <span data-ttu-id="7cdbe-107">说明</span><span class="sxs-lookup"><span data-stu-id="7cdbe-107">Description</span></span>                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| `rejitID`        | <span data-ttu-id="7cdbe-108">方法的 ReJit 修订号。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-108">The ReJit revision number for a method.</span></span>                                                          |
| `flags`          | <span data-ttu-id="7cdbe-109">一个标志，指示给定版本的该方法的 ReJit 检测的当前状态。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-109">A flag indicating the current state of the method's ReJit instrumentation for the given version.</span></span> |
| `NativeCodeAddr` | <span data-ttu-id="7cdbe-110">该方法的 rejitted 实现的基址。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-110">The base address of the method's rejitted implementation.</span></span>                                         |

## <a name="remarks"></a><span data-ttu-id="7cdbe-111">注解</span><span class="sxs-lookup"><span data-stu-id="7cdbe-111">Remarks</span></span>

<span data-ttu-id="7cdbe-112">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-112">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="7cdbe-113">若要使用它，请定义上面指定的结构。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-113">To use it, define the structure as specified above.</span></span> <span data-ttu-id="7cdbe-114">如果不使用 Microsoft 编译器，还必须使用打包来定义结构 `ms_struct` 。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-114">The structure must also be defined using `ms_struct` packing if not using the Microsoft compilers.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cdbe-115">要求</span><span class="sxs-lookup"><span data-stu-id="7cdbe-115">Requirements</span></span>

<span data-ttu-id="7cdbe-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7cdbe-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7cdbe-117">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="7cdbe-117">**Header:** None</span></span>  
<span data-ttu-id="7cdbe-118">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="7cdbe-118">**Library:** None</span></span>  
<span data-ttu-id="7cdbe-119">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7cdbe-119">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7cdbe-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7cdbe-120">See also</span></span>

- [<span data-ttu-id="7cdbe-121">调试</span><span class="sxs-lookup"><span data-stu-id="7cdbe-121">Debugging</span></span>](index.md)
- [<span data-ttu-id="7cdbe-122">调试结构</span><span class="sxs-lookup"><span data-stu-id="7cdbe-122">Debugging Structures</span></span>](debugging-structures.md)
