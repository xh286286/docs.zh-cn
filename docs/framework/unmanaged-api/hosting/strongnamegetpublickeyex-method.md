---
title: StrongNameGetPublicKeyEx 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName2.StrongNameGetPublicKeyEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StrongNameGetPublicKeyEx
helpviewer_keywords:
- StrongNameGetPublicKeyEx method, ICLRStrongName2 interface [.NET Framework hosting]
- ICLRStrongName2::StrongNameGetPublicKeyEx method [.NET Framework hosting]
ms.assetid: 63d8260c-fb32-4f8f-a357-768afd570f68
topic_type:
- apiref
ms.openlocfilehash: 8cc28d9ccd40c65d225a96b269562c9d3dfa2124
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729884"
---
# <a name="strongnamegetpublickeyex-method"></a><span data-ttu-id="f2626-102">StrongNameGetPublicKeyEx 方法</span><span class="sxs-lookup"><span data-stu-id="f2626-102">StrongNameGetPublicKeyEx Method</span></span>

<span data-ttu-id="f2626-103">获取公钥/私钥对中的公钥，并指定哈希算法和签名算法。</span><span class="sxs-lookup"><span data-stu-id="f2626-103">Gets the public key from a public/private key pair, and specifies a hash algorithm and a signature algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2626-104">语法</span><span class="sxs-lookup"><span data-stu-id="f2626-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameGetPublicKey (
    [in]  LPCWSTR   pwzKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
    [in]  ULONG     uHashAlgId,  
    [in]  ULONG     uReserved,  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2626-105">参数</span><span class="sxs-lookup"><span data-stu-id="f2626-105">Parameters</span></span>  

 `pwzKeyContainer`  
 <span data-ttu-id="f2626-106">中包含公钥/私钥对的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="f2626-106">[in] The name of the key container that contains the public/private key pair.</span></span> <span data-ttu-id="f2626-107">如果 `pbKeyBlob` 为 null，则 `szKeyContainer` 必须在加密服务提供程序 (CSP) 中指定有效容器。</span><span class="sxs-lookup"><span data-stu-id="f2626-107">If `pbKeyBlob` is null, `szKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="f2626-108">在这种情况下，该 `StrongNameGetPublicKeyEx` 方法将从存储在容器中的密钥对中提取公钥。</span><span class="sxs-lookup"><span data-stu-id="f2626-108">In this case, the `StrongNameGetPublicKeyEx` method extracts the public key from the key pair stored in the container.</span></span>  
  
 <span data-ttu-id="f2626-109">如果不为 `pbKeyBlob` null，则假定密钥对包含在关键的二进制大型对象 (BLOB) 中。</span><span class="sxs-lookup"><span data-stu-id="f2626-109">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 <span data-ttu-id="f2626-110">密钥必须是1024位 Rivest-Rivest-shamir-adleman (RSA) 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="f2626-110">The keys must be 1024-bit Rivest-Shamir-Adleman (RSA) signing keys.</span></span> <span data-ttu-id="f2626-111">此时不支持其他类型的密钥。</span><span class="sxs-lookup"><span data-stu-id="f2626-111">No other types of keys are supported at this time.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="f2626-112">中指向公钥/私钥对的指针。</span><span class="sxs-lookup"><span data-stu-id="f2626-112">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="f2626-113">此对采用 Win32 函数创建的格式 `CryptExportKey` 。</span><span class="sxs-lookup"><span data-stu-id="f2626-113">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="f2626-114">如果 `pbKeyBlob` 为 null，则假定指定的密钥容器 `szKeyContainer` 包含密钥对。</span><span class="sxs-lookup"><span data-stu-id="f2626-114">If `pbKeyBlob` is null, the key container specified by `szKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="f2626-115">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="f2626-115">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="f2626-116">弄返回的公钥 BLOB。</span><span class="sxs-lookup"><span data-stu-id="f2626-116">[out] The returned public key BLOB.</span></span> <span data-ttu-id="f2626-117">`ppbPublicKeyBlob`参数由公共语言运行时分配并返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="f2626-117">The `ppbPublicKeyBlob` parameter is allocated by the common language runtime and returned to the caller.</span></span> <span data-ttu-id="f2626-118">调用方必须使用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法释放内存。</span><span class="sxs-lookup"><span data-stu-id="f2626-118">The caller must free the memory by using the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="f2626-119">弄返回的公钥 BLOB 的大小。</span><span class="sxs-lookup"><span data-stu-id="f2626-119">[out] The size of the returned public key BLOB.</span></span>  
  
 `uHashAlgId`  
 <span data-ttu-id="f2626-120">中程序集哈希算法。</span><span class="sxs-lookup"><span data-stu-id="f2626-120">[in] The assembly hash algorithm.</span></span> <span data-ttu-id="f2626-121">有关接受值的列表，请参阅 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="f2626-121">See the Remarks section for a list of accepted values.</span></span>  
  
 `uReserved`  
 <span data-ttu-id="f2626-122">中保留以供将来使用;默认值为 null。</span><span class="sxs-lookup"><span data-stu-id="f2626-122">[in] Reserved for future use; defaults to null.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f2626-123">返回值</span><span class="sxs-lookup"><span data-stu-id="f2626-123">Return Value</span></span>  

 <span data-ttu-id="f2626-124">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="f2626-124">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f2626-125">注解</span><span class="sxs-lookup"><span data-stu-id="f2626-125">Remarks</span></span>  

 <span data-ttu-id="f2626-126">公钥包含在 [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) 结构中。</span><span class="sxs-lookup"><span data-stu-id="f2626-126">The public key is contained in a [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f2626-127">注解</span><span class="sxs-lookup"><span data-stu-id="f2626-127">Remarks</span></span>  

 <span data-ttu-id="f2626-128">下表显示了该参数的接受值集 `uHashAlgId` 。</span><span class="sxs-lookup"><span data-stu-id="f2626-128">The following table shows the set of accepted values for the `uHashAlgId` parameter.</span></span>  
  
|<span data-ttu-id="f2626-129">名称</span><span class="sxs-lookup"><span data-stu-id="f2626-129">Name</span></span>|<span data-ttu-id="f2626-130">Value</span><span class="sxs-lookup"><span data-stu-id="f2626-130">Value</span></span>|  
|----------|-----------|  
|<span data-ttu-id="f2626-131">无</span><span class="sxs-lookup"><span data-stu-id="f2626-131">None</span></span>|<span data-ttu-id="f2626-132">0</span><span class="sxs-lookup"><span data-stu-id="f2626-132">0</span></span>|  
|<span data-ttu-id="f2626-133">SHA-1</span><span class="sxs-lookup"><span data-stu-id="f2626-133">SHA-1</span></span>|<span data-ttu-id="f2626-134">0x8004</span><span class="sxs-lookup"><span data-stu-id="f2626-134">0x8004</span></span>|  
|<span data-ttu-id="f2626-135">SHA-256</span><span class="sxs-lookup"><span data-stu-id="f2626-135">SHA-256</span></span>|<span data-ttu-id="f2626-136">0x800c</span><span class="sxs-lookup"><span data-stu-id="f2626-136">0x800c</span></span>|  
|<span data-ttu-id="f2626-137">SHA-384</span><span class="sxs-lookup"><span data-stu-id="f2626-137">SHA-384</span></span>|<span data-ttu-id="f2626-138">0x800d</span><span class="sxs-lookup"><span data-stu-id="f2626-138">0x800d</span></span>|  
|<span data-ttu-id="f2626-139">SHA-512</span><span class="sxs-lookup"><span data-stu-id="f2626-139">SHA-512</span></span>|<span data-ttu-id="f2626-140">0x800e</span><span class="sxs-lookup"><span data-stu-id="f2626-140">0x800e</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f2626-141">要求</span><span class="sxs-lookup"><span data-stu-id="f2626-141">Requirements</span></span>  

 <span data-ttu-id="f2626-142">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2626-142">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2626-143">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="f2626-143">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="f2626-144">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f2626-144">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2626-145">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2626-145">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2626-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2626-146">See also</span></span>

- [<span data-ttu-id="f2626-147">StrongNameTokenFromPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="f2626-147">StrongNameTokenFromPublicKey Method</span></span>](iclrstrongname-strongnametokenfrompublickey-method.md)
- [<span data-ttu-id="f2626-148">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="f2626-148">PublicKeyBlob Structure</span></span>](../strong-naming/publickeyblob-structure.md)
- [<span data-ttu-id="f2626-149">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="f2626-149">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
- [<span data-ttu-id="f2626-150">StrongNameGetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="f2626-150">StrongNameGetPublicKey Method</span></span>](iclrstrongname-strongnamegetpublickey-method.md)
