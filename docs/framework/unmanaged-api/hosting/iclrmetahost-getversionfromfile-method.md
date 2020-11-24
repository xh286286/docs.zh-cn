---
title: ICLRMetaHost::GetVersionFromFile 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.GetVersionFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::GetVersionFromFile
helpviewer_keywords:
- ICLRMetaHost::GetVersionFromFile method [.NET Framework hosting]
- GetVersionFromFile method [.NET Framework hosting]
ms.assetid: 55bb3eb4-f665-42fc-973c-465567570e82
topic_type:
- apiref
ms.openlocfilehash: f5e0ead41ebd13c259c24fa0c02bcc9a3b33e0fb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95689441"
---
# <a name="iclrmetahostgetversionfromfile-method"></a><span data-ttu-id="38893-102">ICLRMetaHost::GetVersionFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="38893-102">ICLRMetaHost::GetVersionFromFile Method</span></span>

<span data-ttu-id="38893-103">获取程序集的原始 .NET Framework 编译版本 (存储在元) 数据中的的文件路径。</span><span class="sxs-lookup"><span data-stu-id="38893-103">Gets an assembly's original .NET Framework compilation version (stored in the metadata), given its file path.</span></span> <span data-ttu-id="38893-104">此方法取代了 [GetFileVersion](getfileversion-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="38893-104">This method supersedes the [GetFileVersion](getfileversion-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38893-105">语法</span><span class="sxs-lookup"><span data-stu-id="38893-105">Syntax</span></span>  
  
```cpp  
HRESULT GetVersionFromFile (  
    [in] LPCWSTR pwzFilePath,  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBuffer);  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="38893-106">参数</span><span class="sxs-lookup"><span data-stu-id="38893-106">Parameters</span></span>  

 `pwzFilePath`  
 <span data-ttu-id="38893-107">中完整的程序集文件路径。</span><span class="sxs-lookup"><span data-stu-id="38893-107">[in] The complete assembly file path.</span></span>  
  
 `pwzbuffer`  
 <span data-ttu-id="38893-108">弄存储在元数据中的 .NET Framework 编译版本，格式为 "v *A*"。*B.*[。*X*] "。</span><span class="sxs-lookup"><span data-stu-id="38893-108">[out] The .NET Framework compilation version stored in the metadata, in the format "v *A*.*B*[.*X*]".</span></span> <span data-ttu-id="38893-109">*A*、 *B* 和 *X* 是与主版本、次版本和生成号对应的十进制数字。</span><span class="sxs-lookup"><span data-stu-id="38893-109">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="38893-110">此字符串的长度仅限 MAX_PATH。</span><span class="sxs-lookup"><span data-stu-id="38893-110">The length of this string is limited to MAX_PATH.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="38893-111">此输出匹配 .NET Framework 版本的目录名称，因为它显示在 C:\Windows\Microsoft.NET\Framework. 下。</span><span class="sxs-lookup"><span data-stu-id="38893-111">This output matches the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="38893-112">示例值为 "v1.0.3705"、"v 1.1.4322"、"v 2.0.50727" 和 "v4.0"。*X*"，其中 *X* 依赖于安装的生成号。</span><span class="sxs-lookup"><span data-stu-id="38893-112">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*X*", where *X* depends on the build number installed.</span></span> <span data-ttu-id="38893-113">请注意，"v" 前缀是必需的。</span><span class="sxs-lookup"><span data-stu-id="38893-113">Note that the "v" prefix is required.</span></span>  
  
 `pcchBuffer`  
 <span data-ttu-id="38893-114">[in，out] `pwzbuffer` 用于避免缓冲区溢出的的大小。</span><span class="sxs-lookup"><span data-stu-id="38893-114">[in, out] The size of `pwzbuffer` to avoid buffer overruns.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="38893-115">返回值</span><span class="sxs-lookup"><span data-stu-id="38893-115">Return Value</span></span>  

 <span data-ttu-id="38893-116">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="38893-116">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="38893-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="38893-117">HRESULT</span></span>|<span data-ttu-id="38893-118">说明</span><span class="sxs-lookup"><span data-stu-id="38893-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="38893-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="38893-119">S_OK</span></span>|<span data-ttu-id="38893-120">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="38893-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="38893-121">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="38893-121">E_POINTER</span></span>|<span data-ttu-id="38893-122">`pwzbuffer` 或 `pcchBuffer` 为 null。</span><span class="sxs-lookup"><span data-stu-id="38893-122">`pwzbuffer` or `pcchBuffer` is null.</span></span>|  
|<span data-ttu-id="38893-123">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span><span class="sxs-lookup"><span data-stu-id="38893-123">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span></span>|<span data-ttu-id="38893-124">缓冲区太小。</span><span class="sxs-lookup"><span data-stu-id="38893-124">The buffer is too small.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="38893-125">要求</span><span class="sxs-lookup"><span data-stu-id="38893-125">Requirements</span></span>  

 <span data-ttu-id="38893-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="38893-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38893-127">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="38893-127">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="38893-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="38893-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="38893-129">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38893-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38893-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38893-130">See also</span></span>

- [<span data-ttu-id="38893-131">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="38893-131">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="38893-132">承载</span><span class="sxs-lookup"><span data-stu-id="38893-132">Hosting</span></span>](index.md)
