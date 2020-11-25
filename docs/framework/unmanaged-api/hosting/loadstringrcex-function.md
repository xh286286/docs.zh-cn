---
title: LoadStringRCEx 函数
ms.date: 03/30/2017
api_name:
- LoadStringRCEx
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- LoadStringRCEx
helpviewer_keywords:
- LoadStringRCEx function [.NET Framework hosting]
ms.assetid: bc789636-ca14-4f07-8f77-9305874d7495
topic_type:
- apiref
ms.openlocfilehash: 1aa5c9f5dd7dd63e69c2eed1f6dd8ad6f007f01f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727531"
---
# <a name="loadstringrcex-function"></a><span data-ttu-id="3e90a-102">LoadStringRCEx 函数</span><span class="sxs-lookup"><span data-stu-id="3e90a-102">LoadStringRCEx Function</span></span>

<span data-ttu-id="3e90a-103">将 HRESULT 值转换为指定区域性的适当错误消息。</span><span class="sxs-lookup"><span data-stu-id="3e90a-103">Translates an HRESULT value to an appropriate error message for the specified culture.</span></span>  
  
 <span data-ttu-id="3e90a-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="3e90a-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e90a-105">语法</span><span class="sxs-lookup"><span data-stu-id="3e90a-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadStringRCEx (  
    [in]  LCID    lcid,
    [in]  UINT    iResouceID,
    [out] LPWSTR  szBuffer,
    [in]  int     iMax,
    [in]  int     bQuiet,
    [out] int    *pcwchUsed  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e90a-106">参数</span><span class="sxs-lookup"><span data-stu-id="3e90a-106">Parameters</span></span>  

 `lcid`  
 <span data-ttu-id="3e90a-107">中区域性标识符。</span><span class="sxs-lookup"><span data-stu-id="3e90a-107">[in] A culture identifier.</span></span> <span data-ttu-id="3e90a-108">为传递-1 `lcid` 以使用默认区域性。</span><span class="sxs-lookup"><span data-stu-id="3e90a-108">Pass -1 for `lcid` to use the default culture.</span></span>  
  
 `iResourceID`  
 <span data-ttu-id="3e90a-109">中HRESULT。</span><span class="sxs-lookup"><span data-stu-id="3e90a-109">[in] An HRESULT.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="3e90a-110">弄一个缓冲区，其中包含成功完成后的错误消息。</span><span class="sxs-lookup"><span data-stu-id="3e90a-110">[out] A buffer that contains the error message upon successful completion.</span></span>  
  
 `iMax`  
 <span data-ttu-id="3e90a-111">中错误消息缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="3e90a-111">[in] The size of the error message buffer.</span></span>  
  
 `bQuiet`  
 <span data-ttu-id="3e90a-112">中掉.</span><span class="sxs-lookup"><span data-stu-id="3e90a-112">[in] Ignored.</span></span>  
  
 `pcwchUsed`  
 <span data-ttu-id="3e90a-113">弄指向错误消息长度的指针。</span><span class="sxs-lookup"><span data-stu-id="3e90a-113">[out] A pointer to the length of the error message.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e90a-114">返回值</span><span class="sxs-lookup"><span data-stu-id="3e90a-114">Return Value</span></span>  

 <span data-ttu-id="3e90a-115">除以下值外，此方法还返回 Winerror.h 中定义的标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="3e90a-115">This method returns standard COM error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="3e90a-116">返回代码</span><span class="sxs-lookup"><span data-stu-id="3e90a-116">Return code</span></span>|<span data-ttu-id="3e90a-117">说明</span><span class="sxs-lookup"><span data-stu-id="3e90a-117">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="3e90a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e90a-118">S_OK</span></span>|<span data-ttu-id="3e90a-119">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="3e90a-119">The method completed successfully.</span></span>|  
|<span data-ttu-id="3e90a-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3e90a-120">E_INVALIDARG</span></span>|<span data-ttu-id="3e90a-121">`szBuffer` 为 null，或者 `iMax` 为零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="3e90a-121">`szBuffer` is null, or `iMax` is zero (0).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3e90a-122">注解</span><span class="sxs-lookup"><span data-stu-id="3e90a-122">Remarks</span></span>  

 <span data-ttu-id="3e90a-123">如果该方法未成功完成，则 `szBuffer` 包含一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="3e90a-123">If the method does not complete successfully, `szBuffer` contains an empty string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e90a-124">要求</span><span class="sxs-lookup"><span data-stu-id="3e90a-124">Requirements</span></span>  

 <span data-ttu-id="3e90a-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3e90a-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e90a-126">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3e90a-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3e90a-127">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3e90a-127">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3e90a-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e90a-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e90a-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3e90a-129">See also</span></span>

- <xref:System.Globalization.CultureInfo.LCID%2A?displayProperty=nameWithType>
- [<span data-ttu-id="3e90a-130">LoadStringRC 函数</span><span class="sxs-lookup"><span data-stu-id="3e90a-130">LoadStringRC Function</span></span>](loadstringrc-function.md)
- [<span data-ttu-id="3e90a-131">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="3e90a-131">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
