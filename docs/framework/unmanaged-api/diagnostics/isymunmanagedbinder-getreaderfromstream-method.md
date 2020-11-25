---
title: ISymUnmanagedBinder::GetReaderFromStream 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder.GetReaderFromStream
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder::GetReaderFromStream
helpviewer_keywords:
- ISymUnmanagedBinder::GetReaderFromStream method [.NET Framework debugging]
- GetReaderFromStream method [.NET Framework debugging]
ms.assetid: aa38efd4-de7e-4482-a5d3-adc152093460
topic_type:
- apiref
ms.openlocfilehash: 2d927b02b7deebecb53a2218e2ec0275a07307b4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706952"
---
# <a name="isymunmanagedbindergetreaderfromstream-method"></a><span data-ttu-id="ed056-102">ISymUnmanagedBinder::GetReaderFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="ed056-102">ISymUnmanagedBinder::GetReaderFromStream Method</span></span>

<span data-ttu-id="ed056-103">给定元数据接口和包含符号存储区的流时，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将从给定的符号存储区中读取调试符号。</span><span class="sxs-lookup"><span data-stu-id="ed056-103">Given a metadata interface and a stream that contains the symbol store, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols from the given symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed056-104">语法</span><span class="sxs-lookup"><span data-stu-id="ed056-104">Syntax</span></span>  
  
```cpp  
HRESULT GetReaderFromStream(  
    [in]  IUnknown  *importer,  
    [in]  IStream   *pstream,  
    [out,retval] ISymUnmanagedReader **pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ed056-105">参数</span><span class="sxs-lookup"><span data-stu-id="ed056-105">Parameters</span></span>  

 `importer`  
 <span data-ttu-id="ed056-106">中指向元数据导入接口的指针。</span><span class="sxs-lookup"><span data-stu-id="ed056-106">[in] A pointer to the metadata import interface.</span></span>  
  
 `pstream`  
 <span data-ttu-id="ed056-107">中指向包含符号存储区的流的指针。</span><span class="sxs-lookup"><span data-stu-id="ed056-107">[in] A pointer to the stream that contains the symbol store.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="ed056-108">弄设置为返回的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="ed056-108">[out] A pointer that is set to the returned [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ed056-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ed056-109">Return Value</span></span>  

 <span data-ttu-id="ed056-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="ed056-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed056-111">要求</span><span class="sxs-lookup"><span data-stu-id="ed056-111">Requirements</span></span>  

 <span data-ttu-id="ed056-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ed056-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed056-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed056-113">See also</span></span>

- [<span data-ttu-id="ed056-114">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="ed056-114">ISymUnmanagedBinder Interface</span></span>](isymunmanagedbinder-interface.md)
