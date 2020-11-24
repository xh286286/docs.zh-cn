---
title: ISymUnmanagedDocument::GetDocumentType 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetDocumentType
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetDocumentType
helpviewer_keywords:
- ISymUnmanagedDocument::GetDocumentType method [.NET Framework debugging]
- GetDocumentType method [.NET Framework debugging]
ms.assetid: 2d381ab1-7e7c-4281-af2b-e54d879b3ef8
topic_type:
- apiref
ms.openlocfilehash: d30ee9318d76aaf3ad2cde789ae292aed54f457e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689675"
---
# <a name="isymunmanageddocumentgetdocumenttype-method"></a><span data-ttu-id="e3f6c-102">ISymUnmanagedDocument::GetDocumentType 方法</span><span class="sxs-lookup"><span data-stu-id="e3f6c-102">ISymUnmanagedDocument::GetDocumentType Method</span></span>

<span data-ttu-id="e3f6c-103">获取此文档的文档类型。</span><span class="sxs-lookup"><span data-stu-id="e3f6c-103">Gets the document type of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3f6c-104">语法</span><span class="sxs-lookup"><span data-stu-id="e3f6c-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDocumentType(  
    [out, retval] GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e3f6c-105">参数</span><span class="sxs-lookup"><span data-stu-id="e3f6c-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="e3f6c-106">弄指向接收文档类型的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="e3f6c-106">[out] Pointer to a variable that receives the document type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e3f6c-107">返回值</span><span class="sxs-lookup"><span data-stu-id="e3f6c-107">Return Value</span></span>  

 <span data-ttu-id="e3f6c-108">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e3f6c-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3f6c-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3f6c-109">See also</span></span>

- [<span data-ttu-id="e3f6c-110">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="e3f6c-110">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
