---
title: ISymUnmanagedDocument::GetCheckSum 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocument::GetCheckSum method [.NET Framework debugging]
- GetCheckSum method [.NET Framework debugging]
ms.assetid: 9bc881b3-e2ce-48a7-ad69-17eaaa304120
topic_type:
- apiref
ms.openlocfilehash: 4030da31400b7075952d146e5d6740306863e9ad
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721083"
---
# <a name="isymunmanageddocumentgetchecksum-method"></a><span data-ttu-id="e745a-102">ISymUnmanagedDocument::GetCheckSum 方法</span><span class="sxs-lookup"><span data-stu-id="e745a-102">ISymUnmanagedDocument::GetCheckSum Method</span></span>

<span data-ttu-id="e745a-103">获取校验和。</span><span class="sxs-lookup"><span data-stu-id="e745a-103">Gets the checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e745a-104">语法</span><span class="sxs-lookup"><span data-stu-id="e745a-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCheckSum(  
    [in]  ULONG32  cData,  
    [out] ULONG32  *pcData,  
    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e745a-105">参数</span><span class="sxs-lookup"><span data-stu-id="e745a-105">Parameters</span></span>  

 `cData`  
 <span data-ttu-id="e745a-106">中参数所提供的缓冲区的长度 `data`</span><span class="sxs-lookup"><span data-stu-id="e745a-106">[in] The length of the buffer provided by the `data` parameter</span></span>  
  
 `pcData`  
 <span data-ttu-id="e745a-107">弄校验和的大小和长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="e745a-107">[out] The size and length of the checksum, in bytes.</span></span>  
  
 `data`  
 <span data-ttu-id="e745a-108">弄接收校验和的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="e745a-108">[out] The buffer that receives the checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e745a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="e745a-109">Return Value</span></span>  

 <span data-ttu-id="e745a-110">如果该方法成功，则 S_OK;否则为错误代码。</span><span class="sxs-lookup"><span data-stu-id="e745a-110">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e745a-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e745a-111">See also</span></span>

- [<span data-ttu-id="e745a-112">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="e745a-112">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
