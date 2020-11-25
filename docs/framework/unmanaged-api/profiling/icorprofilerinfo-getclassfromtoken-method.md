---
title: ICorProfilerInfo::GetClassFromToken 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassFromToken
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassFromToken
helpviewer_keywords:
- ICorProfilerInfo::GetClassFromToken method [.NET Framework profiling]
- GetClassFromToken method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 0afc1197-2a5b-424f-8b82-9cb59a7e00db
topic_type:
- apiref
ms.openlocfilehash: 7d9fe7d6d5c5af32be22ba19b52e7d40033a6eb2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706744"
---
# <a name="icorprofilerinfogetclassfromtoken-method"></a><span data-ttu-id="9e765-102">ICorProfilerInfo::GetClassFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="9e765-102">ICorProfilerInfo::GetClassFromToken Method</span></span>

<span data-ttu-id="9e765-103">给定元数据标记，获取类的 ID。</span><span class="sxs-lookup"><span data-stu-id="9e765-103">Gets the ID of the class, given the metadata token.</span></span> <span data-ttu-id="9e765-104">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="9e765-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="9e765-105">改 [为使用 ICorProfilerInfo2：： GetClassFromTokenAndTypeArgs](icorprofilerinfo2-getclassfromtokenandtypeargs-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="9e765-105">Use [ICorProfilerInfo2::GetClassFromTokenAndTypeArgs](icorprofilerinfo2-getclassfromtokenandtypeargs-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e765-106">语法</span><span class="sxs-lookup"><span data-stu-id="9e765-106">Syntax</span></span>  
  
```cpp  
HRESULT GetClassFromToken(  
    [in]  ModuleID  moduleId,  
    [in]  mdTypeDef typeDef,  
    [out] ClassID   *pClassId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9e765-107">参数</span><span class="sxs-lookup"><span data-stu-id="9e765-107">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="9e765-108">中包含类的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="9e765-108">[in] The ID of the module that contains the class.</span></span>  
  
 `typeDef`  
 <span data-ttu-id="9e765-109">中 `mdTypeDef` 引用类的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="9e765-109">[in] An `mdTypeDef` metadata token that references the class.</span></span>  
  
 `cTypeArgs`  
 <span data-ttu-id="9e765-110">弄指向类 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="9e765-110">[out] A pointer to the class ID.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9e765-111">注解</span><span class="sxs-lookup"><span data-stu-id="9e765-111">Remarks</span></span>  

 <span data-ttu-id="9e765-112">此方法已过时;而是将 `ICorProfilerInfo2::GetClassFromTokenAndTypeArgs` 用于所有类型。</span><span class="sxs-lookup"><span data-stu-id="9e765-112">This method is obsolete; instead, use `ICorProfilerInfo2::GetClassFromTokenAndTypeArgs` for all types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9e765-113">要求</span><span class="sxs-lookup"><span data-stu-id="9e765-113">Requirements</span></span>  

 <span data-ttu-id="9e765-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9e765-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9e765-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9e765-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9e765-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9e765-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9e765-117">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="9e765-117">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e765-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9e765-118">See also</span></span>

- [<span data-ttu-id="9e765-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="9e765-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
