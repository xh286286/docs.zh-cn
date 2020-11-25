---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan 方法
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
ms.openlocfilehash: e4b09e6d89b3ba8ba3bf7e149d31a14a74b945b5
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723930"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a><span data-ttu-id="7d3df-102">ISymUnmanagedWriter5::MapTokenToSourceSpan 方法</span><span class="sxs-lookup"><span data-stu-id="7d3df-102">ISymUnmanagedWriter5::MapTokenToSourceSpan Method</span></span>

<span data-ttu-id="7d3df-103">将给定的元数据标记映射到指定源文件中的给定源行范围。</span><span class="sxs-lookup"><span data-stu-id="7d3df-103">Maps the given metadata token to the given source line span in the specified source file.</span></span>  
  
 <span data-ttu-id="7d3df-104">必须在对 [OpenMapTokensToSourceSpans 方法](isymunmanagedwriter5-openmaptokenstosourcespans-method.md) 和 [CloseMapTokensToSourceSpans 方法](isymunmanagedwriter5-closemaptokenstosourcespans-method.md)的调用之间调用。</span><span class="sxs-lookup"><span data-stu-id="7d3df-104">Must be called between calls to [OpenMapTokensToSourceSpans Method](isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d3df-105">语法</span><span class="sxs-lookup"><span data-stu-id="7d3df-105">Syntax</span></span>  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d3df-106">参数</span><span class="sxs-lookup"><span data-stu-id="7d3df-106">Parameters</span></span>  
  
|<span data-ttu-id="7d3df-107">参数</span><span class="sxs-lookup"><span data-stu-id="7d3df-107">Parameter</span></span>|<span data-ttu-id="7d3df-108">说明</span><span class="sxs-lookup"><span data-stu-id="7d3df-108">Description</span></span>|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a><span data-ttu-id="7d3df-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7d3df-109">Return Value</span></span>  

 <span data-ttu-id="7d3df-110">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="7d3df-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d3df-111">要求</span><span class="sxs-lookup"><span data-stu-id="7d3df-111">Requirements</span></span>  

 <span data-ttu-id="7d3df-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="7d3df-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d3df-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7d3df-113">See also</span></span>

- [<span data-ttu-id="7d3df-114">ISymUnmanagedWriter5 接口</span><span class="sxs-lookup"><span data-stu-id="7d3df-114">ISymUnmanagedWriter5 Interface</span></span>](isymunmanagedwriter5-interface.md)
