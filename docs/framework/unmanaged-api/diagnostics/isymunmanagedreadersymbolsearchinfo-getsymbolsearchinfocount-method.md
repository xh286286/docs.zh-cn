---
title: ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo.GetSymbolSearchInfoCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount
helpviewer_keywords:
- GetSymbolSearchInfoCount method [.NET Framework debugging]
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount method [.NET Framework debugging]
ms.assetid: 4068b6ec-525f-4446-8818-0296178cbd19
topic_type:
- apiref
ms.openlocfilehash: 5883b35bb3f1fec24ec108c9839501f0e81881fc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708863"
---
# <a name="isymunmanagedreadersymbolsearchinfogetsymbolsearchinfocount-method"></a><span data-ttu-id="a5b35-102">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="a5b35-102">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount Method</span></span>

<span data-ttu-id="a5b35-103">获取符号搜索信息的计数。</span><span class="sxs-lookup"><span data-stu-id="a5b35-103">Gets a count of symbol search information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5b35-104">语法</span><span class="sxs-lookup"><span data-stu-id="a5b35-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSymbolSearchInfoCount(  
    [out] ULONG32 *pcSearchInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a5b35-105">参数</span><span class="sxs-lookup"><span data-stu-id="a5b35-105">Parameters</span></span>  

 `pcSearchInfo`  
 <span data-ttu-id="a5b35-106">] out] 指向的指针 `ULONG32` ，该指针接收包含搜索信息所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="a5b35-106">]out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the search information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a5b35-107">返回值</span><span class="sxs-lookup"><span data-stu-id="a5b35-107">Return Value</span></span>  

 <span data-ttu-id="a5b35-108">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="a5b35-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5b35-109">要求</span><span class="sxs-lookup"><span data-stu-id="a5b35-109">Requirements</span></span>  

 <span data-ttu-id="a5b35-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a5b35-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5b35-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a5b35-111">See also</span></span>

- [<span data-ttu-id="a5b35-112">ISymUnmanagedReaderSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="a5b35-112">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](isymunmanagedreadersymbolsearchinfo-interface.md)
