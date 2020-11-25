---
title: ICorProfilerCallback::ExceptionCLRCatcherFound 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionCLRCatcherFound
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherFound
helpviewer_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherFound method [.NET Framework profiling]
- ExceptionCLRCatcherFound method [.NET Framework profiling]
ms.assetid: 73fe8b4b-8f9a-4ba5-a10c-b26521396a66
topic_type:
- apiref
ms.openlocfilehash: 894084978f976bcee71138d35534a80b5f9cda5f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95699971"
---
# <a name="icorprofilercallbackexceptionclrcatcherfound-method"></a><span data-ttu-id="4a9bf-102">ICorProfilerCallback::ExceptionCLRCatcherFound 方法</span><span class="sxs-lookup"><span data-stu-id="4a9bf-102">ICorProfilerCallback::ExceptionCLRCatcherFound Method</span></span>

<span data-ttu-id="4a9bf-103">当在 `catch` 公共语言运行时中找到异常的块时调用 (CLR) 本身。</span><span class="sxs-lookup"><span data-stu-id="4a9bf-103">Called when a `catch` block for an exception is found inside the common language runtime (CLR) itself.</span></span> <span data-ttu-id="4a9bf-104">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="4a9bf-104">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a9bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="4a9bf-105">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionCLRCatcherFound();  
```  
  
## <a name="requirements"></a><span data-ttu-id="4a9bf-106">要求</span><span class="sxs-lookup"><span data-stu-id="4a9bf-106">Requirements</span></span>  

 <span data-ttu-id="4a9bf-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a9bf-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a9bf-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4a9bf-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4a9bf-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a9bf-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a9bf-110">**.NET Framework 版本：** 1。0</span><span class="sxs-lookup"><span data-stu-id="4a9bf-110">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a9bf-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4a9bf-111">See also</span></span>

- [<span data-ttu-id="4a9bf-112">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="4a9bf-112">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="4a9bf-113">ExceptionCLRCatcherExecute 方法</span><span class="sxs-lookup"><span data-stu-id="4a9bf-113">ExceptionCLRCatcherExecute Method</span></span>](icorprofilercallback-exceptionclrcatcherexecute-method.md)
