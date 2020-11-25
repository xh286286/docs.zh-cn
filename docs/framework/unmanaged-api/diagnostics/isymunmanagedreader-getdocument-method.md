---
title: ISymUnmanagedReader::GetDocument 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetDocument
helpviewer_keywords:
- ISymUnmanagedReader::GetDocument method [.NET Framework debugging]
- GetDocument method [.NET Framework debugging]
ms.assetid: bb203853-6a6d-4027-b9e9-603a7f28b9d3
topic_type:
- apiref
ms.openlocfilehash: 4604d78f66b872a30457c51bf65890caf613c4fa
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707628"
---
# <a name="isymunmanagedreadergetdocument-method"></a><span data-ttu-id="dfca6-102">ISymUnmanagedReader::GetDocument 方法</span><span class="sxs-lookup"><span data-stu-id="dfca6-102">ISymUnmanagedReader::GetDocument Method</span></span>

<span data-ttu-id="dfca6-103">查找文档。</span><span class="sxs-lookup"><span data-stu-id="dfca6-103">Finds a document.</span></span> <span data-ttu-id="dfca6-104">文档语言、供应商和类型是可选的。</span><span class="sxs-lookup"><span data-stu-id="dfca6-104">The document language, vendor, and type are optional.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfca6-105">语法</span><span class="sxs-lookup"><span data-stu-id="dfca6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDocument (  
    [in]  WCHAR  *url,  
    [in]  GUID   language,  
    [in]  GUID   languageVendor,  
    [in]  GUID   documentType,  
    [out, retval] ISymUnmanagedDocument** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dfca6-106">参数</span><span class="sxs-lookup"><span data-stu-id="dfca6-106">Parameters</span></span>  

 `url`  
 <span data-ttu-id="dfca6-107">中标识文档的 URL。</span><span class="sxs-lookup"><span data-stu-id="dfca6-107">[in] The URL that identifies the document.</span></span>  
  
 `language`  
 <span data-ttu-id="dfca6-108">中文档语言。</span><span class="sxs-lookup"><span data-stu-id="dfca6-108">[in] The document language.</span></span> <span data-ttu-id="dfca6-109">此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="dfca6-109">This parameter is optional.</span></span>  
  
 `languageVendor`  
 <span data-ttu-id="dfca6-110">中文档语言的供应商标识。</span><span class="sxs-lookup"><span data-stu-id="dfca6-110">[in] The identity of the vendor for the document language.</span></span> <span data-ttu-id="dfca6-111">此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="dfca6-111">This parameter is optional.</span></span>  
  
 `documentType`  
 <span data-ttu-id="dfca6-112">中文档的类型。</span><span class="sxs-lookup"><span data-stu-id="dfca6-112">[in] The type of the document.</span></span> <span data-ttu-id="dfca6-113">此参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="dfca6-113">This parameter is optional.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="dfca6-114">弄指向返回的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="dfca6-114">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dfca6-115">返回值</span><span class="sxs-lookup"><span data-stu-id="dfca6-115">Return Value</span></span>  

 <span data-ttu-id="dfca6-116">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="dfca6-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfca6-117">要求</span><span class="sxs-lookup"><span data-stu-id="dfca6-117">Requirements</span></span>  

 <span data-ttu-id="dfca6-118">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="dfca6-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfca6-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dfca6-119">See also</span></span>

- [<span data-ttu-id="dfca6-120">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="dfca6-120">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
