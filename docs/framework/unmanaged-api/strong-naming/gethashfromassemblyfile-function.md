---
title: GetHashFromAssemblyFile 函数
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFile
helpviewer_keywords:
- GetHashFromAssemblyFile function [.NET Framework strong naming]
ms.assetid: 751ed69f-b7ab-4e07-80de-e17ca9319b0c
topic_type:
- apiref
ms.openlocfilehash: caefc9773b0d208f8b20847b664f7bc017d2c076
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730989"
---
# <a name="gethashfromassemblyfile-function"></a><span data-ttu-id="4c025-102">GetHashFromAssemblyFile 函数</span><span class="sxs-lookup"><span data-stu-id="4c025-102">GetHashFromAssemblyFile Function</span></span>

<span data-ttu-id="4c025-103">使用指定的哈希算法获取指定程序集文件的哈希。</span><span class="sxs-lookup"><span data-stu-id="4c025-103">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="4c025-104">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="4c025-104">This function has been deprecated.</span></span> <span data-ttu-id="4c025-105">改为使用 [ICLRStrongName：： GetHashFromAssemblyFile](../hosting/iclrstrongname-gethashfromassemblyfile-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c025-105">Use the [ICLRStrongName::GetHashFromAssemblyFile](../hosting/iclrstrongname-gethashfromassemblyfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c025-106">语法</span><span class="sxs-lookup"><span data-stu-id="4c025-106">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromAssemblyFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4c025-107">参数</span><span class="sxs-lookup"><span data-stu-id="4c025-107">Parameters</span></span>  

 `szFilePath`  
 <span data-ttu-id="4c025-108">中要进行哈希处理的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="4c025-108">[in] The path to the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="4c025-109">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="4c025-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="4c025-110">使用零作为默认哈希算法。</span><span class="sxs-lookup"><span data-stu-id="4c025-110">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="4c025-111">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="4c025-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="4c025-112">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="4c025-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="4c025-113">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="4c025-113">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4c025-114">要求</span><span class="sxs-lookup"><span data-stu-id="4c025-114">Requirements</span></span>  

 <span data-ttu-id="4c025-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4c025-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c025-116">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="4c025-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="4c025-117">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4c025-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4c025-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c025-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c025-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4c025-119">See also</span></span>

- [<span data-ttu-id="4c025-120">GetHashFromAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="4c025-120">GetHashFromAssemblyFile Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="4c025-121">GetHashFromAssemblyFileW 方法</span><span class="sxs-lookup"><span data-stu-id="4c025-121">GetHashFromAssemblyFileW Method</span></span>](../hosting/iclrstrongname-gethashfromassemblyfilew-method.md)
- [<span data-ttu-id="4c025-122">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="4c025-122">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
