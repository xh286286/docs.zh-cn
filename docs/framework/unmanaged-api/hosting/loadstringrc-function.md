---
title: LoadStringRC 函数
ms.date: 03/30/2017
api_name:
- LoadStringRC
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- LoadStringRC
helpviewer_keywords:
- LoadStringRC function [.NET Framework hosting]
ms.assetid: 752e49b4-987c-4c28-a118-1a0c1ed510c5
topic_type:
- apiref
ms.openlocfilehash: 16f95f8fce20f2cf46d4cda214e4494bd288bf60
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727544"
---
# <a name="loadstringrc-function"></a><span data-ttu-id="932ce-102">LoadStringRC 函数</span><span class="sxs-lookup"><span data-stu-id="932ce-102">LoadStringRC Function</span></span>

<span data-ttu-id="932ce-103">使用当前线程的默认区域性将 HRESULT 值转换为错误消息。</span><span class="sxs-lookup"><span data-stu-id="932ce-103">Translates an HRESULT value into an error message by using the default culture of the current thread.</span></span>  
  
 <span data-ttu-id="932ce-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="932ce-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="932ce-105">语法</span><span class="sxs-lookup"><span data-stu-id="932ce-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadStringRC (  
    [in]  UINT    iResourceID,
    [out] LPWSTR  szBuffer,
    [in]  int     iMax,
    [in]  int     bQuiet  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="932ce-106">参数</span><span class="sxs-lookup"><span data-stu-id="932ce-106">Parameters</span></span>  

 `iResourceID`  
 <span data-ttu-id="932ce-107">中HRESULT。</span><span class="sxs-lookup"><span data-stu-id="932ce-107">[in] An HRESULT.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="932ce-108">弄一个缓冲区，其中包含成功完成后的错误消息。</span><span class="sxs-lookup"><span data-stu-id="932ce-108">[out] A buffer that contains the error message upon successful completion.</span></span>  
  
 `iMax`  
 <span data-ttu-id="932ce-109">中错误消息缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="932ce-109">[in] The size of the error message buffer.</span></span>  
  
 `bQuiet`  
 <span data-ttu-id="932ce-110">中掉.</span><span class="sxs-lookup"><span data-stu-id="932ce-110">[in] Ignored.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="932ce-111">返回值</span><span class="sxs-lookup"><span data-stu-id="932ce-111">Return Value</span></span>  

 <span data-ttu-id="932ce-112">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="932ce-112">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="932ce-113">返回代码</span><span class="sxs-lookup"><span data-stu-id="932ce-113">Return code</span></span>|<span data-ttu-id="932ce-114">说明</span><span class="sxs-lookup"><span data-stu-id="932ce-114">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="932ce-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="932ce-115">S_OK</span></span>|<span data-ttu-id="932ce-116">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="932ce-116">The method completed successfully.</span></span>|  
|<span data-ttu-id="932ce-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="932ce-117">E_INVALIDARG</span></span>|<span data-ttu-id="932ce-118">`szBuffer` 为 null 或 `iMax` 为零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="932ce-118">`szBuffer` is null or `iMax` is zero (0).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="932ce-119">注解</span><span class="sxs-lookup"><span data-stu-id="932ce-119">Remarks</span></span>  

 <span data-ttu-id="932ce-120">如果该方法未成功完成，则 `szBuffer` 包含一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="932ce-120">If the method does not complete successfully, `szBuffer` contains an empty string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="932ce-121">要求</span><span class="sxs-lookup"><span data-stu-id="932ce-121">Requirements</span></span>  

 <span data-ttu-id="932ce-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="932ce-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="932ce-123">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="932ce-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="932ce-124">**库：** MSCorEE.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="932ce-124">**Library:** MSCorEE.dll and Mscorwks.dll.</span></span> <span data-ttu-id="932ce-125">使用 MSCorEE.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="932ce-125">Use MSCorEE.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="932ce-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="932ce-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="932ce-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="932ce-127">See also</span></span>

- [<span data-ttu-id="932ce-128">LoadStringRCEx 函数</span><span class="sxs-lookup"><span data-stu-id="932ce-128">LoadStringRCEx Function</span></span>](loadstringrcex-function.md)
- [<span data-ttu-id="932ce-129">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="932ce-129">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
