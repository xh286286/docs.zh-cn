---
title: IMetaDataEmit::DefineModuleRef 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineModuleRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineModuleRef
helpviewer_keywords:
- DefineModuleRef method [.NET Framework metadata]
- IMetaDataEmit::DefineModuleRef method [.NET Framework metadata]
ms.assetid: f2833594-d90b-4a71-9a53-34b12470c64a
topic_type:
- apiref
ms.openlocfilehash: 96d24705d80dabcda691edec497a4a30b6d37dc4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719549"
---
# <a name="imetadataemitdefinemoduleref-method"></a><span data-ttu-id="1acdc-102">IMetaDataEmit::DefineModuleRef 方法</span><span class="sxs-lookup"><span data-stu-id="1acdc-102">IMetaDataEmit::DefineModuleRef Method</span></span>

<span data-ttu-id="1acdc-103">创建具有指定名称的模块的元数据签名。</span><span class="sxs-lookup"><span data-stu-id="1acdc-103">Creates the metadata signature for a module with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1acdc-104">语法</span><span class="sxs-lookup"><span data-stu-id="1acdc-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineModuleRef (
    [in]  LPCWSTR           szName,
    [out] mdModuleRef       *pmur
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1acdc-105">参数</span><span class="sxs-lookup"><span data-stu-id="1acdc-105">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="1acdc-106">中其他元数据文件（通常为 DLL）的名称。</span><span class="sxs-lookup"><span data-stu-id="1acdc-106">[in] The name of the other metadata file, typically a DLL.</span></span> <span data-ttu-id="1acdc-107">这只是文件名。</span><span class="sxs-lookup"><span data-stu-id="1acdc-107">This is the file name only.</span></span> <span data-ttu-id="1acdc-108">不要使用完整路径名称。</span><span class="sxs-lookup"><span data-stu-id="1acdc-108">Do not use a full path name.</span></span>  
  
 `pmur`  
 <span data-ttu-id="1acdc-109">弄已分配的 `mdModuleRef` 标记。</span><span class="sxs-lookup"><span data-stu-id="1acdc-109">[out] The assigned `mdModuleRef` token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1acdc-110">要求</span><span class="sxs-lookup"><span data-stu-id="1acdc-110">Requirements</span></span>  

 <span data-ttu-id="1acdc-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1acdc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1acdc-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1acdc-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1acdc-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1acdc-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1acdc-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1acdc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1acdc-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1acdc-115">See also</span></span>

- [<span data-ttu-id="1acdc-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="1acdc-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="1acdc-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="1acdc-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
