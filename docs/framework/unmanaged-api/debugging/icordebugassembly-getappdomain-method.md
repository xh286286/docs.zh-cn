---
title: ICorDebugAssembly::GetAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.GetAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::GetAppDomain
helpviewer_keywords:
- ICorDebugAssembly::GetAppDomain method [.NET Framework debugging]
- GetAppDomain method, ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 14e18510-23ac-4cba-9f96-c86147a2df9d
topic_type:
- apiref
ms.openlocfilehash: 55a798bcc575aee3f309c35eb454a0675e0cbd97
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95734070"
---
# <a name="icordebugassemblygetappdomain-method"></a><span data-ttu-id="c4a89-102">ICorDebugAssembly::GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="c4a89-102">ICorDebugAssembly::GetAppDomain Method</span></span>

<span data-ttu-id="c4a89-103">获取一个接口指针，该指针指向包含此实例的应用程序域 `ICorDebugAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="c4a89-103">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4a89-104">语法</span><span class="sxs-lookup"><span data-stu-id="c4a89-104">Syntax</span></span>  
  
```cpp  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c4a89-105">参数</span><span class="sxs-lookup"><span data-stu-id="c4a89-105">Parameters</span></span>  

 `ppAppDomain`  
 <span data-ttu-id="c4a89-106">弄一个指针，指向表示应用程序域的 ICorDebugAppDomain 接口的地址。</span><span class="sxs-lookup"><span data-stu-id="c4a89-106">[out] A pointer to the address of an ICorDebugAppDomain interface that represents the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c4a89-107">注解</span><span class="sxs-lookup"><span data-stu-id="c4a89-107">Remarks</span></span>  

 <span data-ttu-id="c4a89-108">如果此程序集是系统程序集，则 `GetAppDomain` 返回 null。</span><span class="sxs-lookup"><span data-stu-id="c4a89-108">If this assembly is the system assembly, `GetAppDomain` returns null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4a89-109">要求</span><span class="sxs-lookup"><span data-stu-id="c4a89-109">Requirements</span></span>  

 <span data-ttu-id="c4a89-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c4a89-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4a89-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c4a89-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c4a89-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c4a89-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c4a89-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4a89-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
