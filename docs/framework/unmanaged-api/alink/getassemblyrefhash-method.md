---
title: GetAssemblyRefHash 方法
ms.date: 03/30/2017
api_name:
- IALink.GetAssemblyRefHash
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetAssemblyRefHash
helpviewer_keywords:
- GetAssemblyRefHash method
ms.assetid: 091a18bd-e901-46f6-b999-74d71c8a7c41
topic_type:
- apiref
ms.openlocfilehash: af040c4a6c9b85930d2d9261f8587ba69eb204e5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721473"
---
# <a name="getassemblyrefhash-method"></a><span data-ttu-id="e86e3-102">GetAssemblyRefHash 方法</span><span class="sxs-lookup"><span data-stu-id="e86e3-102">GetAssemblyRefHash Method</span></span>

<span data-ttu-id="e86e3-103">检索给定程序集的哈希 blob。</span><span class="sxs-lookup"><span data-stu-id="e86e3-103">Retrieves a hash blob for a given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e86e3-104">语法</span><span class="sxs-lookup"><span data-stu-id="e86e3-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyRefHash(  
    mdToken FileToken,  
    const void** ppvHash,  
    DWORD* pcbHash  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="e86e3-105">参数</span><span class="sxs-lookup"><span data-stu-id="e86e3-105">Parameters</span></span>  

 `FileToken`  
 <span data-ttu-id="e86e3-106">哈希将引用的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="e86e3-106">ID of assembly to which the hash will refer.</span></span>  
  
 `ppvHash`  
 <span data-ttu-id="e86e3-107">接收生成的哈希 blob。</span><span class="sxs-lookup"><span data-stu-id="e86e3-107">Receives the resulting hash blob.</span></span>  
  
 `pcbHash`  
 <span data-ttu-id="e86e3-108">接收哈希 blob 的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="e86e3-108">Receives size, in bytes, of hash blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e86e3-109">返回值</span><span class="sxs-lookup"><span data-stu-id="e86e3-109">Return Value</span></span>  

 <span data-ttu-id="e86e3-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e86e3-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e86e3-111">要求</span><span class="sxs-lookup"><span data-stu-id="e86e3-111">Requirements</span></span>  

 <span data-ttu-id="e86e3-112">需要 alink</span><span class="sxs-lookup"><span data-stu-id="e86e3-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e86e3-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e86e3-113">See also</span></span>

- [<span data-ttu-id="e86e3-114">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="e86e3-114">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="e86e3-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="e86e3-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="e86e3-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="e86e3-116">ALink API</span></span>](index.md)
