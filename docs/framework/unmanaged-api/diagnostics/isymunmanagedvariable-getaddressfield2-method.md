---
title: ISymUnmanagedVariable::GetAddressField2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField2
helpviewer_keywords:
- GetAddressField2 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField2 method [.NET Framework debugging]
ms.assetid: 1f25b294-72b6-4882-a49b-6c9d364b6008
topic_type:
- apiref
ms.openlocfilehash: 858341d5b8b1b3ecbe9dd5bd39a38f9cfd0d08dc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714167"
---
# <a name="isymunmanagedvariablegetaddressfield2-method"></a><span data-ttu-id="04716-102">ISymUnmanagedVariable::GetAddressField2 方法</span><span class="sxs-lookup"><span data-stu-id="04716-102">ISymUnmanagedVariable::GetAddressField2 Method</span></span>

<span data-ttu-id="04716-103">获取此变量的第二个地址字段。</span><span class="sxs-lookup"><span data-stu-id="04716-103">Gets the second address field for this variable.</span></span> <span data-ttu-id="04716-104">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="04716-104">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04716-105">语法</span><span class="sxs-lookup"><span data-stu-id="04716-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressField2(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="04716-106">参数</span><span class="sxs-lookup"><span data-stu-id="04716-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="04716-107">弄指向的指针 `ULONG32` ，该指针接收第二个地址字段。</span><span class="sxs-lookup"><span data-stu-id="04716-107">[out] A pointer to a `ULONG32` that receives the second address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="04716-108">返回值</span><span class="sxs-lookup"><span data-stu-id="04716-108">Return Value</span></span>  

 <span data-ttu-id="04716-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="04716-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04716-110">要求</span><span class="sxs-lookup"><span data-stu-id="04716-110">Requirements</span></span>  

 <span data-ttu-id="04716-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="04716-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04716-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04716-112">See also</span></span>

- [<span data-ttu-id="04716-113">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="04716-113">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
- [<span data-ttu-id="04716-114">GetAddressField1 方法</span><span class="sxs-lookup"><span data-stu-id="04716-114">GetAddressField1 Method</span></span>](isymunmanagedvariable-getaddressfield1-method.md)
- [<span data-ttu-id="04716-115">GetAddressField3 方法</span><span class="sxs-lookup"><span data-stu-id="04716-115">GetAddressField3 Method</span></span>](isymunmanagedvariable-getaddressfield3-method.md)
- [<span data-ttu-id="04716-116">GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="04716-116">GetAddressKind Method</span></span>](isymunmanagedvariable-getaddresskind-method.md)
