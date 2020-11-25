---
title: ICorProfilerFunctionEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum.Clone Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum::Clone
helpviewer_keywords:
- ICorProfilerFunctionEnum::Clone method [.NET Framework profiling]
- Clone method, ICorProfilerFunctionEnum interface [.NET Framework profiling]
ms.assetid: 0c3d4835-e111-4e82-af6d-53f140b8f2c9
topic_type:
- apiref
ms.openlocfilehash: 092c3b328887b7d36ead77c64d31310b614b616a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707524"
---
# <a name="icorprofilerfunctionenumclone-method"></a><span data-ttu-id="5da03-102">ICorProfilerFunctionEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="5da03-102">ICorProfilerFunctionEnum::Clone Method</span></span>

<span data-ttu-id="5da03-103">获取一个接口指针，该指针指向此 [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) 接口的副本。</span><span class="sxs-lookup"><span data-stu-id="5da03-103">Gets an interface pointer to a copy of this [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5da03-104">语法</span><span class="sxs-lookup"><span data-stu-id="5da03-104">Syntax</span></span>  
  
```cpp  
HRESULT Clone([out] ICorProfilerFunctionEnum **ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5da03-105">参数</span><span class="sxs-lookup"><span data-stu-id="5da03-105">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="5da03-106">弄指向接口指针的指针，该指针反过来指向此 [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) 接口的副本。</span><span class="sxs-lookup"><span data-stu-id="5da03-106">[out] A pointer to the interface pointer, which, in turn, points to the copy of this [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) interface.</span></span> <span data-ttu-id="5da03-107">枚举器的副本与此枚举器分别维护自己的枚举状态。</span><span class="sxs-lookup"><span data-stu-id="5da03-107">The copy of the enumerator maintains its own enumeration state separately from this enumerator.</span></span> <span data-ttu-id="5da03-108">但是，副本的初始光标位置与此枚举器的当前游标位置相同。</span><span class="sxs-lookup"><span data-stu-id="5da03-108">However, the copy's initial cursor position is the same as this enumerator's current cursor position.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5da03-109">要求</span><span class="sxs-lookup"><span data-stu-id="5da03-109">Requirements</span></span>  

 <span data-ttu-id="5da03-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5da03-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5da03-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5da03-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5da03-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5da03-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5da03-113">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5da03-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5da03-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5da03-114">See also</span></span>

- [<span data-ttu-id="5da03-115">ICorProfilerFunctionEnum 接口</span><span class="sxs-lookup"><span data-stu-id="5da03-115">ICorProfilerFunctionEnum Interface</span></span>](icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="5da03-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="5da03-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
