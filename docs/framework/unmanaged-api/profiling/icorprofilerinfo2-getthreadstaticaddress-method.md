---
title: ICorProfilerInfo2::GetThreadStaticAddress 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetThreadStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetThreadStaticAddress
helpviewer_keywords:
- GetThreadStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetThreadStaticAddress method [.NET Framework profiling]
ms.assetid: 8e7dbf14-98a2-4384-a950-58a7640e59df
topic_type:
- apiref
ms.openlocfilehash: 8b9b76fd58d8b3ec5c2d98156b7935051aff074b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731211"
---
# <a name="icorprofilerinfo2getthreadstaticaddress-method"></a><span data-ttu-id="a8269-102">ICorProfilerInfo2::GetThreadStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="a8269-102">ICorProfilerInfo2::GetThreadStaticAddress Method</span></span>

<span data-ttu-id="a8269-103">获取指定线程范围内的指定线程静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="a8269-103">Gets the address of the specified thread-static field that is in the scope of the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8269-104">语法</span><span class="sxs-lookup"><span data-stu-id="a8269-104">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadStaticAddress(  
    [in] ClassID     classId,  
    [in] mdFieldDef  fieldToken,  
    [in] ThreadID    threadId,  
    [out] void       **ppAddress);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a8269-105">参数</span><span class="sxs-lookup"><span data-stu-id="a8269-105">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="a8269-106">中包含请求的线程静态字段的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="a8269-106">[in] The ID of the class that contains the requested thread-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="a8269-107">中请求的线程静态字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="a8269-107">[in] The metadata token for the requested thread-static field.</span></span>  
  
 `threadId`  
 <span data-ttu-id="a8269-108">中作为所请求的静态字段的作用域的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="a8269-108">[in] The ID of the thread that is the scope for the requested static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="a8269-109">弄一个指针，指向指定线程内的静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="a8269-109">[out] A pointer to the address of the static field that is within the specified thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a8269-110">注解</span><span class="sxs-lookup"><span data-stu-id="a8269-110">Remarks</span></span>  

 <span data-ttu-id="a8269-111">此 `GetThreadStaticAddress` 方法可能会返回以下内容之一：</span><span class="sxs-lookup"><span data-stu-id="a8269-111">The `GetThreadStaticAddress` method may return one of the following:</span></span>  
  
- <span data-ttu-id="a8269-112">如果未在指定的上下文中为给定的静态字段分配地址，则 CORPROF_E_DATAINCOMPLETE HRESULT。</span><span class="sxs-lookup"><span data-stu-id="a8269-112">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
- <span data-ttu-id="a8269-113">可能位于垃圾回收堆中的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="a8269-113">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="a8269-114">这些地址可能会在垃圾回收后失效，因此在垃圾回收探查器不应假定它们是有效的。</span><span class="sxs-lookup"><span data-stu-id="a8269-114">These addresses may become invalid after garbage collection, so after garbage collection profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="a8269-115">在类的类构造函数完成之前， `GetThreadStaticAddress` 将为其所有静态字段返回 CORPROF_E_DATAINCOMPLETE，不过，某些静态字段可能已经初始化并为垃圾回收对象提供了根。</span><span class="sxs-lookup"><span data-stu-id="a8269-115">Before a class’s class constructor is completed, `GetThreadStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8269-116">要求</span><span class="sxs-lookup"><span data-stu-id="a8269-116">Requirements</span></span>  

 <span data-ttu-id="a8269-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a8269-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8269-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a8269-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a8269-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a8269-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a8269-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8269-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8269-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8269-121">See also</span></span>

- [<span data-ttu-id="a8269-122">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="a8269-122">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="a8269-123">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="a8269-123">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
