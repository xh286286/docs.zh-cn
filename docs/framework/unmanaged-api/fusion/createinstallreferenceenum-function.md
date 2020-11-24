---
title: CreateInstallReferenceEnum 函数
ms.date: 03/30/2017
api_name:
- CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateInstallReference
helpviewer_keywords:
- CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type:
- apiref
ms.openlocfilehash: 0f62b05ebbd8b27dba160c8281c1d40748c90fc9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95688830"
---
# <a name="createinstallreferenceenum-function"></a><span data-ttu-id="cb7be-102">CreateInstallReferenceEnum 函数</span><span class="sxs-lookup"><span data-stu-id="cb7be-102">CreateInstallReferenceEnum Function</span></span>

<span data-ttu-id="cb7be-103">获取一个指针，该指针指向表示应用程序对指定程序集的引用列表的 [IInstallReferenceEnum](iinstallreferenceenum-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="cb7be-103">Gets a pointer to an [IInstallReferenceEnum](iinstallreferenceenum-interface.md) instance that represents a list of an application's references to the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb7be-104">语法</span><span class="sxs-lookup"><span data-stu-id="cb7be-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="cb7be-105">参数</span><span class="sxs-lookup"><span data-stu-id="cb7be-105">Parameters</span></span>  

 `ppRefEnum`  
 <span data-ttu-id="cb7be-106">弄返回的 `IInstallReferenceEnum` 指针。</span><span class="sxs-lookup"><span data-stu-id="cb7be-106">[out] The returned `IInstallReferenceEnum` pointer.</span></span>  
  
 `pName`  
 <span data-ttu-id="cb7be-107">中标识要枚举其引用的程序集的 [IAssemblyName](iassemblyname-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb7be-107">[in] The [IAssemblyName](iassemblyname-interface.md) that identifies the assembly for which to enumerate references.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="cb7be-108">中影响枚举器行为的标志。</span><span class="sxs-lookup"><span data-stu-id="cb7be-108">[in] Flags that influence the enumerator's behavior.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="cb7be-109">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="cb7be-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="cb7be-110">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="cb7be-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cb7be-111">要求</span><span class="sxs-lookup"><span data-stu-id="cb7be-111">Requirements</span></span>  

 <span data-ttu-id="cb7be-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cb7be-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb7be-113">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="cb7be-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="cb7be-114">**库：** Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="cb7be-114">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="cb7be-115">使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="cb7be-115">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="cb7be-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb7be-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb7be-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb7be-117">See also</span></span>

- [<span data-ttu-id="cb7be-118">IInstallReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="cb7be-118">IInstallReferenceEnum Interface</span></span>](iinstallreferenceenum-interface.md)
- [<span data-ttu-id="cb7be-119">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="cb7be-119">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="cb7be-120">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="cb7be-120">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
