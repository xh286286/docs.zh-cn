---
title: ISymUnmanagedWriter::DefineConstant 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineConstant
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineConstant
helpviewer_keywords:
- DefineConstant method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineConstant method [.NET Framework debugging]
ms.assetid: 9e986986-2223-4d5f-b040-85d716146924
topic_type:
- apiref
ms.openlocfilehash: 7c4589c3371d2c66279684a365cde102bef58c6e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727583"
---
# <a name="isymunmanagedwriterdefineconstant-method"></a><span data-ttu-id="64fa9-102">ISymUnmanagedWriter::DefineConstant 方法</span><span class="sxs-lookup"><span data-stu-id="64fa9-102">ISymUnmanagedWriter::DefineConstant Method</span></span>

<span data-ttu-id="64fa9-103">定义常数值的名称。</span><span class="sxs-lookup"><span data-stu-id="64fa9-103">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64fa9-104">语法</span><span class="sxs-lookup"><span data-stu-id="64fa9-104">Syntax</span></span>  
  
```cpp  
HRESULT DefineConstant(  
    [in] const WCHAR *name,  
    [in] VARIANT value,  
    [in] ULONG32 cSig,  
    [in, size_is(cSig)] unsigned char signature[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="64fa9-105">参数</span><span class="sxs-lookup"><span data-stu-id="64fa9-105">Parameters</span></span>  

 `name`  
 <span data-ttu-id="64fa9-106">中一个指针，指向用于 `WCHAR` 定义常量名称的。</span><span class="sxs-lookup"><span data-stu-id="64fa9-106">[in] A pointer to a `WCHAR` that defines the constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="64fa9-107">中常量的值。</span><span class="sxs-lookup"><span data-stu-id="64fa9-107">[in] The value of the constant.</span></span>  
  
 `cSig`  
 <span data-ttu-id="64fa9-108">[in] `signature` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="64fa9-108">[in] The size of the `signature` array.</span></span>  
  
 `signature`  
 <span data-ttu-id="64fa9-109">中常数的类型签名。</span><span class="sxs-lookup"><span data-stu-id="64fa9-109">[in] The type signature for the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="64fa9-110">返回值</span><span class="sxs-lookup"><span data-stu-id="64fa9-110">Return Value</span></span>  

 <span data-ttu-id="64fa9-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="64fa9-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64fa9-112">要求</span><span class="sxs-lookup"><span data-stu-id="64fa9-112">Requirements</span></span>  

 <span data-ttu-id="64fa9-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="64fa9-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64fa9-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64fa9-114">See also</span></span>

- [<span data-ttu-id="64fa9-115">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="64fa9-115">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="64fa9-116">DefineConstant2 方法</span><span class="sxs-lookup"><span data-stu-id="64fa9-116">DefineConstant2 Method</span></span>](isymunmanagedwriter2-defineconstant2-method.md)
