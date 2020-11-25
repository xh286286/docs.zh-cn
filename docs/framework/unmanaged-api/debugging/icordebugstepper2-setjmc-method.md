---
title: ICorDebugStepper2::SetJMC 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper2.SetJMC
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper2::SetJMC
helpviewer_keywords:
- ICorDebugStepper2::SetJMC method [.NET Framework debugging]
- SetJMC method [.NET Framework debugging]
ms.assetid: f5cdc135-6db4-4b32-9dd1-260ec58b774f
topic_type:
- apiref
ms.openlocfilehash: 1bbcbcfbb78d421f247a13f58070b68f701e4ed1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95697202"
---
# <a name="icordebugstepper2setjmc-method"></a><span data-ttu-id="91d2b-102">ICorDebugStepper2::SetJMC 方法</span><span class="sxs-lookup"><span data-stu-id="91d2b-102">ICorDebugStepper2::SetJMC Method</span></span>

<span data-ttu-id="91d2b-103">设置一个值，该值指定此 ICorDebugStepper 是否仅通过应用程序开发人员编写的代码执行步骤。</span><span class="sxs-lookup"><span data-stu-id="91d2b-103">Sets a value that specifies whether this ICorDebugStepper steps only through code that is authored by an application's developer.</span></span> <span data-ttu-id="91d2b-104">此过程也称为 (JMC) 调试的 "仅我的代码"。</span><span class="sxs-lookup"><span data-stu-id="91d2b-104">This process is also known as just my code (JMC) debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91d2b-105">语法</span><span class="sxs-lookup"><span data-stu-id="91d2b-105">Syntax</span></span>  
  
```cpp  
HRESULT SetJMC (  
    [in] BOOL    fIsJMCStepper  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="91d2b-106">参数</span><span class="sxs-lookup"><span data-stu-id="91d2b-106">Parameters</span></span>  

 `fIsJMCStepper`  
 <span data-ttu-id="91d2b-107">中如果设置为， `true` 则仅通过由应用程序开发人员编写的代码执行，否则设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="91d2b-107">[in] Set to `true` to step only through code that is authored by an application's developer; otherwise, set to `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91d2b-108">要求</span><span class="sxs-lookup"><span data-stu-id="91d2b-108">Requirements</span></span>  

 <span data-ttu-id="91d2b-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91d2b-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91d2b-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="91d2b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="91d2b-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="91d2b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="91d2b-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91d2b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
