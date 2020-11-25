---
title: ICorPublishEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorPublishEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum::Clone
helpviewer_keywords:
- Clone method, ICorPublishEnum interface [.NET Framework debugging]
- ICorPublishEnum::Clone method [.NET Framework debugging]
ms.assetid: c9a26ea3-b8eb-4b8e-854f-9a2ca26b3b39
topic_type:
- apiref
ms.openlocfilehash: 44ecba99999d04603477f411e68834548f6a7cda
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95693536"
---
# <a name="icorpublishenumclone-method"></a><span data-ttu-id="be034-102">ICorPublishEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="be034-102">ICorPublishEnum::Clone Method</span></span>

<span data-ttu-id="be034-103">创建此 [ICorPublishEnum](icorpublishenum-interface.md) 对象的副本。</span><span class="sxs-lookup"><span data-stu-id="be034-103">Creates a copy of this [ICorPublishEnum](icorpublishenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be034-104">语法</span><span class="sxs-lookup"><span data-stu-id="be034-104">Syntax</span></span>  
  
```cpp  
HRESULT Clone (  
    [out] ICorPublishEnum   **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="be034-105">参数</span><span class="sxs-lookup"><span data-stu-id="be034-105">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="be034-106">弄指向作为 `ICorPublishEnum` 此对象副本的对象地址的指针 `ICorPublishEnum` 。</span><span class="sxs-lookup"><span data-stu-id="be034-106">[out] A pointer to the address of an `ICorPublishEnum` object that is a copy of this `ICorPublishEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be034-107">要求</span><span class="sxs-lookup"><span data-stu-id="be034-107">Requirements</span></span>  

 <span data-ttu-id="be034-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="be034-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be034-109">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="be034-109">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="be034-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="be034-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="be034-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be034-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be034-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be034-112">See also</span></span>

- [<span data-ttu-id="be034-113">ICorPublishEnum 接口</span><span class="sxs-lookup"><span data-stu-id="be034-113">ICorPublishEnum Interface</span></span>](icorpublishenum-interface.md)
