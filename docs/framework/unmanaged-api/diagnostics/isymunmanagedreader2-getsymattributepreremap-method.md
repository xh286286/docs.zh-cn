---
title: ISymUnmanagedReader2::GetSymAttributePreRemap 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetSymAttributePreRemap
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetSymAttributePreRemap
helpviewer_keywords:
- GetSymAttributePreRemap method [.NET Framework debugging]
- ISymUnmanagedReader2::GetSymAttributePreRemap method [.NET Framework debugging]
ms.assetid: 7580d546-a709-40c5-ad02-aa70d774fd0b
topic_type:
- apiref
ms.openlocfilehash: 812c0d08930efff9140c6e897d3f93c4909e8464
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709084"
---
# <a name="isymunmanagedreader2getsymattributepreremap-method"></a><span data-ttu-id="e9772-102">ISymUnmanagedReader2::GetSymAttributePreRemap 方法</span><span class="sxs-lookup"><span data-stu-id="e9772-102">ISymUnmanagedReader2::GetSymAttributePreRemap Method</span></span>

<span data-ttu-id="e9772-103">根据名称获取自定义属性。</span><span class="sxs-lookup"><span data-stu-id="e9772-103">Gets a custom attribute based upon its name.</span></span> <span data-ttu-id="e9772-104">与元数据自定义特性不同，这些特性保存在符号存储区中。</span><span class="sxs-lookup"><span data-stu-id="e9772-104">Unlike metadata custom attributes, these attributes are held in the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9772-105">语法</span><span class="sxs-lookup"><span data-stu-id="e9772-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSymAttributePreRemap(  
    [in]  mdToken  parent,  
    [in]  WCHAR    *name,  
    [in]  ULONG32  cBuffer,  
    [out] ULONG32  *pcBuffer,  
    [out, size_is(cBuffer),  
        length_is(*pcBuffer)] BYTE buffer[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e9772-106">参数</span><span class="sxs-lookup"><span data-stu-id="e9772-106">Parameters</span></span>  

 `parent`  
 <span data-ttu-id="e9772-107">中父的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e9772-107">[in] The metadata token of the parent.</span></span>  
  
 `name`  
 <span data-ttu-id="e9772-108">中指向包含名称的的指针 `WCHAR` 。</span><span class="sxs-lookup"><span data-stu-id="e9772-108">[in] A pointer to a `WCHAR` that contains the name.</span></span>  
  
 `cBuffer`  
 <span data-ttu-id="e9772-109">中 `ULONG32` 指示数组大小的 `buffer` 。</span><span class="sxs-lookup"><span data-stu-id="e9772-109">[in] A `ULONG32` that indicates the size of the `buffer` array.</span></span>  
  
 `pcBuffer`  
 <span data-ttu-id="e9772-110">弄指向的指针 `ULONG32` ，该指针接收包含特性字节所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="e9772-110">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the attribute bytes.</span></span>  
  
 `buffer`  
 <span data-ttu-id="e9772-111">弄指向接收属性字节的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="e9772-111">[out] A pointer to the buffer that receives the attribute bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e9772-112">返回值</span><span class="sxs-lookup"><span data-stu-id="e9772-112">Return Value</span></span>  

 <span data-ttu-id="e9772-113">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="e9772-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9772-114">要求</span><span class="sxs-lookup"><span data-stu-id="e9772-114">Requirements</span></span>  

 <span data-ttu-id="e9772-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="e9772-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9772-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9772-116">See also</span></span>

- [<span data-ttu-id="e9772-117">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="e9772-117">ISymUnmanagedReader2 Interface</span></span>](isymunmanagedreader2-interface.md)
