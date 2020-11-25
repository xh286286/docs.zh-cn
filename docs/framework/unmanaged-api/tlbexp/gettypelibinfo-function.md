---
title: GetTypeLibInfo 函数
ms.date: 03/30/2017
api_name:
- GetTypeLibInfo
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- GetTypeLibInfo
helpviewer_keywords:
- GetTypeLibInfo function [.NET Framework]
ms.assetid: a1c4d165-9bdc-4ca8-940e-292d4ffcc338
topic_type:
- apiref
ms.openlocfilehash: e9f6ae9a0fcd6651395c54c2e44973e53668c1ac
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708317"
---
# <a name="gettypelibinfo-function"></a><span data-ttu-id="061ca-102">GetTypeLibInfo 函数</span><span class="sxs-lookup"><span data-stu-id="061ca-102">GetTypeLibInfo Function</span></span>

<span data-ttu-id="061ca-103">通过检查指定类型库的 [TLIBATTR](/windows/win32/api/oaidl/ns-oaidl-tlibattr) 结构来返回相关信息。</span><span class="sxs-lookup"><span data-stu-id="061ca-103">Returns information about the specified type library by examining its [TLIBATTR](/windows/win32/api/oaidl/ns-oaidl-tlibattr) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="061ca-104">语法</span><span class="sxs-lookup"><span data-stu-id="061ca-104">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeLibInfo(  
    [in]   LPWSTR     szFile,  
    [out]  GUID      *pTypeLibID,  
    [out]  LCID      *pTypeLibLCID,  
    [out]  SYSKIND   *pTypeLibPlatform,  
    [out]  USHORT    *pTypeLibMajorVer,  
    [out]  USHORT    *pTypeLibMinorVer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="061ca-105">参数</span><span class="sxs-lookup"><span data-stu-id="061ca-105">Parameters</span></span>  

 `szFile`  
 <span data-ttu-id="061ca-106">中类型库的文件名。</span><span class="sxs-lookup"><span data-stu-id="061ca-106">[in] The file name of the type library.</span></span>  
  
 `pTypeLibID`  
 <span data-ttu-id="061ca-107">弄类型库的 GUID。</span><span class="sxs-lookup"><span data-stu-id="061ca-107">[out] The GUID of the type library.</span></span>  
  
 `pTypeLibLCID`  
 <span data-ttu-id="061ca-108">弄类型库的本地化 ID。</span><span class="sxs-lookup"><span data-stu-id="061ca-108">[out] The localization ID of the type library.</span></span>  
  
 `pTypeLibPlatform`  
 <span data-ttu-id="061ca-109">弄标识库的目标操作系统的 [SYSKIND](/windows/win32/api/oaidl/ne-oaidl-syskind) 标志。</span><span class="sxs-lookup"><span data-stu-id="061ca-109">[out] A [SYSKIND](/windows/win32/api/oaidl/ne-oaidl-syskind) flag that identifies the target operating system for the type library.</span></span> <span data-ttu-id="061ca-110">常用值为 SYS_WIN32 和 SYS_WIN64。</span><span class="sxs-lookup"><span data-stu-id="061ca-110">Common values are SYS_WIN32 and SYS_WIN64.</span></span>  
  
 `pTypeLibMajorVer`  
 <span data-ttu-id="061ca-111">弄类型库的主版本号。</span><span class="sxs-lookup"><span data-stu-id="061ca-111">[out] The major version number of the type library.</span></span> <span data-ttu-id="061ca-112">例如，对于版本 *x. y*，主版本号是 *x*。</span><span class="sxs-lookup"><span data-stu-id="061ca-112">For example, for version *x.y*, the major version number is *x*.</span></span>  
  
 `pTypeLibMinorVer`  
 <span data-ttu-id="061ca-113">弄类型库的次版本号。</span><span class="sxs-lookup"><span data-stu-id="061ca-113">[out] The minor version number of the type library.</span></span> <span data-ttu-id="061ca-114">例如，对于版本 *x. y*，次版本号为 *y*。</span><span class="sxs-lookup"><span data-stu-id="061ca-114">For example, for version *x.y*, the minor version number is *y*.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="061ca-115">注解</span><span class="sxs-lookup"><span data-stu-id="061ca-115">Remarks</span></span>  

 <span data-ttu-id="061ca-116">`GetTypeLibInfo`函数由[Tlbexp.exe (类型库导出程序) ](../../tools/tlbexp-exe-type-library-exporter.md)调用。</span><span class="sxs-lookup"><span data-stu-id="061ca-116">The `GetTypeLibInfo` function is called by the [Tlbexp.exe (Type Library Exporter)](../../tools/tlbexp-exe-type-library-exporter.md).</span></span> <span data-ttu-id="061ca-117">此工具将生成一个类型库，该类型库描述公共语言运行时中的类型 (CLR) 程序集。</span><span class="sxs-lookup"><span data-stu-id="061ca-117">This tool generates a type library that describes the types in a common language runtime (CLR) assembly.</span></span>  
  
 <span data-ttu-id="061ca-118">如果任何参数为 null，则函数返回 `HRESULT` 的 `E_POINTER` 。</span><span class="sxs-lookup"><span data-stu-id="061ca-118">If any parameter is null, the function returns an `HRESULT` of `E_POINTER`.</span></span> <span data-ttu-id="061ca-119">否则，它将返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="061ca-119">Otherwise, it returns `S_OK`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="061ca-120">要求</span><span class="sxs-lookup"><span data-stu-id="061ca-120">Requirements</span></span>  

 <span data-ttu-id="061ca-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="061ca-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="061ca-122">**标头：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="061ca-122">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="061ca-123">**库：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="061ca-123">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="061ca-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="061ca-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="061ca-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="061ca-125">See also</span></span>

- [<span data-ttu-id="061ca-126">Tlbexp Helper 函数</span><span class="sxs-lookup"><span data-stu-id="061ca-126">Tlbexp Helper Functions</span></span>](index.md)
- [<span data-ttu-id="061ca-127">LoadTypeLibEx 函数</span><span class="sxs-lookup"><span data-stu-id="061ca-127">LoadTypeLibEx Function</span></span>](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
