---
title: ISymUnmanagedVariable::GetAddressField3 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField3
helpviewer_keywords:
- ISymUnmanagedVariable::GetAddressField3 method [.NET Framework debugging]
- GetAddressField3 method [.NET Framework debugging]
ms.assetid: 4d834721-ad8d-439d-b356-c6b4aef022fc
topic_type:
- apiref
ms.openlocfilehash: 13746c4ac6322a401e547c1c7acc99c0eda9accf
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95723332"
---
# <a name="isymunmanagedvariablegetaddressfield3-method"></a><span data-ttu-id="51c06-102">ISymUnmanagedVariable::GetAddressField3 方法</span><span class="sxs-lookup"><span data-stu-id="51c06-102">ISymUnmanagedVariable::GetAddressField3 Method</span></span>

<span data-ttu-id="51c06-103">获取此变量的第三个地址字段。</span><span class="sxs-lookup"><span data-stu-id="51c06-103">Gets the third address field for this variable.</span></span> <span data-ttu-id="51c06-104">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="51c06-104">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51c06-105">语法</span><span class="sxs-lookup"><span data-stu-id="51c06-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressField3(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="51c06-106">参数</span><span class="sxs-lookup"><span data-stu-id="51c06-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="51c06-107">弄指向的指针 `ULONG32` ，该指针接收第三个地址字段。</span><span class="sxs-lookup"><span data-stu-id="51c06-107">[out] A pointer to a `ULONG32` that receives the third address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="51c06-108">返回值</span><span class="sxs-lookup"><span data-stu-id="51c06-108">Return Value</span></span>  

 <span data-ttu-id="51c06-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="51c06-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51c06-110">要求</span><span class="sxs-lookup"><span data-stu-id="51c06-110">Requirements</span></span>  

 <span data-ttu-id="51c06-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="51c06-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51c06-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="51c06-112">See also</span></span>

- [<span data-ttu-id="51c06-113">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="51c06-113">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
- [<span data-ttu-id="51c06-114">GetAddressField1 方法</span><span class="sxs-lookup"><span data-stu-id="51c06-114">GetAddressField1 Method</span></span>](isymunmanagedvariable-getaddressfield1-method.md)
- [<span data-ttu-id="51c06-115">GetAddressField2 方法</span><span class="sxs-lookup"><span data-stu-id="51c06-115">GetAddressField2 Method</span></span>](isymunmanagedvariable-getaddressfield2-method.md)
- [<span data-ttu-id="51c06-116">GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="51c06-116">GetAddressKind Method</span></span>](isymunmanagedvariable-getaddresskind-method.md)
