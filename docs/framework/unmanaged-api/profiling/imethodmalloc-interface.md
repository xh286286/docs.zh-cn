---
title: IMethodMalloc 接口
ms.date: 03/30/2017
api_name:
- IMethodMalloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc
helpviewer_keywords:
- IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8c8ab5dc-557c-473a-82f2-6e403eca7dac
topic_type:
- apiref
ms.openlocfilehash: 8eccdba75b59df505ae72d74cfcd2bc83de2b45a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688167"
---
# <a name="imethodmalloc-interface"></a><span data-ttu-id="26cd9-102">IMethodMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="26cd9-102">IMethodMalloc Interface</span></span>

<span data-ttu-id="26cd9-103">提供一个方法，用于为新的 Microsoft 中间语言 (MSIL) 函数体分配内存。</span><span class="sxs-lookup"><span data-stu-id="26cd9-103">Provides a method to allocate memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="26cd9-104">`IMethodMalloc`接口是一个简单的内存分配器。</span><span class="sxs-lookup"><span data-stu-id="26cd9-104">The `IMethodMalloc` interface is a simple memory allocator.</span></span> <span data-ttu-id="26cd9-105">它允许您分配内存，但不能释放内存。</span><span class="sxs-lookup"><span data-stu-id="26cd9-105">It allows you to allocate memory, but not to free it.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="26cd9-106">方法</span><span class="sxs-lookup"><span data-stu-id="26cd9-106">Methods</span></span>  
  
|<span data-ttu-id="26cd9-107">方法</span><span class="sxs-lookup"><span data-stu-id="26cd9-107">Method</span></span>|<span data-ttu-id="26cd9-108">说明</span><span class="sxs-lookup"><span data-stu-id="26cd9-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="26cd9-109">Alloc 方法</span><span class="sxs-lookup"><span data-stu-id="26cd9-109">Alloc Method</span></span>](imethodmalloc-alloc-method.md)|<span data-ttu-id="26cd9-110">尝试为新的 MSIL 函数体分配指定的内存量。</span><span class="sxs-lookup"><span data-stu-id="26cd9-110">Attempts to allocate a specified amount of memory for a new MSIL function body.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="26cd9-111">注解</span><span class="sxs-lookup"><span data-stu-id="26cd9-111">Remarks</span></span>  

 <span data-ttu-id="26cd9-112">每个分配器都是特定于模块的，并确保函数体与模块的基偏移为正偏移量。</span><span class="sxs-lookup"><span data-stu-id="26cd9-112">Each allocator is module-specific and ensures that the function body will be at a positive offset from the base of the module.</span></span> <span data-ttu-id="26cd9-113">超出模块基的内存可能非常宝贵，因此应使用分配器仅为函数体分配内存。</span><span class="sxs-lookup"><span data-stu-id="26cd9-113">Memory above the base of a module can be precious, so the allocator should be used to allocate memory only for a function body.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26cd9-114">要求</span><span class="sxs-lookup"><span data-stu-id="26cd9-114">Requirements</span></span>  

 <span data-ttu-id="26cd9-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26cd9-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26cd9-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="26cd9-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="26cd9-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26cd9-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26cd9-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26cd9-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26cd9-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26cd9-119">See also</span></span>

- [<span data-ttu-id="26cd9-120">分析接口</span><span class="sxs-lookup"><span data-stu-id="26cd9-120">Profiling Interfaces</span></span>](profiling-interfaces.md)
