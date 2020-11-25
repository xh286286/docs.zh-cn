---
title: ClrCreateManagedInstance 函数
ms.date: 03/30/2017
api_name:
- ClrCreateManagedInstance
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- ClrCreateManagedInstance
helpviewer_keywords:
- ClrCreateManagedInstance function [.NET Framework hosting]
ms.assetid: 58ba42c0-4857-43bf-a039-73a4dc6544c2
topic_type:
- apiref
ms.openlocfilehash: 9aed79138499f1aa7b6fa3a28ad4505edd51b041
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731758"
---
# <a name="clrcreatemanagedinstance-function"></a><span data-ttu-id="39919-102">ClrCreateManagedInstance 函数</span><span class="sxs-lookup"><span data-stu-id="39919-102">ClrCreateManagedInstance Function</span></span>

<span data-ttu-id="39919-103">创建指定托管类型的实例。</span><span class="sxs-lookup"><span data-stu-id="39919-103">Creates an instance of the specified managed type.</span></span>  
  
 <span data-ttu-id="39919-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="39919-104">This function has been deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="39919-105">使用 COM 激活创建托管类型的实例，或使用宿主 (参阅 [.NET Framework 4 和 4.5) 中添加的 CLR 承载接口](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md) 。</span><span class="sxs-lookup"><span data-stu-id="39919-105">Use COM activation to create an instance of the managed type, or use hosting (see [CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39919-106">语法</span><span class="sxs-lookup"><span data-stu-id="39919-106">Syntax</span></span>  
  
```cpp  
STDAPI ClrCreateManagedInstance (  
    [in]  LPCWSTR  pTypeName,
    [in]  REFIID   riid,
    [out] void     **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="39919-107">参数</span><span class="sxs-lookup"><span data-stu-id="39919-107">Parameters</span></span>  

 `pTypeName`  
 <span data-ttu-id="39919-108">中一个指针，指向所请求的实例类型的名称。</span><span class="sxs-lookup"><span data-stu-id="39919-108">[in] A pointer to the name of the instance type being requested.</span></span>  
  
 `riid`  
 <span data-ttu-id="39919-109">中 `IID` 请求的实例类型的。</span><span class="sxs-lookup"><span data-stu-id="39919-109">[in] The `IID` of the instance type being requested.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="39919-110">弄指向调用方请求的托管类型实例的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="39919-110">[out] A pointer to a pointer to an instance of the managed type that was requested by the caller.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="39919-111">注解</span><span class="sxs-lookup"><span data-stu-id="39919-111">Remarks</span></span>  

 <span data-ttu-id="39919-112">公共语言运行时应已加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="39919-112">The common language runtime should already be loaded into a process.</span></span> <span data-ttu-id="39919-113">例如，在调用函数之前，可以使用对 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 函数的调用来加载该 `ClrCreateManagedInstance` 函数。</span><span class="sxs-lookup"><span data-stu-id="39919-113">For example, it can be loaded by using a call to the [CorBindToRuntimeEx](corbindtoruntimeex-function.md) function before the `ClrCreateManagedInstance` function is called.</span></span> <span data-ttu-id="39919-114">如果未加载运行时，则 `ClrCreateManagedInstance` 首先尝试加载运行时的 v v1.0.3705。</span><span class="sxs-lookup"><span data-stu-id="39919-114">If the runtime is not loaded, `ClrCreateManagedInstance` first tries to load v1.0.3705 of the runtime.</span></span> <span data-ttu-id="39919-115">如果失败，它将尝试加载最新版本的运行时。</span><span class="sxs-lookup"><span data-stu-id="39919-115">If that fails, it attempts to load the latest version of the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39919-116">要求</span><span class="sxs-lookup"><span data-stu-id="39919-116">Requirements</span></span>  

 <span data-ttu-id="39919-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="39919-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39919-118">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="39919-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="39919-119">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="39919-119">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="39919-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39919-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39919-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39919-121">See also</span></span>

- [<span data-ttu-id="39919-122">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="39919-122">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
- [<span data-ttu-id="39919-123">承载</span><span class="sxs-lookup"><span data-stu-id="39919-123">Hosting</span></span>](index.md)
