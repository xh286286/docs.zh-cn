---
title: ICorDebugModule::GetBaseAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetBaseAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetBaseAddress
helpviewer_keywords:
- GetBaseAddress method [.NET Framework debugging]
- ICorDebugModule::GetBaseAddress method [.NET Framework debugging]
ms.assetid: 26a82815-1982-4eb7-92d1-5c3d318d5be4
topic_type:
- apiref
ms.openlocfilehash: 4562318c87b79fba5f3d99860ee438c0144e9aae
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710241"
---
# <a name="icordebugmodulegetbaseaddress-method"></a><span data-ttu-id="6a39f-102">ICorDebugModule::GetBaseAddress 方法</span><span class="sxs-lookup"><span data-stu-id="6a39f-102">ICorDebugModule::GetBaseAddress Method</span></span>

<span data-ttu-id="6a39f-103">获取模块的基址。</span><span class="sxs-lookup"><span data-stu-id="6a39f-103">Gets the base address of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a39f-104">语法</span><span class="sxs-lookup"><span data-stu-id="6a39f-104">Syntax</span></span>  
  
```cpp  
HRESULT GetBaseAddress(  
    [out] CORDB_ADDRESS *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6a39f-105">参数</span><span class="sxs-lookup"><span data-stu-id="6a39f-105">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="6a39f-106">弄一个 `CORDB_ADDRESS` ，它指定模块的基址。</span><span class="sxs-lookup"><span data-stu-id="6a39f-106">[out] A `CORDB_ADDRESS` that specifies the base address of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6a39f-107">注解</span><span class="sxs-lookup"><span data-stu-id="6a39f-107">Remarks</span></span>  

 <span data-ttu-id="6a39f-108">如果该模块是本机映像 (也就是说，如果该模块是由本机映像生成器生成的，则 NGen.exe) ，其基址将为零。</span><span class="sxs-lookup"><span data-stu-id="6a39f-108">If the module is a native image (that is, if the module was produced by the native image generator, NGen.exe), its base address will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a39f-109">要求</span><span class="sxs-lookup"><span data-stu-id="6a39f-109">Requirements</span></span>  

 <span data-ttu-id="6a39f-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6a39f-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a39f-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6a39f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6a39f-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a39f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a39f-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a39f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a39f-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a39f-114">See also</span></span>
