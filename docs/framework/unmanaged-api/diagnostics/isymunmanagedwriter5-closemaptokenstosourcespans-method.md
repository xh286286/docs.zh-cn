---
title: ISymUnmanagedWriter5::CloseMapTokensToSourceSpans 方法
ms.date: 03/30/2017
ms.assetid: f8a0c0a2-a11d-436c-aa85-bc110215cfd6
ms.openlocfilehash: b57174f9f76b174927b8f1997beac3dd1482583a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725906"
---
# <a name="isymunmanagedwriter5closemaptokenstosourcespans-method"></a><span data-ttu-id="5e0df-102">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans 方法</span><span class="sxs-lookup"><span data-stu-id="5e0df-102">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans Method</span></span>

<span data-ttu-id="5e0df-103">关闭 "特定自定义数据" 部分以获取令牌到源范围的映射信息。</span><span class="sxs-lookup"><span data-stu-id="5e0df-103">Close the special custom data section for token-to-source span mapping information.</span></span> <span data-ttu-id="5e0df-104">关闭后，不能再添加映射信息。</span><span class="sxs-lookup"><span data-stu-id="5e0df-104">After it is closed, no more mapping information can be added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e0df-105">语法</span><span class="sxs-lookup"><span data-stu-id="5e0df-105">Syntax</span></span>  
  
```idl  
HRESULT CloseMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="5e0df-106">返回值</span><span class="sxs-lookup"><span data-stu-id="5e0df-106">Return Value</span></span>  

 <span data-ttu-id="5e0df-107">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="5e0df-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e0df-108">要求</span><span class="sxs-lookup"><span data-stu-id="5e0df-108">Requirements</span></span>  

 <span data-ttu-id="5e0df-109">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="5e0df-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e0df-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5e0df-110">See also</span></span>

- [<span data-ttu-id="5e0df-111">ISymUnmanagedWriter5 接口</span><span class="sxs-lookup"><span data-stu-id="5e0df-111">ISymUnmanagedWriter5 Interface</span></span>](isymunmanagedwriter5-interface.md)
