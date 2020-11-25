---
title: IMetaDataConverter::GetMetaDataFromTypeLib 方法
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetMetaDataFromTypeLib
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetMetaDataFromTypeLib
helpviewer_keywords:
- IMetaDataConverter::GetMetaDataFromTypeLib method [.NET Framework metadata]
- GetMetaDataFromTypeLib method [.NET Framework metadata]
ms.assetid: 97dc3a56-adfa-431f-889e-06a35ac84d51
topic_type:
- apiref
ms.openlocfilehash: ed0902824bdbb4d057bf5a7920db4b1d18eb7347
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714661"
---
# <a name="imetadataconvertergetmetadatafromtypelib-method"></a><span data-ttu-id="c4b8a-102">IMetaDataConverter::GetMetaDataFromTypeLib 方法</span><span class="sxs-lookup"><span data-stu-id="c4b8a-102">IMetaDataConverter::GetMetaDataFromTypeLib Method</span></span>

<span data-ttu-id="c4b8a-103">获取一个接口指针，该指针指向表示由指定的实例表示的类型库的元数据签名的 [IMetaDataImport](imetadataimport-interface.md) 实例 `ITypeLib` 。</span><span class="sxs-lookup"><span data-stu-id="c4b8a-103">Gets an interface pointer to an [IMetaDataImport](imetadataimport-interface.md) instance that represents the metadata signature of the type library represented by the specified `ITypeLib` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4b8a-104">语法</span><span class="sxs-lookup"><span data-stu-id="c4b8a-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaDataFromTypeLib (  
    [in]  ITypeLib        *pITL,
    [out] IMetaDataImport **ppMDI  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c4b8a-105">参数</span><span class="sxs-lookup"><span data-stu-id="c4b8a-105">Parameters</span></span>  

 `pITL`  
 <span data-ttu-id="c4b8a-106">中一个指针，指向 `ITypeLib` 表示类型库的对象。</span><span class="sxs-lookup"><span data-stu-id="c4b8a-106">[in] Pointer to an `ITypeLib` object that represents the type library.</span></span>  
  
 `ppMDI`  
 <span data-ttu-id="c4b8a-107">弄指向一个位置的指针，该位置接收 `IMetaDataImport` 表示元数据签名的实例的地址。</span><span class="sxs-lookup"><span data-stu-id="c4b8a-107">[out] Pointer to a location that receives the address of the `IMetaDataImport` instance that represents the metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4b8a-108">要求</span><span class="sxs-lookup"><span data-stu-id="c4b8a-108">Requirements</span></span>  

 <span data-ttu-id="c4b8a-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c4b8a-109">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4b8a-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c4b8a-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c4b8a-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c4b8a-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c4b8a-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4b8a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4b8a-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4b8a-113">See also</span></span>

- [<span data-ttu-id="c4b8a-114">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="c4b8a-114">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="c4b8a-115">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="c4b8a-115">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
