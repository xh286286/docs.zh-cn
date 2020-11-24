---
title: ICLRStrongName::StrongNameTokenFromAssemblyEx 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameTokenFromAssemblyEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromAssemblyEx
helpviewer_keywords:
- StrongNameTokenFromAssemblyEx method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameTokenFromAssemblyEx method [.NET Framework hosting]
ms.assetid: 648ea90e-5e60-40a0-a56a-3e61bf2fba7c
topic_type:
- apiref
ms.openlocfilehash: 35fe86f856360814cfbb5453bfb6e5efaaef02fd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677721"
---
# <a name="iclrstrongnamestrongnametokenfromassemblyex-method"></a><span data-ttu-id="c1cca-102">ICLRStrongName::StrongNameTokenFromAssemblyEx 方法</span><span class="sxs-lookup"><span data-stu-id="c1cca-102">ICLRStrongName::StrongNameTokenFromAssemblyEx Method</span></span>

<span data-ttu-id="c1cca-103">从指定的程序集文件创建强名称令牌，并返回该令牌表示的公钥。</span><span class="sxs-lookup"><span data-stu-id="c1cca-103">Creates a strong name token from the specified assembly file, and returns the public key that the token represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1cca-104">语法</span><span class="sxs-lookup"><span data-stu-id="c1cca-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameTokenFromAssemblyEx (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c1cca-105">参数</span><span class="sxs-lookup"><span data-stu-id="c1cca-105">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="c1cca-106">中适用于程序集的可移植可执行文件 (PE) 文件的路径。</span><span class="sxs-lookup"><span data-stu-id="c1cca-106">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="c1cca-107">弄返回的强名称标记。</span><span class="sxs-lookup"><span data-stu-id="c1cca-107">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="c1cca-108">弄强名称令牌的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c1cca-108">[out] The size, in bytes, of the strong name token.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="c1cca-109">弄返回的公钥。</span><span class="sxs-lookup"><span data-stu-id="c1cca-109">[out] The returned public key.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="c1cca-110">弄公钥的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c1cca-110">[out] The size, in bytes, of the public key.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c1cca-111">返回值</span><span class="sxs-lookup"><span data-stu-id="c1cca-111">Return Value</span></span>  

 <span data-ttu-id="c1cca-112">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="c1cca-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c1cca-113">注解</span><span class="sxs-lookup"><span data-stu-id="c1cca-113">Remarks</span></span>  

 <span data-ttu-id="c1cca-114">强名称标记是公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="c1cca-114">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="c1cca-115">标记是从用于对程序集进行签名的公钥创建的64位哈希。</span><span class="sxs-lookup"><span data-stu-id="c1cca-115">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="c1cca-116">该令牌是程序集的强名称的一部分，并且可以从程序集元数据中读取。</span><span class="sxs-lookup"><span data-stu-id="c1cca-116">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="c1cca-117">检索到密钥并创建令牌后，应调用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法来释放已分配的内存。</span><span class="sxs-lookup"><span data-stu-id="c1cca-117">After the key is retrieved and the token is created, you should call the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c1cca-118">要求</span><span class="sxs-lookup"><span data-stu-id="c1cca-118">Requirements</span></span>  

 <span data-ttu-id="c1cca-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c1cca-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c1cca-120">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="c1cca-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c1cca-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c1cca-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c1cca-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c1cca-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1cca-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1cca-123">See also</span></span>

- [<span data-ttu-id="c1cca-124">StrongNameTokenFromAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="c1cca-124">StrongNameTokenFromAssembly Method</span></span>](iclrstrongname-strongnametokenfromassembly-method.md)
- [<span data-ttu-id="c1cca-125">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="c1cca-125">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
