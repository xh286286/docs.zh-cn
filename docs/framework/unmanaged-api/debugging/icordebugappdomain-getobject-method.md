---
title: ICorDebugAppDomain::GetObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetObject
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetObject
helpviewer_keywords:
- ICorDebugAppDomain::GetObject method [.NET Framework debugging]
- GetObject method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 78232e6f-ae18-4cfa-a6cd-e79471cf9d76
topic_type:
- apiref
ms.openlocfilehash: a163667ea7eca1ed817d642efdb8fc4efa2a0651
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95676057"
---
# <a name="icordebugappdomaingetobject-method"></a><span data-ttu-id="86c7f-102">ICorDebugAppDomain::GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="86c7f-102">ICorDebugAppDomain::GetObject Method</span></span>

<span data-ttu-id="86c7f-103">获取 (CLR) 应用程序域的公共语言运行时的接口指针。</span><span class="sxs-lookup"><span data-stu-id="86c7f-103">Gets an interface pointer to the common language runtime (CLR) application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86c7f-104">语法</span><span class="sxs-lookup"><span data-stu-id="86c7f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86c7f-105">参数</span><span class="sxs-lookup"><span data-stu-id="86c7f-105">Parameters</span></span>  

 `ppObject`  
 <span data-ttu-id="86c7f-106">弄指向表示 CLR 应用程序域的 ICorDebugValue 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="86c7f-106">[out] A pointer to the address of an ICorDebugValue interface object that represents the CLR application domain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="86c7f-107">返回值</span><span class="sxs-lookup"><span data-stu-id="86c7f-107">Return Value</span></span>  

 <span data-ttu-id="86c7f-108">如果 <xref:System.AppDomain?displayProperty=nameWithType> 尚未为此应用程序域构造托管对象，则该方法将返回 `S_FALSE` ，并将放 `NULL` 入 `*ppObject` 。</span><span class="sxs-lookup"><span data-stu-id="86c7f-108">If a managed <xref:System.AppDomain?displayProperty=nameWithType> object hasn't been constructed for this application domain, the method returns `S_FALSE` and places `NULL` in `*ppObject`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="86c7f-109">注解</span><span class="sxs-lookup"><span data-stu-id="86c7f-109">Remarks</span></span>  

 <span data-ttu-id="86c7f-110">进程中的每个应用程序域在运行时中都可能有一个 <xref:System.AppDomain?displayProperty=nameWithType> 表示该对象的托管对象。</span><span class="sxs-lookup"><span data-stu-id="86c7f-110">Each application domain in a process may have a managed <xref:System.AppDomain?displayProperty=nameWithType> object in the runtime that represents it.</span></span> <span data-ttu-id="86c7f-111">此函数获取对应于此托管对象的 ICorDebugValue 接口对象 <xref:System.AppDomain?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="86c7f-111">This function gets an ICorDebugValue interface object that corresponds to this managed <xref:System.AppDomain?displayProperty=nameWithType> object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86c7f-112">要求</span><span class="sxs-lookup"><span data-stu-id="86c7f-112">Requirements</span></span>  

 <span data-ttu-id="86c7f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="86c7f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86c7f-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="86c7f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="86c7f-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="86c7f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="86c7f-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86c7f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>
