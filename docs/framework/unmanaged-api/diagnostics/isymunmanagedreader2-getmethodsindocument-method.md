---
title: ISymUnmanagedReader2::GetMethodsInDocument 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetMethodsInDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument
helpviewer_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument method [.NET Framework debugging]
- GetMethodsInDocument method [.NET Framework debugging]
ms.assetid: c7ae84d6-81e8-4cb7-a1f9-d48b6cde5d79
topic_type:
- apiref
ms.openlocfilehash: 2e7eb183200c6e6de8ee18b58aab457c7e7bf2eb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675745"
---
# <a name="isymunmanagedreader2getmethodsindocument-method"></a><span data-ttu-id="27625-102">ISymUnmanagedReader2::GetMethodsInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="27625-102">ISymUnmanagedReader2::GetMethodsInDocument Method</span></span>

<span data-ttu-id="27625-103">获取所提供文档中包含行信息的每个方法。</span><span class="sxs-lookup"><span data-stu-id="27625-103">Gets every method that has line information in the provided document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27625-104">语法</span><span class="sxs-lookup"><span data-stu-id="27625-104">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodsInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is(cMethod),  
        length_is(*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="27625-105">参数</span><span class="sxs-lookup"><span data-stu-id="27625-105">Parameters</span></span>  

 `document`  
 <span data-ttu-id="27625-106">中指向文档的指针。</span><span class="sxs-lookup"><span data-stu-id="27625-106">[in] A pointer to the document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="27625-107">中 `ULONG32` 指示数组大小的  `pRetVal` 。</span><span class="sxs-lookup"><span data-stu-id="27625-107">[in] A `ULONG32` that indicates the size of the  `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="27625-108">弄指向的指针 `ULONG32` ，该指针接收包含方法所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="27625-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the methods.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="27625-109">弄指向接收方法的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="27625-109">[out] A pointer to the buffer that receives the methods.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="27625-110">返回值</span><span class="sxs-lookup"><span data-stu-id="27625-110">Return Value</span></span>  

 <span data-ttu-id="27625-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="27625-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27625-112">要求</span><span class="sxs-lookup"><span data-stu-id="27625-112">Requirements</span></span>  

 <span data-ttu-id="27625-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="27625-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27625-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27625-114">See also</span></span>

- [<span data-ttu-id="27625-115">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="27625-115">ISymUnmanagedReader2 Interface</span></span>](isymunmanagedreader2-interface.md)
