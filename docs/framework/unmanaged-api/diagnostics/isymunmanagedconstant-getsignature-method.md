---
title: ISymUnmanagedConstant::GetSignature 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetSignature
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetSignature
helpviewer_keywords:
- GetSignature method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetSignature method [.NET Framework debugging]
ms.assetid: 3eb41151-a228-43e3-ba8f-e6dd3ceb8542
topic_type:
- apiref
ms.openlocfilehash: 4436e4528c1dc486eb5c443c5a9467ac69a26c7d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706926"
---
# <a name="isymunmanagedconstantgetsignature-method"></a><span data-ttu-id="07c49-102">ISymUnmanagedConstant::GetSignature 方法</span><span class="sxs-lookup"><span data-stu-id="07c49-102">ISymUnmanagedConstant::GetSignature Method</span></span>

<span data-ttu-id="07c49-103">获取常量的签名。</span><span class="sxs-lookup"><span data-stu-id="07c49-103">Gets the signature of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07c49-104">语法</span><span class="sxs-lookup"><span data-stu-id="07c49-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="07c49-105">参数</span><span class="sxs-lookup"><span data-stu-id="07c49-105">Parameters</span></span>  

 `cSig`  
 <span data-ttu-id="07c49-106">中参数指向的缓冲区的长度 `pcSig` 。</span><span class="sxs-lookup"><span data-stu-id="07c49-106">[in] The length of the buffer that the `pcSig` parameter points to.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="07c49-107">弄指向的指针， `ULONG32` 该指针接收包含签名所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="07c49-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="07c49-108">弄存储签名的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="07c49-108">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="07c49-109">返回值</span><span class="sxs-lookup"><span data-stu-id="07c49-109">Return Value</span></span>  

 <span data-ttu-id="07c49-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="07c49-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07c49-111">要求</span><span class="sxs-lookup"><span data-stu-id="07c49-111">Requirements</span></span>  

 <span data-ttu-id="07c49-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="07c49-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07c49-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="07c49-113">See also</span></span>

- [<span data-ttu-id="07c49-114">ISymUnmanagedConstant 接口</span><span class="sxs-lookup"><span data-stu-id="07c49-114">ISymUnmanagedConstant Interface</span></span>](isymunmanagedconstant-interface.md)
- [<span data-ttu-id="07c49-115">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="07c49-115">GetName Method</span></span>](isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="07c49-116">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="07c49-116">GetValue Method</span></span>](isymunmanagedconstant-getvalue-method.md)
