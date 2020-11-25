---
title: ISymUnmanagedReader::GetSymbolStoreFileName 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetSymbolStoreFileName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetSymbolStoreFileName
helpviewer_keywords:
- GetSymbolStoreFileName method [.NET Framework debugging]
- ISymUnmanagedReader::GetSymbolStoreFileName method [.NET Framework debugging]
ms.assetid: c84f4846-9bc8-44a4-9a76-e39106d6d8b2
topic_type:
- apiref
ms.openlocfilehash: df503e44f20a0b1f02e2c609cc4b52712520faea
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95720563"
---
# <a name="isymunmanagedreadergetsymbolstorefilename-method"></a><span data-ttu-id="fab5a-102">ISymUnmanagedReader::GetSymbolStoreFileName 方法</span><span class="sxs-lookup"><span data-stu-id="fab5a-102">ISymUnmanagedReader::GetSymbolStoreFileName Method</span></span>

<span data-ttu-id="fab5a-103">提供符号存储区的磁盘上的文件名。</span><span class="sxs-lookup"><span data-stu-id="fab5a-103">Provides the on-disk file name of the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fab5a-104">语法</span><span class="sxs-lookup"><span data-stu-id="fab5a-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSymbolStoreFileName (  
    [in]  ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is (cchName),  
        length_is (*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fab5a-105">参数</span><span class="sxs-lookup"><span data-stu-id="fab5a-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="fab5a-106">中缓冲区的大小 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="fab5a-106">[in] The size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="fab5a-107">弄指向一个变量的指针，该变量接收返回的名称的长度 `szName` （包括 null 终止）。</span><span class="sxs-lookup"><span data-stu-id="fab5a-107">[out] A pointer to the variable that receives the length of the name returned in `szName`, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="fab5a-108">弄指向接收符号存储区文件名的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="fab5a-108">[out] A pointer to the variable that receives the file name of the symbol store.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fab5a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="fab5a-109">Return Value</span></span>  

 <span data-ttu-id="fab5a-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="fab5a-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fab5a-111">要求</span><span class="sxs-lookup"><span data-stu-id="fab5a-111">Requirements</span></span>  

 <span data-ttu-id="fab5a-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="fab5a-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fab5a-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fab5a-113">See also</span></span>

- [<span data-ttu-id="fab5a-114">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="fab5a-114">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
