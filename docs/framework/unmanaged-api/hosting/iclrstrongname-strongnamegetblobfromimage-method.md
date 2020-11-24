---
title: ICLRStrongName::StrongNameGetBlobFromImage 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameGetBlobFromImage method [.NET Framework hosting]
ms.assetid: 0f5a2ec8-e776-4fd8-bda6-937b6834575a
topic_type:
- apiref
ms.openlocfilehash: ad5fa510a17a3ce823ff90c4131b349b0d9efd39
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671741"
---
# <a name="iclrstrongnamestrongnamegetblobfromimage-method"></a><span data-ttu-id="7eb5d-102">ICLRStrongName::StrongNameGetBlobFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="7eb5d-102">ICLRStrongName::StrongNameGetBlobFromImage Method</span></span>

<span data-ttu-id="7eb5d-103">获取指定内存地址处程序集映像的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-103">Gets a binary representation of the assembly image at the specified memory address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7eb5d-104">语法</span><span class="sxs-lookup"><span data-stu-id="7eb5d-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7eb5d-105">参数</span><span class="sxs-lookup"><span data-stu-id="7eb5d-105">Parameters</span></span>  

 `pbBase`  
 <span data-ttu-id="7eb5d-106">中映射的程序集清单的内存地址。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-106">[in] The memory address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="7eb5d-107">中中图像的大小（以字节为单位） `pbBase` 。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-107">[in] The size, in bytes, of the image at `pbBase`.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="7eb5d-108">中包含图像的二进制表示形式的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-108">[in] A buffer to contain the binary representation of the image.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="7eb5d-109">[in，out]请求的最大大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-109">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="7eb5d-110">返回时，的实际大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-110">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7eb5d-111">返回值</span><span class="sxs-lookup"><span data-stu-id="7eb5d-111">Return Value</span></span>  

 <span data-ttu-id="7eb5d-112">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7eb5d-113">要求</span><span class="sxs-lookup"><span data-stu-id="7eb5d-113">Requirements</span></span>  

 <span data-ttu-id="7eb5d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7eb5d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7eb5d-115">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="7eb5d-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="7eb5d-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7eb5d-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7eb5d-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7eb5d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7eb5d-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7eb5d-118">See also</span></span>

- [<span data-ttu-id="7eb5d-119">StrongNameGetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="7eb5d-119">StrongNameGetBlob Method</span></span>](iclrstrongname-strongnamegetblob-method.md)
- [<span data-ttu-id="7eb5d-120">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="7eb5d-120">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
