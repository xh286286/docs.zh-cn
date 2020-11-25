---
title: ICorProfilerInfo2::GetBoxClassLayout 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetBoxClassLayout
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetBoxClassLayout
helpviewer_keywords:
- GetBoxClassLayout method [.NET Framework profiling]
- ICorProfilerInfo2::GetBoxClassLayout method [.NET Framework profiling]
ms.assetid: 624672b5-1189-488a-85d2-3e12b49617c1
topic_type:
- apiref
ms.openlocfilehash: ff39a688132112e88438bc192d7c1ab61f169400
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727154"
---
# <a name="icorprofilerinfo2getboxclasslayout-method"></a><span data-ttu-id="10094-102">ICorProfilerInfo2::GetBoxClassLayout 方法</span><span class="sxs-lookup"><span data-stu-id="10094-102">ICorProfilerInfo2::GetBoxClassLayout Method</span></span>

<span data-ttu-id="10094-103">获取有关指定值类型的装箱位置的信息。</span><span class="sxs-lookup"><span data-stu-id="10094-103">Gets information about where the specified value type is located when it is boxed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10094-104">语法</span><span class="sxs-lookup"><span data-stu-id="10094-104">Syntax</span></span>  
  
```cpp  
HRESULT GetBoxClassLayout(  
    [in] ClassID classId,  
    [out] ULONG32 *pBufferOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="10094-105">参数</span><span class="sxs-lookup"><span data-stu-id="10094-105">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="10094-106">中描述装箱的值类型的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="10094-106">[in] The ID of the class that describes the value type that is boxed.</span></span>  
  
 `pBufferOffset`  
 <span data-ttu-id="10094-107">弄一个整数，它是相对于值类型的装箱对象 ID 指针的偏移量。</span><span class="sxs-lookup"><span data-stu-id="10094-107">[out] An integer that is the offset, relative to the boxed object ID pointer, of the value type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="10094-108">注解</span><span class="sxs-lookup"><span data-stu-id="10094-108">Remarks</span></span>  

 <span data-ttu-id="10094-109">`pBufferOffset`值是值类型在框中的位置。</span><span class="sxs-lookup"><span data-stu-id="10094-109">The `pBufferOffset` value is the location of the value type within a box.</span></span> <span data-ttu-id="10094-110">`pBufferOffset`将应用于装箱对象后，可以使用值类型的类布局来解释该对象的值。</span><span class="sxs-lookup"><span data-stu-id="10094-110">After `pBufferOffset` is applied to a boxed object, the value type's class layout can be used to interpret the object's value.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10094-111">要求</span><span class="sxs-lookup"><span data-stu-id="10094-111">Requirements</span></span>  

 <span data-ttu-id="10094-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="10094-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10094-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="10094-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="10094-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="10094-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="10094-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10094-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="10094-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10094-116">See also</span></span>

- [<span data-ttu-id="10094-117">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="10094-117">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="10094-118">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="10094-118">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
