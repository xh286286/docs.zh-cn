---
title: ICorPublishAppDomain::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomain::GetName
helpviewer_keywords:
- GetName method, ICorPublishAppDomain interface [.NET Framework debugging]
- ICorPublishAppDomain::GetName method [.NET Framework debugging]
ms.assetid: 6ef8ac9b-9803-4b65-8b13-25f3e0b1bc6b
topic_type:
- apiref
ms.openlocfilehash: d6b05333b9e02c4202c0fd9bdee9b5c055aa4da3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95694355"
---
# <a name="icorpublishappdomaingetname-method"></a><span data-ttu-id="4a94b-102">ICorPublishAppDomain::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="4a94b-102">ICorPublishAppDomain::GetName Method</span></span>

<span data-ttu-id="4a94b-103">获取此 [ICorPublishAppDomain](icorpublishappdomain-interface.md)所表示的应用程序域的名称。</span><span class="sxs-lookup"><span data-stu-id="4a94b-103">Gets the name of the application domain that is represented by this [ICorPublishAppDomain](icorpublishappdomain-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a94b-104">语法</span><span class="sxs-lookup"><span data-stu-id="4a94b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in]  ULONG32   cchName,
    [out] ULONG32   *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]
        WCHAR       *szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4a94b-105">参数</span><span class="sxs-lookup"><span data-stu-id="4a94b-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="4a94b-106">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="4a94b-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="4a94b-107">弄一个指针，它指向数组中返回的宽字符数，包括 null 字符 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="4a94b-107">[out] A pointer to the number of wide characters, including the null character, returned in the `szName` array.</span></span>  
  
 `szName`  
 <span data-ttu-id="4a94b-108">弄要在其中存储名称的数组。</span><span class="sxs-lookup"><span data-stu-id="4a94b-108">[out] An array in which to store the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4a94b-109">注解</span><span class="sxs-lookup"><span data-stu-id="4a94b-109">Remarks</span></span>  

 <span data-ttu-id="4a94b-110">如果 `szName` 为非 null，则该 `GetName` 方法将最多复制 `cchName` (个字符，包括 null 结束符) 入 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="4a94b-110">If `szName` is non-null, the `GetName` method copies up to `cchName` characters (including the null terminator) into `szName`.</span></span> <span data-ttu-id="4a94b-111">如果在中返回非 null，则 `pcchName` 名称中的实际字符数 (包括 null 结束符) 存储在 `szName` 数组中。</span><span class="sxs-lookup"><span data-stu-id="4a94b-111">If a non-null is returned in `pcchName`, the actual number of characters in the name (including the null terminator) is stored in the `szName` array.</span></span>  
  
 <span data-ttu-id="4a94b-112">`GetName`无论复制了多少个字符，该方法都将返回 S_OK HRESULT。</span><span class="sxs-lookup"><span data-stu-id="4a94b-112">The `GetName` method returns an S_OK HRESULT regardless of how many characters were copied.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a94b-113">要求</span><span class="sxs-lookup"><span data-stu-id="4a94b-113">Requirements</span></span>  

 <span data-ttu-id="4a94b-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a94b-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a94b-115">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="4a94b-115">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="4a94b-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a94b-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a94b-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a94b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a94b-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a94b-118">See also</span></span>

- [<span data-ttu-id="4a94b-119">ICorPublishAppDomain 接口</span><span class="sxs-lookup"><span data-stu-id="4a94b-119">ICorPublishAppDomain Interface</span></span>](icorpublishappdomain-interface.md)
