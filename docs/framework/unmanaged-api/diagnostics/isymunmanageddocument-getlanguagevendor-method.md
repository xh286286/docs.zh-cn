---
title: ISymUnmanagedDocument::GetLanguageVendor 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguageVendor
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguageVendor
helpviewer_keywords:
- GetLanguageVendor method [.NET Framework debugging]
- ISymUnmanagedDocument::GetLanguageVendor method [.NET Framework debugging]
ms.assetid: 1d4b702e-4922-441d-8b44-03804284f70b
topic_type:
- apiref
ms.openlocfilehash: bac0f187409a191dda1ef635ec9b2da1aee25981
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700946"
---
# <a name="isymunmanageddocumentgetlanguagevendor-method"></a><span data-ttu-id="d5dd1-102">ISymUnmanagedDocument::GetLanguageVendor 方法</span><span class="sxs-lookup"><span data-stu-id="d5dd1-102">ISymUnmanagedDocument::GetLanguageVendor Method</span></span>

<span data-ttu-id="d5dd1-103">获取此文档的语言供应商。</span><span class="sxs-lookup"><span data-stu-id="d5dd1-103">Gets the language vendor of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5dd1-104">语法</span><span class="sxs-lookup"><span data-stu-id="d5dd1-104">Syntax</span></span>  
  
```cpp  
HRESULT GetLanguageVendor(  
    [out, retval]  GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5dd1-105">参数</span><span class="sxs-lookup"><span data-stu-id="d5dd1-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="d5dd1-106">弄指向接收语言供应商的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="d5dd1-106">[out] A pointer to a variable that receives the language vendor.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d5dd1-107">返回值</span><span class="sxs-lookup"><span data-stu-id="d5dd1-107">Return Value</span></span>  

 <span data-ttu-id="d5dd1-108">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="d5dd1-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5dd1-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5dd1-109">See also</span></span>

- [<span data-ttu-id="d5dd1-110">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="d5dd1-110">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
