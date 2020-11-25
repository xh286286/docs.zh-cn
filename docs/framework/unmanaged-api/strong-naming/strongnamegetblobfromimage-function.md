---
title: StrongNameGetBlobFromImage 函数
ms.date: 03/30/2017
api_name:
- StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage function [.NET Framework strong naming]
ms.assetid: 1de658e6-da32-4d01-9097-6f43c92222e1
topic_type:
- apiref
ms.openlocfilehash: 3a84221f94bad76d69f0dc67fe695ada3f3862f4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95732237"
---
# <a name="strongnamegetblobfromimage-function"></a><span data-ttu-id="6f0bd-102">StrongNameGetBlobFromImage 函数</span><span class="sxs-lookup"><span data-stu-id="6f0bd-102">StrongNameGetBlobFromImage Function</span></span>

<span data-ttu-id="6f0bd-103">获取指定内存地址处程序集映像的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-103">Gets a binary representation of the assembly image at the specified memory address.</span></span>  
  
 <span data-ttu-id="6f0bd-104">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-104">This function has been deprecated.</span></span> <span data-ttu-id="6f0bd-105">改为使用 [ICLRStrongName：： StrongNameGetBlobFromImage](../hosting/iclrstrongname-strongnamegetblobfromimage-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-105">Use the [ICLRStrongName::StrongNameGetBlobFromImage](../hosting/iclrstrongname-strongnamegetblobfromimage-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f0bd-106">语法</span><span class="sxs-lookup"><span data-stu-id="6f0bd-106">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6f0bd-107">参数</span><span class="sxs-lookup"><span data-stu-id="6f0bd-107">Parameters</span></span>  

 `pbBase`  
 <span data-ttu-id="6f0bd-108">中映射的程序集清单的内存地址。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-108">[in] The memory address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="6f0bd-109">中中图像的大小（以字节为单位） `pbBase` 。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-109">[in] The size, in bytes, of the image at `pbBase`.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="6f0bd-110">中包含图像的二进制表示形式的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-110">[in] A buffer to contain the binary representation of the image.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="6f0bd-111">[in，out]请求的最大大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-111">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="6f0bd-112">返回时，的实际大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-112">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6f0bd-113">返回值</span><span class="sxs-lookup"><span data-stu-id="6f0bd-113">Return Value</span></span>  

 <span data-ttu-id="6f0bd-114">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-114">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6f0bd-115">注解</span><span class="sxs-lookup"><span data-stu-id="6f0bd-115">Remarks</span></span>  

 <span data-ttu-id="6f0bd-116">如果 `StrongNameGetBlobFromImage` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-116">If the `StrongNameGetBlobFromImage` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f0bd-117">要求</span><span class="sxs-lookup"><span data-stu-id="6f0bd-117">Requirements</span></span>  

 <span data-ttu-id="6f0bd-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6f0bd-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f0bd-119">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="6f0bd-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="6f0bd-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6f0bd-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6f0bd-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f0bd-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f0bd-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f0bd-122">See also</span></span>

- [<span data-ttu-id="6f0bd-123">StrongNameGetBlobFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="6f0bd-123">StrongNameGetBlobFromImage Method</span></span>](../hosting/iclrstrongname-strongnamegetblobfromimage-method.md)
- [<span data-ttu-id="6f0bd-124">StrongNameGetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="6f0bd-124">StrongNameGetBlob Method</span></span>](../hosting/iclrstrongname-strongnamegetblob-method.md)
- [<span data-ttu-id="6f0bd-125">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="6f0bd-125">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
