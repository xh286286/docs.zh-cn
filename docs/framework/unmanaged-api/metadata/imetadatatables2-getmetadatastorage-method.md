---
title: IMetaDataTables2::GetMetaDataStorage 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables2.GetMetaDataStorage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables2::GetMetaDataStorage
helpviewer_keywords:
- GetMetaDataStorage method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStorage method [.NET Framework metadata]
ms.assetid: 667a6d1e-753d-4ea2-8fd8-a8337d1bb9cd
topic_type:
- apiref
ms.openlocfilehash: 775b3919d1468f26fc3c374dd8ca143aa17853ce
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708733"
---
# <a name="imetadatatables2getmetadatastorage-method"></a><span data-ttu-id="6eaf4-102">IMetaDataTables2::GetMetaDataStorage 方法</span><span class="sxs-lookup"><span data-stu-id="6eaf4-102">IMetaDataTables2::GetMetaDataStorage Method</span></span>

<span data-ttu-id="6eaf4-103">获取指定节中存储的元数据的大小和内容。</span><span class="sxs-lookup"><span data-stu-id="6eaf4-103">Gets the size and contents of the metadata stored in the specified section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6eaf4-104">语法</span><span class="sxs-lookup"><span data-stu-id="6eaf4-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaDataStorage (  
   [in, out] const void   **ppvMd,  
   [out] ULONG   *pcbMd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6eaf4-105">参数</span><span class="sxs-lookup"><span data-stu-id="6eaf4-105">Parameters</span></span>  

 `ppvMd`  
 <span data-ttu-id="6eaf4-106">[in，out]指向元数据部分的指针。</span><span class="sxs-lookup"><span data-stu-id="6eaf4-106">[in, out] A pointer to a metadata section.</span></span>  
  
 `pcbMd`  
 <span data-ttu-id="6eaf4-107">弄元数据流的大小。</span><span class="sxs-lookup"><span data-stu-id="6eaf4-107">[out] The size of the metadata stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6eaf4-108">要求</span><span class="sxs-lookup"><span data-stu-id="6eaf4-108">Requirements</span></span>  

 <span data-ttu-id="6eaf4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6eaf4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6eaf4-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="6eaf4-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6eaf4-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="6eaf4-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6eaf4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6eaf4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6eaf4-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6eaf4-113">See also</span></span>

- [<span data-ttu-id="6eaf4-114">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="6eaf4-114">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
- [<span data-ttu-id="6eaf4-115">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="6eaf4-115">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
