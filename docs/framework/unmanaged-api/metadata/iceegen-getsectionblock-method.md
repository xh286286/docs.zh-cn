---
title: ICeeGen::GetSectionBlock 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionBlock
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionBlock
helpviewer_keywords:
- GetSectionBlock method [.NET Framework metadata]
- ICeeGen::GetSectionBlock method [.NET Framework metadata]
ms.assetid: 05c78aaf-5bbd-497e-9ae2-55f4fae0c5fb
topic_type:
- apiref
ms.openlocfilehash: 9ce3afded5f914ecf970d8db738becc7f5cfff84
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723137"
---
# <a name="iceegengetsectionblock-method"></a><span data-ttu-id="5100d-102">ICeeGen::GetSectionBlock 方法</span><span class="sxs-lookup"><span data-stu-id="5100d-102">ICeeGen::GetSectionBlock Method</span></span>

<span data-ttu-id="5100d-103">获取代码库的节块。</span><span class="sxs-lookup"><span data-stu-id="5100d-103">Gets a section block of the code base.</span></span>  
  
 <span data-ttu-id="5100d-104">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="5100d-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5100d-105">语法</span><span class="sxs-lookup"><span data-stu-id="5100d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSectionBlock (  
    [in]  HCEESECTION    section,
    [in]  ULONG          len,  
    [in]  ULONG          align     = 1,  
    [out] void           **ppBytes = 0  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="5100d-106">参数</span><span class="sxs-lookup"><span data-stu-id="5100d-106">Parameters</span></span>  

 `section`  
 <span data-ttu-id="5100d-107">中要从中检索基本代码块的部分。</span><span class="sxs-lookup"><span data-stu-id="5100d-107">[in] The section from which to retrieve a block of the code base.</span></span>  
  
 `len`  
 <span data-ttu-id="5100d-108">中要检索的块的长度。</span><span class="sxs-lookup"><span data-stu-id="5100d-108">[in] The length of the block to be retrieved.</span></span>  
  
 `align`  
 <span data-ttu-id="5100d-109">中相对于部分开头的字节，用于对齐块的第一个字节。</span><span class="sxs-lookup"><span data-stu-id="5100d-109">[in] The byte, relative to the beginning of the section, with which to align the first byte of the block.</span></span> <span data-ttu-id="5100d-110">这是块在节中的位置。</span><span class="sxs-lookup"><span data-stu-id="5100d-110">This is the position of the block within the section.</span></span>  
  
 `ppBytes`  
 <span data-ttu-id="5100d-111">弄一个指针，指向接收检索到的块的地址的位置。</span><span class="sxs-lookup"><span data-stu-id="5100d-111">[out] A pointer to a location that receives the address of the retrieved block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5100d-112">注解</span><span class="sxs-lookup"><span data-stu-id="5100d-112">Remarks</span></span>  

 <span data-ttu-id="5100d-113">`GetSectionBlock`仅当有特殊部分的要求不是由其他方法处理时才调用。</span><span class="sxs-lookup"><span data-stu-id="5100d-113">Call `GetSectionBlock` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5100d-114">要求</span><span class="sxs-lookup"><span data-stu-id="5100d-114">Requirements</span></span>  

 <span data-ttu-id="5100d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5100d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5100d-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="5100d-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5100d-117">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5100d-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5100d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5100d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5100d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5100d-119">See also</span></span>

- [<span data-ttu-id="5100d-120">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="5100d-120">ICeeGen Interface</span></span>](iceegen-interface.md)
