---
title: ICorProfilerModuleEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.GetCount Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::GetCount
helpviewer_keywords:
- ICorProfilerModuleEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerModuleEnum interface [.NET Framework profiling]
ms.assetid: f0a4a5e0-4689-474b-b0f4-37ca0639c918
topic_type:
- apiref
ms.openlocfilehash: 53009a1805056b83047299ebdca8f21d98ad5137
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732978"
---
# <a name="icorprofilermoduleenumgetcount-method"></a><span data-ttu-id="db0aa-102">ICorProfilerModuleEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="db0aa-102">ICorProfilerModuleEnum::GetCount Method</span></span>

<span data-ttu-id="db0aa-103">获取已加载到应用程序的托管模块数。</span><span class="sxs-lookup"><span data-stu-id="db0aa-103">Gets the number of managed modules that were loaded into the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db0aa-104">语法</span><span class="sxs-lookup"><span data-stu-id="db0aa-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCount([out] ULONG * pcelt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db0aa-105">参数</span><span class="sxs-lookup"><span data-stu-id="db0aa-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="db0aa-106">弄集合中的运行时模块数。</span><span class="sxs-lookup"><span data-stu-id="db0aa-106">[out] The number of runtime modules in the collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db0aa-107">要求</span><span class="sxs-lookup"><span data-stu-id="db0aa-107">Requirements</span></span>  

 <span data-ttu-id="db0aa-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db0aa-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db0aa-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="db0aa-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="db0aa-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db0aa-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db0aa-111">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db0aa-111">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db0aa-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db0aa-112">See also</span></span>

- [<span data-ttu-id="db0aa-113">ICorProfilerModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="db0aa-113">ICorProfilerModuleEnum Interface</span></span>](icorprofilermoduleenum-interface.md)
- [<span data-ttu-id="db0aa-114">分析接口</span><span class="sxs-lookup"><span data-stu-id="db0aa-114">Profiling Interfaces</span></span>](profiling-interfaces.md)
