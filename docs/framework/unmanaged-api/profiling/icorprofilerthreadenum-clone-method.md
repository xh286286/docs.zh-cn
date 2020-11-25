---
title: ICorProfilerThreadEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.Clone
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerThreadEnum interface [.NET Framework profiling]
- ICorProfilerThreadEnum::Clone method [.NET Framework profiling]
ms.assetid: 5a278bc9-88e2-4c69-b035-9d550dd77081
topic_type:
- apiref
ms.openlocfilehash: de2584b56701f4cffb6a108a5872641ec40e5762
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702519"
---
# <a name="icorprofilerthreadenumclone-method"></a><span data-ttu-id="424f1-102">ICorProfilerThreadEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="424f1-102">ICorProfilerThreadEnum::Clone Method</span></span>

<span data-ttu-id="424f1-103">获取一个接口指针，该指针指向此 [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) 接口的副本。</span><span class="sxs-lookup"><span data-stu-id="424f1-103">Gets an interface pointer to a copy of this [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="424f1-104">语法</span><span class="sxs-lookup"><span data-stu-id="424f1-104">Syntax</span></span>  
  
```cpp  
HRESULT Clone (    [out] ICorProfilerThreadEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="424f1-105">参数</span><span class="sxs-lookup"><span data-stu-id="424f1-105">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="424f1-106">弄指向接口指针的指针，该指针反过来指向此 [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) 接口的副本。</span><span class="sxs-lookup"><span data-stu-id="424f1-106">[out] A pointer to the interface pointer, which, in turn, points to the copy of this [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) interface.</span></span> <span data-ttu-id="424f1-107">枚举器的副本与此枚举器分别维护自己的枚举状态。</span><span class="sxs-lookup"><span data-stu-id="424f1-107">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="424f1-108">但是，副本的初始光标位置与枚举器的当前游标位置相同。</span><span class="sxs-lookup"><span data-stu-id="424f1-108">However, the initial cursor position of the copy is the same as this current cursor position of the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="424f1-109">要求</span><span class="sxs-lookup"><span data-stu-id="424f1-109">Requirements</span></span>  

 <span data-ttu-id="424f1-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="424f1-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="424f1-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="424f1-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="424f1-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="424f1-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="424f1-113">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="424f1-113">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="424f1-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="424f1-114">See also</span></span>

- [<span data-ttu-id="424f1-115">ICorProfilerThreadEnum</span><span class="sxs-lookup"><span data-stu-id="424f1-115">ICorProfilerThreadEnum</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="424f1-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="424f1-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
