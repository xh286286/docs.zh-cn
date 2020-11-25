---
title: ICorDebugClass::GetStaticFieldValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetStaticFieldValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetStaticFieldValue
helpviewer_keywords:
- GetStaticFieldValue method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetStaticFieldValue method [.NET Framework debugging]
ms.assetid: 56e718b4-fabd-418b-a5b3-3cc33c745683
topic_type:
- apiref
ms.openlocfilehash: dd1608badf553650b05b7de98d9bbcd76b2f3edf
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728428"
---
# <a name="icordebugclassgetstaticfieldvalue-method"></a><span data-ttu-id="b5896-102">ICorDebugClass::GetStaticFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="b5896-102">ICorDebugClass::GetStaticFieldValue Method</span></span>

<span data-ttu-id="b5896-103">获取指定的静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="b5896-103">Gets the value of the specified static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5896-104">语法</span><span class="sxs-lookup"><span data-stu-id="b5896-104">Syntax</span></span>  
  
```cpp  
HRESULT GetStaticFieldValue (  
    [in]  mdFieldDef         fieldDef,  
    [in]  ICorDebugFrame     *pFrame,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b5896-105">参数</span><span class="sxs-lookup"><span data-stu-id="b5896-105">Parameters</span></span>  

 `fieldDef`  
 <span data-ttu-id="b5896-106">中 `Def` 引用要检索的字段的字段标记。</span><span class="sxs-lookup"><span data-stu-id="b5896-106">[in] A field `Def` token that references the field to be retrieved.</span></span>  
  
 `pFrame`  
 <span data-ttu-id="b5896-107">中指向 ICorDebugFrame 对象的指针，该对象表示要用于区分线程、上下文或应用程序域静态对象的帧。</span><span class="sxs-lookup"><span data-stu-id="b5896-107">[in] A pointer to an ICorDebugFrame object that represents the frame to be used to disambiguate among thread, context, or application domain statics.</span></span>  
  
 <span data-ttu-id="b5896-108">如果静态字段相对于线程、上下文或应用程序域，则该框架将确定正确的值。</span><span class="sxs-lookup"><span data-stu-id="b5896-108">If the static field is relative to a thread, a context, or an application domain, the frame will determine the proper value.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="b5896-109">弄指向 ICorDebugValue 对象的地址的指针，该对象表示静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="b5896-109">[out] A pointer to the address of an ICorDebugValue object that represents the value of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b5896-110">注解</span><span class="sxs-lookup"><span data-stu-id="b5896-110">Remarks</span></span>  

 <span data-ttu-id="b5896-111">对于参数化类型，静态字段的值是相对于特定实例化的。</span><span class="sxs-lookup"><span data-stu-id="b5896-111">For parameterized types, the value of a static field is relative to the particular instantiation.</span></span> <span data-ttu-id="b5896-112">因此，如果类构造函数采用类型的参数 <xref:System.Type> ，请调用 [ICorDebugType：： GetStaticFieldValue](icordebugtype-getstaticfieldvalue-method.md) 而不是 `ICorDebugClass::GetStaticFieldValue` 。</span><span class="sxs-lookup"><span data-stu-id="b5896-112">Therefore, if the class constructor takes parameters of type <xref:System.Type>, call [ICorDebugType::GetStaticFieldValue](icordebugtype-getstaticfieldvalue-method.md) instead of `ICorDebugClass::GetStaticFieldValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5896-113">要求</span><span class="sxs-lookup"><span data-stu-id="b5896-113">Requirements</span></span>  

 <span data-ttu-id="b5896-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b5896-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5896-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b5896-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b5896-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b5896-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b5896-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b5896-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
