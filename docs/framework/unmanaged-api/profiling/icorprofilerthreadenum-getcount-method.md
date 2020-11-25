---
title: ICorProfilerThreadEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.GetCount
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::GetCount
helpviewer_keywords:
- ICorProfilerThreadEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: d6dbdc4a-6115-455d-a3f3-704a81d3646b
topic_type:
- apiref
ms.openlocfilehash: a35f2e69515ea520396641effc05371b54ad8afc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702324"
---
# <a name="icorprofilerthreadenumgetcount-method"></a><span data-ttu-id="e01f9-102">ICorProfilerThreadEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="e01f9-102">ICorProfilerThreadEnum::GetCount Method</span></span>

<span data-ttu-id="e01f9-103">获取应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="e01f9-103">Gets the number of threads that are used by the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e01f9-104">语法</span><span class="sxs-lookup"><span data-stu-id="e01f9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCount (    [out] ULONG * pcelt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e01f9-105">参数</span><span class="sxs-lookup"><span data-stu-id="e01f9-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="e01f9-106">弄应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="e01f9-106">[out] The number of threads used by the application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e01f9-107">要求</span><span class="sxs-lookup"><span data-stu-id="e01f9-107">Requirements</span></span>  

 <span data-ttu-id="e01f9-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e01f9-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e01f9-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e01f9-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e01f9-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e01f9-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e01f9-111">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e01f9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e01f9-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e01f9-112">See also</span></span>

- [<span data-ttu-id="e01f9-113">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e01f9-113">ICorProfilerThreadEnum Interface</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="e01f9-114">分析接口</span><span class="sxs-lookup"><span data-stu-id="e01f9-114">Profiling Interfaces</span></span>](profiling-interfaces.md)
