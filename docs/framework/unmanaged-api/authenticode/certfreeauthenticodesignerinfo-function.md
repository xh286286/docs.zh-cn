---
title: CertFreeAuthenticodeSignerInfo 函数
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeSignerInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 8029633c-b6e4-4665-a7c2-89607c3247ef
ms.openlocfilehash: dc6bb5a137a50ec07f89f292e5d9beac4349c3c7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95674172"
---
# <a name="certfreeauthenticodesignerinfo-function"></a><span data-ttu-id="8ebdb-102">CertFreeAuthenticodeSignerInfo 函数</span><span class="sxs-lookup"><span data-stu-id="8ebdb-102">CertFreeAuthenticodeSignerInfo Function</span></span>

<span data-ttu-id="8ebdb-103">释放为 [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) 结构分配的资源。</span><span class="sxs-lookup"><span data-stu-id="8ebdb-103">Frees resources allocated for the [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ebdb-104">语法</span><span class="sxs-lookup"><span data-stu-id="8ebdb-104">Syntax</span></span>  
  
```cpp  
HRESULT CertFreeAuthenticodeSignerInfo (  
    [in, out]  PAXL_AUTHENTICODE_SIGNER_INFO   pSignerInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8ebdb-105">参数</span><span class="sxs-lookup"><span data-stu-id="8ebdb-105">Parameters</span></span>  

 `pSignerInfo`  
 <span data-ttu-id="8ebdb-106">[in, out] 要释放的签署人信息。</span><span class="sxs-lookup"><span data-stu-id="8ebdb-106">[in, out] Signer information to be released.</span></span> <span data-ttu-id="8ebdb-107">请参阅 [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) 结构。</span><span class="sxs-lookup"><span data-stu-id="8ebdb-107">See the [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8ebdb-108">返回值</span><span class="sxs-lookup"><span data-stu-id="8ebdb-108">Return Value</span></span>  

 <span data-ttu-id="8ebdb-109">如果此函数成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="8ebdb-109">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="8ebdb-110">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="8ebdb-110">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ebdb-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ebdb-111">See also</span></span>

- [<span data-ttu-id="8ebdb-112">验证码</span><span class="sxs-lookup"><span data-stu-id="8ebdb-112">Authenticode</span></span>](index.md)
