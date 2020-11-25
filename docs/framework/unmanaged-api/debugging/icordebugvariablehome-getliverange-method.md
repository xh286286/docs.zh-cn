---
title: IcorDebugVariableHome：： GetLiveRange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetLiveRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetLiveRange
helpviewer_keywords:
- ICorDebugVariableHome::GetLiveRange method [.NET Framework debugging]
- GetLiveRange method, ICorDebugVariableFrame interface [.NET Framework debugging]
ms.assetid: 87277e1a-1595-4729-9e25-d1c3ac18ce5f
topic_type:
- apiref
ms.openlocfilehash: 4d66d09e02b907281f64400b0c605a7b5c44d476
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731041"
---
# <a name="icordebugvariablehomegetliverange-method"></a><span data-ttu-id="99bca-102">IcorDebugVariableHome：： GetLiveRange 方法</span><span class="sxs-lookup"><span data-stu-id="99bca-102">IcorDebugVariableHome::GetLiveRange Method</span></span>

<span data-ttu-id="99bca-103">获取此变量的生存期的本机范围。</span><span class="sxs-lookup"><span data-stu-id="99bca-103">Gets the native range over which this variable is live.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99bca-104">语法</span><span class="sxs-lookup"><span data-stu-id="99bca-104">Syntax</span></span>  
  
```cpp  
HRESULT GetLiveRange(  
    [out] ULONG32* pStartOffset,  
    [out] ULONG32 *pEndOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="99bca-105">参数</span><span class="sxs-lookup"><span data-stu-id="99bca-105">Parameters</span></span>  

 `pStartOffset`  
 <span data-ttu-id="99bca-106">弄变量首次处于活动状态的逻辑偏移量。</span><span class="sxs-lookup"><span data-stu-id="99bca-106">[out] The logical offset at which the variable is first live.</span></span>  
  
 `pEndOffset`  
 <span data-ttu-id="99bca-107">弄紧跟在变量上一次生存点之后的逻辑偏移量。</span><span class="sxs-lookup"><span data-stu-id="99bca-107">[out] The logical offset immediately after the point at which the variable is last live.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99bca-108">要求</span><span class="sxs-lookup"><span data-stu-id="99bca-108">Requirements</span></span>  

 <span data-ttu-id="99bca-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="99bca-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="99bca-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="99bca-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="99bca-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="99bca-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="99bca-112">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="99bca-112">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99bca-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99bca-113">See also</span></span>

- [<span data-ttu-id="99bca-114">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="99bca-114">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
