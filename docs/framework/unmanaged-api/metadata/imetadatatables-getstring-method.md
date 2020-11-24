---
title: IMetaDataTables::GetString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetString
helpviewer_keywords:
- IMetaDataTables::GetString method [.NET Framework metadata]
- GetString method, IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 895c35cf-b95d-4e3b-93b5-cfc1cf9044fc
topic_type:
- apiref
ms.openlocfilehash: 8ecaa003084064be1071a85aa726c38d773ec0b4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95672573"
---
# <a name="imetadatatablesgetstring-method"></a><span data-ttu-id="84a10-102">IMetaDataTables::GetString 方法</span><span class="sxs-lookup"><span data-stu-id="84a10-102">IMetaDataTables::GetString Method</span></span>

<span data-ttu-id="84a10-103">从当前引用范围内的表列中获取指定索引处的字符串。</span><span class="sxs-lookup"><span data-stu-id="84a10-103">Gets the string at the specified index from the table column in the current reference scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84a10-104">语法</span><span class="sxs-lookup"><span data-stu-id="84a10-104">Syntax</span></span>  
  
```cpp  
HRESULT GetString (
    [in]  ULONG       ixString,  
    [out] const char  **ppString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84a10-105">参数</span><span class="sxs-lookup"><span data-stu-id="84a10-105">Parameters</span></span>  

 `ixString`  
 <span data-ttu-id="84a10-106">中开始搜索下一个值的索引位置。</span><span class="sxs-lookup"><span data-stu-id="84a10-106">[in] The index at which to start to search for the next value.</span></span>  
  
 `ppString`  
 <span data-ttu-id="84a10-107">弄指向返回的字符串值的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="84a10-107">[out] A pointer to a pointer to the returned string value.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84a10-108">要求</span><span class="sxs-lookup"><span data-stu-id="84a10-108">Requirements</span></span>  

 <span data-ttu-id="84a10-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84a10-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84a10-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="84a10-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="84a10-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="84a10-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="84a10-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84a10-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84a10-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84a10-113">See also</span></span>

- [<span data-ttu-id="84a10-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="84a10-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="84a10-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="84a10-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
