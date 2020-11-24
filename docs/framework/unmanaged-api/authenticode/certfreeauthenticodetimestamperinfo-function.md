---
title: CertFreeAuthenticodeTimestamperInfo 函数
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeTimestamperInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 3eb14c49-68c2-4516-ac89-e5bd7473831c
ms.openlocfilehash: 1ef71b14faf66c179030dff2a7d953e27463c1f7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95674159"
---
# <a name="certfreeauthenticodetimestamperinfo-function"></a><span data-ttu-id="d1f00-102">CertFreeAuthenticodeTimestamperInfo 函数</span><span class="sxs-lookup"><span data-stu-id="d1f00-102">CertFreeAuthenticodeTimestamperInfo Function</span></span>

<span data-ttu-id="d1f00-103">释放为 [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) 结构分配的资源。</span><span class="sxs-lookup"><span data-stu-id="d1f00-103">Frees resources allocated for the [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1f00-104">语法</span><span class="sxs-lookup"><span data-stu-id="d1f00-104">Syntax</span></span>  
  
```cpp  
HRESULT CertFreeAuthenticodeTimestamperInfo (  
    [in, out]  PAXL_AUTHENTICODE_TIMESTAMPER_INFO   pTimestamperInfo  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d1f00-105">参数</span><span class="sxs-lookup"><span data-stu-id="d1f00-105">Parameters</span></span>  

 `pTimestamperInfo`  
 <span data-ttu-id="d1f00-106">[in, out] 要释放的时间戳签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="d1f00-106">[in, out] The time stamper information to be released.</span></span> <span data-ttu-id="d1f00-107">请参阅 [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) 结构。</span><span class="sxs-lookup"><span data-stu-id="d1f00-107">See the [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) structure.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d1f00-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d1f00-108">Return Value</span></span>  

 <span data-ttu-id="d1f00-109">如果此函数成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="d1f00-109">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="d1f00-110">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="d1f00-110">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1f00-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1f00-111">See also</span></span>

- [<span data-ttu-id="d1f00-112">验证码</span><span class="sxs-lookup"><span data-stu-id="d1f00-112">Authenticode</span></span>](index.md)
