---
title: IMetaDataTables2::GetMetaDataStreamInfo 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables2.GetMetaDataStreamInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables2::GetMetaDataStreamInfo
helpviewer_keywords:
- GetMetaDataStreamInfo method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStreamInfo method [.NET Framework metadata]
ms.assetid: 8b280627-cc74-4789-95da-1fefc966de05
topic_type:
- apiref
ms.openlocfilehash: 21fc79f62dba4b16a7a067dff8fb9dcc795c9d35
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708720"
---
# <a name="imetadatatables2getmetadatastreaminfo-method"></a><span data-ttu-id="26f1c-102">IMetaDataTables2::GetMetaDataStreamInfo 方法</span><span class="sxs-lookup"><span data-stu-id="26f1c-102">IMetaDataTables2::GetMetaDataStreamInfo Method</span></span>

<span data-ttu-id="26f1c-103">获取指定索引处的元数据流的名称、大小和内容。</span><span class="sxs-lookup"><span data-stu-id="26f1c-103">Gets the name, size, and contents of the metadata stream at the specified index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26f1c-104">语法</span><span class="sxs-lookup"><span data-stu-id="26f1c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaDataStreamInfo (  
   [in]  ULONG        ix,  
   [out] const char   **ppchName,  
   [out] const void   **ppv,  
   [out] ULONG        *pcb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="26f1c-105">参数</span><span class="sxs-lookup"><span data-stu-id="26f1c-105">Parameters</span></span>  

 `ix`  
 <span data-ttu-id="26f1c-106">中请求的元数据流的索引。</span><span class="sxs-lookup"><span data-stu-id="26f1c-106">[in] The index of the requested metadata stream.</span></span>  
  
 `ppchName`  
 <span data-ttu-id="26f1c-107">弄指向流名称的指针。</span><span class="sxs-lookup"><span data-stu-id="26f1c-107">[out] A pointer to the name of the stream.</span></span>  
  
 `ppv`  
 <span data-ttu-id="26f1c-108">弄指向元数据流的指针。</span><span class="sxs-lookup"><span data-stu-id="26f1c-108">[out] A pointer to the metadata stream.</span></span>  
  
 `pcb`  
 <span data-ttu-id="26f1c-109">弄的大小（以字节为单位） `ppv` 。</span><span class="sxs-lookup"><span data-stu-id="26f1c-109">[out] The size, in bytes, of `ppv`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26f1c-110">要求</span><span class="sxs-lookup"><span data-stu-id="26f1c-110">Requirements</span></span>  

 <span data-ttu-id="26f1c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26f1c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26f1c-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="26f1c-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="26f1c-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="26f1c-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="26f1c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26f1c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26f1c-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26f1c-115">See also</span></span>

- [<span data-ttu-id="26f1c-116">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="26f1c-116">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
- [<span data-ttu-id="26f1c-117">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="26f1c-117">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
