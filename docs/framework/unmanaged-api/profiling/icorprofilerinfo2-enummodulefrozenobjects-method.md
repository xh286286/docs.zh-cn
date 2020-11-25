---
title: ICorProfilerInfo2::EnumModuleFrozenObjects 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.EnumModuleFrozenObjects
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::EnumModuleFrozenObjects
helpviewer_keywords:
- EnumModuleFrozenObjects method [.NET Framework profiling]
- ICorProfilerInfo2::EnumModuleFrozenObjects method [.NET Framework profiling]
ms.assetid: 920b6483-7064-4d64-8613-fcc38ccf9b1e
topic_type:
- apiref
ms.openlocfilehash: fe4f3a7355339c9b5adbe5de062f0a5688d81c23
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727180"
---
# <a name="icorprofilerinfo2enummodulefrozenobjects-method"></a><span data-ttu-id="2f482-102">ICorProfilerInfo2::EnumModuleFrozenObjects 方法</span><span class="sxs-lookup"><span data-stu-id="2f482-102">ICorProfilerInfo2::EnumModuleFrozenObjects Method</span></span>

<span data-ttu-id="2f482-103">获取一个枚举器，该枚举数允许对指定模块中的冻结对象进行迭代。此方法已过时。</span><span class="sxs-lookup"><span data-stu-id="2f482-103">Gets an enumerator that allows iteration over the frozen objects in the specified module.This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f482-104">语法</span><span class="sxs-lookup"><span data-stu-id="2f482-104">Syntax</span></span>  
  
```cpp  
HRESULT EnumModuleFrozenObjects(  
    [in] ModuleID moduleID,  
    [out] ICorProfilerObjectEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2f482-105">参数</span><span class="sxs-lookup"><span data-stu-id="2f482-105">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="2f482-106">中包含要枚举的冻结对象的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="2f482-106">[in] The ID of the module that contains the frozen objects to be enumerated.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="2f482-107">弄一个指针，指向用于枚举冻结对象的 [ICorProfilerObjectEnum](icorprofilerobjectenum-interface.md) 接口的地址。</span><span class="sxs-lookup"><span data-stu-id="2f482-107">[out] A pointer to the address of an [ICorProfilerObjectEnum](icorprofilerobjectenum-interface.md) interface, which enumerates the frozen objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f482-108">要求</span><span class="sxs-lookup"><span data-stu-id="2f482-108">Requirements</span></span>  

 <span data-ttu-id="2f482-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2f482-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2f482-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2f482-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2f482-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2f482-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2f482-112">**.NET Framework 版本：** 3.5、3.0 SP1、3.0、2.0 SP1、2。0</span><span class="sxs-lookup"><span data-stu-id="2f482-112">**.NET Framework Versions:** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f482-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f482-113">See also</span></span>

- [<span data-ttu-id="2f482-114">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="2f482-114">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="2f482-115">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="2f482-115">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
