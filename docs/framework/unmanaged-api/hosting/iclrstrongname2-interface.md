---
title: ICLRStrongName2 接口
ms.date: 03/30/2017
api_name:
- ICLRStrongName2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName2
helpviewer_keywords:
- ICLRStrongName2 interface [.NET Framework hosting]
ms.assetid: 9f098a74-201e-4628-a468-8dee9ab99b4a
topic_type:
- apiref
ms.openlocfilehash: df570f32d694ec21e9642e75b4965e169afaccfc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677643"
---
# <a name="iclrstrongname2-interface"></a><span data-ttu-id="058e1-102">ICLRStrongName2 接口</span><span class="sxs-lookup"><span data-stu-id="058e1-102">ICLRStrongName2 Interface</span></span>

<span data-ttu-id="058e1-103">提供使用 SHA-256、SHA-384 和 SHA-512)  (sha-1 安全哈希算法组创建强名称的功能。</span><span class="sxs-lookup"><span data-stu-id="058e1-103">Provides the ability to create strong names using the SHA-2 group of Secure Hash Algorithms (SHA-256, SHA-384, and SHA-512).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="058e1-104">方法</span><span class="sxs-lookup"><span data-stu-id="058e1-104">Methods</span></span>  
  
|<span data-ttu-id="058e1-105">方法</span><span class="sxs-lookup"><span data-stu-id="058e1-105">Method</span></span>|<span data-ttu-id="058e1-106">说明</span><span class="sxs-lookup"><span data-stu-id="058e1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="058e1-107">StrongNameGetPublicKeyEx 方法</span><span class="sxs-lookup"><span data-stu-id="058e1-107">StrongNameGetPublicKeyEx Method</span></span>](strongnamegetpublickeyex-method.md)|<span data-ttu-id="058e1-108">获取公钥/私钥对中的公钥，并指定哈希算法和签名算法。</span><span class="sxs-lookup"><span data-stu-id="058e1-108">Gets the public key from a public/private key pair, and specifies a hash algorithm and a signature algorithm.</span></span>|  
|[<span data-ttu-id="058e1-109">StrongNameSignatureVerificationEx2 方法</span><span class="sxs-lookup"><span data-stu-id="058e1-109">StrongNameSignatureVerificationEx2 Method</span></span>](strongnamesignatureverificationex2-method.md)|<span data-ttu-id="058e1-110">验证强名称程序集的签名，并提供从 ECMA 密钥到实际密钥的映射。</span><span class="sxs-lookup"><span data-stu-id="058e1-110">Verifies the signature of a strongly named assembly, and provides a mapping from the ECMA key to a real key.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="058e1-111">备注</span><span class="sxs-lookup"><span data-stu-id="058e1-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="058e1-112">要求</span><span class="sxs-lookup"><span data-stu-id="058e1-112">Requirements</span></span>  

 <span data-ttu-id="058e1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="058e1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="058e1-114">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="058e1-114">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="058e1-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="058e1-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="058e1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="058e1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>
