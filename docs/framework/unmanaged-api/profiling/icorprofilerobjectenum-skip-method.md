---
title: ICorProfilerObjectEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Skip
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Skip
helpviewer_keywords:
- ICorProfilerObjectEnum::Skip method [.NET Framework profiling]
- Skip method, ICorProfilerObjectEnum interface [.NET Framework profiling]
ms.assetid: f8e498f8-f93a-4b82-bd22-55bdbf5e8d45
topic_type:
- apiref
ms.openlocfilehash: 83c6af74ebc3eb668317bd64628af17513a2aed6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702350"
---
# <a name="icorprofilerobjectenumskip-method"></a><span data-ttu-id="82c0e-102">ICorProfilerObjectEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="82c0e-102">ICorProfilerObjectEnum::Skip Method</span></span>

<span data-ttu-id="82c0e-103">将此枚举器的光标从其当前位置前移，以便跳过指定数目的元素。</span><span class="sxs-lookup"><span data-stu-id="82c0e-103">Advances the cursor of this enumerator from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82c0e-104">语法</span><span class="sxs-lookup"><span data-stu-id="82c0e-104">Syntax</span></span>  
  
```cpp  
HRESULT Skip (  
    [in] ULONG   celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="82c0e-105">参数</span><span class="sxs-lookup"><span data-stu-id="82c0e-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="82c0e-106">中要跳过的元素数。</span><span class="sxs-lookup"><span data-stu-id="82c0e-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="82c0e-107">注解</span><span class="sxs-lookup"><span data-stu-id="82c0e-107">Remarks</span></span>  

 <span data-ttu-id="82c0e-108">此枚举器的游标的新位置为： (当前位置) + `celt` 。</span><span class="sxs-lookup"><span data-stu-id="82c0e-108">The new position of this enumerator's cursor is: (current position) + `celt` .</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82c0e-109">要求</span><span class="sxs-lookup"><span data-stu-id="82c0e-109">Requirements</span></span>  

 <span data-ttu-id="82c0e-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="82c0e-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82c0e-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="82c0e-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="82c0e-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="82c0e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="82c0e-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82c0e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82c0e-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82c0e-114">See also</span></span>

- [<span data-ttu-id="82c0e-115">ICorProfilerObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="82c0e-115">ICorProfilerObjectEnum Interface</span></span>](icorprofilerobjectenum-interface.md)
