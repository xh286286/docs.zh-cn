---
title: StrongNameSignatureVerificationEx2 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName2.StrongNameSignatureVerificationEx2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StrongNameSignatureVerificationEx2
helpviewer_keywords:
- StrongNameSignatureVerificationEx2 method, ICLRStrongName2 interface [.NET Framework hosting]
- ICLRStrongName2::StrongNameSignatureVerificationEx2 method [.NET Framework hosting]
ms.assetid: dfd4133f-a074-4db3-a7ee-4f250fe9ad3a
topic_type:
- apiref
ms.openlocfilehash: 423f6ee91d79a9e668de29d2e9e9a09a2bb779d4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729871"
---
# <a name="strongnamesignatureverificationex2-method"></a><span data-ttu-id="0414b-102">StrongNameSignatureVerificationEx2 方法</span><span class="sxs-lookup"><span data-stu-id="0414b-102">StrongNameSignatureVerificationEx2 Method</span></span>

<span data-ttu-id="0414b-103">验证强名称程序集的签名，并提供从 ECMA 密钥到实际密钥的映射。</span><span class="sxs-lookup"><span data-stu-id="0414b-103">Verifies the signature of a strongly named assembly, and provides a mapping from the ECMA key to a real key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0414b-104">语法</span><span class="sxs-lookup"><span data-stu-id="0414b-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameSignatureVerificationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  BOOLEAN   fForceVerification,    [in]  BYTE      *pbEcmaPublicKey,  
    [in]  DWORD     cbEcmaPublicKey,  
    [out] BOOLEAN   *pfWasVerified  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0414b-105">参数</span><span class="sxs-lookup"><span data-stu-id="0414b-105">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="0414b-106">中要验证的程序集的可移植可执行文件的路径 ( .exe 或 .dll) 文件。</span><span class="sxs-lookup"><span data-stu-id="0414b-106">[in] The path to the portable executable (.exe or .dll) file for the assembly to be verified.</span></span>  
  
 `fForceVerification`  
 <span data-ttu-id="0414b-107">[in] `true` 若要执行验证，即使需要重写注册表设置，否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="0414b-107">[in] `true` to perform verification, even if it is necessary to override registry settings; otherwise, `false`.</span></span>  
  
 `pbEcmaPublicKey`  
 <span data-ttu-id="0414b-108">中一个指针，指向用于验证的从 ECMA 公钥到实际密钥的映射。</span><span class="sxs-lookup"><span data-stu-id="0414b-108">[in] A pointer to the mapping from the ECMA public key to the real key used for verification.</span></span>  
  
 `cbEcmaPublicKey`  
 <span data-ttu-id="0414b-109">中实际 ECMA 公钥的长度。</span><span class="sxs-lookup"><span data-stu-id="0414b-109">[in] The length of the real ECMA public key.</span></span>  
  
 `pfWasVerified`  
 <span data-ttu-id="0414b-110">[out] `true` 如果验证了强名称签名，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="0414b-110">[out] `true` if the strong name signature was verified; otherwise, `false`.</span></span> <span data-ttu-id="0414b-111">`false`如果验证因为注册表设置而成功，则也将此参数设置为。</span><span class="sxs-lookup"><span data-stu-id="0414b-111">This parameter is also set to `false` if the verification was successful due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0414b-112">返回值</span><span class="sxs-lookup"><span data-stu-id="0414b-112">Return Value</span></span>  

 <span data-ttu-id="0414b-113">`S_OK` 如果验证成功，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="0414b-113">`S_OK` if the verification was successful; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0414b-114">要求</span><span class="sxs-lookup"><span data-stu-id="0414b-114">Requirements</span></span>  

 <span data-ttu-id="0414b-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0414b-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0414b-116">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="0414b-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="0414b-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0414b-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0414b-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0414b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0414b-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0414b-119">See also</span></span>

- [<span data-ttu-id="0414b-120">StrongNameSignatureVerification 方法</span><span class="sxs-lookup"><span data-stu-id="0414b-120">StrongNameSignatureVerification Method</span></span>](iclrstrongname-strongnamesignatureverification-method.md)
- [<span data-ttu-id="0414b-121">StrongNameSignatureVerificationEx 方法</span><span class="sxs-lookup"><span data-stu-id="0414b-121">StrongNameSignatureVerificationEx Method</span></span>](iclrstrongname-strongnamesignatureverificationex-method.md)
- [<span data-ttu-id="0414b-122">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="0414b-122">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
