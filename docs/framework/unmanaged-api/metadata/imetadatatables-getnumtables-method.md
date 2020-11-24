---
title: IMetaDataTables::GetNumTables 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNumTables
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNumTables
helpviewer_keywords:
- GetNumTables method [.NET Framework metadata]
- IMetaDataTables::GetNumTables method [.NET Framework metadata]
ms.assetid: 8196f2a3-bbf2-45d3-a6cd-74502c356644
topic_type:
- apiref
ms.openlocfilehash: 7e1ea16e7954f21b1349e88d43d7e3b271a57ed7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95680283"
---
# <a name="imetadatatablesgetnumtables-method"></a><span data-ttu-id="efae1-102">IMetaDataTables::GetNumTables 方法</span><span class="sxs-lookup"><span data-stu-id="efae1-102">IMetaDataTables::GetNumTables Method</span></span>

<span data-ttu-id="efae1-103">获取当前实例的范围中的表数 `IMetaDataTables` 。</span><span class="sxs-lookup"><span data-stu-id="efae1-103">Gets the number of tables in the scope of the current `IMetaDataTables` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efae1-104">语法</span><span class="sxs-lookup"><span data-stu-id="efae1-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNumTables (  
    [out]  ULONG   *pcTables  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="efae1-105">参数</span><span class="sxs-lookup"><span data-stu-id="efae1-105">Parameters</span></span>  

 `pcTables`  
 <span data-ttu-id="efae1-106">弄一个指针，指向当前实例范围中的表数。</span><span class="sxs-lookup"><span data-stu-id="efae1-106">[out] A pointer to the number of tables in the current instance scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="efae1-107">要求</span><span class="sxs-lookup"><span data-stu-id="efae1-107">Requirements</span></span>  

 <span data-ttu-id="efae1-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="efae1-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="efae1-109">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="efae1-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="efae1-110">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="efae1-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="efae1-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="efae1-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efae1-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="efae1-112">See also</span></span>

- [<span data-ttu-id="efae1-113">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="efae1-113">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="efae1-114">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="efae1-114">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
