---
title: IMethodMalloc::Alloc 方法
ms.date: 03/30/2017
api_name:
- IMethodMalloc.Alloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc::Alloc
helpviewer_keywords:
- IMethodMalloc::Alloc method [.NET Framework profiling]
- Alloc method, IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8653bd4c-2290-43d2-a3e1-cbbd50033f4f
topic_type:
- apiref
ms.openlocfilehash: 58809f12e4dd4419b754caafc3f8b883b8bc5089
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721161"
---
# <a name="imethodmallocalloc-method"></a><span data-ttu-id="dbc41-102">IMethodMalloc::Alloc 方法</span><span class="sxs-lookup"><span data-stu-id="dbc41-102">IMethodMalloc::Alloc Method</span></span>

<span data-ttu-id="dbc41-103">尝试将指定数量的内存分配给新的 Microsoft 中间语言 (MSIL) 函数体。</span><span class="sxs-lookup"><span data-stu-id="dbc41-103">Attempts to allocate a specified amount of memory for a new Microsoft intermediate language (MSIL) function body.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc41-104">语法</span><span class="sxs-lookup"><span data-stu-id="dbc41-104">Syntax</span></span>

```cpp
PVOID Alloc (
    [in] ULONG   cb
);
```

## <a name="parameters"></a><span data-ttu-id="dbc41-105">参数</span><span class="sxs-lookup"><span data-stu-id="dbc41-105">Parameters</span></span>

`cb`\
<span data-ttu-id="dbc41-106">中要为方法主体分配的字节数。</span><span class="sxs-lookup"><span data-stu-id="dbc41-106">[in] The number of bytes to allocate for the method body.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc41-107">注解</span><span class="sxs-lookup"><span data-stu-id="dbc41-107">Remarks</span></span>

 <span data-ttu-id="dbc41-108">分配的内存将以大于与此分配器关联的模块的基址的地址开始。</span><span class="sxs-lookup"><span data-stu-id="dbc41-108">The allocated memory will begin at an address greater than the base address of the module that is associated with this allocator.</span></span> <span data-ttu-id="dbc41-109">换言之，每个分配器都是为特定模块创建的，并将尝试从其基址的正偏移量处分配内存。</span><span class="sxs-lookup"><span data-stu-id="dbc41-109">In other words, each allocator is created for a particular module, and will attempt to allocate memory at a positive offset from its base address.</span></span> <span data-ttu-id="dbc41-110">如果 `Alloc` 无法在大于模块基址的地址分配请求的字节数，则将返回 E_OUTOFMEMORY，而不考虑实际可用的内存空间量。</span><span class="sxs-lookup"><span data-stu-id="dbc41-110">If `Alloc` fails to allocate the requested number of bytes at an address greater than the base address of the module, it returns E_OUTOFMEMORY, regardless of the actual amount of memory space available.</span></span>

 <span data-ttu-id="dbc41-111">`Alloc`应将方法与[ICorProfilerInfo：： SetILFunctionBody](icorprofilerinfo-setilfunctionbody-method.md)方法结合使用。</span><span class="sxs-lookup"><span data-stu-id="dbc41-111">The `Alloc` method should be used in conjunction with the [ICorProfilerInfo::SetILFunctionBody](icorprofilerinfo-setilfunctionbody-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc41-112">要求</span><span class="sxs-lookup"><span data-stu-id="dbc41-112">Requirements</span></span>

 <span data-ttu-id="dbc41-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dbc41-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

 <span data-ttu-id="dbc41-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dbc41-114">**Header:** CorProf.idl, CorProf.h</span></span>

 <span data-ttu-id="dbc41-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dbc41-115">**Library:** CorGuids.lib</span></span>

 <span data-ttu-id="dbc41-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dbc41-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="dbc41-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbc41-117">See also</span></span>

- [<span data-ttu-id="dbc41-118">IMethodMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="dbc41-118">IMethodMalloc Interface</span></span>](imethodmalloc-interface.md)
