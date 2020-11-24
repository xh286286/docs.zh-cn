---
title: IMetaDataAssemblyEmit::DefineAssemblyRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineAssemblyRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineAssemblyRef
helpviewer_keywords:
- DefineAssemblyRef method [.NET Framework metadata]
- IMetaDataAssemblyEmit::DefineAssemblyRef method [.NET Framework metadata]
ms.assetid: 0b284b18-0084-4b3a-912a-5ebe9f29c88b
topic_type:
- apiref
ms.openlocfilehash: ba53ff30f0b6d0ae7fed7db422b7c0a242204a2c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689424"
---
# <a name="imetadataassemblyemitdefineassemblyref-method"></a><span data-ttu-id="ab286-102">IMetaDataAssemblyEmit::DefineAssemblyRef 方法</span><span class="sxs-lookup"><span data-stu-id="ab286-102">IMetaDataAssemblyEmit::DefineAssemblyRef Method</span></span>

<span data-ttu-id="ab286-103">创建包含此程序集引用的程序集的元数据的 `AssemblyRef` 结构，并返回关联的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ab286-103">Creates an `AssemblyRef` structure containing metadata for the assembly that this assembly references, and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab286-104">语法</span><span class="sxs-lookup"><span data-stu-id="ab286-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineAssemblyRef (  
    [in]  void                *pbPublicKeyOrToken,  
    [in]  ULONG               cbPublicKeyOrToken,  
    [in]  LPCWSTR             szName,  
    [in]  ASSEMBLYMETADATA    pMetaData,  
    [in]  void                *pbHashValue,  
    [in]  ULONG               cbHashValue,  
    [in]  DWORD               dwAssemblyRefFlags,  
    [out] mdAssemblyRef       *pmdar  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab286-105">参数</span><span class="sxs-lookup"><span data-stu-id="ab286-105">Parameters</span></span>  

 `pbPublicKeyOrToken`  
 <span data-ttu-id="ab286-106">中所引用程序集的发行者的公钥。</span><span class="sxs-lookup"><span data-stu-id="ab286-106">[in] The public key of the publisher of the referenced assembly.</span></span> <span data-ttu-id="ab286-107">Helper 函数 [StrongNameTokenFromAssembly](../strong-naming/strongnametokenfromassembly-function.md) 可用于获取公钥哈希作为此参数传递。</span><span class="sxs-lookup"><span data-stu-id="ab286-107">The helper function [StrongNameTokenFromAssembly](../strong-naming/strongnametokenfromassembly-function.md) can be used to get the hash of the public key to pass as this parameter.</span></span>  
  
 `cbPublicKeyOrToken`  
 <span data-ttu-id="ab286-108">中的大小（以字节为单位） `pbPublicKeyOrToken` 。</span><span class="sxs-lookup"><span data-stu-id="ab286-108">[in] The size in bytes of `pbPublicKeyOrToken`.</span></span>  
  
 `szName`  
 <span data-ttu-id="ab286-109">中程序集的用户可读文本名称。</span><span class="sxs-lookup"><span data-stu-id="ab286-109">[in] The human-readable text name of the assembly.</span></span> <span data-ttu-id="ab286-110">此值不能超过1024个字符。</span><span class="sxs-lookup"><span data-stu-id="ab286-110">This value must not exceed 1024 characters.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="ab286-111">中一个 ASSEMBLYMETADATA 实例，其中包含所引用程序集的版本、平台和区域设置信息。</span><span class="sxs-lookup"><span data-stu-id="ab286-111">[in] An ASSEMBLYMETADATA instance that contains the version, platform and locale information of the referenced assembly.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="ab286-112">中与所引用的程序集关联的哈希数据。</span><span class="sxs-lookup"><span data-stu-id="ab286-112">[in] The hash data associated with the referenced assembly.</span></span> <span data-ttu-id="ab286-113">可选。</span><span class="sxs-lookup"><span data-stu-id="ab286-113">Optional.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="ab286-114">中的大小（以字节为单位） `pbHashValue` 。</span><span class="sxs-lookup"><span data-stu-id="ab286-114">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwAssemblyRefFlags`  
 <span data-ttu-id="ab286-115">中影响执行引擎行为的 [CorAssemblyFlags](corassemblyflags-enumeration.md) 值的按位组合。</span><span class="sxs-lookup"><span data-stu-id="ab286-115">[in] A bitwise combination of [CorAssemblyFlags](corassemblyflags-enumeration.md) values that influence the behavior of the execution engine.</span></span>  
  
 `pmdar`  
 <span data-ttu-id="ab286-116">弄指向返回的 `AssemblyRef` 元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="ab286-116">[out] A pointer to the returned `AssemblyRef` metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ab286-117">注解</span><span class="sxs-lookup"><span data-stu-id="ab286-117">Remarks</span></span>  

 <span data-ttu-id="ab286-118">`AssemblyRef`必须为此程序集引用的每个程序集定义一个元数据结构。</span><span class="sxs-lookup"><span data-stu-id="ab286-118">One `AssemblyRef` metadata structure must be defined for each assembly that this assembly references.</span></span>  
  
 <span data-ttu-id="ab286-119">在运行时，被引用程序集的详细信息将传递给程序集解析程序，并指示它们表示 "生成的" 信息。</span><span class="sxs-lookup"><span data-stu-id="ab286-119">At run time, the details of a referenced assembly are passed to the assembly resolver with an indication that they represent the "as built" information.</span></span> <span data-ttu-id="ab286-120">然后，程序集冲突解决程序将应用策略。</span><span class="sxs-lookup"><span data-stu-id="ab286-120">The assembly resolver then applies policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab286-121">要求</span><span class="sxs-lookup"><span data-stu-id="ab286-121">Requirements</span></span>  

 <span data-ttu-id="ab286-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ab286-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab286-123">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="ab286-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ab286-124">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="ab286-124">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ab286-125">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab286-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab286-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ab286-126">See also</span></span>

- [<span data-ttu-id="ab286-127">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="ab286-127">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
