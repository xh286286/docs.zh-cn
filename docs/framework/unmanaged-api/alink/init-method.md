---
title: Init 方法
ms.date: 03/30/2017
api_name:
- IALink.Init
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- Init
helpviewer_keywords:
- Init method
ms.assetid: e48b5c64-049f-4f93-ad87-d07ae9cd5845
topic_type:
- apiref
ms.openlocfilehash: 25a1c29ab94a785304b83d5b1bcb2d7176742a68
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726013"
---
# <a name="init-method"></a><span data-ttu-id="e5b3b-102">Init 方法</span><span class="sxs-lookup"><span data-stu-id="e5b3b-102">Init Method</span></span>

<span data-ttu-id="e5b3b-103">准备实现 [IALink 接口](ialink-interface.md) 以便使用的对象。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-103">Prepares objects implementing the [IALink Interface](ialink-interface.md) for use.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5b3b-104">语法</span><span class="sxs-lookup"><span data-stu-id="e5b3b-104">Syntax</span></span>  
  
```cpp  
HRESULT Init(  
    IMetaDataDispenserEx* pDispenser,  
    IMetaDataError* pErrorHandler  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="e5b3b-105">参数</span><span class="sxs-lookup"><span data-stu-id="e5b3b-105">Parameters</span></span>  

 `pDispenser`  
 <span data-ttu-id="e5b3b-106">指向元数据分配器的[IMetaDataDispenserEx 接口](../metadata/imetadatadispenserex-interface.md)指针。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-106">[IMetaDataDispenserEx Interface](../metadata/imetadatadispenserex-interface.md) pointer to the metadata dispenser.</span></span>  
  
 `pErrorHandler`  
 <span data-ttu-id="e5b3b-107">指向可选错误处理接口的[IMetaDataError 接口](../metadata/imetadataerror-interface.md)指针。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-107">[IMetaDataError Interface](../metadata/imetadataerror-interface.md) pointer to an optional error handling interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e5b3b-108">返回值</span><span class="sxs-lookup"><span data-stu-id="e5b3b-108">Return Value</span></span>  

 <span data-ttu-id="e5b3b-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5b3b-110">要求</span><span class="sxs-lookup"><span data-stu-id="e5b3b-110">Requirements</span></span>  

 <span data-ttu-id="e5b3b-111">需要 alink</span><span class="sxs-lookup"><span data-stu-id="e5b3b-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5b3b-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e5b3b-112">See also</span></span>

- [<span data-ttu-id="e5b3b-113">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="e5b3b-113">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="e5b3b-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="e5b3b-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="e5b3b-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="e5b3b-115">ALink API</span></span>](index.md)
