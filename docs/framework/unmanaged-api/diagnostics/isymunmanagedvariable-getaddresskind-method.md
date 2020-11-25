---
title: ISymUnmanagedVariable::GetAddressKind 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressKind
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressKind
helpviewer_keywords:
- GetAddressKind method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressKind method [.NET Framework debugging]
ms.assetid: a71563c0-62f2-4eb4-970c-825d61827613
topic_type:
- apiref
ms.openlocfilehash: 6a7824949edc905a3edcd58f60d40f8b1a40c53c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726907"
---
# <a name="isymunmanagedvariablegetaddresskind-method"></a><span data-ttu-id="77592-102">ISymUnmanagedVariable::GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="77592-102">ISymUnmanagedVariable::GetAddressKind Method</span></span>

<span data-ttu-id="77592-103">获取此变量的地址类型。</span><span class="sxs-lookup"><span data-stu-id="77592-103">Gets the kind of address of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77592-104">语法</span><span class="sxs-lookup"><span data-stu-id="77592-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressKind(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77592-105">参数</span><span class="sxs-lookup"><span data-stu-id="77592-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="77592-106">弄指向接收值的的指针 `ULONG32` 。</span><span class="sxs-lookup"><span data-stu-id="77592-106">[out] A pointer to a `ULONG32` that receives the value.</span></span> <span data-ttu-id="77592-107">可能的值是在 [CorSymAddrKind](corsymaddrkind-enumeration.md) 枚举中定义的。</span><span class="sxs-lookup"><span data-stu-id="77592-107">The possible values are defined in the [CorSymAddrKind](corsymaddrkind-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="77592-108">返回值</span><span class="sxs-lookup"><span data-stu-id="77592-108">Return Value</span></span>  

 <span data-ttu-id="77592-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="77592-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77592-110">要求</span><span class="sxs-lookup"><span data-stu-id="77592-110">Requirements</span></span>  

 <span data-ttu-id="77592-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="77592-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77592-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77592-112">See also</span></span>

- [<span data-ttu-id="77592-113">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="77592-113">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
