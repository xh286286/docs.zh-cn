---
title: IMetaDataImport::GetFieldMarshal 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetFieldMarshal
helpviewer_keywords:
- GetFieldMarshal method [.NET Framework metadata]
- IMetaDataImport::GetFieldMarshal method [.NET Framework metadata]
ms.assetid: 4e2d88c6-8a3a-4fbe-900b-b4f4c06bf6bf
topic_type:
- apiref
ms.openlocfilehash: 35f73135dbeea1c79d15e0a9e9367c5d533487ce
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95676851"
---
# <a name="imetadataimportgetfieldmarshal-method"></a><span data-ttu-id="a91c2-102">IMetaDataImport::GetFieldMarshal 方法</span><span class="sxs-lookup"><span data-stu-id="a91c2-102">IMetaDataImport::GetFieldMarshal Method</span></span>

<span data-ttu-id="a91c2-103">获取一个指针，该指针指向由指定的字段元数据标记表示的字段的本机非托管类型。</span><span class="sxs-lookup"><span data-stu-id="a91c2-103">Gets a pointer to the native, unmanaged type of the field represented by the specified field metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a91c2-104">语法</span><span class="sxs-lookup"><span data-stu-id="a91c2-104">Syntax</span></span>  
  
```cpp  
HRESULT GetFieldMarshal (  
   [in]  mdToken             tk,
   [out] PCCOR_SIGNATURE     *ppvNativeType,  
   [out] ULONG               *pcbNativeType
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a91c2-105">参数</span><span class="sxs-lookup"><span data-stu-id="a91c2-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="a91c2-106">中表示要为其获取互操作封送处理信息的字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="a91c2-106">[in] The metadata token that represents the field to get interop marshaling information for.</span></span>  
  
 `ppvNativeType`  
 <span data-ttu-id="a91c2-107">弄指向字段本地类型的元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="a91c2-107">[out] A pointer to the metadata signature of the field's native type.</span></span>  
  
 `pcbNativeType`  
 <span data-ttu-id="a91c2-108">弄的大小（以字节为单位） `ppvNativeType` 。</span><span class="sxs-lookup"><span data-stu-id="a91c2-108">[out] The size in bytes of `ppvNativeType`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a91c2-109">要求</span><span class="sxs-lookup"><span data-stu-id="a91c2-109">Requirements</span></span>  

 <span data-ttu-id="a91c2-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a91c2-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a91c2-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a91c2-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a91c2-112">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a91c2-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a91c2-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a91c2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a91c2-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a91c2-114">See also</span></span>

- [<span data-ttu-id="a91c2-115">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="a91c2-115">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="a91c2-116">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="a91c2-116">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
