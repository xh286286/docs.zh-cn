---
title: ICorDebugModule::GetClassFromToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetClassFromToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetClassFromToken
helpviewer_keywords:
- GetClassFromToken method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetClassFromToken method [.NET Framework debugging]
ms.assetid: 622a4d3c-0425-4c54-a7e4-0735377cdad2
topic_type:
- apiref
ms.openlocfilehash: 011d763ce244e18c7ba1203e18eb0700a8c8b13a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710228"
---
# <a name="icordebugmodulegetclassfromtoken-method"></a><span data-ttu-id="27bf8-102">ICorDebugModule::GetClassFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="27bf8-102">ICorDebugModule::GetClassFromToken Method</span></span>

<span data-ttu-id="27bf8-103">获取元数据标记指定的类。</span><span class="sxs-lookup"><span data-stu-id="27bf8-103">Gets the class specified by the metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27bf8-104">语法</span><span class="sxs-lookup"><span data-stu-id="27bf8-104">Syntax</span></span>  
  
```cpp  
HRESULT GetClassFromToken(  
    [in]  mdTypeDef        typeDef,  
    [out] ICorDebugClass **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="27bf8-105">参数</span><span class="sxs-lookup"><span data-stu-id="27bf8-105">Parameters</span></span>  

 `typedef`  
 <span data-ttu-id="27bf8-106">中 `mdTypeDef` 引用类的元数据的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="27bf8-106">[in] An `mdTypeDef` metadata token that references the metadata of a class.</span></span>  
  
 `ppClass`  
 <span data-ttu-id="27bf8-107">弄指向表示类的 ICorDebugClass 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="27bf8-107">[out] A pointer to the address of an ICorDebugClass object that represents the class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27bf8-108">要求</span><span class="sxs-lookup"><span data-stu-id="27bf8-108">Requirements</span></span>  

 <span data-ttu-id="27bf8-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="27bf8-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27bf8-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="27bf8-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="27bf8-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="27bf8-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="27bf8-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27bf8-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
