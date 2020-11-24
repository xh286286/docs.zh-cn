---
title: IMetaDataAssemblyEmit::SetAssemblyRefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetAssemblyRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetAssemblyRefProps
helpviewer_keywords:
- SetAssemblyRefProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetAssemblyRefProps method [.NET Framework metadata]
ms.assetid: 70a32bf3-9051-4f96-ae87-11356d06a073
topic_type:
- apiref
ms.openlocfilehash: e28659f3c6912489775dd09951610f19e4400942
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95672742"
---
# <a name="imetadataassemblyemitsetassemblyrefprops-method"></a><span data-ttu-id="e22bd-102">IMetaDataAssemblyEmit::SetAssemblyRefProps 方法</span><span class="sxs-lookup"><span data-stu-id="e22bd-102">IMetaDataAssemblyEmit::SetAssemblyRefProps Method</span></span>

<span data-ttu-id="e22bd-103">修改指定的 `AssemblyRef` 元数据结构。</span><span class="sxs-lookup"><span data-stu-id="e22bd-103">Modifies the specified `AssemblyRef` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e22bd-104">语法</span><span class="sxs-lookup"><span data-stu-id="e22bd-104">Syntax</span></span>  
  
```cpp  
HRESULT SetAssemblyRefProps (  
    [in] mdAssemblyRef              ar,  
    [in] const void                 *pbPublicKeyOrToken,  
    [in] ULONG                      cbPublicKeyOrToken,  
    [in] LPCWSTR                    szName,
    [in] const ASSEMBLYMETADATA     *pMetaData,
    [in] const void                 *pbHashValue,  
    [in] ULONG                      cbHashValue,  
    [in] DWORD                      dwAssemblyRefFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e22bd-105">参数</span><span class="sxs-lookup"><span data-stu-id="e22bd-105">Parameters</span></span>  

 `ar`  
 <span data-ttu-id="e22bd-106">中 `AssemblyRef` 用于指定要修改的元数据结构的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e22bd-106">[in] The metadata token that specifies the `AssemblyRef` metadata structure to be modified.</span></span>  
  
 `pbPublicKeyOrToken`  
 <span data-ttu-id="e22bd-107">中所引用程序集的发行者的公钥。</span><span class="sxs-lookup"><span data-stu-id="e22bd-107">[in] The public key of the publisher of the referenced assembly.</span></span>  
  
 `cbPublicKeyOrToken`  
 <span data-ttu-id="e22bd-108">中的大小（以字节为单位） `pbPublicKeyOrToken` 。</span><span class="sxs-lookup"><span data-stu-id="e22bd-108">[in] The size in bytes of `pbPublicKeyOrToken`.</span></span>  
  
 `szName`  
 <span data-ttu-id="e22bd-109">中程序集的用户可读文本名称。</span><span class="sxs-lookup"><span data-stu-id="e22bd-109">[in] The human-readable text name of the assembly.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="e22bd-110">中指向 ASSEMBLYMETADATA 实例的指针，其中包含程序集的版本、平台和区域设置信息。</span><span class="sxs-lookup"><span data-stu-id="e22bd-110">[in] A pointer to an ASSEMBLYMETADATA instance that contains the version, platform, and locale information for the assembly.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="e22bd-111">中指向与程序集关联的哈希数据的指针。</span><span class="sxs-lookup"><span data-stu-id="e22bd-111">[in] A pointer to the hash data associated with the assembly.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="e22bd-112">中的大小（以字节为单位） `pbHashValue` 。</span><span class="sxs-lookup"><span data-stu-id="e22bd-112">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwAssemblyRefFlags`  
 <span data-ttu-id="e22bd-113">中 [AssemblyRefFlags](assemblyrefflags-enumeration.md) 值的按位组合，用于指定所引用程序集的特性。</span><span class="sxs-lookup"><span data-stu-id="e22bd-113">[in] A bitwise combination of [AssemblyRefFlags](assemblyrefflags-enumeration.md) values that specify attributes of the referenced assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e22bd-114">注解</span><span class="sxs-lookup"><span data-stu-id="e22bd-114">Remarks</span></span>  

 <span data-ttu-id="e22bd-115">若要创建 `AssemblyRef` 元数据结构，请使用 [IMetaDataAssemblyEmit：:D efineassemblyref](imetadataassemblyemit-defineassemblyref-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e22bd-115">To create an `AssemblyRef` metadata structure, use the [IMetaDataAssemblyEmit::DefineAssemblyRef](imetadataassemblyemit-defineassemblyref-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e22bd-116">要求</span><span class="sxs-lookup"><span data-stu-id="e22bd-116">Requirements</span></span>  

 <span data-ttu-id="e22bd-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e22bd-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e22bd-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e22bd-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e22bd-119">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e22bd-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e22bd-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e22bd-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e22bd-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e22bd-121">See also</span></span>

- [<span data-ttu-id="e22bd-122">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="e22bd-122">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
