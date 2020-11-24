---
title: ICLRStrongName::StrongNameSignatureVerificationFromImage 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameSignatureVerificationFromImage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameSignatureVerificationFromImage
helpviewer_keywords:
- ICLRStrongName::StrongNameSignatureVerificationFromImage method [.NET Framework hosting]
- StrongNameSignatureVerificationFromImage method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: da91c138-ee30-4fd4-a040-464d97d7e41a
topic_type:
- apiref
ms.openlocfilehash: 134b32b6b281a08997849f4c23edfc1f357dadcd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95674393"
---
# <a name="iclrstrongnamestrongnamesignatureverificationfromimage-method"></a><span data-ttu-id="ddefc-102">ICLRStrongName::StrongNameSignatureVerificationFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="ddefc-102">ICLRStrongName::StrongNameSignatureVerificationFromImage Method</span></span>

<span data-ttu-id="ddefc-103">验证已映射到内存的程序集对关联的公钥是否有效。</span><span class="sxs-lookup"><span data-stu-id="ddefc-103">Verifies that an assembly that has already been mapped to memory is valid for the associated public key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddefc-104">语法</span><span class="sxs-lookup"><span data-stu-id="ddefc-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameSignatureVerificationFromImage (  
    [in]  BYTE    *pbBase,  
    [in]  DWORD   dwLength,  
    [in]  DWORD   dwInFlags,  
    [out] DWORD   *pdwOutFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ddefc-105">参数</span><span class="sxs-lookup"><span data-stu-id="ddefc-105">Parameters</span></span>  

 `pbBase`  
 <span data-ttu-id="ddefc-106">中映射的程序集清单的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="ddefc-106">[in] The relative virtual address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="ddefc-107">中映射的图像的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddefc-107">[in] The size, in bytes, of the mapped image.</span></span>  
  
 `dwInFlags`  
 <span data-ttu-id="ddefc-108">中影响验证行为的标志。</span><span class="sxs-lookup"><span data-stu-id="ddefc-108">[in] Flags that influence verification behavior.</span></span> <span data-ttu-id="ddefc-109">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="ddefc-109">The following values are supported:</span></span>  
  
- <span data-ttu-id="ddefc-110">`SN_INFLAG_FORCE_VER` (0x00000001) -即使需要重写注册表设置，也强制进行验证。</span><span class="sxs-lookup"><span data-stu-id="ddefc-110">`SN_INFLAG_FORCE_VER` (0x00000001) - Forces verification even if it is necessary to override registry settings.</span></span>  
  
- <span data-ttu-id="ddefc-111">`SN_INFLAG_INSTALL` (0x00000002) -指定这是在此映像上执行的第一次验证。</span><span class="sxs-lookup"><span data-stu-id="ddefc-111">`SN_INFLAG_INSTALL` (0x00000002) - Specifies that this is the first verification performed on this image.</span></span>  
  
- <span data-ttu-id="ddefc-112">`SN_INFLAG_ADMIN_ACCESS` (0x00000004) -指定缓存只允许具有管理权限的用户访问。</span><span class="sxs-lookup"><span data-stu-id="ddefc-112">`SN_INFLAG_ADMIN_ACCESS` (0x00000004) - Specifies that the cache will allow access only to users who have administrative privileges.</span></span>  
  
- <span data-ttu-id="ddefc-113">`SN_INFLAG_USER_ACCESS` (0x00000008) -指定只能向当前用户访问程序集。</span><span class="sxs-lookup"><span data-stu-id="ddefc-113">`SN_INFLAG_USER_ACCESS` (0x00000008) - Specifies that the assembly will be accessible only to the current user.</span></span>  
  
- <span data-ttu-id="ddefc-114">`SN_INFLAG_ALL_ACCESS` (0x00000010) -指定缓存将不提供访问限制。</span><span class="sxs-lookup"><span data-stu-id="ddefc-114">`SN_INFLAG_ALL_ACCESS` (0x00000010) - Specifies that the cache will provide no guarantees of access restriction.</span></span>  
  
- <span data-ttu-id="ddefc-115">`SN_INFLAG_RUNTIME` (0x80000000) 为内部调试保留。</span><span class="sxs-lookup"><span data-stu-id="ddefc-115">`SN_INFLAG_RUNTIME` (0x80000000) - Reserved for internal debugging.</span></span>  
  
 `pdwOutFlags`  
 <span data-ttu-id="ddefc-116">弄用于附加输出信息的标志。</span><span class="sxs-lookup"><span data-stu-id="ddefc-116">[out] A flag for additional output information.</span></span> <span data-ttu-id="ddefc-117">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="ddefc-117">The following value is supported:</span></span>  
  
- <span data-ttu-id="ddefc-118">`SN_OUTFLAG_WAS_VERIFIED` (0x00000001) -将此值设置为， `false` 以指定验证是否由于注册表设置而成功。</span><span class="sxs-lookup"><span data-stu-id="ddefc-118">`SN_OUTFLAG_WAS_VERIFIED` (0x00000001) - This value is set to `false` to specify that the verification succeeded due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ddefc-119">返回值</span><span class="sxs-lookup"><span data-stu-id="ddefc-119">Return Value</span></span>  

 <span data-ttu-id="ddefc-120">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="ddefc-120">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ddefc-121">要求</span><span class="sxs-lookup"><span data-stu-id="ddefc-121">Requirements</span></span>  

 <span data-ttu-id="ddefc-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ddefc-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ddefc-123">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="ddefc-123">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="ddefc-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ddefc-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ddefc-125">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ddefc-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddefc-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ddefc-126">See also</span></span>

- [<span data-ttu-id="ddefc-127">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="ddefc-127">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
