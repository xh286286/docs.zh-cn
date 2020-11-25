---
title: ISymUnmanagedAsyncMethod::GetAsyncStepInfo 方法
ms.date: 03/30/2017
ms.assetid: 3ef5b4b8-4ac7-4906-849b-f932c5e3db07
ms.openlocfilehash: f9392dae4119e59b4eb0fdb87e2b334b32b77109
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707251"
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfo-method"></a><span data-ttu-id="bdaff-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo 方法</span><span class="sxs-lookup"><span data-stu-id="bdaff-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo Method</span></span>

<span data-ttu-id="bdaff-103">请参阅 [DefineAsyncStepInfo 方法](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)。</span><span class="sxs-lookup"><span data-stu-id="bdaff-103">See [DefineAsyncStepInfo Method](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdaff-104">语法</span><span class="sxs-lookup"><span data-stu-id="bdaff-104">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfo(    [in] ULONG32 cStepInfo,    [out] ULONG32 *pcStepInfo,    [in, size_is(cStepInfo)] ULONG32 yieldOffsets[],    [in, size_is(cStepInfo)] ULONG32 breakpointOffset[],    [in, size_is(cStepInfo)] mdToken breakpointMethod[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bdaff-105">参数</span><span class="sxs-lookup"><span data-stu-id="bdaff-105">Parameters</span></span>  
  
|<span data-ttu-id="bdaff-106">参数</span><span class="sxs-lookup"><span data-stu-id="bdaff-106">Parameter</span></span>|<span data-ttu-id="bdaff-107">说明</span><span class="sxs-lookup"><span data-stu-id="bdaff-107">Description</span></span>|  
|---------------|-----------------|  
|`cStepInfo`||  
|`pcStepInfo`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="bdaff-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bdaff-108">Return Value</span></span>  

 <span data-ttu-id="bdaff-109">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="bdaff-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdaff-110">要求</span><span class="sxs-lookup"><span data-stu-id="bdaff-110">Requirements</span></span>  

 <span data-ttu-id="bdaff-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="bdaff-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdaff-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdaff-112">See also</span></span>

- [<span data-ttu-id="bdaff-113">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="bdaff-113">ISymUnmanagedAsyncMethod Interface</span></span>](isymunmanagedasyncmethod-interface.md)
