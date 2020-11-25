---
title: ICeeGen::GetSectionDataLen 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionDataLen
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionDataLen
helpviewer_keywords:
- ICeeGen::GetSectionDataLen method [.NET Framework metadata]
- GetSectionDataLen method [.NET Framework metadata]
ms.assetid: e2a06ee4-b8ee-49c7-935a-c1031a29eef2
topic_type:
- apiref
ms.openlocfilehash: b45b0a59a29a27e7b0a395f3928215959450f9a5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95698463"
---
# <a name="iceegengetsectiondatalen-method"></a><span data-ttu-id="bec7e-102">ICeeGen::GetSectionDataLen 方法</span><span class="sxs-lookup"><span data-stu-id="bec7e-102">ICeeGen::GetSectionDataLen Method</span></span>

<span data-ttu-id="bec7e-103">获取指定节的长度。</span><span class="sxs-lookup"><span data-stu-id="bec7e-103">Gets the length of the specified section.</span></span>  
  
 <span data-ttu-id="bec7e-104">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="bec7e-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bec7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="bec7e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSectionDataLen (  
    [in]  HCEESECTION  section,  
    [out] ULONG        *dataLen  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bec7e-106">参数</span><span class="sxs-lookup"><span data-stu-id="bec7e-106">Parameters</span></span>  

 `section`  
 <span data-ttu-id="bec7e-107">中将检索其长度的数据部分。</span><span class="sxs-lookup"><span data-stu-id="bec7e-107">[in] The data section whose length will be retrieved.</span></span>  
  
 `dataLen`  
 <span data-ttu-id="bec7e-108">弄指定节的返回长度。</span><span class="sxs-lookup"><span data-stu-id="bec7e-108">[out] The returned length of the specified section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bec7e-109">注解</span><span class="sxs-lookup"><span data-stu-id="bec7e-109">Remarks</span></span>  

 <span data-ttu-id="bec7e-110">`GetSectionDataLen`仅当有特殊部分的要求不是由其他方法处理时才调用。</span><span class="sxs-lookup"><span data-stu-id="bec7e-110">Call `GetSectionDataLen` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bec7e-111">要求</span><span class="sxs-lookup"><span data-stu-id="bec7e-111">Requirements</span></span>  

 <span data-ttu-id="bec7e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bec7e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bec7e-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="bec7e-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bec7e-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="bec7e-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bec7e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bec7e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bec7e-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bec7e-116">See also</span></span>

- [<span data-ttu-id="bec7e-117">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="bec7e-117">ICeeGen Interface</span></span>](iceegen-interface.md)
