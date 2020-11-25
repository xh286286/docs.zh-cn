---
title: IMapToken::Map 方法
ms.date: 03/30/2017
api_name:
- IMapToken.Map
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMapToken::Map
helpviewer_keywords:
- IMapToken::Map method [.NET Framework metadata]
- Map method [.NET Framework metadata]
ms.assetid: b9b4bf2f-1098-43d6-9619-a99b4bda1940
topic_type:
- apiref
ms.openlocfilehash: 51cca1ab61027090b0d22781dfd740038bc9372d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95718197"
---
# <a name="imaptokenmap-method"></a><span data-ttu-id="0cfd1-102">IMapToken::Map 方法</span><span class="sxs-lookup"><span data-stu-id="0cfd1-102">IMapToken::Map Method</span></span>

<span data-ttu-id="0cfd1-103">使用元数据签名映射程序集之间的关系。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-103">Maps a relationship between the assemblies using metadata signatures.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0cfd1-104">语法</span><span class="sxs-lookup"><span data-stu-id="0cfd1-104">Syntax</span></span>  
  
```cpp  
HRESULT Map (  
    [in]  mdToken tkImp,
    [in]  mdToken tkEmit  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0cfd1-105">参数</span><span class="sxs-lookup"><span data-stu-id="0cfd1-105">Parameters</span></span>  

 `tkImp`  
 <span data-ttu-id="0cfd1-106">中表示导入的代码对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-106">[in] The metadata token that represents the imported code object.</span></span>  
  
 `tkEmit`  
 <span data-ttu-id="0cfd1-107">中表示发出的代码对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-107">[in] The metadata token that represents the emitted code object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0cfd1-108">注解</span><span class="sxs-lookup"><span data-stu-id="0cfd1-108">Remarks</span></span>  

 <span data-ttu-id="0cfd1-109">如果在合并过程中发生令牌重新映射，则原始令牌的范围将在导入的 (源) 元数据范围内，并且新令牌的范围限定为发出的 (目标) 元数据范围。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-109">When the token re-map occurs during a merge, the original token is scoped in the imported (source) metadata scope and the new token is scoped in the emitted (target) metadata scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0cfd1-110">要求</span><span class="sxs-lookup"><span data-stu-id="0cfd1-110">Requirements</span></span>  

 <span data-ttu-id="0cfd1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0cfd1-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0cfd1-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0cfd1-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0cfd1-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0cfd1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0cfd1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0cfd1-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0cfd1-115">See also</span></span>

- [<span data-ttu-id="0cfd1-116">IMapToken 接口</span><span class="sxs-lookup"><span data-stu-id="0cfd1-116">IMapToken Interface</span></span>](imaptoken-interface.md)
