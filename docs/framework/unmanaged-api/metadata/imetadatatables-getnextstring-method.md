---
title: IMetaDataTables::GetNextString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextString
helpviewer_keywords:
- IMetaDataTables::GetNextString method [.NET Framework metadata]
- GetNextString method [.NET Framework metadata]
ms.assetid: d9720428-c353-4f07-a7e8-899e106a1b37
topic_type:
- apiref
ms.openlocfilehash: b79dbdd64ac171d1bc4cd30b96ee76b4a853afb6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727245"
---
# <a name="imetadatatablesgetnextstring-method"></a><span data-ttu-id="0539b-102">IMetaDataTables::GetNextString 方法</span><span class="sxs-lookup"><span data-stu-id="0539b-102">IMetaDataTables::GetNextString Method</span></span>

<span data-ttu-id="0539b-103">获取当前表列中的下一个字符串的索引。</span><span class="sxs-lookup"><span data-stu-id="0539b-103">Gets the index of the next string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0539b-104">语法</span><span class="sxs-lookup"><span data-stu-id="0539b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNextString (
    [in]  ULONG   ixString,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0539b-105">参数</span><span class="sxs-lookup"><span data-stu-id="0539b-105">Parameters</span></span>  

 `ixString`  
 <span data-ttu-id="0539b-106">中字符串表列的索引值。</span><span class="sxs-lookup"><span data-stu-id="0539b-106">[in] The index value from a string table column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="0539b-107">弄指向列中的下一个字符串的索引的指针。</span><span class="sxs-lookup"><span data-stu-id="0539b-107">[out] A pointer to the index of the next string in the column.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0539b-108">要求</span><span class="sxs-lookup"><span data-stu-id="0539b-108">Requirements</span></span>  

 <span data-ttu-id="0539b-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0539b-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0539b-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0539b-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0539b-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0539b-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0539b-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0539b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0539b-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0539b-113">See also</span></span>

- [<span data-ttu-id="0539b-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="0539b-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="0539b-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="0539b-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
