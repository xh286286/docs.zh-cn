---
title: ICorDebugFrame::GetCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCode
helpviewer_keywords:
- GetCode method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetCode method [.NET Framework debugging]
ms.assetid: fbaa0794-a031-4015-8beb-2749e47ac340
topic_type:
- apiref
ms.openlocfilehash: 29dc87bf465fc9751b5af795f7640b095e535e63
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95690377"
---
# <a name="icordebugframegetcode-method"></a><span data-ttu-id="188f2-102">ICorDebugFrame::GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="188f2-102">ICorDebugFrame::GetCode Method</span></span>

<span data-ttu-id="188f2-103">获取一个指针，该指针指向与此堆栈帧关联的代码。</span><span class="sxs-lookup"><span data-stu-id="188f2-103">Gets a pointer to the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="188f2-104">语法</span><span class="sxs-lookup"><span data-stu-id="188f2-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCode (  
    [out] ICorDebugCode      **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="188f2-105">参数</span><span class="sxs-lookup"><span data-stu-id="188f2-105">Parameters</span></span>  

 `ppCode`  
 <span data-ttu-id="188f2-106">弄指向 ICorDebugCode 对象的地址的指针，该对象表示与此帧关联的代码。</span><span class="sxs-lookup"><span data-stu-id="188f2-106">[out] A pointer to the address of an ICorDebugCode object that represents the code associated with this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="188f2-107">要求</span><span class="sxs-lookup"><span data-stu-id="188f2-107">Requirements</span></span>  

 <span data-ttu-id="188f2-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="188f2-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="188f2-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="188f2-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="188f2-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="188f2-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="188f2-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="188f2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
