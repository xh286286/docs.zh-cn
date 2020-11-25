---
title: ICorDebugModule::GetGlobalVariableValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetGlobalVariableValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetGlobalVariableValue
helpviewer_keywords:
- ICorDebugModule::GetGlobalVariableValue method [.NET Framework debugging]
- GetGlobalVariableValue method [.NET Framework debugging]
ms.assetid: bbc0881c-6a59-41a0-b5ee-2f3d1b71684c
topic_type:
- apiref
ms.openlocfilehash: 94fe7deb10c23ea0bc824bb2244e8d1d87f831e9
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710021"
---
# <a name="icordebugmodulegetglobalvariablevalue-method"></a><span data-ttu-id="22132-102">ICorDebugModule::GetGlobalVariableValue 方法</span><span class="sxs-lookup"><span data-stu-id="22132-102">ICorDebugModule::GetGlobalVariableValue Method</span></span>

<span data-ttu-id="22132-103">获取指定全局变量的值。</span><span class="sxs-lookup"><span data-stu-id="22132-103">Gets the value of the specified global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22132-104">语法</span><span class="sxs-lookup"><span data-stu-id="22132-104">Syntax</span></span>  
  
```cpp  
HRESULT GetGlobalVariableValue(  
    [in]  mdFieldDef      fieldDef,  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22132-105">参数</span><span class="sxs-lookup"><span data-stu-id="22132-105">Parameters</span></span>  

 `fieldDef`  
 <span data-ttu-id="22132-106">中 `mdFieldDef` 引用描述全局变量的元数据的令牌。</span><span class="sxs-lookup"><span data-stu-id="22132-106">[in] An `mdFieldDef` token that references the metadata describing the global variable.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="22132-107">弄指向 ICorDebugValue 对象的地址的指针，该对象表示指定的全局变量的值。</span><span class="sxs-lookup"><span data-stu-id="22132-107">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified global variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22132-108">要求</span><span class="sxs-lookup"><span data-stu-id="22132-108">Requirements</span></span>  

 <span data-ttu-id="22132-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22132-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22132-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="22132-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="22132-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22132-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22132-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22132-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
