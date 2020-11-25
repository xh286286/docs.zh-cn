---
title: ISymUnmanagedScope2::GetConstantCount 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstantCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstantCount
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstantCount method [.NET Framework debugging]
- GetConstantCount method [.NET Framework debugging]
ms.assetid: 1e1f0be6-c4e8-4d6c-98cd-d5fa9f686e87
topic_type:
- apiref
ms.openlocfilehash: 59f4d85f1d8f24724a2d7eef332ac3b3387b7c91
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725854"
---
# <a name="isymunmanagedscope2getconstantcount-method"></a><span data-ttu-id="a0911-102">ISymUnmanagedScope2::GetConstantCount 方法</span><span class="sxs-lookup"><span data-stu-id="a0911-102">ISymUnmanagedScope2::GetConstantCount Method</span></span>

<span data-ttu-id="a0911-103">获取在此范围中定义的常量的计数。</span><span class="sxs-lookup"><span data-stu-id="a0911-103">Gets a count of the constants defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0911-104">语法</span><span class="sxs-lookup"><span data-stu-id="a0911-104">Syntax</span></span>  
  
```cpp  
HRESULT GetConstantCount(  
    [out, retval] ULONG32 *pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a0911-105">参数</span><span class="sxs-lookup"><span data-stu-id="a0911-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="a0911-106">弄指向的指针， `ULONG32` 该指针接收包含常量所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="a0911-106">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a0911-107">返回值</span><span class="sxs-lookup"><span data-stu-id="a0911-107">Return Value</span></span>  

 <span data-ttu-id="a0911-108">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="a0911-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0911-109">要求</span><span class="sxs-lookup"><span data-stu-id="a0911-109">Requirements</span></span>  

 <span data-ttu-id="a0911-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a0911-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0911-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a0911-111">See also</span></span>

- [<span data-ttu-id="a0911-112">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="a0911-112">ISymUnmanagedScope2 Interface</span></span>](isymunmanagedscope2-interface.md)
