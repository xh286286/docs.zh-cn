---
title: ICorRuntimeHost::MapFile 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.MapFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::MapFile
helpviewer_keywords:
- ICorRuntimeHost::MapFile method [.NET Framework hosting]
- MapFile method [.NET Framework hosting]
ms.assetid: 45ae0502-0a31-4342-b7e3-f36e1cf738f3
topic_type:
- apiref
ms.openlocfilehash: 60e1d5d49f6f8c6fec060d8751e94410986aa3fd
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95671377"
---
# <a name="icorruntimehostmapfile-method"></a><span data-ttu-id="86da4-102">ICorRuntimeHost::MapFile 方法</span><span class="sxs-lookup"><span data-stu-id="86da4-102">ICorRuntimeHost::MapFile Method</span></span>

<span data-ttu-id="86da4-103">将指定的文件映射到内存。</span><span class="sxs-lookup"><span data-stu-id="86da4-103">Maps the specified file into memory.</span></span> <span data-ttu-id="86da4-104">此方法已过时。</span><span class="sxs-lookup"><span data-stu-id="86da4-104">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86da4-105">语法</span><span class="sxs-lookup"><span data-stu-id="86da4-105">Syntax</span></span>  
  
```cpp  
HRESULT MapFile(  
    [in]  HANDLE    hFile,  
    [out] HMODULE*  hMapAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86da4-106">参数</span><span class="sxs-lookup"><span data-stu-id="86da4-106">Parameters</span></span>  

 `hFile`  
 <span data-ttu-id="86da4-107">中要映射的文件的句柄。</span><span class="sxs-lookup"><span data-stu-id="86da4-107">[in] The handle of the file to be mapped.</span></span>  
  
 `hMapAddress`  
 <span data-ttu-id="86da4-108">弄开始映射文件的起始内存地址。</span><span class="sxs-lookup"><span data-stu-id="86da4-108">[out] The starting memory address at which to begin mapping the file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86da4-109">要求</span><span class="sxs-lookup"><span data-stu-id="86da4-109">Requirements</span></span>  

 <span data-ttu-id="86da4-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="86da4-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86da4-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="86da4-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="86da4-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="86da4-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="86da4-113">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="86da4-113">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86da4-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="86da4-114">See also</span></span>

- [<span data-ttu-id="86da4-115">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="86da4-115">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
