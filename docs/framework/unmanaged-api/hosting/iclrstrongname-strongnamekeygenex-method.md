---
title: ICLRStrongName::StrongNameKeyGenEx 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyGenEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyGenEx
helpviewer_keywords:
- ICLRStrongName::StrongNameKeyGenEx method [.NET Framework hosting]
- StrongNameKeyGenEx method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 1f8b59d0-5b72-45b8-ab74-c2b43ffc806e
topic_type:
- apiref
ms.openlocfilehash: 9ba50616b25f9c7c592f19947c82a890ae6b5a4a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671676"
---
# <a name="iclrstrongnamestrongnamekeygenex-method"></a><span data-ttu-id="a1730-102">ICLRStrongName::StrongNameKeyGenEx 方法</span><span class="sxs-lookup"><span data-stu-id="a1730-102">ICLRStrongName::StrongNameKeyGenEx Method</span></span>

<span data-ttu-id="a1730-103">使用指定的密钥大小生成新的公钥/私钥对，以便使用强名称。</span><span class="sxs-lookup"><span data-stu-id="a1730-103">Generates a new public/private key pair with the specified key size, for strong name use.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1730-104">语法</span><span class="sxs-lookup"><span data-stu-id="a1730-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameKeyGenEx (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [in]  DWORD     dwKeySize,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a1730-105">参数</span><span class="sxs-lookup"><span data-stu-id="a1730-105">Parameters</span></span>  

 `wszKeyContainer`  
 <span data-ttu-id="a1730-106">中请求的密钥容器名称。</span><span class="sxs-lookup"><span data-stu-id="a1730-106">[in] The requested key container name.</span></span> <span data-ttu-id="a1730-107">`wszKeyContainer` 必须为非空字符串，或者为 null 以生成临时名称。</span><span class="sxs-lookup"><span data-stu-id="a1730-107">`wszKeyContainer` must either be a non-empty string or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="a1730-108">中一个值，该值指定是否保留注册的密钥。</span><span class="sxs-lookup"><span data-stu-id="a1730-108">[in] A value that specifies whether to leave the key registered.</span></span> <span data-ttu-id="a1730-109">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="a1730-109">The following values are supported:</span></span>  
  
- <span data-ttu-id="a1730-110">0x00000000-在 `wszKeyContainer` 为 null 时用于生成临时密钥容器名称。</span><span class="sxs-lookup"><span data-stu-id="a1730-110">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
- <span data-ttu-id="a1730-111">0x00000001 (`SN_LEAVE_KEY`) -指定应保持注册该密钥。</span><span class="sxs-lookup"><span data-stu-id="a1730-111">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `dwKeySize`  
 <span data-ttu-id="a1730-112">中请求的密钥大小，以位为单位。</span><span class="sxs-lookup"><span data-stu-id="a1730-112">[in] The requested size of the key, in bits.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="a1730-113">弄返回的公钥/私钥对。</span><span class="sxs-lookup"><span data-stu-id="a1730-113">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="a1730-114">弄的大小（以字节为单位） `ppbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="a1730-114">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a1730-115">返回值</span><span class="sxs-lookup"><span data-stu-id="a1730-115">Return Value</span></span>  

 <span data-ttu-id="a1730-116">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="a1730-116">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a1730-117">注解</span><span class="sxs-lookup"><span data-stu-id="a1730-117">Remarks</span></span>  

 <span data-ttu-id="a1730-118">.NET Framework 版本1.0 和1.1 需要 `dwKeySize` 1024 位才能使用强名称对程序集进行签名; 版本2.0 增加了对2048位密钥的支持。</span><span class="sxs-lookup"><span data-stu-id="a1730-118">The .NET Framework versions 1.0 and 1.1 require a `dwKeySize` of 1024 bits to sign an assembly with a strong name; version 2.0 adds supports for 2048-bit keys.</span></span>  
  
 <span data-ttu-id="a1730-119">检索到密钥后，应调用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法来释放已分配的内存。</span><span class="sxs-lookup"><span data-stu-id="a1730-119">After the key is retrieved, you should call the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1730-120">要求</span><span class="sxs-lookup"><span data-stu-id="a1730-120">Requirements</span></span>  

 <span data-ttu-id="a1730-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1730-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1730-122">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="a1730-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a1730-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a1730-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a1730-124">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1730-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1730-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1730-125">See also</span></span>

- [<span data-ttu-id="a1730-126">StrongNameKeyGen 方法</span><span class="sxs-lookup"><span data-stu-id="a1730-126">StrongNameKeyGen Method</span></span>](iclrstrongname-strongnamekeygen-method.md)
- [<span data-ttu-id="a1730-127">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="a1730-127">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
