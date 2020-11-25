---
title: ICeeGen::GenerateCeeMemoryImage 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GenerateCeeMemoryImage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GenerateCeeMemoryImage
helpviewer_keywords:
- ICeeGen::GenerateCeeMemoryImage method [.NET Framework metadata]
- GenerateCeeMemoryImage method [.NET Framework metadata]
ms.assetid: b3847495-0ae6-4a72-b496-65ce2424afc6
topic_type:
- apiref
ms.openlocfilehash: 69c4a64dee0eb12481a78aa6f185ab568266ee30
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95715376"
---
# <a name="iceegengenerateceememoryimage-method"></a><span data-ttu-id="0e8b6-102">ICeeGen::GenerateCeeMemoryImage 方法</span><span class="sxs-lookup"><span data-stu-id="0e8b6-102">ICeeGen::GenerateCeeMemoryImage Method</span></span>

<span data-ttu-id="0e8b6-103">为基本代码在内存中生成一个图像。</span><span class="sxs-lookup"><span data-stu-id="0e8b6-103">Generates an image in memory for the code base.</span></span>  
  
 <span data-ttu-id="0e8b6-104">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="0e8b6-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e8b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e8b6-105">Syntax</span></span>  
  
```cpp  
HRESULT GenerateCeeMemoryImage (  
    [out] void    **ppImage  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e8b6-106">参数</span><span class="sxs-lookup"><span data-stu-id="0e8b6-106">Parameters</span></span>  

 `ppImage`  
 <span data-ttu-id="0e8b6-107">弄指向生成的图像的指针。</span><span class="sxs-lookup"><span data-stu-id="0e8b6-107">[out] A pointer to the generated image.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e8b6-108">要求</span><span class="sxs-lookup"><span data-stu-id="0e8b6-108">Requirements</span></span>  

 <span data-ttu-id="0e8b6-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0e8b6-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e8b6-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="0e8b6-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0e8b6-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="0e8b6-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0e8b6-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e8b6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e8b6-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0e8b6-113">See also</span></span>

- [<span data-ttu-id="0e8b6-114">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="0e8b6-114">ICeeGen Interface</span></span>](iceegen-interface.md)
