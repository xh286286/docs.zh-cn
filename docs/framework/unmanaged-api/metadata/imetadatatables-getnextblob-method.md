---
title: IMetaDataTables::GetNextBlob 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextBlob
helpviewer_keywords:
- IMetaDataTables::GetNextBlob method [.NET Framework metadata]
- GetNextBlob method [.NET Framework metadata]
ms.assetid: 017c8ab4-4c09-4754-9935-5b0b49cabecb
topic_type:
- apiref
ms.openlocfilehash: ba694f485d5a51870a1283b6ccbcb7b042a14501
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95685625"
---
# <a name="imetadatatablesgetnextblob-method"></a><span data-ttu-id="4d5ed-102">IMetaDataTables::GetNextBlob 方法</span><span class="sxs-lookup"><span data-stu-id="4d5ed-102">IMetaDataTables::GetNextBlob Method</span></span>

<span data-ttu-id="4d5ed-103">获取表中 (BLOB) 的下一个二进制大型对象的索引。</span><span class="sxs-lookup"><span data-stu-id="4d5ed-103">Gets the index of the next binary large object (BLOB) in the table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d5ed-104">语法</span><span class="sxs-lookup"><span data-stu-id="4d5ed-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNextBlob (  
    [in]  ULONG   ixBlob,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4d5ed-105">参数</span><span class="sxs-lookup"><span data-stu-id="4d5ed-105">Parameters</span></span>  

 `ixBlob`  
 <span data-ttu-id="4d5ed-106">中从 Blob 的列中返回的索引。</span><span class="sxs-lookup"><span data-stu-id="4d5ed-106">[in] The index, as returned from a column of BLOBs.</span></span>  
  
 `pNext`  
 <span data-ttu-id="4d5ed-107">弄指向下一个 BLOB 的索引的指针。</span><span class="sxs-lookup"><span data-stu-id="4d5ed-107">[out] A pointer to the index of the next BLOB.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4d5ed-108">要求</span><span class="sxs-lookup"><span data-stu-id="4d5ed-108">Requirements</span></span>  

 <span data-ttu-id="4d5ed-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4d5ed-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4d5ed-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="4d5ed-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4d5ed-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="4d5ed-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4d5ed-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4d5ed-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d5ed-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d5ed-113">See also</span></span>

- [<span data-ttu-id="4d5ed-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="4d5ed-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="4d5ed-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="4d5ed-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
