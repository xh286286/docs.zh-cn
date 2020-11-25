---
title: DacpGetModuleAddress 结构
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress Structure
helpviewer.keywords:
- DacpGetModuleAddress Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a65fa9974165fa36e59a7fb83dca6dd902f7d8dc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95724389"
---
# <a name="dacpgetmoduleaddress-structure"></a><span data-ttu-id="32e32-102">DacpGetModuleAddress 结构</span><span class="sxs-lookup"><span data-stu-id="32e32-102">DacpGetModuleAddress Structure</span></span>

<span data-ttu-id="32e32-103">定义模块地址请求的容器。</span><span class="sxs-lookup"><span data-stu-id="32e32-103">Defines the container for a module address request.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="32e32-104">语法</span><span class="sxs-lookup"><span data-stu-id="32e32-104">Syntax</span></span>

```cpp
struct DacpGetModuleAddress
{
    CLRDATA_ADDRESS ModulePtr;
};
```

## <a name="members"></a><span data-ttu-id="32e32-105">成员</span><span class="sxs-lookup"><span data-stu-id="32e32-105">Members</span></span>

| <span data-ttu-id="32e32-106">成员</span><span class="sxs-lookup"><span data-stu-id="32e32-106">Member</span></span>      | <span data-ttu-id="32e32-107">说明</span><span class="sxs-lookup"><span data-stu-id="32e32-107">Description</span></span>                |
| ----------- | -------------------------- |
| `ModulePtr` | <span data-ttu-id="32e32-108">指向模块的指针。</span><span class="sxs-lookup"><span data-stu-id="32e32-108">The pointer to the module.</span></span> |

## <a name="methods"></a><span data-ttu-id="32e32-109">方法</span><span class="sxs-lookup"><span data-stu-id="32e32-109">Methods</span></span>

| <span data-ttu-id="32e32-110">方法</span><span class="sxs-lookup"><span data-stu-id="32e32-110">Method</span></span>                                                                                               | <span data-ttu-id="32e32-111">说明</span><span class="sxs-lookup"><span data-stu-id="32e32-111">Description</span></span>                                                                    |
| ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [<span data-ttu-id="32e32-112">请求</span><span class="sxs-lookup"><span data-stu-id="32e32-112">Request</span></span>](dacpgetmoduleaddress-request-method.md) | <span data-ttu-id="32e32-113">执行从给定的运行时结构填充结构的请求。</span><span class="sxs-lookup"><span data-stu-id="32e32-113">Performs a request to populate the structure from the given runtime structure.</span></span> |

## <a name="remarks"></a><span data-ttu-id="32e32-114">注解</span><span class="sxs-lookup"><span data-stu-id="32e32-114">Remarks</span></span>

<span data-ttu-id="32e32-115">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="32e32-115">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="32e32-116">若要使用它，请定义上面指定的结构，其中 `CLRDATA_ADDRESS` 是一个64位无符号整数。</span><span class="sxs-lookup"><span data-stu-id="32e32-116">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e32-117">要求</span><span class="sxs-lookup"><span data-stu-id="32e32-117">Requirements</span></span>

<span data-ttu-id="32e32-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="32e32-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="32e32-119">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="32e32-119">**Header:** None</span></span>  
<span data-ttu-id="32e32-120">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="32e32-120">**Library:** None</span></span>  
<span data-ttu-id="32e32-121">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="32e32-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="32e32-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="32e32-122">See also</span></span>

- [<span data-ttu-id="32e32-123">调试</span><span class="sxs-lookup"><span data-stu-id="32e32-123">Debugging</span></span>](index.md)
- [<span data-ttu-id="32e32-124">调试结构</span><span class="sxs-lookup"><span data-stu-id="32e32-124">Debugging Structures</span></span>](debugging-structures.md)
