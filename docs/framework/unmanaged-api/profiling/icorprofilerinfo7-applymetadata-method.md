---
title: ICorProfilerInfo7：： ApplyMetaData 方法
ms.date: 02/15/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo7.ApplyMetaData
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: a1bfb649-4584-4d35-b3e6-8fe59b53992a
ms.openlocfilehash: 2c71db25422740880d8b29576eff247d5eba5f1d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95686106"
---
# <a name="icorprofilerinfo7applymetadata-method"></a><span data-ttu-id="fedc2-102">ICorProfilerInfo7：： ApplyMetaData 方法</span><span class="sxs-lookup"><span data-stu-id="fedc2-102">ICorProfilerInfo7::ApplyMetaData Method</span></span>

<span data-ttu-id="fedc2-103">[仅在 .NET Framework 4.6.1 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="fedc2-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="fedc2-104">将方法的新定义的元数据应用于 `IMetadataEmit::Define*` 指定的模块。</span><span class="sxs-lookup"><span data-stu-id="fedc2-104">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fedc2-105">语法</span><span class="sxs-lookup"><span data-stu-id="fedc2-105">Syntax</span></span>  
  
```cpp
HRESULT ApplyMetaData(  
        [in] ModuleID moduleID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fedc2-106">参数</span><span class="sxs-lookup"><span data-stu-id="fedc2-106">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="fedc2-107">中已更改其元数据的模块的标识符。</span><span class="sxs-lookup"><span data-stu-id="fedc2-107">[in] The identifier of the module whose metadata was changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fedc2-108">注解</span><span class="sxs-lookup"><span data-stu-id="fedc2-108">Remarks</span></span>  

 <span data-ttu-id="fedc2-109">如果在 [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 回调之后进行元数据更改，则必须在使用新元数据之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="fedc2-109">If metadata changes are made after the [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) callback, you must call this method before using the new metadata.</span></span>  
  
 <span data-ttu-id="fedc2-110">`ApplyMetaData` 仅支持添加以下类型的元数据：</span><span class="sxs-lookup"><span data-stu-id="fedc2-110">`ApplyMetaData` only supports adding the following types of metadata:</span></span>  
  
- <span data-ttu-id="fedc2-111">`AssemblyRef` 通过调用 [IMetaDataAssemblyEmit：:D efineassemblyref](../metadata/imetadataassemblyemit-defineassemblyref-method.md)创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-111">`AssemblyRef` records, which you create by calling the [IMetaDataAssemblyEmit::DefineAssemblyRef](../metadata/imetadataassemblyemit-defineassemblyref-method.md).</span></span> <span data-ttu-id="fedc2-112">方法。</span><span class="sxs-lookup"><span data-stu-id="fedc2-112">method.</span></span>  
  
- <span data-ttu-id="fedc2-113">`TypeRef` 通过调用 [IMetaDataEmit：:D efinetyperefbyname](../metadata/imetadataemit-definetyperefbyname-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-113">`TypeRef` records, which you create by calling the [IMetaDataEmit::DefineTypeRefByName](../metadata/imetadataemit-definetyperefbyname-method.md) method.</span></span>  
  
- <span data-ttu-id="fedc2-114">`TypeSpec` 通过调用 [IMetaDataEmit：： GetTokenFromTypeSpec](../metadata/imetadataemit-gettokenfromtypespec-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-114">`TypeSpec` records, which you create by calling the [IMetaDataEmit::GetTokenFromTypeSpec](../metadata/imetadataemit-gettokenfromtypespec-method.md) method.</span></span>  
  
- <span data-ttu-id="fedc2-115">`MemberRef` 通过调用 [IMetaDataEmit：:D efinememberref](../metadata/imetadataemit-definememberref-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-115">`MemberRef` records, which you create by calling the [IMetaDataEmit::DefineMemberRef](../metadata/imetadataemit-definememberref-method.md) method.</span></span>  
  
- <span data-ttu-id="fedc2-116">`MemberSpec` 通过调用 [IMetaDataEmit2：:D efinemethodspec](../metadata/imetadataemit2-definemethodspec-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-116">`MemberSpec` records, which you create by calling the [IMetaDataEmit2::DefineMethodSpec](../metadata/imetadataemit2-definemethodspec-method.md) method.</span></span>  
  
- <span data-ttu-id="fedc2-117">`UserString` 通过调用 [IMetaDataEmit：:D efineuserstring](../metadata/imetadataemit-defineuserstring-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-117">`UserString` records, which you create by calling the [IMetaDataEmit::DefineUserString](../metadata/imetadataemit-defineuserstring-method.md) method.</span></span>  

<span data-ttu-id="fedc2-118">从 .NET Core 3.0 开始， `ApplyMetaData` 还支持以下类型：</span><span class="sxs-lookup"><span data-stu-id="fedc2-118">Starting with .NET Core 3.0, `ApplyMetaData` also supports the following types:</span></span>

- <span data-ttu-id="fedc2-119">`TypeDef` 通过调用 [IMetaDataEmit：:D efinetypedef](../metadata/imetadataemit-definetypedef-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-119">`TypeDef` records, which you create by calling the [IMetaDataEmit::DefineTypeDef](../metadata/imetadataemit-definetypedef-method.md) method.</span></span>

- <span data-ttu-id="fedc2-120">`MethodDef` 通过调用 [IMetaDataEmit：:D efinemethod](../metadata/imetadataemit-definemethod-method.md) 方法创建的记录。</span><span class="sxs-lookup"><span data-stu-id="fedc2-120">`MethodDef` records, which you create by calling the [IMetaDataEmit::DefineMethod](../metadata/imetadataemit-definemethod-method.md) method.</span></span> <span data-ttu-id="fedc2-121">但是，不支持向现有类型添加虚拟方法。</span><span class="sxs-lookup"><span data-stu-id="fedc2-121">However, adding virtual methods to an existing type is not supported.</span></span> <span data-ttu-id="fedc2-122">必须在 [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 回调之前添加虚拟方法。</span><span class="sxs-lookup"><span data-stu-id="fedc2-122">Virtual methods must be added before the [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedc2-123">要求</span><span class="sxs-lookup"><span data-stu-id="fedc2-123">Requirements</span></span>  

 <span data-ttu-id="fedc2-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fedc2-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fedc2-125">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fedc2-125">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fedc2-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fedc2-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fedc2-127">**.NET Framework 版本：**[!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fedc2-127">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fedc2-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fedc2-128">See also</span></span>

- [<span data-ttu-id="fedc2-129">ICorProfilerInfo7 接口</span><span class="sxs-lookup"><span data-stu-id="fedc2-129">ICorProfilerInfo7 Interface</span></span>](icorprofilerinfo7-interface.md)
