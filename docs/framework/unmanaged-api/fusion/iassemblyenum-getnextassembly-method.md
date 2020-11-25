---
title: IAssemblyEnum::GetNextAssembly 方法
ms.date: 03/30/2017
api_name:
- IAssemblyEnum.GetNextAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyEnum::GetNextAssembly
helpviewer_keywords:
- GetNextAssembly method [.NET Framework fusion]
- IAssemblyEnum::GetNextAssembly method [.NET Framework fusion]
ms.assetid: 5d7a4ca2-5f46-4ef1-a9a2-257884e9dc11
topic_type:
- apiref
ms.openlocfilehash: af43d9cf4d5aa790036a13d060fc6ccf113f335d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719887"
---
# <a name="iassemblyenumgetnextassembly-method"></a><span data-ttu-id="a93af-102">IAssemblyEnum::GetNextAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="a93af-102">IAssemblyEnum::GetNextAssembly Method</span></span>

<span data-ttu-id="a93af-103">获取一个指针，该指针指向此[IAssemblyEnum](iassemblyenum-interface.md)对象中包含的下一个[IAssemblyName](iassemblyname-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="a93af-103">Gets a pointer to the next [IAssemblyName](iassemblyname-interface.md) contained in this [IAssemblyEnum](iassemblyenum-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a93af-104">语法</span><span class="sxs-lookup"><span data-stu-id="a93af-104">Syntax</span></span>  
  
```cpp  
HRESULT GetNextAssembly (  
    [in]  LPVOID          pvReserved,  
    [out] IAssemblyName   **ppName,  
    [in]  DWORD           dwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a93af-105">参数</span><span class="sxs-lookup"><span data-stu-id="a93af-105">Parameters</span></span>  

 `pvReserved`  
 <span data-ttu-id="a93af-106">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="a93af-106">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="a93af-107">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="a93af-107">`pvReserved` must be a null reference.</span></span>  
  
 `ppName`  
 <span data-ttu-id="a93af-108">弄返回的 `IAssemblyName` 指针。</span><span class="sxs-lookup"><span data-stu-id="a93af-108">[out] The returned `IAssemblyName` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="a93af-109">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="a93af-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="a93af-110">`dwFlags` 必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="a93af-110">`dwFlags` must be 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a93af-111">要求</span><span class="sxs-lookup"><span data-stu-id="a93af-111">Requirements</span></span>  

 <span data-ttu-id="a93af-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a93af-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a93af-113">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="a93af-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a93af-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a93af-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a93af-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a93af-115">See also</span></span>

- [<span data-ttu-id="a93af-116">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="a93af-116">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="a93af-117">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="a93af-117">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)
