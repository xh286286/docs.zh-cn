---
title: ICorDebugModule::GetSize 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetSize method [.NET Framework debugging]
ms.assetid: 5c68375d-145d-46ef-a7c8-2dc4257472de
topic_type:
- apiref
ms.openlocfilehash: 0cfc31839b263c2e8cf44d15439b44ffacccf5bf
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709890"
---
# <a name="icordebugmodulegetsize-method"></a><span data-ttu-id="5197b-102">ICorDebugModule::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="5197b-102">ICorDebugModule::GetSize Method</span></span>

<span data-ttu-id="5197b-103">获取模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5197b-103">Gets the size, in bytes, of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5197b-104">语法</span><span class="sxs-lookup"><span data-stu-id="5197b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
    [out] ULONG32 *pcBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5197b-105">参数</span><span class="sxs-lookup"><span data-stu-id="5197b-105">Parameters</span></span>  

 `pcBytes`  
 <span data-ttu-id="5197b-106">弄模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5197b-106">[out] The size of the module in bytes.</span></span>  
  
 <span data-ttu-id="5197b-107">如果该模块是通过本机映像生成器生成的 ( # A0) ，则该模块的大小将为零。</span><span class="sxs-lookup"><span data-stu-id="5197b-107">If the module was produced from the native image generator (NGen.exe), the size of the module will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5197b-108">要求</span><span class="sxs-lookup"><span data-stu-id="5197b-108">Requirements</span></span>  

 <span data-ttu-id="5197b-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5197b-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5197b-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5197b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5197b-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5197b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5197b-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5197b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
