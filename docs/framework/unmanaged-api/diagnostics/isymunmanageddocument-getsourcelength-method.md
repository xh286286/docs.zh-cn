---
title: ISymUnmanagedDocument::GetSourceLength 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceLength
helpviewer_keywords:
- GetSourceLength method [.NET Framework debugging]
- ISymUnmanagedDocument::GetSourceLength method [.NET Framework debugging]
ms.assetid: e087dbbb-f4fb-4fbe-8292-e4f1a14d0df2
topic_type:
- apiref
ms.openlocfilehash: c384fe6c4357c63bc56f9f9b1cc907dea64fddf7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95700933"
---
# <a name="isymunmanageddocumentgetsourcelength-method"></a><span data-ttu-id="973d9-102">ISymUnmanagedDocument::GetSourceLength 方法</span><span class="sxs-lookup"><span data-stu-id="973d9-102">ISymUnmanagedDocument::GetSourceLength Method</span></span>

<span data-ttu-id="973d9-103">获取嵌入源的长度（以字节表示）。</span><span class="sxs-lookup"><span data-stu-id="973d9-103">Gets the length, in bytes, of the embedded source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="973d9-104">语法</span><span class="sxs-lookup"><span data-stu-id="973d9-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSourceLength(  
    [out, retval]  ULONG32*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="973d9-105">参数</span><span class="sxs-lookup"><span data-stu-id="973d9-105">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="973d9-106">弄指向变量的指针，该变量指示嵌入源的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="973d9-106">[out] A pointer to a variable that indicates the length, in bytes, of the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="973d9-107">返回值</span><span class="sxs-lookup"><span data-stu-id="973d9-107">Return Value</span></span>  

 <span data-ttu-id="973d9-108">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="973d9-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="973d9-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="973d9-109">See also</span></span>

- [<span data-ttu-id="973d9-110">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="973d9-110">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
