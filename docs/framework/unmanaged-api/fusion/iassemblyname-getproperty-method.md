---
title: IAssemblyName::GetProperty 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetProperty
helpviewer_keywords:
- IAssemblyName::GetProperty method [.NET Framework fusion]
- GetProperty method [.NET Framework fusion]
ms.assetid: e59fda62-77d5-4e37-89cb-ce7ae4627975
topic_type:
- apiref
ms.openlocfilehash: 3a6f19d9fc90972e767625fadf30cc4af50d9017
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727882"
---
# <a name="iassemblynamegetproperty-method"></a><span data-ttu-id="3cfbf-102">IAssemblyName::GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="3cfbf-102">IAssemblyName::GetProperty Method</span></span>

<span data-ttu-id="3cfbf-103">获取一个指针，该指针指向由指定的属性标识符引用的属性。</span><span class="sxs-lookup"><span data-stu-id="3cfbf-103">Gets a pointer to the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cfbf-104">语法</span><span class="sxs-lookup"><span data-stu-id="3cfbf-104">Syntax</span></span>  
  
```cpp  
HRESULT GetProperty (  
    [in]      DWORD    PropertyId,  
    [out]     LPVOID   pvProperty,  
    [in, out] LPDWORD  pcbProperty  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3cfbf-105">参数</span><span class="sxs-lookup"><span data-stu-id="3cfbf-105">Parameters</span></span>  

 `PropertyId`  
 <span data-ttu-id="3cfbf-106">中请求的属性的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3cfbf-106">[in] The unique identifier for the requested property.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="3cfbf-107">弄返回的属性数据。</span><span class="sxs-lookup"><span data-stu-id="3cfbf-107">[out] The returned property data.</span></span>  
  
 `pcbProperty`  
 <span data-ttu-id="3cfbf-108">[in，out]的大小（以字节为单位） `pvProperty` 。</span><span class="sxs-lookup"><span data-stu-id="3cfbf-108">[in, out] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3cfbf-109">要求</span><span class="sxs-lookup"><span data-stu-id="3cfbf-109">Requirements</span></span>  

 <span data-ttu-id="3cfbf-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3cfbf-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3cfbf-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="3cfbf-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="3cfbf-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3cfbf-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3cfbf-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3cfbf-113">See also</span></span>

- [<span data-ttu-id="3cfbf-114">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="3cfbf-114">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
