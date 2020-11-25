---
title: GetHashFromAssemblyFileW 函数
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFileW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFileW
helpviewer_keywords:
- GetHashFromAssemblyFileW function [.NET Framework strong naming]
ms.assetid: d1b2b172-5353-42af-a877-cf653c68ece0
topic_type:
- apiref
ms.openlocfilehash: b895c77850c0457fd2a152c1128c016093599f76
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730976"
---
# <a name="gethashfromassemblyfilew-function"></a><span data-ttu-id="4a753-102">GetHashFromAssemblyFileW 函数</span><span class="sxs-lookup"><span data-stu-id="4a753-102">GetHashFromAssemblyFileW Function</span></span>

<span data-ttu-id="4a753-103">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="4a753-103">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span> <span data-ttu-id="4a753-104">必须将程序集文件的路径指定为 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="4a753-104">The path to the assembly file must be specified as a Unicode string.</span></span>  
  
 <span data-ttu-id="4a753-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="4a753-105">This function has been deprecated.</span></span> <span data-ttu-id="4a753-106">改为使用 [ICLRStrongName：： GetHashFromAssemblyFileW](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4a753-106">Use the [ICLRStrongName::GetHashFromAssemblyFileW](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a753-107">语法</span><span class="sxs-lookup"><span data-stu-id="4a753-107">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4a753-108">参数</span><span class="sxs-lookup"><span data-stu-id="4a753-108">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="4a753-109">中要进行哈希处理的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="4a753-109">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="4a753-110">此参数必须是 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="4a753-110">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="4a753-111">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="4a753-111">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="4a753-112">使用零作为默认哈希算法。</span><span class="sxs-lookup"><span data-stu-id="4a753-112">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="4a753-113">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="4a753-113">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="4a753-114">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="4a753-114">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="4a753-115">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="4a753-115">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a753-116">要求</span><span class="sxs-lookup"><span data-stu-id="4a753-116">Requirements</span></span>  

 <span data-ttu-id="4a753-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a753-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a753-118">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="4a753-118">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="4a753-119">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4a753-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4a753-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a753-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a753-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a753-121">See also</span></span>

- [<span data-ttu-id="4a753-122">GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="4a753-122">GetHashFromAssemblyFileW Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md)
- [<span data-ttu-id="4a753-123">GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="4a753-123">GetHashFromAssemblyFile Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="4a753-124">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="4a753-124">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
