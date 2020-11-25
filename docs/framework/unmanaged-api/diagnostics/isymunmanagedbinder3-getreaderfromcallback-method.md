---
title: ISymUnmanagedBinder3::GetReaderFromCallback 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3.GetReaderFromCallback
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3::GetReaderFromCallback
helpviewer_keywords:
- GetReaderFromCallback method [.NET Framework debugging]
- ISymUnmanagedBinder3::GetReaderFromCallback method [.NET Framework debugging]
ms.assetid: 4ef83bd2-3d8e-499e-8a12-d9d6fd6ced30
topic_type:
- apiref
ms.openlocfilehash: d48c2bdd55e487038048f432c5586d49f393118c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95706939"
---
# <a name="isymunmanagedbinder3getreaderfromcallback-method"></a><span data-ttu-id="44199-102">ISymUnmanagedBinder3::GetReaderFromCallback 方法</span><span class="sxs-lookup"><span data-stu-id="44199-102">ISymUnmanagedBinder3::GetReaderFromCallback Method</span></span>

<span data-ttu-id="44199-103">允许用户通过回调来实现或提供， `IID_IDiaReadExeAtRVACallback` `IID_IDiaReadExeAtOffsetCallback` 以从内存中获取调试目录信息。</span><span class="sxs-lookup"><span data-stu-id="44199-103">Allows the user to implement or supply via callback either an `IID_IDiaReadExeAtRVACallback` or `IID_IDiaReadExeAtOffsetCallback` to obtain the debug directory information from memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44199-104">语法</span><span class="sxs-lookup"><span data-stu-id="44199-104">Syntax</span></span>  
  
```cpp  
HRESULT GetReaderFromCallback(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [in]  ULONG32      searchPolicy,  
    [in]  IUnknown     *callback,  
    [out,retval] ISymUnmanagedReader  **pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="44199-105">参数</span><span class="sxs-lookup"><span data-stu-id="44199-105">Parameters</span></span>  

 `importer`  
 <span data-ttu-id="44199-106">中指向元数据导入接口的指针。</span><span class="sxs-lookup"><span data-stu-id="44199-106">[in] A pointer to the metadata import interface.</span></span>  
  
 `fileName`  
 <span data-ttu-id="44199-107">中指向文件名的指针。</span><span class="sxs-lookup"><span data-stu-id="44199-107">[in] A pointer to the file name.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="44199-108">中指向搜索路径的指针。</span><span class="sxs-lookup"><span data-stu-id="44199-108">[in] A pointer to the search path.</span></span>  
  
 `searchPolicy`  
 <span data-ttu-id="44199-109">中 [CorSymSearchPolicyAttributes](corsymsearchpolicyattributes-enumeration.md) 枚举的一个值，该值指定在搜索符号读取器时要使用的策略。</span><span class="sxs-lookup"><span data-stu-id="44199-109">[in] A value of the [CorSymSearchPolicyAttributes](corsymsearchpolicyattributes-enumeration.md) enumeration that specifies the policy to be used when doing a search for a symbol reader.</span></span>  
  
 `callback`  
 <span data-ttu-id="44199-110">中指向回调函数的指针。</span><span class="sxs-lookup"><span data-stu-id="44199-110">[in] A pointer to the callback function.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="44199-111">弄设置为返回的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="44199-111">[out] A pointer that is set to the returned [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="44199-112">返回值</span><span class="sxs-lookup"><span data-stu-id="44199-112">Return Value</span></span>  

 <span data-ttu-id="44199-113">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="44199-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44199-114">要求</span><span class="sxs-lookup"><span data-stu-id="44199-114">Requirements</span></span>  

 <span data-ttu-id="44199-115">**标头：** CorSym .idl</span><span class="sxs-lookup"><span data-stu-id="44199-115">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44199-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="44199-116">See also</span></span>

- [<span data-ttu-id="44199-117">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="44199-117">ISymUnmanagedBinder3 Interface</span></span>](isymunmanagedbinder3-interface.md)
