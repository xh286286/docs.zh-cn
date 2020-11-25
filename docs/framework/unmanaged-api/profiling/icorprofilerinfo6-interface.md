---
title: ICorProfilerInfo6 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo6
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 6f2bb148-1e2b-4e45-a5a5-0ceddc40064b
ms.openlocfilehash: b3aed97e19694675fd5e0c1070dbbf6d9321eedd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95733836"
---
# <a name="icorprofilerinfo6-interface"></a><span data-ttu-id="c6144-102">ICorProfilerInfo6 接口</span><span class="sxs-lookup"><span data-stu-id="c6144-102">ICorProfilerInfo6 Interface</span></span>

<span data-ttu-id="c6144-103">[.NET Framework 4.6 及更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="c6144-103">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="c6144-104">[ICorProfilerInfo5](icorprofilerinfo5-interface.md)的子类，为在给定的 NGen 模块中定义并内联给定方法的所有方法提供了一个枚举器。</span><span class="sxs-lookup"><span data-stu-id="c6144-104">A subclass of [ICorProfilerInfo5](icorprofilerinfo5-interface.md) that provides an enumerator for all methods that are defined in a given NGen module and inline a given method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c6144-105">方法</span><span class="sxs-lookup"><span data-stu-id="c6144-105">Methods</span></span>  
  
|<span data-ttu-id="c6144-106">方法</span><span class="sxs-lookup"><span data-stu-id="c6144-106">Method</span></span>|<span data-ttu-id="c6144-107">说明</span><span class="sxs-lookup"><span data-stu-id="c6144-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c6144-108">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod 方法</span><span class="sxs-lookup"><span data-stu-id="c6144-108">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>](icorprofilerinfo6-enumngenmodulemethodsinliningthismethod-method.md)|<span data-ttu-id="c6144-109">返回属于给定的 NGen 模块并在给定方法的主体中内联的所有方法的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c6144-109">Returns an enumerator for all methods that belong to a given NGen module and that are inlined in the body of a given method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c6144-110">要求</span><span class="sxs-lookup"><span data-stu-id="c6144-110">Requirements</span></span>  

 <span data-ttu-id="c6144-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c6144-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c6144-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c6144-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c6144-113">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c6144-113">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6144-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6144-114">See also</span></span>

- [<span data-ttu-id="c6144-115">分析接口</span><span class="sxs-lookup"><span data-stu-id="c6144-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
