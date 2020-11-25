---
title: ICorDebugProcess5::GetObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetObject
helpviewer_keywords:
- GetObject method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::GetObject method [.NET Framework debugging]
ms.assetid: c8111502-5a20-447f-9dc2-76e8acd7ed5a
topic_type:
- apiref
ms.openlocfilehash: ff2913399e1dbeb33bbfb697058db3caf2a8d1fb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95713101"
---
# <a name="icordebugprocess5getobject-method"></a><span data-ttu-id="381cb-102">ICorDebugProcess5::GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="381cb-102">ICorDebugProcess5::GetObject Method</span></span>

<span data-ttu-id="381cb-103">将对象地址转换为 "ICorDebugObjectValue" 对象。</span><span class="sxs-lookup"><span data-stu-id="381cb-103">Converts an object address to an "ICorDebugObjectValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="381cb-104">语法</span><span class="sxs-lookup"><span data-stu-id="381cb-104">Syntax</span></span>  
  
```cpp  
HRESULT GetObject(  
    [in] CORDB_ADDRESS addr,
    [out] ICorDebugObjectValue **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="381cb-105">参数</span><span class="sxs-lookup"><span data-stu-id="381cb-105">Parameters</span></span>  

 `addr`  
 <span data-ttu-id="381cb-106">中对象地址。</span><span class="sxs-lookup"><span data-stu-id="381cb-106">[in] The object address.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="381cb-107">弄一个指向 "ICorDebugObjectValue" 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="381cb-107">[out] A pointer to the address of an  "ICorDebugObjectValue" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="381cb-108">注解</span><span class="sxs-lookup"><span data-stu-id="381cb-108">Remarks</span></span>  

 <span data-ttu-id="381cb-109">如果不 `addr` 指向有效的托管对象，该方法将 `GetObject` 返回 `E_FAIL` 。</span><span class="sxs-lookup"><span data-stu-id="381cb-109">If `addr` does not point to a valid managed object, the `GetObject` method returns `E_FAIL`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="381cb-110">要求</span><span class="sxs-lookup"><span data-stu-id="381cb-110">Requirements</span></span>  

 <span data-ttu-id="381cb-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="381cb-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="381cb-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="381cb-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="381cb-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="381cb-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="381cb-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="381cb-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="381cb-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="381cb-115">See also</span></span>

- [<span data-ttu-id="381cb-116">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="381cb-116">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="381cb-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="381cb-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
