---
title: IInstallReferenceItem::GetReference 方法
ms.date: 03/30/2017
api_name:
- IInstallReferenceItem.GetReference
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceItem::GetReference
helpviewer_keywords:
- IInstallReferenceItem::GetReference method [.NET Framework fusion]
- GetReference method [.NET Framework fusion]
ms.assetid: 8960332f-c98a-405a-ba92-7003de0c1187
topic_type:
- apiref
ms.openlocfilehash: 14286970a4f7093d72b47b780ea880f5ccb1bca5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721067"
---
# <a name="iinstallreferenceitemgetreference-method"></a><span data-ttu-id="24cce-102">IInstallReferenceItem::GetReference 方法</span><span class="sxs-lookup"><span data-stu-id="24cce-102">IInstallReferenceItem::GetReference Method</span></span>

<span data-ttu-id="24cce-103">获取一个指针，该指针指向此[IInstallReferenceItem](iinstallreferenceitem-interface.md)对象表示的[FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md)结构。</span><span class="sxs-lookup"><span data-stu-id="24cce-103">Gets a pointer to the [FUSION_INSTALL_REFERENCE](fusion-install-reference-structure.md) structure represented by this [IInstallReferenceItem](iinstallreferenceitem-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24cce-104">语法</span><span class="sxs-lookup"><span data-stu-id="24cce-104">Syntax</span></span>  
  
```cpp  
HRESULT GetReference (  
    [out] LPFUSION_INSTALL_REFERENCE *ppRefData,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="24cce-105">参数</span><span class="sxs-lookup"><span data-stu-id="24cce-105">Parameters</span></span>  

 `ppRefData`  
 <span data-ttu-id="24cce-106">弄返回的 `FUSION_INSTALL_REFERENCE` 指针。</span><span class="sxs-lookup"><span data-stu-id="24cce-106">[out] The returned `FUSION_INSTALL_REFERENCE` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="24cce-107">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="24cce-107">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="24cce-108">`dwFlags` 必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="24cce-108">`dwFlags` must be 0 (zero).</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="24cce-109">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="24cce-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="24cce-110">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="24cce-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24cce-111">要求</span><span class="sxs-lookup"><span data-stu-id="24cce-111">Requirements</span></span>  

 <span data-ttu-id="24cce-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24cce-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24cce-113">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="24cce-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="24cce-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24cce-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24cce-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24cce-115">See also</span></span>

- [<span data-ttu-id="24cce-116">IInstallReferenceItem 接口</span><span class="sxs-lookup"><span data-stu-id="24cce-116">IInstallReferenceItem Interface</span></span>](iinstallreferenceitem-interface.md)
- [<span data-ttu-id="24cce-117">FUSION_INSTALL_REFERENCE 结构</span><span class="sxs-lookup"><span data-stu-id="24cce-117">FUSION_INSTALL_REFERENCE Structure</span></span>](fusion-install-reference-structure.md)
