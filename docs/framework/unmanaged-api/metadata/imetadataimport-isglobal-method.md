---
title: IMetaDataImport::IsGlobal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.IsGlobal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::IsGlobal
helpviewer_keywords:
- IsGlobal method [.NET Framework metadata]
- IMetaDataImport::IsGlobal method [.NET Framework metadata]
ms.assetid: 44cf6908-f555-4ae8-b2cf-24bd974bf2fe
topic_type:
- apiref
ms.openlocfilehash: 0d76abf8a9c923089f367ab4e1786ac8cc92622d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702961"
---
# <a name="imetadataimportisglobal-method"></a><span data-ttu-id="d90a0-102">IMetaDataImport::IsGlobal 方法</span><span class="sxs-lookup"><span data-stu-id="d90a0-102">IMetaDataImport::IsGlobal Method</span></span>

<span data-ttu-id="d90a0-103">获取一个值，该值指示由指定的元数据标记表示的字段、方法或类型是否具有全局范围。</span><span class="sxs-lookup"><span data-stu-id="d90a0-103">Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d90a0-104">语法</span><span class="sxs-lookup"><span data-stu-id="d90a0-104">Syntax</span></span>  
  
```cpp  
HRESULT IsGlobal (  
   [in]  mdToken     pd,  
   [out] int         *pbGlobal  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d90a0-105">参数</span><span class="sxs-lookup"><span data-stu-id="d90a0-105">Parameters</span></span>  

 `pd`  
 <span data-ttu-id="d90a0-106">中表示类型、字段或方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="d90a0-106">[in] A metadata token that represents a type, field, or method.</span></span>  
  
 `pbGlobal`  
 <span data-ttu-id="d90a0-107">[out] 如果对象具有全局范围，则为 1;否则，0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="d90a0-107">[out] 1 if the object has global scope; otherwise, 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d90a0-108">要求</span><span class="sxs-lookup"><span data-stu-id="d90a0-108">Requirements</span></span>  

 <span data-ttu-id="d90a0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d90a0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d90a0-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d90a0-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d90a0-111">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d90a0-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d90a0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d90a0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d90a0-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d90a0-113">See also</span></span>

- [<span data-ttu-id="d90a0-114">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="d90a0-114">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="d90a0-115">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="d90a0-115">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
