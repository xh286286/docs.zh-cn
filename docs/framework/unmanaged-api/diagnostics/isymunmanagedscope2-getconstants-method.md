---
title: ISymUnmanagedScope2::GetConstants 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstants
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstants
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstants method [.NET Framework debugging]
- GetConstants method [.NET Framework debugging]
ms.assetid: f241b620-9ec5-42fd-92ef-3b22329db72a
topic_type:
- apiref
ms.openlocfilehash: df42e58a9bb3bf00b3fa4df45086dc2219658e25
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725841"
---
# <a name="isymunmanagedscope2getconstants-method"></a><span data-ttu-id="f14a1-102">ISymUnmanagedScope2::GetConstants 方法</span><span class="sxs-lookup"><span data-stu-id="f14a1-102">ISymUnmanagedScope2::GetConstants Method</span></span>

<span data-ttu-id="f14a1-103">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="f14a1-103">Gets the local constants defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f14a1-104">语法</span><span class="sxs-lookup"><span data-stu-id="f14a1-104">Syntax</span></span>  
  
```cpp  
HRESULT GetConstants(  
     [in]  ULONG32  cConstants,  
     [out] ULONG32  *pcConstants,  
     [out, size_is(cConstants),  
         length_is(*pcConstants)] ISymUnmanagedConstant*
             constants[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f14a1-105">参数</span><span class="sxs-lookup"><span data-stu-id="f14a1-105">Parameters</span></span>  

 `cConstants`  
 <span data-ttu-id="f14a1-106">中参数指向的缓冲区的长度 `pcConstants` 。</span><span class="sxs-lookup"><span data-stu-id="f14a1-106">[in] The length of the buffer that the `pcConstants` parameter points to.</span></span>  
  
 `pcConstants`  
 <span data-ttu-id="f14a1-107">弄指向的指针， `ULONG32` 该指针接收包含常量所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="f14a1-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the constants.</span></span>  
  
 `constants`  
 <span data-ttu-id="f14a1-108">弄用于存储常量的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="f14a1-108">[out] The buffer that stores the constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f14a1-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f14a1-109">Return Value</span></span>  

 <span data-ttu-id="f14a1-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="f14a1-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f14a1-111">要求</span><span class="sxs-lookup"><span data-stu-id="f14a1-111">Requirements</span></span>  

 <span data-ttu-id="f14a1-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f14a1-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f14a1-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f14a1-113">See also</span></span>

- [<span data-ttu-id="f14a1-114">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="f14a1-114">ISymUnmanagedScope2 Interface</span></span>](isymunmanagedscope2-interface.md)
