---
title: IMetaDataValidate::ValidatorInit 方法
ms.date: 03/30/2017
api_name:
- IMetaDataValidate.ValidatorInit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataValidate::ValidatorInit
helpviewer_keywords:
- IMetaDataValidate::ValidatorInit method [.NET Framework metadata]
- ValidatorInit method [.NET Framework metadata]
ms.assetid: 6bafd75a-e2d0-4aea-aed1-074374d5dff6
topic_type:
- apiref
ms.openlocfilehash: e2f54e11906cd4ba1440e220530f2ca5b9de769f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708551"
---
# <a name="imetadatavalidatevalidatorinit-method"></a><span data-ttu-id="9712c-102">IMetaDataValidate::ValidatorInit 方法</span><span class="sxs-lookup"><span data-stu-id="9712c-102">IMetaDataValidate::ValidatorInit Method</span></span>

<span data-ttu-id="9712c-103">设置一个标志，该标志指定当前元数据范围内的模块类型，并注册验证错误的指定回调方法。</span><span class="sxs-lookup"><span data-stu-id="9712c-103">Sets a flag that specifies the type of the module in the current metadata scope, and registers the specified callback method for validation errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9712c-104">语法</span><span class="sxs-lookup"><span data-stu-id="9712c-104">Syntax</span></span>  
  
```cpp  
HRESULT ValidatorInit (  
   [in] DWORD       dwModuleType,  
   [in] IUnknown    *pUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9712c-105">参数</span><span class="sxs-lookup"><span data-stu-id="9712c-105">Parameters</span></span>  

 `dwModule`  
 <span data-ttu-id="9712c-106">中 [CorValidatorModuleType](corvalidatormoduletype-enumeration.md) 枚举的一个值，该值指定当前元数据范围内的模块的类型。</span><span class="sxs-lookup"><span data-stu-id="9712c-106">[in] A value of the [CorValidatorModuleType](corvalidatormoduletype-enumeration.md) enumeration that specifies the type of the module in the current metadata scope.</span></span>  
  
 `pUnk`  
 <span data-ttu-id="9712c-107">中指向 [IUnknown](/cpp/atl/iunknown) 实例的指针，该实例用作验证错误的函数回调。</span><span class="sxs-lookup"><span data-stu-id="9712c-107">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) instance that serves as a function callback for validation errors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9712c-108">要求</span><span class="sxs-lookup"><span data-stu-id="9712c-108">Requirements</span></span>  

 <span data-ttu-id="9712c-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9712c-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9712c-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9712c-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9712c-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9712c-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9712c-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9712c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9712c-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9712c-113">See also</span></span>

- [<span data-ttu-id="9712c-114">IMetaDataValidate 接口</span><span class="sxs-lookup"><span data-stu-id="9712c-114">IMetaDataValidate Interface</span></span>](imetadatavalidate-interface.md)
