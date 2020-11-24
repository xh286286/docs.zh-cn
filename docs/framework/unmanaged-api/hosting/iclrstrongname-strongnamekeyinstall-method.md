---
title: ICLRStrongName::StrongNameKeyInstall 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyInstall
helpviewer_keywords:
- ICLRStrongName::StrongNameKeyInstall method [.NET Framework hosting]
- StrongNameKeyInstall method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5c15cf3b-164c-49d1-8e57-e42949d55acf
topic_type:
- apiref
ms.openlocfilehash: 7e0c689dad0c288e3af3a3d64ee1bba1c44053c1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95674523"
---
# <a name="iclrstrongnamestrongnamekeyinstall-method"></a><span data-ttu-id="8f6a2-102">ICLRStrongName::StrongNameKeyInstall 方法</span><span class="sxs-lookup"><span data-stu-id="8f6a2-102">ICLRStrongName::StrongNameKeyInstall Method</span></span>

<span data-ttu-id="8f6a2-103">将公钥/私钥对导入容器。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-103">Imports a public/private key pair into a container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f6a2-104">语法</span><span class="sxs-lookup"><span data-stu-id="8f6a2-104">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8f6a2-105">参数</span><span class="sxs-lookup"><span data-stu-id="8f6a2-105">Parameters</span></span>  

 `wszKeyContainer`  
 <span data-ttu-id="8f6a2-106">中密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-106">[in] The name of the key container.</span></span> <span data-ttu-id="8f6a2-107">`wszKeyContainer` 必须为非空字符串。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-107">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="8f6a2-108">中二进制密钥对。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-108">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="8f6a2-109">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-109">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8f6a2-110">返回值</span><span class="sxs-lookup"><span data-stu-id="8f6a2-110">Return Value</span></span>  

 <span data-ttu-id="8f6a2-111">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-111">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8f6a2-112">注解</span><span class="sxs-lookup"><span data-stu-id="8f6a2-112">Remarks</span></span>  

 <span data-ttu-id="8f6a2-113">使用 [ICLRStrongName：： StrongNameKeyDelete](iclrstrongname-strongnamekeydelete-method.md) 方法删除密钥容器。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-113">Use the [ICLRStrongName::StrongNameKeyDelete](iclrstrongname-strongnamekeydelete-method.md) method to delete the key container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f6a2-114">要求</span><span class="sxs-lookup"><span data-stu-id="8f6a2-114">Requirements</span></span>  

 <span data-ttu-id="8f6a2-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8f6a2-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f6a2-116">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="8f6a2-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8f6a2-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8f6a2-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8f6a2-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f6a2-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f6a2-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f6a2-119">See also</span></span>

- [<span data-ttu-id="8f6a2-120">StrongNameKeyDelete 方法</span><span class="sxs-lookup"><span data-stu-id="8f6a2-120">StrongNameKeyDelete Method</span></span>](iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="8f6a2-121">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="8f6a2-121">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
