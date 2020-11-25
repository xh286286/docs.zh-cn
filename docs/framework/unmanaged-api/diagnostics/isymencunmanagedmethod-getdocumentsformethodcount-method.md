---
title: ISymENCUnmanagedMethod::GetDocumentsForMethodCount 方法
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetDocumentsForMethodCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount
helpviewer_keywords:
- GetDocumentsForMethodCount method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount method [.NET Framework debugging]
ms.assetid: cc1a823a-3ff3-4a33-b641-96edc93d2b17
topic_type:
- apiref
ms.openlocfilehash: 53897b6f964afb1f8ca95bc8f93c532e148ad129
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730508"
---
# <a name="isymencunmanagedmethodgetdocumentsformethodcount-method"></a><span data-ttu-id="2261c-102">ISymENCUnmanagedMethod::GetDocumentsForMethodCount 方法</span><span class="sxs-lookup"><span data-stu-id="2261c-102">ISymENCUnmanagedMethod::GetDocumentsForMethodCount Method</span></span>

<span data-ttu-id="2261c-103">获取此方法在中包含行的文档数。</span><span class="sxs-lookup"><span data-stu-id="2261c-103">Gets the number of documents that this method has lines in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2261c-104">语法</span><span class="sxs-lookup"><span data-stu-id="2261c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDocumentsForMethodCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2261c-105">参数</span><span class="sxs-lookup"><span data-stu-id="2261c-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="2261c-106">弄指向的指针 `ULONG32` ，该指针接收包含文档所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="2261c-106">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the documents.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2261c-107">返回值</span><span class="sxs-lookup"><span data-stu-id="2261c-107">Return Value</span></span>  

 <span data-ttu-id="2261c-108">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="2261c-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2261c-109">要求</span><span class="sxs-lookup"><span data-stu-id="2261c-109">Requirements</span></span>  

 <span data-ttu-id="2261c-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="2261c-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2261c-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2261c-111">See also</span></span>

- [<span data-ttu-id="2261c-112">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="2261c-112">ISymENCUnmanagedMethod Interface</span></span>](isymencunmanagedmethod-interface.md)
