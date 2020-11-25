---
title: ICorDebugThread::GetObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetObject
helpviewer_keywords:
- GetObject method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetObject method [.NET Framework debugging]
ms.assetid: 1590febe-96c2-4046-97db-d81d81d67e01
topic_type:
- apiref
ms.openlocfilehash: 2c13ead228296525b57245be8b3bdbcdf38ae173
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95727999"
---
# <a name="icordebugthreadgetobject-method"></a><span data-ttu-id="236d7-102">ICorDebugThread::GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="236d7-102">ICorDebugThread::GetObject Method</span></span>

<span data-ttu-id="236d7-103"> (CLR) 线程获取公共语言运行时的接口指针。</span><span class="sxs-lookup"><span data-stu-id="236d7-103">Gets an interface pointer to the common language runtime (CLR) thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="236d7-104">语法</span><span class="sxs-lookup"><span data-stu-id="236d7-104">Syntax</span></span>  
  
```cpp  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="236d7-105">参数</span><span class="sxs-lookup"><span data-stu-id="236d7-105">Parameters</span></span>  

 `ppObject`  
 <span data-ttu-id="236d7-106">弄指向表示 CLR 线程的 ICorDebugValue 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="236d7-106">[out] A pointer to the address of an ICorDebugValue interface object that represents the CLR thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="236d7-107">要求</span><span class="sxs-lookup"><span data-stu-id="236d7-107">Requirements</span></span>  

 <span data-ttu-id="236d7-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="236d7-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="236d7-109">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="236d7-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="236d7-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="236d7-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="236d7-111">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="236d7-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="236d7-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="236d7-112">See also</span></span>

- <xref:System.Threading.Thread>
