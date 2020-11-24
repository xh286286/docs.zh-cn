---
title: IMetaDataAssemblyEmit::DefineExportedType 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineExportedType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineExportedType
helpviewer_keywords:
- IMetaDataAssemblyEmit::DefineExportedType method [.NET Framework metadata]
- DefineExportedType method [.NET Framework metadata]
ms.assetid: fad01d7a-3178-4c8c-9f0a-4641e3701c9b
topic_type:
- apiref
ms.openlocfilehash: 6b30218cc7373494870ec54a3196857fcc5c08a5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689389"
---
# <a name="imetadataassemblyemitdefineexportedtype-method"></a><span data-ttu-id="4eba9-102">IMetaDataAssemblyEmit::DefineExportedType 方法</span><span class="sxs-lookup"><span data-stu-id="4eba9-102">IMetaDataAssemblyEmit::DefineExportedType Method</span></span>

<span data-ttu-id="4eba9-103">创建包含指定导出类型的元数据的 `ExportedType` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="4eba9-103">Creates an `ExportedType` structure containing metadata for the specified exported type, and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4eba9-104">语法</span><span class="sxs-lookup"><span data-stu-id="4eba9-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineExportedType (  
    [in]  LPCWSTR             szName,  
    [in]  mdToken             tkImplementation,
    [in]  mdTypeDef           tkTypeDef,  
    [in]  DWORD               dwExportedTypeFlags,  
    [out] mdExportedType      *pmdct  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4eba9-105">参数</span><span class="sxs-lookup"><span data-stu-id="4eba9-105">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="4eba9-106">中要导出的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="4eba9-106">[in] The name of type to be exported.</span></span> <span data-ttu-id="4eba9-107">对于公共语言运行时版本1.1，导出类型的名称必须与在类型中为指定的名称完全匹配 `TypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="4eba9-107">For version 1.1 of the common language runtime, the name of the exported type must exactly match the name given in the `TypeDef` for the type.</span></span>  
  
 `tkImplementation`  
 <span data-ttu-id="4eba9-108">中指定在何处实现导出类型的标记。</span><span class="sxs-lookup"><span data-stu-id="4eba9-108">[in] A token specifying where the exported type is implemented.</span></span> <span data-ttu-id="4eba9-109">有效值及其关联的含义如下：</span><span class="sxs-lookup"><span data-stu-id="4eba9-109">The valid values and their associated meanings are:</span></span>  
  
- <span data-ttu-id="4eba9-110">`mdFile` 该类型在此程序集内的其他文件中实现。</span><span class="sxs-lookup"><span data-stu-id="4eba9-110">`mdFile` The type is implemented in a different file within this assembly.</span></span>  
  
- <span data-ttu-id="4eba9-111">`mdAssemblyRef` 类型是在不同的程序集中实现的。</span><span class="sxs-lookup"><span data-stu-id="4eba9-111">`mdAssemblyRef` The type is implemented in a different assembly.</span></span>  
  
- <span data-ttu-id="4eba9-112">`mdExportedTYpe` 类型嵌套在某个其他类型中。</span><span class="sxs-lookup"><span data-stu-id="4eba9-112">`mdExportedTYpe` The type is nested within some other type.</span></span>  
  
- <span data-ttu-id="4eba9-113">`mdFileNil` 该类型与清单位于同一文件中，并且不是嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="4eba9-113">`mdFileNil` The type is in the same file as the manifest and is not a nested type.</span></span>  
  
 `tkTypeDef`  
 <span data-ttu-id="4eba9-114">中用于指定要导出的类型的元数据的令牌。</span><span class="sxs-lookup"><span data-stu-id="4eba9-114">[in] A token to the metadata that specifies the type to be exported.</span></span> <span data-ttu-id="4eba9-115">此值输入在 `TypeDef` 实现类型的文件中的表中，并且仅当该文件在此程序集中时，此值才适用。</span><span class="sxs-lookup"><span data-stu-id="4eba9-115">This value is entered in the `TypeDef` table in the file that implements the type and is relevant only if that file is in this assembly.</span></span>  
  
 `dwExportedTypeFlags`  
 <span data-ttu-id="4eba9-116">中 [CorTypeAttr](cortypeattr-enumeration.md) 枚举值的按位组合，用于定义导出的类型的属性设置。</span><span class="sxs-lookup"><span data-stu-id="4eba9-116">[in] A bitwise combination of [CorTypeAttr](cortypeattr-enumeration.md) enumeration values that define the property settings for the exported type.</span></span>  
  
 `pmdct`  
 <span data-ttu-id="4eba9-117">弄指向返回的元数据标记的指针，该标记指示导出的类型。</span><span class="sxs-lookup"><span data-stu-id="4eba9-117">[out] A pointer to the returned metadata token that indicates the exported type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4eba9-118">注解</span><span class="sxs-lookup"><span data-stu-id="4eba9-118">Remarks</span></span>  

 <span data-ttu-id="4eba9-119">`ExportedType`必须为此程序集公开的每个类型定义元数据结构，该结构在包含清单的模块中实现。</span><span class="sxs-lookup"><span data-stu-id="4eba9-119">An `ExportedType` metadata structure must be defined for each type that is exposed by this assembly and that is implemented in a module other than the one containing the manifest.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4eba9-120">要求</span><span class="sxs-lookup"><span data-stu-id="4eba9-120">Requirements</span></span>  

 <span data-ttu-id="4eba9-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4eba9-121">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4eba9-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="4eba9-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4eba9-123">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="4eba9-123">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4eba9-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4eba9-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4eba9-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4eba9-125">See also</span></span>

- [<span data-ttu-id="4eba9-126">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="4eba9-126">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
