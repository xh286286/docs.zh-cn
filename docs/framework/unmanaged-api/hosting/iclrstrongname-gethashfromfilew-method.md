---
title: ICLRStrongName::GetHashFromFileW 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromFileW
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromFileW
helpviewer_keywords:
- GetHashFromFileW method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::GetHashFromFileW method [.NET Framework hosting]
ms.assetid: c6ff45fc-905d-4c6e-b00c-97c6c7c55d99
topic_type:
- apiref
ms.openlocfilehash: eda78976f175230cc2405b9cb151993e63697e48
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95685755"
---
# <a name="iclrstrongnamegethashfromfilew-method"></a><span data-ttu-id="c0f6c-102">ICLRStrongName::GetHashFromFileW 方法</span><span class="sxs-lookup"><span data-stu-id="c0f6c-102">ICLRStrongName::GetHashFromFileW Method</span></span>

<span data-ttu-id="c0f6c-103">生成由 Unicode 字符串指定的文件内容的哈希。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0f6c-104">语法</span><span class="sxs-lookup"><span data-stu-id="c0f6c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromFileW (
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="c0f6c-105">参数</span><span class="sxs-lookup"><span data-stu-id="c0f6c-105">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="c0f6c-106">中要进行哈希处理的文件的 Unicode 名称。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-106">[in] The Unicode name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="c0f6c-107">[in，out]生成哈希时要使用的算法。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-107">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="c0f6c-108">有效算法是由 Win32 CryptoAPI 定义的算法。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-108">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="c0f6c-109">如果 `piHashAlg` 设置为0，则使用默认算法 CALG_SHA-1。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-109">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="c0f6c-110">弄一个字节数组，其中包含生成的哈希。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-110">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="c0f6c-111">中所指向的缓冲区的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-111">[in] The maximum size of the buffer pointed to by `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="c0f6c-112">弄的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-112">[out] The size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c0f6c-113">返回值</span><span class="sxs-lookup"><span data-stu-id="c0f6c-113">Return Value</span></span>  

 <span data-ttu-id="c0f6c-114">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0f6c-115">注解</span><span class="sxs-lookup"><span data-stu-id="c0f6c-115">Remarks</span></span>  

 <span data-ttu-id="c0f6c-116">此方法与 [ICLRStrongName：： GetHashFromFile](iclrstrongname-gethashfromfile-method.md) 方法相同，不同之处在于文件名规范是 Unicode 而不是 ANSI。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-116">This method is the same as the [ICLRStrongName::GetHashFromFile](iclrstrongname-gethashfromfile-method.md) method, except that the file name specification is Unicode instead of ANSI.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0f6c-117">要求</span><span class="sxs-lookup"><span data-stu-id="c0f6c-117">Requirements</span></span>  

 <span data-ttu-id="c0f6c-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c0f6c-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0f6c-119">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="c0f6c-119">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c0f6c-120">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0f6c-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c0f6c-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0f6c-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0f6c-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0f6c-122">See also</span></span>

- [<span data-ttu-id="c0f6c-123">GetHashFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="c0f6c-123">GetHashFromFile Method</span></span>](iclrstrongname-gethashfromfile-method.md)
- [<span data-ttu-id="c0f6c-124">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="c0f6c-124">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
