---
title: ICLRStrongName::GetHashFromAssemblyFile 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromAssemblyFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromAssemblyFile
helpviewer_keywords:
- ICLRStrongName::GetHashFromAssemblyFile method [.NET Framework hosting]
- GetHashFromAssemblyFile method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 0b67ea03-d474-4605-acaa-57455790250c
topic_type:
- apiref
ms.openlocfilehash: 0a15a4d237f63da54615ee1801e6cd39620e8274
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727856"
---
# <a name="iclrstrongnamegethashfromassemblyfile-method"></a><span data-ttu-id="e601d-102">ICLRStrongName::GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="e601d-102">ICLRStrongName::GetHashFromAssemblyFile Method</span></span>

<span data-ttu-id="e601d-103">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="e601d-103">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e601d-104">语法</span><span class="sxs-lookup"><span data-stu-id="e601d-104">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromAssemblyFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e601d-105">参数</span><span class="sxs-lookup"><span data-stu-id="e601d-105">Parameters</span></span>  

 `szFilePath`  
 <span data-ttu-id="e601d-106">中要进行哈希处理的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="e601d-106">[in] The path to the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="e601d-107">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="e601d-107">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="e601d-108">使用零作为默认哈希算法。</span><span class="sxs-lookup"><span data-stu-id="e601d-108">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="e601d-109">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e601d-109">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="e601d-110">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="e601d-110">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="e601d-111">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="e601d-111">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e601d-112">返回值</span><span class="sxs-lookup"><span data-stu-id="e601d-112">Return Value</span></span>  

 <span data-ttu-id="e601d-113">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="e601d-113">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e601d-114">要求</span><span class="sxs-lookup"><span data-stu-id="e601d-114">Requirements</span></span>  

 <span data-ttu-id="e601d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e601d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e601d-116">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="e601d-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="e601d-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e601d-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e601d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e601d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e601d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e601d-119">See also</span></span>

- [<span data-ttu-id="e601d-120">GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="e601d-120">GetHashFromAssemblyFileW Method</span></span>](iclrstrongname-gethashfromassemblyfilew-method.md)
- [<span data-ttu-id="e601d-121">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="e601d-121">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
