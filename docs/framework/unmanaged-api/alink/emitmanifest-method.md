---
title: EmitManifest 方法
ms.date: 03/30/2017
api_name:
- EmitManifest
- IALink.EmitManifest
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitManifest
helpviewer_keywords:
- EmitManifest method
ms.assetid: fdebc1f3-b62e-4d9e-b775-8ccaa8ecb250
topic_type:
- apiref
ms.openlocfilehash: b1c005e58f18b03a7da5f3836f719b95c41bca95
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95684936"
---
# <a name="emitmanifest-method"></a><span data-ttu-id="f00a6-102">EmitManifest 方法</span><span class="sxs-lookup"><span data-stu-id="f00a6-102">EmitManifest Method</span></span>

<span data-ttu-id="f00a6-103">发出最终清单。</span><span class="sxs-lookup"><span data-stu-id="f00a6-103">Emits the final manifest.</span></span> <span data-ttu-id="f00a6-104">导入所有其他文件并设置所有选项后，调用此方法。</span><span class="sxs-lookup"><span data-stu-id="f00a6-104">Call this method after importing all other files and setting all options.</span></span> <span data-ttu-id="f00a6-105">不要对未绑定的模块调用此方法。</span><span class="sxs-lookup"><span data-stu-id="f00a6-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f00a6-106">语法</span><span class="sxs-lookup"><span data-stu-id="f00a6-106">Syntax</span></span>  
  
```cpp  
HRESULT EmitManifest(  
    mdAssembly   AssemblyID,  
    DWORD*       pdwReserveSize,  
    mdAssembly*  ptkManifest  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="f00a6-107">参数</span><span class="sxs-lookup"><span data-stu-id="f00a6-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="f00a6-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="f00a6-108">ID of the assembly.</span></span>  
  
 `pdwReserveSize`  
 <span data-ttu-id="f00a6-109">接收程序集文件中要保留的大小，从 [StrongNameSignatureSize 函数](../strong-naming/strongnamesignaturesize-function.md)检索。</span><span class="sxs-lookup"><span data-stu-id="f00a6-109">Receives the size to reserve in the assembly file, retrieved from [StrongNameSignatureSize Function](../strong-naming/strongnamesignaturesize-function.md).</span></span>  
  
 `ptkManifest`  
 <span data-ttu-id="f00a6-110">可以选择接收程序集清单标记。</span><span class="sxs-lookup"><span data-stu-id="f00a6-110">Optionally receives the assembly manifest token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f00a6-111">返回值</span><span class="sxs-lookup"><span data-stu-id="f00a6-111">Return Value</span></span>  

 <span data-ttu-id="f00a6-112">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="f00a6-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f00a6-113">要求</span><span class="sxs-lookup"><span data-stu-id="f00a6-113">Requirements</span></span>  

 <span data-ttu-id="f00a6-114">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="f00a6-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f00a6-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f00a6-115">See also</span></span>

- [<span data-ttu-id="f00a6-116">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="f00a6-116">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="f00a6-117">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="f00a6-117">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="f00a6-118">ALink API</span><span class="sxs-lookup"><span data-stu-id="f00a6-118">ALink API</span></span>](index.md)
