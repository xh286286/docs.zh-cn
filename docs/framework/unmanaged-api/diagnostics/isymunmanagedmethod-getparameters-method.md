---
title: ISymUnmanagedMethod::GetParameters 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetParameters
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetParameters
helpviewer_keywords:
- ISymUnmanagedMethod::GetParameters method [.NET Framework debugging]
- GetParameters method [.NET Framework debugging]
ms.assetid: 3a8074f1-facc-4a3f-bb9b-d6574fc2fc74
topic_type:
- apiref
ms.openlocfilehash: c66fd810ae4976bc0b5e04572b899465cebe4bbb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95699503"
---
# <a name="isymunmanagedmethodgetparameters-method"></a><span data-ttu-id="25959-102">ISymUnmanagedMethod::GetParameters 方法</span><span class="sxs-lookup"><span data-stu-id="25959-102">ISymUnmanagedMethod::GetParameters Method</span></span>

<span data-ttu-id="25959-103">获取此方法的参数。</span><span class="sxs-lookup"><span data-stu-id="25959-103">Gets the parameters for this method.</span></span> <span data-ttu-id="25959-104">按参数在方法签名中的定义顺序返回参数。</span><span class="sxs-lookup"><span data-stu-id="25959-104">The parameters are returned in the order in which they are defined within the method's signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25959-105">语法</span><span class="sxs-lookup"><span data-stu-id="25959-105">Syntax</span></span>  
  
```cpp  
HRESULT GetParameters(  
    [in]  ULONG32  cParams,  
    [out] ULONG32  *pcParams,  
    [out, size_is(cParams),  
        length_is(*pcParams)] ISymUnmanagedVariable*  params[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="25959-106">参数</span><span class="sxs-lookup"><span data-stu-id="25959-106">Parameters</span></span>  

 `cParams`  
 <span data-ttu-id="25959-107">[in] `params` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="25959-107">[in] The size of the `params` array.</span></span>  
  
 `pcParams`  
 <span data-ttu-id="25959-108">中指向的指针 `ULONG32` ，该指针接收包含参数所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="25959-108">[in] A pointer to a `ULONG32` that receives the size of the buffer that is required to contain the parameters.</span></span>  
  
 `params`  
 <span data-ttu-id="25959-109">弄指向接收参数的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="25959-109">[out] A pointer to the buffer that receives the parameters.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="25959-110">返回值</span><span class="sxs-lookup"><span data-stu-id="25959-110">Return Value</span></span>  

 <span data-ttu-id="25959-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="25959-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25959-112">要求</span><span class="sxs-lookup"><span data-stu-id="25959-112">Requirements</span></span>  

 <span data-ttu-id="25959-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="25959-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25959-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="25959-114">See also</span></span>

- [<span data-ttu-id="25959-115">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="25959-115">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
