---
title: IMetaDataEmit::DefinePinvokeMap 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefinePinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefinePinvokeMap
helpviewer_keywords:
- DefinePinvokeMap method [.NET Framework metadata]
- IMetaDataEmit::DefinePinvokeMap method [.NET Framework metadata]
ms.assetid: 03abf921-5154-4070-88fa-10b7092901fb
topic_type:
- apiref
ms.openlocfilehash: b46d39ab3958227c1fca24ceb3a9934f2778aa2c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719497"
---
# <a name="imetadataemitdefinepinvokemap-method"></a><span data-ttu-id="bb5a1-102">IMetaDataEmit::DefinePinvokeMap 方法</span><span class="sxs-lookup"><span data-stu-id="bb5a1-102">IMetaDataEmit::DefinePinvokeMap Method</span></span>

<span data-ttu-id="bb5a1-103">设置指定的标记所引用的方法的 PInvoke 签名功能。</span><span class="sxs-lookup"><span data-stu-id="bb5a1-103">Sets features of the PInvoke signature of the method referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb5a1-104">语法</span><span class="sxs-lookup"><span data-stu-id="bb5a1-104">Syntax</span></span>  
  
```cpp  
HRESULT DefinePinvokeMap (
    [in]  mdToken            tk,
    [in]  DWORD              dwMappingFlags,
    [in]  LPCWSTR            szImportName,
    [in]  mdModuleRef        mrImportDLL
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb5a1-105">参数</span><span class="sxs-lookup"><span data-stu-id="bb5a1-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="bb5a1-106">中目标方法的标记。</span><span class="sxs-lookup"><span data-stu-id="bb5a1-106">[in] The token for the target method.</span></span>  
  
 `dwMappingFlags`  
 <span data-ttu-id="bb5a1-107">中PInvoke 用来执行映射的标志。</span><span class="sxs-lookup"><span data-stu-id="bb5a1-107">[in] Flags used by PInvoke to do the mapping.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="bb5a1-108">中非托管 DLL 中目标导出方法的名称。</span><span class="sxs-lookup"><span data-stu-id="bb5a1-108">[in] The name of the target export method in an unmanaged DLL.</span></span>  
  
 `mrImportDLL`  
 <span data-ttu-id="bb5a1-109">中目标本机 DLL 的标记。</span><span class="sxs-lookup"><span data-stu-id="bb5a1-109">[in] The token for the target native DLL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb5a1-110">要求</span><span class="sxs-lookup"><span data-stu-id="bb5a1-110">Requirements</span></span>  

 <span data-ttu-id="bb5a1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb5a1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb5a1-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="bb5a1-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bb5a1-113">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="bb5a1-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bb5a1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb5a1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb5a1-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb5a1-115">See also</span></span>

- [<span data-ttu-id="bb5a1-116">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="bb5a1-116">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="bb5a1-117">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="bb5a1-117">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
