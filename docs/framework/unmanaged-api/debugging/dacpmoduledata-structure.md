---
title: DacpModuleData 结构
ms.date: 02/01/2019
api.name:
- DacpModuleData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpModuleData Structure
helpviewer.keywords:
- DacpModuleData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 5d27ba2de9ff6ed184b6ddf50a517d0dae7715f5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723046"
---
# <a name="dacpmoduledata-structure"></a><span data-ttu-id="cc1a8-102">DacpModuleData 结构</span><span class="sxs-lookup"><span data-stu-id="cc1a8-102">DacpModuleData Structure</span></span>

<span data-ttu-id="cc1a8-103">定义模块的运行时信息的传输缓冲区。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-103">Defines a transport buffer for a module's runtime information.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="cc1a8-104">语法</span><span class="sxs-lookup"><span data-stu-id="cc1a8-104">Syntax</span></span>

```cpp
struct DacpModuleData
{
    CLRDATA_ADDRESS Address;
    CLRDATA_ADDRESS File;
    CLRDATA_ADDRESS  ilBase;
    char payLoad[132];
};
```

## <a name="members"></a><span data-ttu-id="cc1a8-105">成员</span><span class="sxs-lookup"><span data-stu-id="cc1a8-105">Members</span></span>

| <span data-ttu-id="cc1a8-106">成员</span><span class="sxs-lookup"><span data-stu-id="cc1a8-106">Member</span></span>    | <span data-ttu-id="cc1a8-107">说明</span><span class="sxs-lookup"><span data-stu-id="cc1a8-107">Description</span></span>                                                             |
| --------- | ----------------------------------------------------------------------- |
| `Address` | <span data-ttu-id="cc1a8-108">Module 对象的地址。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-108">Address of the module object.</span></span>                                           |
| `File`    | <span data-ttu-id="cc1a8-109">指向可移植可执行文件 (PE) 文件的指针。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-109">A pointer to the portable executable (PE) file.</span></span>                       |
| `ilBase`  | <span data-ttu-id="cc1a8-110">加载的映像的基址。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-110">The address of the loaded image's base.</span></span>                                 |
| `payLoad` | <span data-ttu-id="cc1a8-111">运行时使用的其他模块信息的负载缓冲区。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-111">A payload buffer for additional module information used by the runtime.</span></span> |

## <a name="remarks"></a><span data-ttu-id="cc1a8-112">注解</span><span class="sxs-lookup"><span data-stu-id="cc1a8-112">Remarks</span></span>

<span data-ttu-id="cc1a8-113">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-113">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="cc1a8-114">若要使用它，请定义上面指定的结构。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-114">To use it, define the structure as specified above.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1a8-115">要求</span><span class="sxs-lookup"><span data-stu-id="cc1a8-115">Requirements</span></span>

<span data-ttu-id="cc1a8-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cc1a8-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="cc1a8-117">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="cc1a8-117">**Header:** None</span></span>  
<span data-ttu-id="cc1a8-118">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="cc1a8-118">**Library:** None</span></span>  
<span data-ttu-id="cc1a8-119">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="cc1a8-119">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="cc1a8-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cc1a8-120">See also</span></span>

- [<span data-ttu-id="cc1a8-121">调试</span><span class="sxs-lookup"><span data-stu-id="cc1a8-121">Debugging</span></span>](index.md)
- [<span data-ttu-id="cc1a8-122">调试结构</span><span class="sxs-lookup"><span data-stu-id="cc1a8-122">Debugging Structures</span></span>](debugging-structures.md)
