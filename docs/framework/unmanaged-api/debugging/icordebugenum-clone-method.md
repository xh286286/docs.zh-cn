---
title: ICorDebugEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::Clone
helpviewer_keywords:
- Clone method, ICorDebugEnum interface [.NET Framework debugging]
- ICorDebugEnum::Clone method [.NET Framework debugging]
ms.assetid: 57eefaf3-75cf-4496-bc94-88c0706861b7
topic_type:
- apiref
ms.openlocfilehash: 28e0cded33b49e3aadc0564bae3a60bee76c4396
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95677370"
---
# <a name="icordebugenumclone-method"></a><span data-ttu-id="1627a-102">ICorDebugEnum::Clone 方法</span><span class="sxs-lookup"><span data-stu-id="1627a-102">ICorDebugEnum::Clone Method</span></span>

<span data-ttu-id="1627a-103">创建此 ICorDebugEnum 对象的副本。</span><span class="sxs-lookup"><span data-stu-id="1627a-103">Creates a copy of this ICorDebugEnum object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1627a-104">语法</span><span class="sxs-lookup"><span data-stu-id="1627a-104">Syntax</span></span>  
  
```cpp  
HRESULT Clone (  
    [out] ICorDebugEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1627a-105">参数</span><span class="sxs-lookup"><span data-stu-id="1627a-105">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="1627a-106">弄指向作为 `ICorDebugEnum` 此对象副本的对象地址的指针 `ICorDebugEnum` 。</span><span class="sxs-lookup"><span data-stu-id="1627a-106">[out] A pointer to the address of an `ICorDebugEnum` object that is a copy of this `ICorDebugEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1627a-107">要求</span><span class="sxs-lookup"><span data-stu-id="1627a-107">Requirements</span></span>  

 <span data-ttu-id="1627a-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1627a-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1627a-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1627a-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1627a-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1627a-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1627a-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1627a-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
