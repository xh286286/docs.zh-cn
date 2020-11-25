---
title: PublicKeyBlob 结构
ms.date: 03/30/2017
api_name:
- PublicKeyBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- PublicKeyBlob
helpviewer_keywords:
- PublicKeyBlob structure [.NET Framework strong naming]
ms.assetid: b9240712-829c-4c8d-9a09-a6e7aa63f63a
topic_type:
- apiref
ms.openlocfilehash: 42cd3cc22fbbb8eb3d5ac44544fce36650b6461f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705925"
---
# <a name="publickeyblob-structure"></a><span data-ttu-id="a086d-102">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="a086d-102">PublicKeyBlob Structure</span></span>

<span data-ttu-id="a086d-103">表示公钥/私钥对的公钥，采用二进制格式。</span><span class="sxs-lookup"><span data-stu-id="a086d-103">Represents, in binary format, the public key of a public/private key pair.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a086d-104">语法</span><span class="sxs-lookup"><span data-stu-id="a086d-104">Syntax</span></span>  
  
```cpp  
typedef struct {  
    unsigned int SigAlgId;  
    unsigned int HashAlgId;  
    ULONG cbPublicKey;  
    BYTE PublicKey[1]  
} PublicKeyBlob;
```  
  
## <a name="members"></a><span data-ttu-id="a086d-105">成员</span><span class="sxs-lookup"><span data-stu-id="a086d-105">Members</span></span>  
  
|<span data-ttu-id="a086d-106">成员</span><span class="sxs-lookup"><span data-stu-id="a086d-106">Member</span></span>|<span data-ttu-id="a086d-107">说明</span><span class="sxs-lookup"><span data-stu-id="a086d-107">Description</span></span>|  
|------------|-----------------|  
|`SigAlgId`|<span data-ttu-id="a086d-108"> (类型的签名算法的标识符 `ALG_ID` ，在公钥的 wincrypt.h) 中定义。</span><span class="sxs-lookup"><span data-stu-id="a086d-108">The identifier for the signature algorithm (of type `ALG_ID`, as defined in WinCrypt.h) of the public key.</span></span>|  
|`HashAlgId`|<span data-ttu-id="a086d-109"> (类型的哈希算法的标识符 `ALG_ID` ，在公钥的 wincrypt.h) 中定义。</span><span class="sxs-lookup"><span data-stu-id="a086d-109">The identifier for the hash algorithm (of type `ALG_ID`, as defined in WinCrypt.h) of the public key.</span></span>|  
|`cbPublicKey`|<span data-ttu-id="a086d-110">密钥的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a086d-110">The length of the key in bytes.</span></span>|  
|`PublicKey`|<span data-ttu-id="a086d-111">可变长度的字节数组，其中包含由 CryptoAPI 返回的格式的键值。</span><span class="sxs-lookup"><span data-stu-id="a086d-111">A variable-length byte array that contains the key value in the format returned by the CryptoAPI.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a086d-112">注解</span><span class="sxs-lookup"><span data-stu-id="a086d-112">Remarks</span></span>  

 <span data-ttu-id="a086d-113">`PublicKeyBlob`结构由[StrongNameGetPublicKey](strongnamegetpublickey-function.md)、 [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md)和其他强名称函数用来表示公钥/私钥对的公钥。</span><span class="sxs-lookup"><span data-stu-id="a086d-113">The `PublicKeyBlob` structure is used by [StrongNameGetPublicKey](strongnamegetpublickey-function.md), [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md), and other strong name functions to represent the public key of a public/private key pair.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a086d-114">要求</span><span class="sxs-lookup"><span data-stu-id="a086d-114">Requirements</span></span>  

 <span data-ttu-id="a086d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a086d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a086d-116">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="a086d-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="a086d-117">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a086d-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a086d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a086d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a086d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a086d-119">See also</span></span>

- [<span data-ttu-id="a086d-120">StrongNameGetPublicKey 函数</span><span class="sxs-lookup"><span data-stu-id="a086d-120">StrongNameGetPublicKey Function</span></span>](strongnamegetpublickey-function.md)
- [<span data-ttu-id="a086d-121">StrongNameSignatureGeneration 函数</span><span class="sxs-lookup"><span data-stu-id="a086d-121">StrongNameSignatureGeneration Function</span></span>](strongnamesignaturegeneration-function.md)
