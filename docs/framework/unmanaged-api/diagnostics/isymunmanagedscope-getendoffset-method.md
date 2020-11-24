---
title: ISymUnmanagedScope::GetEndOffset 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetEndOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedScope::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 1d0b15c9-8059-435f-9fce-346a08b9bd36
topic_type:
- apiref
ms.openlocfilehash: 14e747e81e467019d464212e75513bdf98344916
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95678358"
---
# <a name="isymunmanagedscopegetendoffset-method"></a><span data-ttu-id="b927b-102">ISymUnmanagedScope::GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="b927b-102">ISymUnmanagedScope::GetEndOffset Method</span></span>

<span data-ttu-id="b927b-103">获取此范围的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="b927b-103">Gets the end offset for this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b927b-104">语法</span><span class="sxs-lookup"><span data-stu-id="b927b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b927b-105">参数</span><span class="sxs-lookup"><span data-stu-id="b927b-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="b927b-106">弄指向的指针 `ULONG32` ，该指针接收结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="b927b-106">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b927b-107">返回值</span><span class="sxs-lookup"><span data-stu-id="b927b-107">Return Value</span></span>  

 <span data-ttu-id="b927b-108">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="b927b-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b927b-109">要求</span><span class="sxs-lookup"><span data-stu-id="b927b-109">Requirements</span></span>  

 <span data-ttu-id="b927b-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="b927b-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b927b-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b927b-111">See also</span></span>

- [<span data-ttu-id="b927b-112">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="b927b-112">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
- [<span data-ttu-id="b927b-113">GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="b927b-113">GetStartOffset Method</span></span>](isymunmanagedscope-getstartoffset-method.md)
